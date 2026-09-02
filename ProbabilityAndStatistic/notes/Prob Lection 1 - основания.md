**Мини-словарь:**
- sample space $S$ — множество всех исходов случайного эксперимента.
- event — подмножество $A\subseteq S$; позже вероятности живут на $\sigma$-алгебре $\mathcal{F}$.
- probability measure $P$ — функция $\mathcal{F}\to[0,1]$ с тремя аксиомами Колмогорова.

### Концепт

Путеводитель **Probability and Statistics, lection 1 — основания**: случайный эксперимент → пространство исходов → события и операции → относительная частота → аксиомы $P$ → классическая и геометрическая вероятность → зачем $\sigma$-алгебра.

Курс: Nasibullin, Lecture 1: Foundations, Fall 2026.

```text
random experiment
  → S (исходы) → события (подмножества / элементы F)
  → операции ∩ ∪ ′ \
  → P: аксиомы → следствия (пустое, дополнение, inclusion-exclusion)
  → спецслучаи: equally likely, geometric
```

### Карта лекции

#### Язык эксперимента
- [[Random experiment]] — что считается случайным опытом и его исходами
- [[Empirical probability]] — относительная частота, стабилизация при $n\to\infty$
- [[Sample space]] — $S$; конечное / счётное / несчётное; выбор $S$ не единственен
- [[Event]] — $A\subseteq S$; происходит, если $\omega\in A$; пустое и достоверное

#### Операции
- [[Intersection of events]] — оба произошли
- [[Union of events]] — хотя бы одно
- [[Complement]] — событие не произошло
- [[Mutually exclusive events]] — $A\cap B=\emptyset$
- [[Event identities]] — пустое/полное, двойное дополнение, де Морган

#### Вероятность
- [[Kolmogorov axioms]] — неотрицательность, $P(S)=1$, счётная аддитивность
- [[Probability space]] — тройка $(S,\mathcal{F},P)$
- [[Sigma-algebra]] — какие множества вообще получают $P$
- [[Properties of probability]] — $P(\emptyset)=0$, конечная аддитивность, дополнение, монотонность, union bound
- [[Inclusion-exclusion]] — два и три события
- [[Classical probability]] — equally likely, $n/N$; ограничение
- [[Geometric probability]] — отношение мер; встреча Alice и Bob

### Problems
- [[Prob Example 1]] — две монеты, хотя бы один орёл
- [[Prob Example 2]] — шулерская кость, $P(E)$ для числа $<4$
- [[Prob Example 3]] — та же кость, $P(A\cup B)$ и $P(A\cap B)$
- [[Prob Example 4]] — выбор студента в классе
- [[Prob Example 5]] — офферы двух компаний
- [[Prob Example 6]] — сумма 7 или 11 на двух костях
- [[Prob Example 7]] — механик, хотя бы 5 машин
- [[Prob Example 8]] — геометрическая встреча за 15 минут

### Sources
- [[Prob_Lecture01.pdf]] — Lecture 1: Foundations; курс [F26] Probability and Statistics
