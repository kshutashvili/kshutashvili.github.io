---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects

{:.lead}
Здесь собраны проекты над которыми я работал , работаю, учусь. Многие из них есть на моем [GitHub](https://github.com/domoritz).

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
