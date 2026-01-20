---
layout: default
title: "root@carlosmoreno:~$"
---

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d" }} ]
# ---------------------------------------------------------

$ whoami
> carlosmoreno — Periodista y Entusiasta de la Tecnología.

$ tail -n 1 /logs/latest_post

{% for post in site.posts limit:1 %}
---
### > {{ post.title | upcase }}
**DATE:** {{ post.date | date: "%d/%m/%Y" }}
---

{{ post.content }}

{% endfor %}

---

$ ls -R /archive
{% for post in site.posts offset:1 %}
* {{ post.date | date: "%Y-%m-%d" }} - [{{ post.title }}]({{ post.url }})
{% endfor %}

---

$ help
> Usa el archivo inferior para navegar por entradas antiguas.
