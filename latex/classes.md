---
title: Полезные классы документов и пакеты LaTeX
---

# Классы документов

- [eskdx](https://www.ctan.org/pkg/eskdx) --- оформление документов в
  соответствии с ЕСКД
- [standalone](https://www.ctan.org/pkg/standalone) --- сборка
  фрагментов документа отдельно от основного документа (например,
  рисунков в [TikZ](https://www.ctan.org/pkg/pgf) внутри большого
  документа)
  - конвертирование в рисунок (при сборке отдельно от основного
    документа) на
    [tex.stackexchange.com](http://tex.stackexchange.com/a/11880/119485)
	или так `\documentclass[convert]{standalone}`

# Пакеты

- [pgf/tikz](http://ctan.org/pkg/pgf) --- **превосходные** рисунки,
  графики, схемы, диаграммы и прочий графический материал
- [listings](http://ctan.org/pkg/listings) --- оформление листингов
  программ на многих языках
- [biblatex-gost](http://ctan.org/pkg/biblatex-gost) --- оформление
  библиографии согласно
  [ГОСТ Р 7.0.5-2008](https://ru.wikisource.org/wiki/ГОСТ_Р_7.0.5-2008),
  (подробнее об оформлении согласно
  [ГОСТ 7.1-2003](https://ru.wikisource.org/wiki/ГОСТ_7.1-2003)
  и различиях
  [страница 3 в документации пакета](http://mirrors.ctan.org/macros/latex/contrib/biblatex-contrib/biblatex-gost/doc/biblatex-gost.pdf#page=3)
