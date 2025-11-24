---
layout: post
title: Tutorials
cover: datum.jpg
categories: posts
permalink: tutorials
tag: 2026
year: 2026
---

---
During this course, you will develop a computational prowess that will aid in your understanding of physical biology. These will be done using Jupyter notebooks through Google Colab, so you will need to sign into a Google Account to create new notebooks.

We will post links to Jupyter Notebooks hosted on Colab of the tutorial sessions here.

{% for topic in site.data.2026.tutorials %}
# {{topic[0]}}
{% for script in topic[1] %}
* {%if script.colab %}<a href="{{script.colab}}" target="_blank">**{{script.title}}**</a>{%else%}**{{script.title}}**{%endif%}\|
  {{script.description}}   {%if script.links %} <br/>  {%for l in script.links
  %} <i> <a href="{{l[1]}}" target="_blank">**{{l[0]}}**</a> </i> <br/>{%endfor%}   {%endif%}
{%endfor%}
{%endfor%}