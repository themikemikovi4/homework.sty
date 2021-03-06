# homework.sty

Для использования этого пакета, поместите следующую строку в преамбулу документа:
```tex
\usepackage{homework}
```
Вы можете испльзовать русскую версию:
```tex
\usepackage[russian]{homework}
```
This package has a number of features. First of all, it looks awesome!
But also, it makes writing down your homework a bit easier.
Этот пакет предоставляет множество возможностей. Прежде всего, ваша домашняя
работа будет выглятеть бесподобно! Но также он упрощает написание домашней работы.

# Полный список возможностей

* *\nset* - красивая буква N (часто используется для обозначения множества натуральных чисел)
* Аналогично предыдущему: *\zset*, *\qset*, *\rset*, *\cset*
* *\comb* - опреатор сочетания. Испльзовать так:
```tex
\comb_n^k % n choose k
```
* *\impl* - бинарный оператор импликации
* *\timesdots* - *\ldots* в русской версии, *\cdots* в базовой
* *\No* - символ №
* окружения *statement* и *statement*\* - используйте для утверждений, на которые вы будете ссылаться.
```tex
\begin{statement}
Простых чисел~--- бесконечно много. \label{sttm:prime}
\end{statement}
... но $p$ не может быть последним простым числом (см. утверждение~\ref{sttm:prime}).
```
*statement* нумеруется, *statement*\* - нет.
* *\homework* - используйте сразу после *\begin{document}*.
У нее три аггумента - имя домашней работы, автор (обязательные), дата (опционально, по умолчанию - *\today*).
* Окружение *problem* - помещайте каждую зачачу внутрь этого окружения. У него один обязательный аргумент - имя задачи.
* *\Definitions*, *\Statement*, *\Proof*, *\Solution* and *\Answer* - используйте перед соответствующей частью задачи.
* Окружение *definitions* - помещайте в него свои определения. *Кажде определение должно нвчинаться с \item*.
```tex
\begin{definitions}
\item $n$ is any natural number
\item $f(n) = \sum_{k=1}n \frac 1 {k!}$
\end{definitions}
```
* Окружение *localdefinitions* - аналогично предыдущему, но не делает *\clearpage*.
* *\DefineNaturalNumberSet* и *\DefineNaturalNumberSetWithIndex* - помещайте внутрь *[local]definitions*, для стандартного определения множества натурльных чисел.
Это полезно, т.к. некоторые любят начинать натуральные числа с единицы, а некоторые - с нуля. У *\DefineNaturalNumberSet* один опционатьный аргумент -
первое натуральное число (по умолчанию 1).
```tex
\begin{definitions}
\DefineNaturalNumberSet[0]
\end{definitions}
```
* *\DefineNChooseK* - аналогично предыдущему.
Это полезно, т.к. существует два способа написать "количество сочетаний из n по k".
* *\QED* - макрос, равный "Что и требовалось доказать.". Если передан опциональный аргумент
то равен "Что и требовалось доказать в #1."

## Только русская версия

* *\asbuk\* * - русские буквы для нумерованного списка.
```tex
\begin{enumerate}[label=\asbuk*]
```
* В Росии принято писать *tg* и *ctg*, а не *tan* и *cot*. Поэтому добавляются операторы *\tg* и *\ctg*.
Также, *\tan* и *\cot* на них заменяются.
* *\leq* и *\geq* выглядят так, как это принято в России.
* *\times* заменяется на *\cdot*.
