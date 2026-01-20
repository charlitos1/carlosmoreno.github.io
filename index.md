---
layout: default
title: "root@carlosmoreno:~$"
---

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d %H:%M" }} ]
# ---------------------------------------------------------

$ whoami
> carlosmoreno — Periodista y Entusiasta de la Tecnología.

$ tail -n 1 /logs/latest_post
{% assign latest_post = site.posts.first %}
---
### > {{ latest_post.title | uppercase }}
**DATE:** {{ latest_post.date | date: "%d/%m/%Y" }}
**STATUS:** Published
**READ_TIME:** 2 min read
---

{{ latest_post.content }}

---

$ ls -l /archive
{% for post in site.posts offset:1 %}
* {{ post.date | date: "%Y-%m-%d" }} - [{{ post.title }}]({{ post.url }})
{% endfor %}

$ help
> El sistema muestra automáticamente la última entrada. Usa el archivo para ver posts anteriores.
