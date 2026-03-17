---
layout: about
lang: de
permalink: /de/
profile:
  align: right
  image: devashish_square.jpg
published: true
---

# Ueber Mich

Hallo, ich bin Dev - Masterstudent an der RWTH Aachen. Derzeit schreibe ich meine Thesis im Bereich Process Mining zu logisch getriebener und bias-freier Anomaly Detection. Ich habe 2 Jahre bei Bosch in Abstatt und Stuttgart an der Messung und Optimierung des (Shared-)Memory-Bedarfs von kritischen Echtzeit-Softwaresystemen gearbeitet.

Ich suche aktuell Vollzeitstellen in Deutschland. Lassen wir uns gerne vernetzen!

**[Schreib mir!](mailto:ishay.gaikwad@gmail.com)**

# Projekte

{% include project-rows.html lang='de' %}

# Neueste Posts

<div class="article-list">
  {% for post in site.posts limit:5 %}
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
  {% endfor %}
</div>

<p><a href="{{ '/blog/' | relative_url }}">Alle Posts ansehen</a></p>

***
