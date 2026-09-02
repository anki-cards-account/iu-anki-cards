**Мини-словарь:**
- mutually exclusive (disjoint) — $A\cap B=\emptyset$: нет общего исхода, не могут произойти вместе.
- disjoint vs independent — в этой лекции независимости нет. Непересекающиеся $\neq$ «не влияют друг на друга».

Milestone: [[Prob Lection 1 - основания]]

### Концепт

Два события несовместны, если им нечем делиться в $S$: ни один исход не отмечает оба. Канал NBC и канал CBS на одном включённом ТВ без выбора — в примере лекции программы не пересекаются.

Это про **множества**, не про «маловероятно оба». Пустое пересечение $\Rightarrow$ в [[Inclusion-exclusion]] вычитаемый член ноль $\Rightarrow$ $P(A\cup B)=P(A)+P(B)$. Аксиома 3 [[Kolmogorov axioms]] как раз про счётную сумму **таких** событий.

### Под капотом

Определение: $A$ и $B$ mutually exclusive / disjoint, если $A\cap B=\emptyset$.

Пример TV: $A$ — программа NBC, $B$ — CBS; общих программ нет, $A\cap B$ пусто.

Следствие для вероятности ([[Inclusion-exclusion]]):

$$
P(A\cup B)=P(A)+P(B)\quad\text{если }A\cap B=\emptyset
$$

потому что $P(A\cap B)=P(\emptyset)=0$.
