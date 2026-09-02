**Мини-словарь:**
- De Morgan — $(A\cap B)'=A'\cup B'$ и $(A\cup B)'=A'\cap B'$.
- involution — $(A')'=A$: два дополнения возвращают множество.
- set difference $A\setminus B$ — $A$ произошло, $B$ нет: $\{\omega\in A:\omega\notin B\}$.

Milestone: [[Prob Lection 1 - основания]]

### Концепт

Это алгебра событий как множеств: пустое «съедает» пересечение, с дополнением даёт $S$, де Морган переворачивает «и» в «или». На экзамене просят равенство, не картинку. Картинка Венна только подсказка.

Разность $A\setminus B$ — отдельная операция со слайда «оба произошли / хотя бы одно / не A»: «A, но не B».

### Под капотом

Равенства лекции (относительно одного $S$):

1. $A\cap\emptyset=\emptyset$
2. $A\cup\emptyset=A$
3. $A\cap A'=\emptyset$
4. $A\cup A'=S$
5. $S'=\emptyset$
6. $\emptyset'=S$
7. $(A')'=A$
8. $(A\cap B)'=A'\cup B'$
9. $(A\cup B)'=A'\cap B'$

Разность: $A\setminus B=\{\omega\in A:\omega\notin B\}$.

Связанные атомы: [[Complement]], [[Intersection of events]], [[Union of events]].
