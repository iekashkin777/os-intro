---
## Front matter
title: "Отчёта по лабораторной работе №2"
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

-Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux 

# Задание

– Получить практические навыки работы в консоли с атрибутами файлов 

# Теоретическая часть

Одним из коренных отличий семейства ОС Linux от ОС Windows является ведущая роль командной строки или терминала в администрировании системы. Для успешной работы с «Линукс» одного графического интерфейса недостаточно. Полноценное управление тут возможно только через терминал. А в работе с терминалом никак не обойтись без изучения основных команд Linux.

В Linux насчитывается несколько сотен основных команд и их модификаций. Они группируются по нескольким категориям. По расположению — могут быть утилитами командной строки или встроенной функцией командной оболочки. По частоте применения – используемыми постоянно, эпизодически и редко. По типам действий – от получения справки до управления файлами и процессами.

# Выполнение лабораторной работы

-Для начала мы создадим учётную запись пользователя guest (рис. [-@fig:001])

![Создание Уч.записи](1.png)
{ #fig:001 width=70% }

-Задайте пароль для пользователя gues (рис. [-@fig:002])

![Пороль](2.png){ #fig:002 width=70% }

-Войдем в систему от имени пользователя guest (рис. [-@fig:003])

![Вход в guest](3.png){ #fig:003 width=70% }

-Определим директорию, в которой вы находитесь, командой pwd. Уточним имя вашего пользователя командой whoami.(рис. [-@fig:003]) 

-Далее по заданию уточним имя нашего пользователя, его группу, а также группы, куда вхо- дит пользователь, командой id. Выведенные значения uid, gid (рис. [-@fig:004])

![Узнаем id и тд.](4.png){ #fig:004 width=70% }

-Сравните полученную информацию об имени пользователя с данными, выводимыми в приглашении командной строки(рис. [-@fig:005])

![groups](5.png){ #fig:005 width=70% }


-Просмотрите файл /etc/passwd командой
cat  /etc/passwd
Полученные команды идентичные тем, что были получены в предыдущих пунктах (рис. [-@fig:006])

![cat](6.png)
{ #fig:006 width=70% }

-Определиv существующие в системе директории командой
ls  -l  /home/
Удалось ли вам получить список поддиректорий директории /home? Да, удалось 
Ка кие права установлены на директориях? Права на чтение, запись и редактирование (рис. [-@fig:007])

![ls -l home](7.png)
{ #fig:007 width=70% }

-Проверbv, какие расширенные атрибуты установлены на поддиректориях, находящихся в директории /home, командой:
lsattr  /home
Эта команда выдала ошибку (рис. [-@fig:008])

![lsattr](8.png)
{ #fig:008 width=70% }

-Создадим в домашней директории поддиректорию dir1 командой mkdir  dir1 (рис. [-@fig:9])

![mkdir](9.png)
{ #fig:009 width=70% }

![ls -l](11.png)
{ #fig:010 width=70% }

-Снимите с директории dir1 все атрибуты командой
chmod  000  dir1
и проверьте с её помощью правильность выполнения команды
ls  -l (рис. [-@fig:12])

![chmod](12.png)
{ #fig:011 width=70% }


-Попытайтесь создать в директории dir1 файл file1 командой
echo  "test"  >  /home/guest/dir1/file1
Объясните, почему вы получили отказ в выполнении операции по созда- нию файла?
Оцените, как сообщение об ошибке отразилось на создании файла? Про- верьте командой
ls  -l  /home/guest/dir1
действительно ли файл file1 не находится внутри директории dir1.

![mkdir](13.png)
{ #fig:0012 width=70% }

-Заполните таблицу «Установленные права и разрешённые действия» (см. табл. 2.1), выполняя действия от имени владельца директории (фай- лов), определив опытным путём, какие операции разрешены, а какие нет. Если операция разрешена, занесите в таблицу знак «+», если не разре- шена, знак «-».

В моем случаи нет прав для создания файла и редактирования директории от имени пользователя "гость"

# Выводы

-Получил практические навыки работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux 

# Список литературы{.unnumbered}

::: {#https://eternalhost.net/blog/sozdanie-saytov/osnovnye-komandy-linux}
:::


