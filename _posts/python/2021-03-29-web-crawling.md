---
layout: post
title: Web Crawling / Web Scraping
categories: python
author: Simon Lee
permalink: /:categories/:title
---

[freeCodeCamp YouTube][youtube]

## 1. Web Scraping

### What is Web Scraping

- Web scraping is basically extracting data from websites in an automated manner.
- It is automated because it uses bots to scrape the information or content from websites.
- Data scraping involves locating data and then extracting it. It does not copy and paste but directly fetches the data in a precise and accurate manner. It does not limit itself to the web; data can be scraped virtually from anywhere it is stored. It does not have to be from the Internet. It is about data and not where it is stored.

### How the Web Scraping Work?

#### #1 Request-Response

The first step is to request the target website for the contents of a specific URL. In return, the scraper gets the requested information in HTML format.

#### #2 Parse and Extract

When it comes to Parsing, it usually applies to any computer language. It is the process of taking the code as text and producing a structure in memory that the computer can understand and work with. To put it simply, HTML parsing is basically taking in HTML code and extracting relevant information like the title of the page, paragraphs in the page, headings in the page, links, bold text, etc.

#### #3 Download Data

The final part is where you download and save the data in a CSV, JSON or in a database so that it can be retrieved and used manually or employed in any other program.

### Web Scraping Tools

<strong>[ProWebScrapper][prowebscraper] <-- LINK</strong>

<strong>[Webscraper.io][webscraper] <-- LINK</strong>

<br>
<br>
<br>

## 2. Web Crawling

### What is Web Crawling

- The term crawling comes from the way a spider would crawl. That’s why a web crawler is also sometimes called a spider. It’s basically an internet bot that systematically browses (read crawls) the World Wide Web, usually for the purpose of web indexing.
- It is used for indexing the information on the page using bots also known as crawlers.
- It involves looking at a page in its entirety and indexing it, including its last letter and dot on the page, in the quest for information.
- Crawling through every nook and crevice of the World Wide Web, the spider locates and retrieves the information lying in the deeper layers. Web crawlers or bots navigate through heaps of data and information and procure whatever is relevant for your project.

### How the Web Crawling Work?

#### #1 Select a starting seed URL or URLs

#### #2 Add it to the frontier

#### #3 Now pick the URL from the frontier

#### #4 Fetch the web-page corresponding to that URL

#### #5 Parse that web-page to find new URL links

#### #6 Add all the newly found URLs into the frontier

#### #7 Go to step 3 and reiterate till the frontier is empty

### Web Crawling Tools

<strong>[Scrapy][scrapy] <-- LINK</strong>

<strong>[Apache Nutch][apache] <-- LINK</strong>

<br>
<br>
<br>

[prowebscraper]: https://prowebscraper.com/
[webscraper]: https://webscraper.io/
[scrapy]: https://scrapy.org/
[apache]: https://nutch.apache.org/
[youtube]: https://www.youtube.com/watch?v=XVv6mJpFOb0
