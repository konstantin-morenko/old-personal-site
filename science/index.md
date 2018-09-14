---
title: Научные труды
---

# Учёная степень {#degree}

| 2014 | Кандидат технических наук по специальности 05.14.08 «Энергоустановки на основе возобновляемых видов энергии» <br /> Тема диссертации: Ветроэлектрическая установка с двухроторным генератором и стабилизацией частоты выходного напряжения | [Объявление на сайте ВАК](http://vak.ed.gov.ru/dis-details?xPARAM=165203) <br /> [Файл автореферата](http://vak.ed.gov.ru/az/server/php/filer.php?table=att_case&fld=autoref&key[]=165203) |

# Научные труды {#publications}

[Профиль в elibrary.ru](http://elibrary.ru/author_items.asp?authorid=705280)

Оформление списка выполнено с помощью
системы [LaTeX]({% link latex/index.md %}) и пакета
[biblatex-gost]({% link latex/classes.md %}) согласно
[ГОСТ Р 7.0.5-2008](https://ru.wikisource.org/wiki/ГОСТ_Р_7.0.5-2008).

Тексты всех статей можно скачать в формате pdf с помощью ссылок после
каждой статьи.

Список моих научных трудов в хронологическом порядке в
[pdf](https://github.com/konstantin-morenko/list-of-scholarly-writings/blob/travis/konstantin-morenko.pdf), или
[biblatex](https://github.com/konstantin-morenko/list-of-scholarly-writings/blob/travis/konstantin-morenko.bst).

Статьи в настоящее время в стадии заполнения.  Обращайтесь к профилю в
elibrary или к pdf.

{% for year in site.data.articles.years %}
  <h2>{{ year.year }}</h2>

  <table>
  {% for article in year.articles %}
  <tr><td> {{ article.biblio }} </td><td><a href="{{ article.file }}">pdf</a></td></tr>
  {% endfor %}
  </table>

{% endfor %}
