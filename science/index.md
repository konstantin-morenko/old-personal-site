---
title: Научные труды
---

# Учёная степень

| 2014 | Кандидат технических наук по специальности 05.14.08 «Энергоустановки на основе возобновляемых видов энергии»  Тема диссертации: Ветроэлектрическая установка с двухроторным генератором и стабилизацией частоты выходного напряжения |

- [Объявление на сайте ВАК](http://vak.ed.gov.ru/dis-details?xPARAM=165203)
- [Файл автореферата](http://vak.ed.gov.ru/az/server/php/filer.php?table=att_case&fld=autoref&key[]=165203)

# Научные труды

[Профиль в elibrary.ru](http://elibrary.ru/author_items.asp?authorid=705280)

Оформление списка выполнено с помощью
системы [LaTeX]({% link latex/index.md %}) и пакета
[biblatex-gost]({% link latex/classes.md %}) согласно
[ГОСТ Р 7.0.5-2008](https://ru.wikisource.org/wiki/ГОСТ_Р_7.0.5-2008).

Тексты всех статей можно скачать в формате pdf с помощью ссылок после
каждой статьи.

Список моих научных трудов в хронологическом порядке:
- в pdf,
- или biblatex.


{% for year in site.data.articles.years %}
  <h2>{{ year.year }}</h2>

  {% for article in year.articles %}
  {{ article.biblio }} <a href="{{ article.file }}">pdf</a>
  {% endfor %}

{% endfor %}
