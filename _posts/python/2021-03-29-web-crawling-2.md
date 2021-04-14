---
layout: post
title: Python - Web Crawling / Web Scraping (2)
categories: sql cheatsheet
author: Simon Lee
permalink: /:categories/:title
---

[freeCodeCamp YouTube][youtube]

## 3. Packages

`pip install bs4`  
`pip install requests`  
`pip install requests`  
`pip install selenium`  
`pip install webdriver-manager`

{% highlight python %}
from selenium import webdriver
from webdriver_manager.chrome import ChromeDriverManager

driver = webdriver.Chrome(ChromeDriverManager().install())
{% endhighlight %}

<br>
<br>
<br>

## 4. Selenium Selectors / Commands

[SELENIUM COMMANDS][selenium_command]

<br>
<br>
<br>

[youtube]: https://www.youtube.com/watch?v=XVv6mJpFOb0
[selenium_command]: https://blog.naver.com/deepplin/221512366470
