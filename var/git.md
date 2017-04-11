---
title: Git
---

# Git в Bash

Часто при работе с `git`-репозиториями возникает необходимость в том,
чтобы видеть состояние репозитория прямо в строке приглашения.  В этом
случае поможет файл `git-prompt.sh`, который находится в составе
пакета.  В начале файла подробно описана методика настройки и
переменные оболочки, которые влияют на форматирование приглашения.

Этот файл нужно загрузить при запуске оболочки, затем сформировать
приглашение, например

    PS1='[\u@\h \W$(__git_ps1 " (%s)")]\$ '

[Настройка в Arch Linux](https://wiki.archlinux.org/index.php/git#Git_prompt)

# Отмена изменений в строке

Для отмены изменений в *некоторых* строках файла с помощью git, можно
воспользоваться ключем `-p` в команде `checkout`

    git checkout -p filename

Кроме прочего, эта команда позволяет разбивать элементы коммита на
отдельные строки (подробнее о клавишах по команде `?` в интерфейсе).

[Ответ на stackoverflow.com](http://stackoverflow.com/a/6963150/5762462)

# Способ управления файлом ChangeLog при использовании Git

Управление может быть осуществлено через экспорт файла

    git log --oneline --decorate

или в цвете

    git log --oneline --decorate --color

Использование при сборке проекта в Makefile

    .PHONY: update-ChangeLog
    update-ChangeLog:
        if test -d $(srcdir)/.git; then                         \
           $(srcdir)/build-aux/gitlog-to-changelog              \
              --format='%s%n%n%b%n' --no-cluster                \
              --strip-tab --strip-cherry-pick                   \
              -- $$(cat $(srcdir)/.last-cl-gen)..               \
            >ChangeLog.tmp                                      \
          && git rev-list -n 1 HEAD >.last-cl-gen.tmp           \
          && (echo; cat $(srcdir)/ChangeLog) >>ChangeLog.tmp    \
          && mv -f ChangeLog.tmp $(srcdir)/ChangeLog            \
          && mv -f .last-cl-gen.tmp $(srcdir)/.last-cl-gen      \
          && rm -f ChangeLog.tmp;                               \
        fi
    EXTRA_DIST += .last-cl-gen

[stackoverflow.com](http://stackoverflow.com/questions/3523534/good-ways-to-manage-a-changelog-using-git)
