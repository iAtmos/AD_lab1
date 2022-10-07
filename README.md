# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #2 выполнил(а):
- Азеев Борис Михайлович
- АТ210950
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | # | 20 |

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
Познакомиться с программными средствами для организции передачи данных между инструментами google, Python и Unity

## Задание 1
### Реализовать совместную работу и передачу данных в связке Python - Google-Sheets – Unity. При выполнении задания используйте видео-материалы и исходные данные, предоставленные преподавателя курса.
 - Согласно последовательности методички и приложенных материалов было выполнено: создание новых проектов и установка связи между Google Sheet, Python и Unity
![image](https://user-images.githubusercontent.com/114149527/194495488-846ddf47-fb5e-45b8-ad24-9c3b504c40b3.png)
![image](https://user-images.githubusercontent.com/114149527/194495589-1920f35c-8398-438f-bd49-f8f53864be29.png)
![image](https://user-images.githubusercontent.com/114149527/194495676-391f1d15-fb8a-4138-a5a2-ee540b389bc5.png)
 - Реализован алгоритм изменения инфляции с выводом соответствующих звуковых дорожек
![image](https://user-images.githubusercontent.com/114149527/194496219-0b701ead-5d37-4c5f-8e7b-4639e4d21c0e.png)
![image](https://user-images.githubusercontent.com/114149527/194496311-428544ce-9939-4e4c-9ef8-6d489d54cb65.png)



## Задание 2
### Реализовать запись в Google-таблицу набора данных, полученных с помощью линейной регрессии из лабораторной работы № 1
 - Используя ту же модель, как и предыдущем задании, на основе связи нескольких сервисов и библиотеки Gspread алгоритмом из Лабараторной работы #1 были сгенерированны значения величин a, b и автоматически перенесены в Google Sheets.
![image](https://user-images.githubusercontent.com/114149527/194614878-39935077-f489-4b4a-9665-30d43959c950.png)
![image](https://user-images.githubusercontent.com/114149527/194606058-876e64f8-4c33-42d8-97f7-22d4e5116485.png)
 - Для этого был модифицирован метод "iterate(a, b, x, y, times)" (5) и дописанно несколько информационных строк о представленной информации в столбцах таблицы.
![image](https://user-images.githubusercontent.com/114149527/194614972-f6a4fc4d-390c-4e51-b73d-cc3b5dd6c710.png)

## Задание 3
### Самостоятельно разработать сценарий воспроизведения звукового сопровождения в Unity в зависимости от изменения считанных данных в задании 2
 - ...

## Выводы

Данная работа наглядно демонстрирует каким образом можно устанавливать взаимосвязь между различными сервисами, выгружать/изменять данные и использовать их уже на других платформах.

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
