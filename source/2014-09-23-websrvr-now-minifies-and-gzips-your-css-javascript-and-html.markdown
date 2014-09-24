---
title: Websrvr now minifies and gzips your css, javascript and html
date: 2014-09-23
tags: performance, gzip, minification
---

I have deployed a new update to websrvr today which minifies and gzips css,
javascript and html files in our websites. You don't have to do anything to
start using this feature. Just relax and enjoy the performance improvements :)
I did a simple test on [www.websrvr.in's](http://www.websrvr.in/) home page (by the way www.websrvr.in is
also hosted on websrvr, How cool is that :) ) and the size of the page had
reduced from **8799 to 2649** bytes which is a decrease in size by **70%**.

However, for some reason if you want to turn of css or javascript or html
minification, you can go to your *site's edit page* and uncheck the
*Minify HTML* or *Minify Javascript* or *Minify CSS* options, once you do that
your html/js/css won't be minified.
