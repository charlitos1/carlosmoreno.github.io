---
layout: default
title: "/archive"
---

# [ SYSTEM ARCHIVE: FULL LIST ]
# ---------------------------------------------------------

$ ls -R /posts/history

{% assign postsByMonth = site.posts | group_by_exp: "post", "post.date | date: '%B %Y'" %}
{% for month in postsByMonth %}
**[{{ month.name }}]**
{% for post in month.items %}
  |-- [{{ post.date | date: "%d" }}] > [{{ post.title }}]({{ post.url }})
{% endfor %}

{% endfor %}

---
$ cd ..
[ Volver al inicio ](/)
