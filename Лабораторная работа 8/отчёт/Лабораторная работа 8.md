---
# Front matter
lang: ru-RU
title: "Лабораторная работа 8"
subtitle: "Отчет по лабораторной работе 8"
author: "Милёхин Александр НПМмд-02-21"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
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
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Научиться находить в Octave собственные значения и собственные векторы матрицы, а также научиться предсказывать вероятность состояния системы.

# Теоретические сведения

Вся теоретическая часть по выполнению лабораторной работы была взята из инструкции по лабораторной работе №8 ("Лабораторная работа №8. Описание") на сайте:
https://esystem.rudn.ru/course/view.php?id=12766

# Задание

Выполните работу и задокументируйте процесс выполнения.

# Выполнение лабораторной работы

**1. Собственные значения и собственные векторы**

Включим журналирование работы. После чего зададим матрицу А. Для нахождения собственных значений и собственных векторов матрицы используем команду eig с двумя выходными аргументами. Данные действия продемонстрированы на Fig. 1.

![Собственные значения и векторы матрицы](image/lab_8.1.png){ #fig:001 width=70% }

Для того, чтобы получить матрицу с действительными собственными значениями, создадим симмитричную матрицу путём умножения исходной матрицы на транспонированную. И повторим шаги, проделанные ранее. См. Fig. 2.

![Действительные собственные значения](image/lab_8.2.png){ #fig:002 width=70% }

**2. Случайное блуждание**

На курсе "Теория случайных процессов" мы дополнительно ознакомились с цепями Маркова. Наша задача - предсказать вероятности состояния системы. Для примера случайного блуждания найдем вектор вероятности после 5 шагов для каждого начального вектора. На Fig. 3 показано, как мы задаем матрицу, начальные векторы, а затем находим соответствующие вероятности.  

![Нахождение вероятностей](image/lab_8.3.png){ #fig:003 width=70% }

Теперь найдём вектор равновесного состояния для цепи Маркова с переходной матрицей. Ход решения приведен на Fig. 4.

![Вектор равновесного состояния](image/lab_8.4.png){ #fig:004 width=70% }

Таким образом, x = (0.37631  0.29287  0.33082), является вектором равновесного состояния. Проверим это. Проверка показана на Fig. 5.

![Проверка вектора равновесия](image/lab_8.5.png){ #fig:005 width=70% }

# Выводы

Я научился в Octave находить собственные значения и собственные векторы матрицы. Также научился работать с цепями Маркова и находить вектор равновесия.