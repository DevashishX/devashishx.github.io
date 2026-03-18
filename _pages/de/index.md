---
layout: about
lang: de
permalink: /de/
profile:
  align: right
  image: devashish_square.jpg
published: true
---

# über Mich

Hallo, ich bin Dev, ML/AI Engineer in Aachen mit Fokus auf LLM-Systeme, Data Science und MLOps.

Ich habe im 10/2025 meinen Abschluss an der RWTH Aachen im MSc Softwaretechnik (MSc Software Systems Engineering) gemacht.

Ich arbeite an Process Mining, Anomalieerkennung und LLM-Automatisierung. Mit TensorFlow habe ich die Erkennungsleistung um bis zu 47% verbessert und produktive Workflows mit LangChain, MCP, Ollama, Docker und SQL umgesetzt.

Zuvor war ich bei Robert Bosch und Societe Generale und habe Software end-to-end von Requirements bis Produktion geliefert. Ich suche Vollzeitrollen in Deutschland im Bereich ML/AI Software Engineering und MLOps.

<div style="display: flex; gap: 1rem; margin: 1.5rem 0; flex-wrap: wrap;">
  <a href="mailto:devashish.gaikwad@outlook.com" style="display: inline-block; padding: 0.75rem 1.5rem; background-color: #004e89; color: white; text-decoration: none; border-radius: 4px; font-weight: bold; transition: background-color 0.3s;" onmouseover="this.style.backgroundColor='#003d6b'" onmouseout="this.style.backgroundColor='#004e89'">Schreib mir!</a>
  <a href="{{ 'Lebenslauf_DevashishGaikwad.pdf' | relative_url }}" style="display: inline-block; padding: 0.75rem 1.5rem; background-color: #004e89; color: white; text-decoration: none; border-radius: 4px; font-weight: bold; transition: background-color 0.3s;" onmouseover="this.style.backgroundColor='#003d6b'" onmouseout="this.style.backgroundColor='#004e89'">Lebenslauf Herunterladen!</a>
</div>

# Erfahrung

{% include experience-tiles.html lang='de' %}

# Projekte

{% include project-tiles.html lang='de' %}

# Neueste Posts

<div class="article-list">
  {% for post in site.posts limit:5 %}
    <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
  {% endfor %}
</div>

<p><a href="{{ '/blog/' | relative_url }}">Alle Posts ansehen</a></p>

***
