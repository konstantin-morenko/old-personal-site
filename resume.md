---
title: Резюме
---

[Научная квалификация]({% link science/index.md %})

{% for type in site.data.diplomas.types %}
  {% assign color = type.color | default: "w3-yellow" %}
  <h2>{{ type.name }}</h2>
  {% for year in type.years %}
  <h3>{{ year.year }}</h3>
  {% for item in year.items %}
  <div class="w3-card w3-light-gray w3-section">
  <div class="w3-container w3-padding {{ color }}">{{ item.inst }}</div>
  <div class="w3-container w3-xlarge">{{ item.title }}</div>
  <div class="w3-container w3-padding {{ color }}">
  {% if item.href %}
  <a href="{{ item.href }}">
  {% endif %}
  {{ item.spec | default: "Диплом" }}
  {% if item.href %}
  <i class="fa fa-external-link"></i></a>
  {% endif %}
  </div>
  </div>
  {% endfor %}
  {% endfor %}
{% endfor %}

# Научные труды

- [Список научных трудов с pdf]({% link science/index.md %})

# Прочие труды

- Перевод материалов для сайта [battery-info.ru](battery-info.ru)
  (общий объём TODO)
