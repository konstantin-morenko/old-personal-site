# Подсветка изменений в буфере перед сохранением

В Emacs может быть выполнена командой

    M-x diff-buffer-with-file

[stackoverflow.com](http://stackoverflow.com/questions/626492/highlight-buffer-modifications)

# Подсчёт количества вхождений регулярного выражения

Интерактивная команда для такого подсчёта

	M-x how-many

или её синоним

    M-x count-matches

[stackoverflow.com](http://stackoverflow.com/a/11848283/5762462)

# Дублирование строки

Иногда в Emacs возникает необходимость дублировать строку, для этого
поможет функция

    (defun duplicate-line()
      (interactive)
	  (progn
        (move-beginning-of-line 1)
        (kill-line)
        (yank)
        (open-line 1)
        (next-line 1)
        (yank)))

Которую можно назначить глобальной комбинации клавиш

    (global-set-key (kbd "C-c d") 'duplicate-line)

Иногда я использую такое в файлах конфигурации, когда копирую
закомментированную опцию с параметрами по умолчанию, затем
раскомментирую с помощью `M-;` и вношу необходимые изменения.  В любой
момент у меня есть оригинальная строка.
