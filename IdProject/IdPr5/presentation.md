---
## Front matter
lang: ru-RU
title: Индивидуальный проект - этап 5
author: |
	 Кашкин Иван Евгеньевич\inst{1}

institute: |
	\inst{1}Российский Университет Дружбы Народов

date: 12 октября, 2024, Москва, Россия

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

# Цели и задачи работы

Целью данной работы является изучение приложения BurpSuite.
## Введение

**Burp Suite** – это набор инструментов для тестирования безопасности веб-приложений. Этот инструмент используется для обнаружения уязвимостей, анализа трафика и проведения различных атак на веб-приложения, таких как XSS, SQL-инъекции и другие.
## Введение

**SQL-инъекции** – это тип уязвимости, который позволяет злоумышленникам выполнять произвольные SQL-запросы в базе данных через приложение. Это может привести к несанкционированному доступу к данным, их модификации или даже удалению.

## Работа перехватчика запросов

![Перехваченные данные](image/01.png){ #fig:001 width=70% height=70% }

## Подмена данных в запросе

![Подмена запроса](image/02.png){ #fig:002 width=70% height=70% }
## Ответ от DVWA

![Реакция на подмену](image/03.png){ #fig:003 width=70% height=70% }
## Подмена данных в запросе

![Подмена запроса](image/04.png){ #fig:004 width=70% height=70% }
## Ответ от DVWA

![Реакция на подмену](image/05.png){ #fig:005 width=70% height=70% }
## Подмена данных в запросе

![Подмена запроса](image/06.png){ #fig:006 width=70% height=70% }

## Ответ от DVWA

![Реакция на подмену](image/07.png){ #fig:007 width=70% height=70% }

# Выводы по проделанной работе

## Вывод

Мы изучили возможности BurpSuite.