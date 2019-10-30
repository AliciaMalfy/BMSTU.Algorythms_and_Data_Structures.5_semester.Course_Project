# Задание
```
Напишите программу для составления учебного плана по специальности. Входные данные: список курсов, 
зависимости между ними (например,для АиСД нужно пройти МЛТА), количество часов, количество часов в
курсе, общее количество часов в каждом семестре и т. п. Выходные данные: перечень курсов для
каждого семестра.
```
## Теорретическая часть
Для начала рассмотрим несколько определений, которые будем использовать далее.

*Графом G = (V, E)* называется конечное множество *V* с заданным семейством *E* его двухэлементных подмножеств. Элементы множества *V* называются *вершинами (vertices)*, а элементы множества *E* - *рёбрами (edges)*. Если *v1, v2 ∈ V* и {*v1, v2*} ∈ *E*, то говорят, что вершины *v1* и *v2* смежны. Поэтому граф можно определить также как заданное на множестве *V* бинарное отношение смежности. Это отношение является иррефлексивным и симметричным.

Распространённой стандартной формой задания *n*-вершинного графа является бинарная (*n*x*n*)-*матрица смежности* **A** = ||a[i][j]||, где a[i][j] = a[j][i] = 1, если {v[i], v[j]} ∈ *E*, и a[i][j] = a[j][i] = 0, если {v[i], v[j]} ∉ *E*.

Если вершина *v* инцидентна (смежна) *k* рёбрам, то говорят, что она имеет *степень k* и пишут deg*v=k*.

Помимо простых графов часто рассматриваются так называемые *ориентированные графы* или *орграфы*.
*Орграф* - это пара (*V, A*), где *V* - множество вершин (vertices), а *A* - множество упорядоченных пар вершин, или ориентированных рёбер, которые называются также *дугами* (arcs). Ориентированный граф можно расматривать как иррефлексивное бинарное отношение, т.е. в отличие от обычных графов (неориентированных) опускается условие симметричности.

Если рёбрам графа или дугам орграфа приписаны некоторые действительные числа, как правило, положительные, то их называют *весами*, а граф - *взвешенным графом*.

Взвешенный граф или орграф задаётся матрицей, подобной матрице смежности, в которой вместо соответствующих рёбрам или дугам единиц стоят веса, а нули остаются нулями.

## Краткая иструкция по использованию программы

## Описание логики программы
**Примечание:**
```
На данный момент план примерный. Окончательный будет после написания программы.
```
Зависимость между предметами задаётся в виде ориентированного графа. Данные заносятся в отдельный массив (матрицу смежности), с которым будет вестись работа. 

Общее количество часов в семестре хранится в отдельной переменной.

Количество часов в каждом курсе хранится в контейнере map в виде <ключ> - <значение>, где ключ - название курса, а значение - количество часов в курсе.

В первую очередь в семеcтры, начиная с первого, ставятся те предметы, у которых нет никаких зависимостей. Далее мы их учитывать не будем. Если по количеству часов курсов больше, чем можно уместить в семестр, то оставшиеся переносятся на следующий семестр. Если меньше - то далее распределяем все предметы, у которых одна зависимость. Аналогично, если таких предметов больше, чем можно уместить в семестр, то оставшиеся переносятся на следующий семестр, если меньше - далее рассматриваем курсы с двумя зависимостями и т. д. 

Количество часов в семестре дожно быть примерно одинаковым, но не больше заданного числа. Необходимо это учитывать при распределении курсов. Поэтому (...?).

## Описание всех использованных структур данных и обоснование их выбора

## Описание форматов входных и выходных данных
*Входные данные:* файл, в котором хранится зависимость между курсами в виде таблицы смежности, общее количество часов в семестре и количество часов в каждом курсе, который нужно пройти.

*Выходные данные:* файлв, в котором после компиляции программы будут записаны все семестры и курсы, которые будут изучаться в каждом из них.

## Описание тестов

## Оценка сложности основных алгоритмов программы

## Оценка использования памяти основными алгоритмами
