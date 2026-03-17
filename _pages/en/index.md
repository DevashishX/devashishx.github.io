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

Hi, I am Dev, an ML/AI engineer in Aachen focused on LLM systems, data science, and MLOps.

I graduated in 10/2025 from RWTH Aachen in MSc Software Systems Engineering (MSc Softwaretechnik).

My work spans process mining, anomaly detection, and LLM automation. I improved anomaly detection by up to 47% with TensorFlow and built production workflows with LangChain, MCP, Ollama, Docker, and SQL.

I previously worked at Robert Bosch and Societe Generale, delivering end-to-end software from requirements to production. I am open to full-time ML/AI software engineering and MLOps roles in Germany.

**[Email me!](mailto:devashish.gaikwad@outlook.com)**

# Experience

{% include experience-tiles.html lang='en' %}

# Projects

{% include project-tiles.html lang='en' %}

# Recent Posts

<div class="article-list">
  {% for post in site.posts limit:5 %}
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
  {% endfor %}
</div>

<p><a href="{{ '/blog/' | relative_url }}">View all posts</a></p>

***
