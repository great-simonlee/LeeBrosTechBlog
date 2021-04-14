---
layout: post
title: Python - SQL Server Connection
categories: python json
author: Simon Lee
permalink: /:categories/:title
---

<strong>[Python SQL Server Connection][python-sql]</strong>

## 1. Hello world

`pip install pysql-connector`

{% highlight python %}
import mysql.connector

db = mysql.connector.connect(
host="",
user="",
passwd="",
database="",
)

mycursor = db.cursor()
{% endhighlight %}

<br>
<br>
<br>

[python-sql]: https://www.freecodecamp.org/news/connect-python-with-sql/
