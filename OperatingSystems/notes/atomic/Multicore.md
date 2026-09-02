**Мини-словарь:**
- core — полный процессор на одном чипе.
- GPU (Graphics Processing Unit) — процессор с тысячами tiny cores под мелкий параллелизм (полигоны и т.п.).
- L1 / L2 cache — уровни кэша у ядер; на слайде shared L2 vs separate L2.

Milestone: [[OS Lection 1 - введение]]

### Концепт

Не «два потока притворяются ядром», а **несколько настоящих CPU** на кристалле. ОС должна уметь планировать multiprocessor. GPU — другой зверь: тысячи слабых ядер, зато массово.

### Под капотом

- Многие CPU chips содержат несколько **complete processors or cores**. Чтобы ими пользоваться, нужна **multiprocessor OS**.
- Современный **GPU** — процессор с **thousands of tiny cores**, хорош для многих маленьких вычислений **in parallel** (rendering polygons).
- Формулировка лекции: **multicore chips do true parallelism** (в отличие от [[Multithreading]]).

Две раскладки quad-core (Fig. слайда):

- (a) четыре ядра, у каждого L1, **общий L2**;
- (b) четыре ядра, у каждого L1 и **свой L2**.

Связано: кэш вообще — [[Cache]]; типы ОС под много CPU — [[OS Zoo]] (multiprocessor OS).
