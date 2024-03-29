# Java Developer Tinkoff

Вступительные испытания на учебный курс от Финтеха (Тинькофф Образование)

[Подать заявку](https://fintech.tinkoff.ru/study/fintech/java/?utm_source=telegram_fintech&utm_medium=smm.unp&utm_campaign=fintech.java_osen2023&dsp_click_id=3efb4829-60a3-440f-8cf9-951c51ff571b)

## Tasks

|#|Description|Difficulty|Tag|Solution|
|--:|---|---|---|---|
|1|[The first task](#the-first-task)|---|---|Java|
|2|[The second task](#the-second-task)|---|---|Java|
|3|[The third task](#the-third-task)|---|---|Java|
|4|[The fourth task](#the-fourth-task)|---|---|Java|
|5|[The fifth task](#the-fifth-task)|---|---|Java|

## The first task

|Ограничение времени|Ограничение памяти|
|---|---|
|1 секунда|256 МБ|

Пин часто ассистирует в лаборатории Лосяша. Они проводят то химические, то физические
эксперименты. Разумеется, каждый эксперимент требуется для улучшения бытовых условия всех Смешариков. В этот раз они проводят эксперимент с новым видом мха.

Можно считать, что эксперимент проводится на бесконечной клетчатой сетке, каждая клетка может быть занята или не занята мхом. Об этом мхе известно следующее:

1. Спустя минуту мох размножается и занимает все соседние клетки, где он до этого еще не
вырастал.

2. Сразу после этого мох умирает и больше не растет в этой клетке никогда.
   
Соответственно, каждую минуту мох разрастается по соседним клеткам (клетки считаются соседними, если у них есть общая сторона, таким образом у каждой клетки ровно 4 соседних клетки), после чего моментально умирает и эту клетку больше никогда не займет мох.

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

### ***Java***

```java

public class Main {
    public static void main(String[] args) {
        int n = 2;
        int p = 0;

        if (n > 1){
            p = (n - 1) * 4;
        } else {
            p = n;
        }

        System.out.println(p);
    }
}
```

## The second task
|Ограничение времени|Ограничение памяти|
|---|---|
|2 секунда|256 МБ|


После окончания кардебалета Ёжик решил записать в книжечку натуральные числа на клеточном тетрадном листе по специальному правилу. Он начинает с числа 1 в левом верхнем углу и затем продолжает по диагоналям: справа от первого числа он записывает 2, а под ним - 3. На следующей
диагонали будут числа 4, 5 и 6, и так далее.

Предположим, что ширина листа составляет n клеток, а высота равна m клеткам. Ваша задача помочь Ёжику и показать, как будут записаны числа!

*Формат входных данных*

В единственной строке ввода через пробел записаны числа n и m (1 ≤ n, m ≤ 2 * 10^5; 1 ≤ n * m ≤ 2 * 10^5) - размеры листа из книжечки.

*Формат выходных данных*

Выведите все натуральные числа от 1 до n * m в указанном формате, разделяя числа в одной строке пробелами, а между строками - переводами строки.

### Примеры данных
|Пример 1||
|---|---|
|Ввод|Вывод|
|3 3|1 2 4|
||3 5 7|
||6 8 9|

|Пример 2||
|---|---|
|Ввод|Вывод|
|4 3|1 2 4 7|
||3 5 8 10|
||6 9 11 12|

## The third task

|Ограничение времени|Ограничение памяти|
|---|---|
|2 секунды|256 МБ|

Пин очень любит свою мастерскую, ведь именно здесь он разработал и собрал так много полезных для Смешариков вещей - например, железную няню. Мастерская Пина имеет полки, пронумерованные от 1 до n. Когда Пин хочет положить деталь на полку - он всегда выбирает свободную полку с наименьшим номером, чтобы не ходить далеко от рабочего стола. Для удобства Пин нумерует все свои детали целыми числами.

Вам предстоит написать программу, которая будет обрабатывать m событий. Каждое событие может быть либо «Пин положил деталь с номером Х», либо «Пин взял с полки деталь с номером Х». Для каждого события первого типа требуется определить номер полки, на которую Пин положит деталь.

Обратите внимание, что в мастерской у Пина всегда есть свободные полки, и ситуации, когда все полки заняты, не возникает.

*Формат входных данных*

В первой строке вводится число m (1 ≤ m ≤ 2 * 10^5) - число событий. Далее следуют m строк, описывающих события. Каждая деталь задаётся номером - числом от 1 до 10^5. Событие « + Х» означает, что Пин положил деталь с номером Х, событие «- Х» - что деталь убрали и полка стала свободной. В нулевой момент времени все полки свободны.

*Формат выходных данных*

Для каждого события «Пин положил деталь» выведите номер полки, на которую её положили, в том порядке, в котором эти события происходили.

### Примеры данных

|Ввод|Вывод|
|---|---|
|8|1|
|+ 11|2|
|+ 1|1|
|- 11|1|
|+ 2|3|
|- 2||
|+ 3||
|+ 2||
|- 1|| 

## The fourth task

|Ограничение времени|Ограничение памяти|
|---|---|
|2 секунды|64 МБ|

Сегодня Нюша и Бараш отдыхают на берегу моря. Нюша написала на песке математическое выражение, поставив в конце точку, а Барашу стало интересно, можно ли получившееся выражение вычислить.

Помогите Барашу вычислить значение выражения или скажите, содержится ли в нем ошибка. В правильном выражении могут встречаться числа, а также знаки сложения, вычитания, умножения и скобки. Приоритет операций стандартный. Все числа в выражении целые и принадлежат диапазону [-2^63; 2^63 - 1].

Также гарантируется, что все промежуточные вычисления умещаются в этот тип. Унарный плюс и унарный минус в выражении встречаться не могут, как и два знака подряд.

*Формат входных данных*

Единственная строка ввода содержит заданное выражение. Его длина не превосходит 100 знаков. Гарантируется, что выражение заканчивается точкой.

*Формат выходных данных*

Выведите значение этого выражения или слово «WRONG» (без кавычек), если значение не определено.

### Примеры данных

|Пример 1||
|---|---|
|Ввод|Вывод|
| 1+(2*2-3). | 2 |

|Пример 2||
|---|---|
|Ввод|Вывод|
| 1+a+1. | WRONG |

## The fifth task

|Ограничение времени|Ограничение памяти|
|---|---|
|2 секунды|64 МБ|

Место жительства Смешариков представляет из себя поселение, состоящее из N домиков, пронумерованных от 1 до N. Каждый из них соединен двунаправленными дорожками с некоторыми другими. При этом между любыми двумя домами существует не более одной прямой дорожки. В ясную погоду из любого домика можно попасть в любой другой. Однако из-за затяжного ливня некоторые дорожки начали затапливаться. Каждая дорожка в поселении имеет свою высоту над уровнем моря. Дорожка считается затопленной, если высота подтопления больше или равна высоте самой дорожки.

Смешарики очень любят ходить друг к другу в гости, а особенно собираться вместе. Поэтому они очень сильно расстроятся, если кто-то не сможет прийти. Помогите им определить минимальный уровень воды над уровнем моря, при котором найдутся такие два домика, что от одного из них нельзя добраться до другого.

*Формат входных данных*

В первой строке даны два числа N и M (2 ≤ N ≤ 10^4; 1 ≤ M ≤ 2 * 10^4) - количество домиков и дорожек соответственно. Следующие M строк содержат тройки чисел s(i) f(i), h(i) (1 ≤ s(i) ≤ N; 1 ≤ f(i) N; 1 ≤ h(i) ≤ 10^6) - описания дорожек, где s(i) и f(i) - номера домиков, которые соединяет i-я
дорожка, а h(i) - её высота над уровнем моря.

*Формат выходных данных*

Выведите минимальную высоту, на которую должна подняться вода, чтобы в поселении нашлось хотя бы два домика, между которыми нельзя пройти (в том числе через другие домики).

### Примеры данных

|Пример 1||
|---|---|
|Ввод|Вывод|
| 2 1 | 100 |
| 1 2 100 ||

|Пример 2||
|---|---|
|Ввод|Вывод|
| 4 5 | 300 |
| 1 2 100 ||
| 1 3 400 ||
| 2 3 300 ||
| 2 4 200 ||
| 3 4 500 ||
