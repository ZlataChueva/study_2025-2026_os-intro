---
## Front matter
title: "Отчёт по лабораторной работе 7"
subtitle: "Анализ файловой системы Linux"
author: "Чуева Злата Станиславовна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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
1. Цель
2. Задание 
3. Теоретическое введение
4. Выполнение лабораторной работы
5. Ответы на контрольные вопросы 
6. Вывод

# Цель работы

Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретение практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.

# Задание

1. Выполнить примеры из первой части 
2. Ввести команды 
2.1 Скопировать файл в домашний каталог
2.2 Создать директорию
2.3 Переместь файл в новый каталог
2.4 Переименовать файл 
2.5 Создать файл и скопировать в новыйй катлог
2.6 Переместить файлы
2.7 Создать и переместить катлог
3. Определить опции команды chmod
4. Ввести команды и выполнить задания
5. Ответить на контрольные вопросы 

# Теоретическое введение

Каждый файл или каталог имеет права доступа.
В сведениях о файле или каталоге указываются:
– тип файла (символ (-) обозначает файл, а символ (d) — каталог);
– права для владельца файла (r — разрешено чтение, w — разрешена запись, x — разре-
шено выполнение, - — право доступа отсутствует);
– права для членов группы (r — разрешено чтение, w — разрешена запись, x — разрешено
выполнение, - — право доступа отсутствует);
– права для всех остальных (r — разрешено чтение, w — разрешена запись, x — разрешено
выполнение, - — право доступа отсутствует).

# Выполнение лабораторной работы

Ввести команды из первой части (см рис 1)

![рис 1](image/5424980330269502805.jpg){#fig:001 width=100%}

Выполнить задания лабораторной работы (см рис 1)

Скопировать файл usr/include/sys/io.h в домашний каталог и назвать его equipment с помощью команды ср. 

В домашнем каталоге создать директорию ~/ski.plases с помошью команды mkdir

Переместить файл equipment в каталог ~/ski.plases используюя команду mv

Переименуйте файл ~/ski.plases/equipment в ~/ski.plases/equiplist с помощью команды mv

Создайть в домашнем каталоге файл abc1 и скопировать его в каталог ~/ski.plases, назовать его equiplist2 с помощью команд touch, cp

Создать каталог с именем equipment в каталоге ~/ski.plases используя команду mkdir

Переместить файлы ~/ski.plases/equiplist и equiplist2 в каталог
~/ski.plases/equipment с помощью команды mv

Создайть и переместить каталог ~/newdir в каталог ~/ski.plases и назовать его plans.

Определить опции команды chmod, необходимые для того, чтобы присвоить перечисленным ниже файлам выделенные права доступа (см рис 2 и рис 3)

![рис 2](image/5424980330269502806.jpg){#fig:001 width=100%}
![рис 3](image/5424980330269502807.jpg){#fig:001 width=100%}

Выполнить следующие задания: (см рис 3)
Просмотреть содержимое файла /etc/password командой cat
Скопировать файл ~/feathers в файл ~/file.old командой cp
Переместить файл ~/file.old в каталог ~/play командой mv
Скопировать каталог ~/play в каталог ~/fun командой cp
Переместить каталог ~/fun в каталог ~/play и назовать его games командой mv
Лишить владельца файла ~/feathers права на чтение командой chmod u-r
Если попытаться просмотреть файл ~/feathers командой cat, будет отказано в доступе
Если попытаться скопировать файл ~/feathers, будет отказано в доступе
Дать владельцу файла ~/feathers право на чтение chmod u+r
Лишить владельца каталога ~/play права на выполнение u-x
Перейти в каталог ~/play. Система не даст выполнить переход, будет отказано в доступе
Дать владельцу каталога ~/play право на выполнение chmod u+x
Прочитать man по командам mount, fsck, mkfs, kill и кратко их охарактеризовать

man mount (см рис 4)

![рис 4](image/5424980330269502808.jpg){#fig:001 width=100%}

man fsck (см рис 5)

![рис 5](image/5424980330269502809.jpg){#fig:001 width=100%}

man mkfs (см рис 6)

![рис 6](image/5424980330269502811.jpg){#fig:001 width=100%}

man kill (см рис 7)

![рис 7](image/5424980330269502810.jpg){#fig:001 width=100%}


Ответить на контрольные вопросы:


# Выводы

Ознакомлась с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобрела  практические навыки по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.


# Список литературы{.unnumbered}

::: {#refs}
:::
