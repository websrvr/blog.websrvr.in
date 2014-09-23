---
title: Hello world
date: 2014-09-11
tags: greeting
---

It has been an awesome experience building [http://www.websrvr.in](http://www.websrvr.in)

I strongly believe in [dogfooding](http://en.wikipedia.org/wiki/Eating_your_own_dog_food) so
I created this blog using jekyll and websrvr.in, it was actually very
easy to setup. All I did was:

  1. Create a directory called `websrvrblog` by running `jekyll new  websrvrblog` in my code directory. This can be named anything.
  2. Edit the `_config.yml` to add a `destination: /home/minhajuddin/Dropbox/Apps/websrvr/blog`

That's it, now whenever I run `jekyll build` it exports this blog to the
`blog` subdirectory in my dropbox folder which is hooked up via websrvr to
show up at [http://blog.websrvr.in](http://blog.websrvr.in)
