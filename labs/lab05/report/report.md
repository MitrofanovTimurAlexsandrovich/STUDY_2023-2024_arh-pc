---
## Front matter
title: "Лабораторная работа №5"
subtitle: "Основы работы с Midnight Commander (mc). Структура программы на языке ассемблера NASM. Системные вызовы в ОС GNU Linux"
author: "Митрофанов Тимур Александрович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"

lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Приобретение практических навыков работы в Midnight Commander. Освоение инструкций языка ассемблера mov и int.


# Выполнение лабораторной работы

При помощи команды ***mc*** введённой в терминал попал в *Midnight Commander* (рис. @fig:001).

![Интерфейс *Midnight Commander*](image/001.png){#fig:001}

При помощи стандартных клавиш управления перешел в каталог *~/work/arch-pc* (рис. @fig:002).

![каталог *~/work/arch-pc*](image/002.png){#fig:002}

Создал подкаталог *lab05* (рис. @fig:003).

![каталог *~/work/arch-pc/lab05*](image/003.png){#fig:003}

При помощи команды ***touch*** создал файл *lab5-1.asm* (рис. @fig:004).

![файл *lab5-1.asm* в каталоге *~/work/arch-pc/lab05*](image/004.png){#fig:004}

Занёс представленную в материале к лабораторной работе программу в файл *lab5-1.asm* (рис. @fig:005).

![файл *lab5-1.asm* после редактирования](image/005.png){#fig:005}

При помощи ряда команд скомпелировал файл *lab5-1.asm*(рис. @fig:006) (рис. @fig:007) и запустил его(рис. @fig:008).

![исторя ввода команд компеляции кода и его запуска](image/007.png){#fig:006}

![Демонстрация скомпилированных файлов](image/008.png){#fig:007}

![Демонстрация работы кода](image/009.png){#fig:008}

Скачал приложенный к лабораторной работе файл с ТУИС (рис. @fig:009).

![Демонстрация скаченного файла](image/010.png){#fig:009}

При помощи *Midnight Commander* перенёс скаченный файл в папку лабораторной работы с кодами программ (рис. @fig:010).

![Демонстрация перенесённого файла](image/011.png){#fig:010}

Из файла *lab5-1.asm* создал файл *lab5-2.asm* (рис. @fig:011).

![Демонстрация скопироного файла *lab5-2.asm*](image/013.png){#fig:011}

Внёс изменения в файл как было указано в лабораторной работе(рис. @fig:012).

![Содержимое файла *lab5-2.asm* после изменения](image/014-1.png){#fig:012}

Затем скпомпелировал файл (рис. @fig:013) и запустил его (рис. @fig:014)

![Компеляция файла *lab5-2.asm*](image/014-2.png){#fig:013}

![Запуск файла *lab5-2.asm*](image/014-3.png){#fig:014}

Заменил команду ***sprintLF*** на ***sprint***(рис. @fig:015).

![Изменённый файл *lab5-2.asm*](image/014.png){#fig:015}


После чего скомпелировал (рис. @fig:016) и вновь запустил его (рис. @fig:017). Изменяние по сравнению с предидущим разом заключается в том, что в последний раз не произошло переноса строки т.к. команда ***sprint*** этого не предусматривает.

![Компеляция файла *lab5-2.asm*](image/015.png){#fig:016}

![Запуск файла *lab5-2.asm*](image/016.png){#fig:017}

# Выполнение заданий для самостоятельной работы

Создал файл *lab5-1с.asm* на основе *lab5-1.asm*(рис. @fig:018)

![Демонстрация созданного файла *lab5-1с.asm*](image/017.png){#fig:018}

Внёс изменения в файл  *lab5-1с.asm*(рис. @fig:019).

![Содержимое файла  *lab5-1с.asm* после изменения](image/018.png){#fig:019}

После чего скомпелировал (рис. @fig:020) и запустил его (рис. @fig:021).

![Компеляция файла *lab5-2.asm*](image/019.png){#fig:020}

![Запуск файла *lab5-2.asm*](image/020.png){#fig:021}

Создал файл *lab5-2с.asm* и внёс изменения в него (рис. @fig:022).

![Содержимое файла  *lab5-2с.asm* после изменения](image/021.png){#fig:022}

После чего скомпелировал и запустил его (рис. @fig:023). 

![Компеляция файла *lab5-2.asm*](image/022.png){#fig:023}

# Выводы

Сегодня я приобрёл практические навыки работы в Midnight Commander. Освоил инструкций языка ассемблера mov и int.

:::
