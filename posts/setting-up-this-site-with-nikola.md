<!--
.. title: Setting up this site with Nikola
.. slug: setting-up-this-site-with-nikola
.. date: 2018-05-29 13:06:50 UTC+02:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text
.. status: draft
-->

# Setting up this site with Nikola

Teasers also work in ipython notebook

	<!-- TEASER_END -->

Drafts:

	.. status: draft

Build:

	nikola build

Serve and view:

	nikola serve -b

Automatically rebuild, serve and view

	nikola auto -b

For an about page at the top make a page called about.

	NAVIGATION_LINKS = {
	    DEFAULT_LANG: (
	        ("/about", "About"),
	        ("/archive.html", "Archive"),
	        ("/rss.xml", "RSS feed"),
	    ),
	}

	 PAGES = (
	    ("pages/about.*", "", "page.tmpl"),
	    ("pages/*.rst", "pages", "page.tmpl"),
	    ("pages/*.md", "pages", "page.tmpl"),
	    ("pages/*.txt", "pages", "page.tmpl"),
	    ("pages/*.html", "pages", "page.tmpl"),
	    ("pages/*.ipynb", "pages", "page.tmpl"),
	)

New post:

	nikola new_post -f markdown
	nikola new_post -i some-notebook.ipynb
