---
layout: default
title: "root@carlosmoreno:~$"
---

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d %H:%M" }} ]
# ---------------------------------------------------------

$ tail -n 1 /logs/latest_post
{% assign latest_post = site.posts.first %}
---
### > {{ latest_post.title | upcase }}
**DATE:** {{ latest_post.date | date: "%d/%m/%Y" }} | **CATEGORY:** {{ latest_post.categories | first | upcase }}
---

{{ latest_post.content }}

---

$ ls -R /archive
{% assign postsByMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for month in postsByMonth %}
**[{{ month.name }}]**
{% for post in month.items %}
  |-- [{{ post.date | date: "%d" }}] > [{{ post.title }}]({{ post.url }})
{% endfor %}
{% endfor %}

---

$ help
> Sistema de archivos organizado por meses. Los posts anteriores se listan en el árbol superior.
