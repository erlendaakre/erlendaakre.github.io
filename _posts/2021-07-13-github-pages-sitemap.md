---
layout: post
title:  "Simple Sitemap on Github pages"
categories: coding
tags: coding software git github github-pages jekyll sitemap web seo
---

I was trying to get the jekyll-sitemap plugin to work on github pages, but I could not seem to get it to run.

So here is a very simple jekyll template that will generate a sitemap.xml file from your blog posts (not pages!)

{% raw %}
```xml
---
layout: null
---
<?xml version="1.0" encoding="UTF-8"?>
<urlset xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9 http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
      <url>
        <loc>{{ site.url }}{{ site.baseurl }}</loc>
        <lastmod>{{ site.time | date_to_rfc822 }}</lastmod>
        <priority>1.00</priority>
      </url>
    
    {% for post in site.posts %}
      <url>
        <loc>{{ post.url | prepend: site.baseurl | prepend: site.url }}</loc>
        <lastmod>{{ post.date | date_to_rfc822 }}</lastmod>
        <priority>0.80</priority>
      </url>
    {% endfor %}
</urlset>
```
{% endraw %}

And here is the resulting [sitemap.xml](/sitemap.xml) file.
