---
title: Справка по pgf/tikz
---

[Официальная документация на ctan.org](http://mirrors.ctan.org/graphics/pgf/base/doc/pgfmanual.pdf)

# Рисование прямых линий

    \draw (x1,y1) -- (x2,y2);

# Рисование дуг и кругов

    \draw (x1,y1) arc[start angle=0, end angle=90, radius=5cm];
	\draw (x1,y1) circle(radius);

# Стрелки

    \draw[->]
	\draw[-Stealth]

# Обозначение углов

Обозначение угла с центром в `(x,y)`, радиус обозначения `<rad>`,
начальный и конечный углы `<start>` и `<end>`, позиция привязки
обозначения угла `<anchor>`

    \draw (x,y) +(<start>:<rad>)
	arc[start angle=<start>, end angle=<end>, radius=<rad>]
	node[pos=.5,<anchor>]{alpha};

- [Обозначение углов в `tikz`](http://tex.stackexchange.com/questions/20826/label-angle-with-tikz)

# Обозначение фигурной скобкой

    \usepackage{tikz}
    \usetikzlibrary{decorations.pathreplacing}
	...
	\draw [decorate,decoration={brace,amplitude=10pt},xshift=-4pt,yshift=0pt]
    (0.5,0.5) -- (0.5,5.0) node [black,midway,xshift=-0.6cm]
    {\footnotesize $P_1$};

Полный текст на [tex.stackexchange.com](http://tex.stackexchange.com/a/20887/119485)

# Смещение и поворот в относительных координатах

	\begin{tikzpicture}
	  ...
      \begin{scope}[shift={(-5,0)},rotate=45]
        ...
      \end{scope}
	  ...
	\end{tikzpicture}

Текст на [tex.stackexchange.com](http://tex.stackexchange.com/a/7557/119485)

# Переворот координатной системы

Направить ось y вниз

    \begin{tikzpicture}[y=-1cm]
	...
    \end{tikzpicture}

Текст на [tex.stackexchange.com](http://tex.stackexchange.com/a/90001/119485)

# Ограничение ширины надписи в `node`

    \draw (x1,y1) node[text width=2cm]{text}
