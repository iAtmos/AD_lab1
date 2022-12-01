# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил(а):
- Азеев Борис Михайлович
- АТ210950
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
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
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1
### Измените параметры файла. yaml-агента и определить какие параметры и как влияют на обучение модели.
## Задание 2
### Опишите результаты, выведенные в TensorBoard.

## Реализация
- Изначально была осуществелна настройка среды, в которой будет происходить дальнейшее изучение экономической модели, основанной на алгоритме mlagenta, который учитывает ряд параметров при обучение. А так же осуществленно обучение с первичными параметрами (1/5) на основе 50.000 итераций.

![image](https://user-images.githubusercontent.com/114149527/205102984-26d466af-605c-4b8c-ad6d-5167c52e3052.png)
![image](https://user-images.githubusercontent.com/114149527/205111409-7a0c6ec8-1fff-4174-8e10-7f9edf5b829c.png)
На первом графике наглядо видно, что накопления ресурса RollerAgentom значительно превосходит показатели экономики, которые падают после 25.000 итераций. Следовательно требуются корректировки экономики.

На графике два мы видим прямые, поскльку продолжительность эпизодов равноценна для каждого из них.

На оставшихся двух графиках мы наблюдаем темпы снижения ценности игрового ресурса.

- Изменение 1. Замедление персонажа относительно добычи руды и уменшьение разброса показателей. Предположение: возникнет обратная корреляция графиков в пользу Economicy, поскольку игрок будет добыватьи доставлять золото с меньшей эффективностью. Осуществленно 50.000 итераций.

      speedMove = Mathf.Clamp(actionBuffers.ContinuousActions[0], 1.5f, 6f);
      Debug.Log("SpeedMove: " + speedMove);
      timeMining = Mathf.Clamp(actionBuffers.ContinuousActions[1], 1f, 4f);

![image](https://user-images.githubusercontent.com/114149527/205115220-b8bcaa3c-8703-4db5-a81f-2ecfb3c47377.png)
Результаты экспермента частично потверждают данную теорию, но интервальные значения подобраны слишком строго.


- Изменение 2. Изменение показателей влияющих на рост накоплений игрока (profitPercentage, pickaxeСost). Предположение: более лояльное накопление игроком игровой валюты. Итерации 40.000
      
      pickaxeСost = Mathf.Clamp(actionBuffers.ContinuousActions[3], 50f, 1100f);
      Debug.Log("pickaxeСost: " + pickaxeСost);
      profitPercentage = Mathf.Clamp(actionBuffers.ContinuousActions[4], 0.05f, 0.6f);
      
![image](https://user-images.githubusercontent.com/114149527/205129591-6ce1314d-4893-4b48-94f4-53467101bcdc.png)

Исходя из первого графика (Cumulative Reward) можно сделать заключение, что это действительно сказалось на росте благосостояния игрока, но при этом значительно ослабило экономику. Следовательно, для их стабилизации стоит повысить коэфициент инфляции валюты.


- Изменение 3. Снижение негативной стороны обучения RollerAgenta (SetReward(...)) и уменьшение количества получаемого золота (amountGold). Предположение: скажется на первом графике, уменьшив обратную кореляцию между ними. Итерации 40.000
      
      amountGold = Mathf.Clamp(actionBuffers.ContinuousActions[2], 1f, 6f);
      SetReward(0.5f);




## Выводы
Из проделаной работы можно сделать заключение, что наиболее оправданная экономическая модель строится на .... Помимо этого, в данной работе было расмотренно еще однин из смособов использования mlagentф, который упрощает настройку игрового баланса задействуя минимальное количество ресурсов.

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
