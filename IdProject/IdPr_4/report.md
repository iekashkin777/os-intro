---
lang: ru-RU
title: Индивидуальный проект - этап 4
subtitle: Использование nikto
author: Кашкин Иван Евгеньевич
toc-title: Содержание
toc: true
toc_depth: 2
lof: true
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10
  - \interlinepenalty=0
  - \hyphenpenalty=50
  - \exhyphenpenalty=50
  - \binoppenalty=700
  - \relpenalty=500
  - \clubpenalty=150
  - \widowpenalty=150
  - \displaywidowpenalty=50
  - \brokenpenalty=100
  - \predisplaypenalty=10000
  - \postdisplaypenalty=0
  - \floatingpenalty = 20000
  - \raggedbottom
  - \usepackage{float}
  - \floatplacement{figure}{H}
---

# Цель работы

Целью данной работы является изучение сканера уязвимостей nikto.

# Введение

## Nikto: Описание

**Nikto** — это популярный сканер веб-серверов с открытым исходным кодом, который проверяет веб-серверы на наличие уязвимостей, неправильных настроек, устаревших версий ПО и прочих проблем безопасности.

Основные задачи Nikto:

- Поиск общих уязвимостей веб-серверов.

- Проверка наличия опасных файлов и конфигураций.

- Выявление устаревших версий веб-серверов и их компонентов.

- Определение серверных технологий и модулей.

Особенности:


- Поддержка множества серверов и протоколов (HTTP, HTTPS, HTTP/2 и другие).

- Возможность добавления собственных правил для обнаружения уязвимостей.

- Регулярные обновления базы данных уязвимостей.

Nikto — это пассивный сканер, и он не пытается активно взламывать систему, а только собирает информацию о потенциальных уязвимостях.

Рекомендуется использовать Nikto в сочетании с другими инструментами безопасности, такими как Nmap и OpenVAS, для более полного анализа безопасности веб-сервера.

## Полезные параметры и примеры

Nikto написан на Perl, и для его работы необходимо наличие Perl на системе.

Сканирование веб-сервера
```bash
perl nikto.pl -h <URL>
```

Сканирование определенного порта
```bash
perl nikto.pl -h <URL> -p <port>
```

Вывод результатов в файл
```bash
perl nikto.pl -h <URL> -o output.txt
```

Дополнительные аргументы:


* -ssl — принудительное использование SSL (HTTPS).

* -no_ssl — игнорирование SSL-сертификатов.

* -Tuning — настройка интенсивности сканирования (например, отключение проверки директорий).

* -Plugins — выбор определенных плагинов для сканирования.

* -timeout — установка таймаута для запросов.

# Выполнение работы

Nikto может использоваться для пассивного сканирования DVWA, выявления базовых уязвимостей и проверок на неправильную конфигурацию.

Когда DVWA запущено, мы можем использовать Nikto для сканирования. Основной командой для сканирования будет:
```bash
perl nikto.pl -h http://localhost/dvwa/
```

## Сканирование localhost
![Тестирование localhost](image/01.png){ #fig:001 width=70% height=70% }

## Сканирование localhost/dvwa/

![Тестирование localhost/dvwa/](image/02.png){ #fig:002 width=70% height=70% }

# Вывод

Мы изучили возможности сканера nikto.