---
layout: default
title: "root@carlosmoreno:~$"
---

# [ SESSION STARTED: {{ "now" | date: "%Y-%m-%d" }} ]
# ---------------------------------------------------------

$ whoami
> carlosmoreno — Tech Consulting | Deploying Digital Archive Infraestructure | Project Manager at Bitseat | Presidency NGO paulvenezuela.org | Journalist | Developing enterprise project.

$ /novedad

{% for post in site.posts limit:1 %}
---
### > {{ post.title | upcase }}
**DATE:** {{ post.date | date: "%d/%m/%Y" }}
---

{{ post.content }}

{% endfor %}

---

$ /archive
{% for post in site.posts offset:1 %}
* {{ post.date | date: "%Y-%m-%d" }} - [{{ post.title }}]({{ post.url }})
{% endfor %}


---

$ help
> Usa el archivo inferior para navegar por entradas antiguas.
