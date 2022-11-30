# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #4 выполнил(а):
- Азеев Борис Михайлович
- АТ-210950
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | # | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Ознакомиться с основами постоения линейной модели перцептронов для базовых оцераций OR, AND, NAND, XOR.

## Задание 1
### В проекте Unity реализовать перцептрон, который умеет производить вычисления (OR | дать коментарии о корректности работы, AND | дать коментарии о корректности работы, NAND | дать коментарии о корректности работы, XOR | дать коментарии о корректности работы):

- OR. Для безошибочного обучения и последующего использования логической модели "or", в среднем, требуется пройти 3,5 -> 4 эпохи обучения. Данный результат основывается на среднем показатели эпох, в которой колличество TOTAL ERROR == 0 на основание 10 проведенных экспериментах. Для большей точности можно произвести и большее количество испытаний.
![image](https://user-images.githubusercontent.com/114149527/204771214-2559ef4c-585b-438f-8225-d6f71b56ff09.png)
- AND. Для корректного обучения данной логической модели, в среднем, алгоритму требуется большее количество обучаемых эпох, а в частности 6,7 -> 7 итераций. Даннаое наблюдение основывается на 10 оытах.
![image](https://user-images.githubusercontent.com/114149527/204774347-96f1330e-570a-4597-bd3f-c53bd7e90b21.png)
- NAND. Для корректного обучения данной логической модели, в среднем, алгоритму требуется 5,9 -> 6 итераций. Даннаое наблюдение основывается на 10 оытах.
![image](https://user-images.githubusercontent.com/114149527/204777972-baf565ee-6cf1-4b76-a0bc-009ce2a7fcbb.png)
- XOR. Поскольку, при обучение используется класическая вариация перцептрона, реализовать корректное обучение модели логической операции "XOR" не представляется возможным. Для наглядности данного феномена так же былы проведены многократные испытания с увеличением колличества эпох до 20.
![image](https://user-images.githubusercontent.com/114149527/204780522-ce614d15-221f-4873-b29c-b2874733208e.png)

- PC: Сводная таблица результатов проведенных опытов.
![image](https://user-images.githubusercontent.com/114149527/204780924-6b03d99e-9eb2-4629-b0fe-a7d24c7fbe14.png)

## Задание 3
### Представить визуальную модель работы перцептрона на сцене Unity
- Реализована система изменения цвета главного объекта (куба) при успешном обучение перцептрона. За успешное обучение считается эпоха, TOTAL ERROR которой равен 0. При выполнение условия происходит случайное изменение цвета куба на любое случаное.
https://user-images.githubusercontent.com/114149527/204876923-ceb63893-f7ff-4383-a939-9bdc3c4fea7c.mp4

## Выводы
Данная работа наглядно демонстрирует базовые возможности использования простейших перцептронов, суть которых заключается в самостоятельном обучение и подборе оптимальных коэффициентов на основе многократного повторения обучающих эпизодов. Так же, работа и раскрывает недостатки используемой технологии, а именно невозможность ее применения с некоторыми логическими операциями.

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
