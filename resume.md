---
title: Резюме
---

# Образование

## [Научная квалификация]({% link science/index.md %})

## Высшее образование

## Курсы

### Интернет-университет ИТ-технологий

Сайт университета [intuit.ru](intuit.ru)

{% for year in site.data.diplomas.years %}
  <h2>{{ year.year }}</h2>
  <ul>
  {% for item in year.items %}
    <li><a href="{{ item.hyper }}">{{ item.title }}</a></li>
  {% endfor %}
  </ul>
{% endfor %}

# Научные труды

- [Список научных трудов с pdf]({% link science/index.md %})

# Прочие труды

- Перевод материалов для сайта [battery-info.ru](battery-info.ru)
  (общий объём TODO)
