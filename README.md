# Java Developer Tinkoff

Вступительные испытания на учебный курс от Финтеха (Тинькофф Образование)

[Подать заявку](https://fintech.tinkoff.ru/study/fintech/java/?utm_source=telegram_fintech&utm_medium=smm.unp&utm_campaign=fintech.java_osen2023&dsp_click_id=3efb4829-60a3-440f-8cf9-951c51ff571b)

## Tasks

|#|Description|Difficulty|Tag|Solution|
|--:|---|---|---|---|
|1|[The first task](the-first-task)|---|---|Java|
|2|---|---|---|---|
|3|---|---|---|---|
|4|---|---|---|---|
|5|---|---|---|---|

## [The first task](the-first-task)

|Ограничение времени|Ограничение памяти|
|---|---|
|1 секунда|256 МБ|

Пин часто ассистирует в лаборатории Лосяша. Они проводят то химические, то физические
эксперименты. Разумеется, каждый эксперимент требуется для улучшения бытовых условия всех
Смешариков. В этот раз они проводят эксперимент с новым видом мха.

Можно считать, что эксперимент проводится на бесконечной клетчатой сетке, каждая клетка может
быть занята или не занята мхом. Об этом мхе известно следующее:

1. Спустя минуту мох размножается и занимает все соседние клетки, где он до этого еще не
вырастал.

2. Сразу после этого мох умирает и больше не растет в этой клетке никогда.
   
Соответственно, каждую минуту мох разрастается по соседним клеткам (клетки считаются
соседними, если у них есть общая сторона, таким образом у каждой клетки ровно 4 соседних
клетки), после чего моментально умирает и эту клетку больше никогда не займет мох.

Лосяша интересует количество занятых мхом клеток на n-й минуте эксперимента.

*Формат входных данных*

Единственная строка содержит целое число n (1 ≤ n ≤ 10^8) - номер минуты от начала
эксперимента. Для примера, n = 1 означает «первую» минуту, то есть отрезок времени длиной в
минуту, начинающийся от самого начала эксперимента.

*Формат выходных данных*

Выведите единственное число - количество занятых мхом клеток на n-й минуте эксперимента.

### Примеры данных
|Пример 1||
|---|---|
|Ввод|Вывод|
|1|1|

|Пример 2||
|---|---|
|Ввод|Вывод|
|2|4|

|Пример 3||
|---|---|
|Ввод|Вывод|
|6|20|


