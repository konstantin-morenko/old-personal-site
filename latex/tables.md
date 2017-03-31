---
title: Таблицы в LaTeX
---

# Повернуть заголовок в таблице

Повернуть заголовок в таблице достаточно просто, для этого нужно
вставить в преамбулу документа этот код

    \newcolumntype{R}[2]{ %
        >{\adjustbox{angle=#1,lap=\width-(#2)}\bgroup} %
        l %
        <{\egroup} %
    }
    \newcommand*\rot{\multicolumn{1}{R{90}{1em}}}% no optional argument here, please!

и далее все ячейки в заголовке заключить в команду `\rot{содержимое}`.

Более подробный ответ на [tex.stackexchange.com](http://tex.stackexchange.com/a/98439/119485)
