---
layout: default
title: "root@carlosmoreno:~$"
---

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d %H:%M" }} ]

[$ /novedades
{% assign latest_post = site.posts.first %}
---
### > {{ latest_post.title | upcase }}
**DATE:** {{ latest_post.date | date: "%d/%m/%Y" }}

---

{{ latest_post.content }}

---

$ /recent_posts (Showing last 5)
{% for post in site.posts offset:1 limit:5 %}
* {{ post.date | date: "%Y-%m-%d" }} - [{{ post.title }}]({{ post.url }})
{% endfor %}

$ archive
> [ Ver todos los registros del sistema (Full Archive) ](/archive)

---

$ help
> El sistema muestra el post más reciente y los 5 anteriores. Usa /archive para el historial completo.
