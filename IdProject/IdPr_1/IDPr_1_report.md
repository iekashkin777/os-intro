---
## Front matter
title: "Отчёта по индивидуальному проекту №1"
subtitle: "дисциплина: Информационная безопасность"
author: "Кашкин Иван Евгеньевич"

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
lot: true # List of tables
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
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

-Установите дистрибутив Kali Linux в виртуальную машину.

# Задание

–Установите дистрибутив Kali Linux в виртуальную машину. 

# Теоретическая часть

Одним из коренных отличий семейства ОС Linux от ОС Windows является ведущая роль командной строки или терминала в администрировании системы. Для успешной работы с «Линукс» одного графического интерфейса недостаточно. Полноценное управление тут возможно только через терминал. А в работе с терминалом никак не обойтись без изучения основных команд Linux.

В Linux насчитывается несколько сотен основных команд и их модификаций. Они группируются по нескольким категориям. По расположению — могут быть утилитами командной строки или встроенной функцией командной оболочки. По частоте применения – используемыми постоянно, эпизодически и редко. По типам действий – от получения справки до управления файлами и процессами.

# Выполнение лабораторной работы

-Создаем новую виртуальную машину (рис. [-@fig:001])

![Создание новой машины](1.png)
{ #fig:001 width=70% }

-Параметры вирт. машины (рис. [-@fig:002])

![Параметры](2.png){ #fig:002 width=70% }

-Установка системы (рис. [-@fig:003])

![Установка](3.png){ #fig:003 width=70% }

-Задаем имя пользователя (рис. [-@fig:004])

![Имя](4.png){ #fig:004 width=70% }

-Выбираем нужные параметры (рис. [-@fig:005])

![groups](5.png){ #fig:005 width=70% }


-Перезагрузка и запуск системы  (рис. [-@fig:006])

![Система](6.png)
{ #fig:006 width=70% }

# Выводы

-научился устанавливать дистрибутив Kali Linux в виртуальную машину.

# Список литературы{.unnumbered}

::: {#https://eternalhost.net/blog/sozdanie-saytov/osnovnye-komandy-linux}
:::


