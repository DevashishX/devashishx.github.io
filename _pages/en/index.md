---
layout: about
lang: en
permalink: /en/
profile:
  align: right
  image: devashish_square.jpg
published: true
---

# About Me

Hi, I am Dev - a Master's student at RWTH Aachen, I am currently writing my thesis in Process Mining on logic driven and bias-free Anomaly Detection. I have worked for 2 years at Bosch in Abstatt and Stuttgart on measurement and optimization of (shared) memory occupied by critical real time software systems.

I am currently looking for full time jobs in Germany, so let's connect!

**[Email me!](mailto:ishay.gaikwad@gmail.com)**

# Projects

{% include project-rows.html lang='en' %}

# Recent Posts

<div class="article-list">
  {% for post in site.posts limit:5 %}
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
  {% endfor %}
</div>

<p><a href="{{ '/blog/' | relative_url }}">View all posts</a></p>

***
