---
layout: post
title: Jekyll Blog (1)
categories: jekyll
author: Simon Lee
permalink: /:categories/:title
---

## 1. Installation

`xcode-select --install`  
`ruby -v`  
`gem -v`  
`gem install jekyll bundler`  
`jekyll -v`
<br>
<br>
<br>

## 2. Creating a new blog

`jekyll new (BLOG_NAME)`

For my tech blog, I have created a blog called Simon_Blog. So it would be `jekyll new Simon_Blog`.
<br>
<br>
<br>

## 3. Buliding a blog page

`bundle exec jekyll serve`

Every time the Config file or Gemfile have a change, you should build them again.

`jekyll serve`

After buliding the page, the server can be open only using the command above.

`http://127.0.0.1:4000/`

Mostly the Jekyll blog is built on the address above.
<br>
<br>
<br>

### Reference

[Jekyll Website][jekyll-site]  
[Jekyll Documents][jekyll-docs]  
[Jekyll Github][jekyll-gh]  
[Jekyll Talk][jekyll-talk]  
[Jekyll Theme][jekyll-theme]

[jekyll-site]: https://jekyllrb.com/
[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]: https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[jekyll-theme]: https://rubygems.org/search?utf8=%E2%9C%93&query=jekyll-theme
