---
## Front matter
title: "Шаблон отчёта по лабораторной работе"
subtitle: "Простейший вариант"
author: "Bansimba claudely"

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

- В этой лабораторной работе мы познакомимся с git - системой контроля версий, где мы получим некоторые практические навыки о том, как обращаться и использовать этот инструмент (git).

# Ход работы:

 a. Настройка github:
В нашем случае мы будем использовать GitHub, поэтому вам необходимо создать учетную запись в https://github.com где будут заполнены основные данные  

![Название рисунка 1](image 1.1 /placeimg_800_600_tech.jpg){#fig:1 width=100%}

 b. Базовая настройка git:
 
             ▪ здесь нам нужно настроить его с помощью некоторых команд через наш терминал (Рисунок 2).
            ▪ сначала нам нужно было ввести наше имя пользователя и адрес электронной почты, с помощью которого мы создали наш репозиторий (Рисунок 2).
            ▪ Настроили utf-8 в выводе сообщений git (Рисунок 2).
            ▪ Мы задали имя начальной ветки (мы назвали её master). (Рисунок 2).
            ▪ конфигурация autocrlf (Рисунок 2).
            ▪ конфигурация safecrlf (Рисунок 2).
            
    ![Название рисунка 2](image 1.2/placeimg_800_600_tech.jpg){#fig:2 width=100%}

 c.Создание SSH ключа:
             ▪ Здесь нам нужно было сгенерировать пару ключей (открытый и закрытый) Для последующей идентификации пользователя на сервере репозитория (Рисунок 3).
            ▪ после генерации ключей они были сохранены по пути "/home/amugari/.ssh/"(Рисунок 3).
  
  ![Название рисунка 3](image 1.3 /placeimg_800_600_tech.jpg){#fig:3 width=100%}
  Нам пришлось скопировать открытый ключ из локальной консоли, но команда "xclip" не была установлена, поэтому нам пришлось установить ее, чтобы мы могли скопировать ключ 
  
   ![Название рисунка 4](image 1.4/placeimg_800_600_tech.jpg){#fig:4 width=100%}
   
   после установки команды мы скопировали открытый ключ, затем в настройках нашей учетной записи github в разделе "Ключи SSH и PGP" мы создали новый SSH-ключ, который назвали "Лабораторная работа". (Рисунок 5).  
   
   ![Название рисунка 5](image 1.5/placeimg_800_600_tech.jpg){#fig:5 width=100%}
   
          d. Сознание рабочего пространства и репозитория курса на основе шаблона:
На этом шаге нам нужно было создать рабочее пространство и репозиторий курса на основе шаблона, поэтому через терминал мы создали каталог для предмета "Архитектура компьютера", следуя необходимой иерархии (Рисунок 6).

[Название рисунка 6](image 1.6/placeimg_800_600_tech.jpg){#fig:6 width=100%}

        e. Сознание репозитория курса на основе шаблона:
  здесь, чтобы создать репозиторий курсов на основе шаблона, нам пришлось использовать уже созданный шаблон в github пользователем "yamadharma" (Рисунок 7).
  
  [Название рисунка 7](image 1.7/placeimg_800_600_tech.jpg){#fig:7 width=100%}
  
     После выбора шаблона мы должны были дать нашему репозиторию имя, которое было "study_2022–2023_arh-pc", а затем мы создали репозиторий из шаблона (Рисунок 8).

 [Название рисунка 8](image 1.8/placeimg_800_600_tech.jpg){#fig:2 width=100%}
      Затем через терминал мы переместились в каталог курса, после чего клонировали только что созданный репозиторий (Рисунок 9).
      [Название рисунка 9](image 1.9/placeimg_800_600_tech.jpg){#fig:8 width=100%}
      
              f. Настройка каталога курса:
   Чтобы настроить каталог "Курс", мы переместились в каталог
"~/work/study/2022-2023/"Архитектура компьютера"/study_2022-2023_arh-pc ", затем мы удалили файл "package.json" (Рисунок 10).

[Название рисунка 1.11](image 1.11/placeimg_800_600_tech.jpg){#fig:11 width=100%

     мы зашли в рабочее пространство в локальном репозитории и на странице github, где мы нашли все правильно (Рисунок 12).
     [Название рисунка 1.12](image 1.12/placeimg_800_600_tech.jpg){#fig:12 width=100%}

      

  

  
