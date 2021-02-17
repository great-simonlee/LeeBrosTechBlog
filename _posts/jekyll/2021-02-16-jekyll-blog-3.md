---
layout: post
title: Jekyll Blog (3)
categories: jekyll
author: Simon Lee
permalink: /:categories/:title
---

## 7. Layouts

Layouts is the template for making the posts and pages on the website. It includes only HTML files consisting of the base pages of the website. Markdown files are recognized based on the different forms from the layouts.  
Examples: `default`, `home`, `page`, `post`
<br>
<br>
<br>

## 8. Includes

Includes contains the code blocks that consist of the layouts. These blocks can be dependent on one another.  
Examples: `head`, `header`, `footer`
<br>
<br>
<br>

## 9. Theme

The basic theme of the Jekyll website is 'Minima'. You can find this theme in the `_config.yml` file. In order to change the theme of your blog, you should find the one you like on the [Jekyll Theme][jekyll-theme] website.

Choose what you like and go to the 'Hompage' on the right side. Then you can find the preview of the theme and how to use the theme.

In the `Gemfile`, you should add `gem jekyll-theme-primer`.
In the `_config.yml`, you should change the theme part to `theme: jekyll-theme-primer`.
In the terminal, execute the following commands. `bundle install`.

Because the `Gemfile` and `_config.yml` files are changed, you should build the code again by executing `bundle exec jekyll serve`.

[jekyll-theme]: https://rubygems.org/search?utf8=%E2%9C%93&query=jekyll-theme
