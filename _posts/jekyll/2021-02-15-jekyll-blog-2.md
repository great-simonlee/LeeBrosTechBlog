---
layout: post
title: Jekyll Blog (2)
categories: jekyll
author: Simon Lee
permalink: /:categories/:title
---

## 4. Folders and Files

`_data` folder can contain .yml .json files.  
`_drafts` folder can contain all the draft posts before publishing.  
`_includes` folder can contain the code snippets which can repeatedly be used in the layouts.  
`_layouts` folder can contain layouts displayed on the webpage.  
`_posts` folder can contain the posts which you want to publish on the webpage.  
`_site` folder contains the files already built. So the user no need to edit anything in this folder.  
`page` folder can contain the markdown files for making pages.  
`assets` folder can contain the static files, such as img, logo, svg, etc.  
`_config.yml` file is for configuring the setting of the website.
`Gemfile` file is for managing the dependencies that the website needs.
<br>
<br>
<br>

## 5. Adding a Post

To add a post, the file should be made in the `_posts` folders. The name of the file has a specific way to be made as below.  
`yyyy-mm-dd-file-name.md`
<br>
<br>
These post files can be stored in the separate category folders. Foldering does not affect the display of the posts.

In the header of the markdown file, the code snippet below should be included so that the Jekyll utilizes the information about the post and displays on the blog.
{% highlight markdown %}

---

layout: post
title: New Title
date: yyyy-mm-dd hh:mm:ss
categories: New Category
author: New Author
permalink: /:categories/:title

---

{% endhighlight %}
<br>
<br>
<br>

## 6. Adding a Page

To add a page, the page file should be made in the page folder. The file should also be a markdown file with the page layout.
<br>
<br>
In the header of the markdown fle, the code snippet below should be included.  
{% highlight markdown %}

---

layout: page
title: Page Name
permalink: /PageURL/

---

{% endhighlight %}
