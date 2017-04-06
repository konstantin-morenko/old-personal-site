---
title: Резюме
---

# Образование

## Высшее образование

## Научная степень

(2014) Кандидат технических наук по специальности 05.14.08
«Энергоустановки на основе возобновляемых видов энергии»

Тема диссертации: Ветроэлектрическая установка с двухроторным
генератором и стабилизацией частоты выходного напряжения

- [Объявление на сайте ВАК](http://vak.ed.gov.ru/dis-details?xPARAM=165203)
- [Файл автореферата](http://vak.ed.gov.ru/az/server/php/filer.php?table=att_case&fld=autoref&key[]=165203)

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

- [Профиль автора в elibrary.ru](http://elibrary.ru/author_items.asp?authorid=705280)
- [Список научных трудов с pdf]({% link science/index.md %})

# Прочие труды

- Перевод материалов для сайта [battery-info.ru](battery-info.ru)
  (общий объём TODO)
