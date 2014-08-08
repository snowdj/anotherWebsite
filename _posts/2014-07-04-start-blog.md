---
layout : post
title : Start blog!
subtitle : Adopt from gh-pages-blog
category : github blog
tags :
  - github
  - blog
---

Hello, World!

I just borrow the blog system from https://github.com/thedereck/gh-pages-blog/

It looks good. Hope I can use it for my blog.

* The only thing I don't know is what is the setting of disqus.

I think I need to change body/sections/javascript/post/disqus.html.

But actually just change config.yml

disqus :
  enabled : true
  shortname : snowdj
  show_comment_count : true

* Change footer.html. 


* A substitution is pelican

http://docs.getpelican.com/en/latest/content.html

https://github.com/getpelican/pelican/wiki/Tutorials

http://hackercodex.com/guide/pelican-static-site-generator-install/

http://docs.getpelican.com/en/latest/quickstart.html


* The same page

This one seems on the same page to try different format
https://github.com/OpenJC

One thing is worth mention

source: https://github.com/jekyll/jekyll/issues/332

I finally figured out the trick, if you're looking for a solution with the standard URL for GitHub Pages (username.github.io/project-name/). Here's what to do:

In _config.yml, set the baseurl option to /project-name -- note the leading slash and the absence of a trailing slash.

Now you'll need to change the way you do links in your templates and posts, in the following two ways:

When referencing JS or CSS files, do it like this: {{ site.baseurl }}/path/to/css.css -- note the slash immediately following the variable (just before "path").

When doing permalinks or internal links, do it like this: {{ site.baseurl }}{{ post.url }} -- note that there is no slash between the two variables.

Finally, if you'd like to preview your site before committing/deploying using jekyll serve, be sure to pass an empty string to the --baseurl option, so that you can view everything at localhost:4000 normally (without /project-name getting in there to muck everything up): jekyll serve --baseurl ''

This way you can preview your site locally from the site root on localhost, but when GitHub generates your pages from the gh-pages branch all the URLs will start with /project-name and resolve properly.
