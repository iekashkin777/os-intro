---
## Front matter
lang: ru-RU
title: Отчет по лабораторной работе №3
author: Кашкин Иван Евгеньевич
institute: РУДН, Москва, Россия
date: 21 сентябрь 2024 г.

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

## Цель работы 

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux 

## Задание

Получить практические навыки работы в консоли с атрибутами файлов 

## Создание учетной записи 

- Создаем второго пользователя guest2, потому что guest был создан в предыдущей работе. (рис. [-@fig:001])

![Создание guest2](image/01.png)
{ #fig:001 width=70% }

## Groups

- Добавьте пользователя guest2 в группу guest: gpasswd  -a  guest2  guest (рис. [-@fig:002])

![Groups](image/02.png){ #fig:002 width=70% }

## PWD

- Для обоих пользователей командой pwd определим директорию, в кото- рой вы находитесь (рис. [-@fig:003]) 

![pwd](image/03.png){ #fig:003 width=70% }

## cat

- -Сравним полученную информацию с содержимым файла /etc/group. Просмотрите файл командой cat  /etc/group (рис. [-@fig:005])

![cat](image/05.png){ #fig:005 width=70% }

## NEWGRP

- От имени пользователя guest2 выполниv регистрацию пользователя guest2 в группе guest командой
newgrp  guest (рис. [-@fig:006])

![newgrp](image/06.png)
{ #fig:006 width=70% }

## CHMOD

- От имени пользователя guest измениv права директории /home/guest, разрешив все действия для пользователей группы:
chmod  g+rwx  /home/guest (рис. [-@fig:007])

![chmod](image/07.png)
{ #fig:007 width=70% }

## CHMOD

- От имени пользователя guest снимиv с директории /home/guest/dir1 все атрибуты командой
chmod  000  dirl (рис. [-@fig:008])

![dir1](image/08.png)
{ #fig:008 width=70% }

## Вывод

-Получил практические навыки работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе ОС Linux 

## {.standout}

Спасибо за внимание!
