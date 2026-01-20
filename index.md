---
layout: default
title: "root@carlosmoreno:~$"
---

$ whoami
carlosmoreno — Tech Consulting | Deploying Digital Archive Infraestructure - Residencia de Estudiantes de Madrid | Project Manager | Presidency NGO paulvenezuela.org | Journalist |

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d %H:%M" }} ]

$ /novedades
{% assign latest_post = site.posts.first %}
---
### > {{ latest_post.title | upcase }}
**DATE:** {{ latest_post.date | date: "%d/%m/%Y" }}
**TAGS:** {% for category in latest_post.categories %}<{{ category | upcase }}> {% endfor %}
---

{{ latest_post.content }}

---

$ ls -l /recent_posts (Showing last 5)
{% for post in site.posts offset:1 limit:5 %}
* {{ post.date | date: "%Y-%m-%d" }} - [{{ post.title }}]({{ post.url }})
{% endfor %}

$ cd /archive
> [ Ver todos los registros del sistema (Full Archive) ](/archive)

---

$ help
> El sistema muestra el post más reciente y los 5 anteriores. Usa /archive para el historial completo.
