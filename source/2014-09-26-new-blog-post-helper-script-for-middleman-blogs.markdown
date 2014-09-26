---
title: New blog post helper script for middleman blogs
date: 2014-09-26
tags: tiny, utility, middleman
---

This blog is built using the [awesome middlemanapp](http://middlemanapp.com/).
However, to create a new blog post you need to create a file with a name similar
to `2014-09-26-new-blog-post-helper-script-for-middleman-blogs.markdown`, it
also needs to have it's title, date and tags in the YAML frontmatter. So, I just
wrote a quick script which helps me create new blog posts easily. It also
creates a neat symlink in your root directory with a name `current.markdown` so
that you can open this file easily, without tabbing a hundred times :)

~~~ruby
#!/usr/bin/env ruby
#Contents of ./new
#Usage:
# ./new 'New blog post helper script for middleman blogs' \
#           'tiny, utility, middleman'
#Edit your post by running vi current.markdown
#Author Khaja Minhajuddin
require 'fileutils'

title = ARGV[0]
categories = ARGV[1] || ''
date = Time.now.strftime("%Y-%m-%d")
content = DATA.read.gsub('TITLE', title).gsub('DATE', date)
              .gsub('CATEGORIES', categories)
filename = title.downcase.gsub(/[^a-z0-9]/, '-').gsub(/\-+/, '-')

CURRENT_SYMLINK = './current.markdown'

filepath = "./source/#{date}-#{filename}.markdown"
puts "writing #{filepath}"
File.write(filepath, content)
FileUtils.rm_f(CURRENT_SYMLINK)
FileUtils.ln_s(filepath, CURRENT_SYMLINK)
puts "symlinked new article with #{CURRENT_SYMLINK}"

__END__
---
title: TITLE
date: DATE
tags: CATEGORIES
---
~~~

The code is kind of self explanatory, so I won't go into the details explaining
it.
