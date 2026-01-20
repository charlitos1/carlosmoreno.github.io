
---
layout: default
title: "root@carlosmoreno:~$"
---

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d %H:%M" }} ]

$ tail -n 1 /logs/latest_post
{% assign latest_post = site.posts.first %}

{% if latest_post %}
---
### > {{ latest_post.title | upcase }}
**DATE:** {{ latest_post.date | date: "%d/%m/%Y" }}
---

{{ latest_post.content }}

{% else %}
$ system_err: No se detectan posts. Verifica la fecha del archivo.
{% endif %}

---

$ ls -R /archive
{% for post in site.posts %}
* {{ post.date | date: "%Y-%m-%d" }} - [{{ post.title }}]({{ post.url }})
{% endfor %}

