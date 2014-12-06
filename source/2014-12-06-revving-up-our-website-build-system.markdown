---
title: Revving up our website build system
date: 2014-12-06
tags: performance, golang, nodejs
---

We deployed our new website build system which uses http://golang.org/ and http://nodejs.org/
a few days ago. And we are very happy with the performance improvements.

It now takes under 5 seconds to build and publish a website with ~50 resources
(http://perftest.websrvr.in/).

Under 5 seconds our build system

  1. Downloads these 50 resources from dropbox
  2. Minifies all your **HTML, Javascript and CSS**
  3. Gzips all your text content with the highest compression, so that it can be
     served fast without on the fly compression.

For subsequent builds it only builds the resources which change which should be
much faster.

Now, the changes are published within the time you save your changes and refresh your browser.


Enjoy the speed improvements :)
