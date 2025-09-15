---
layout: default
title: "Projects"
permalink: /projects/
---

# Projektit

Tälle sivulle kerään kaikki julkiset projektini. Klikkaa nimeä niin pääset projektisivulle, jossa on tarkempi kuvaus.

---

{% for p in site.projects %}
## [{{ p.title }}]({{ p.url }})

{{ p.excerpt | strip_html }}

**Teknologiat:** {% for tag in p.tags %}{{ tag }}{% if forloop.last == false %}, {% endif %}{% endfor %}  

{% if p.repo %}
🔗 [GitHub repo]({{ p.repo }})
{% endif %}

---

{% endfor %}
