**Мини-словарь:**
- complement $A'$ или $A^c$ — все исходы из $S$, которых **нет** в $A$; событие «$A$ не произошло».
- relative to $S$ — дополнение всегда относительно выбранного [[Sample space]], не «относительно вселенной».

Milestone: [[Prob Lection 1 - основания]]

### Концепт

Дополнение — переворот да/нет: не «выпало чёт», а «выпало нечёт», если $S$ — грани кости. Сменил $S$ — сменилось и дополнение.

Вероятностный ход: часто легче найти $P(A^c)$, потом $P(A)=1-P(A^c)$ ([[Properties of probability]]).

### Под капотом

Определение: дополнение $A$ относительно $S$ — подмножество элементов $S$, не лежащих в $A$. Обозначения $A'$ или $A^c$.

$$
A^c=\{\omega\in S:\omega\notin A\}
$$

Пример: $S=\{\text{book, cell phone, mp3, paper, stationery, laptop}\}$, $A=\{\text{book, stationery, laptop, paper}\}$ $\Rightarrow$ $A'=\{\text{cell phone, mp3}\}$.

Тождества с дополнением — в [[Event identities]]. Теорема $P(A)+P(A')=1$ — в [[Properties of probability]].
