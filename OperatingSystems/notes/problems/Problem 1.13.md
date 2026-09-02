### Формулировка

<div class="lang-pair">
<input class="lang-sw" type="checkbox" id="p113-q"><label for="p113-q"></label>
<div class="lang-ru">

Система с двумя CPU, на каждом по два потока (hyperthreading). Три программы $P0$, $P1$, $P2$ со временами $5$, $10$ и $20$ msec.

За сколько закончится выполнение? Все программы $100\%$ CPU-bound, не блокируются и не меняют CPU после назначения.

</div>
<div class="lang-en">

Consider a system that has two CPUs, each CPU having two threads (hyperthreading). Suppose three programs, $P0$, $P1$, and $P2$, are started with run times of $5$, $10$ and $20$ msec, respectively.

How long will it take to complete the execution of these programs? Assume that all three programs are $100\%$ CPU bound, do not block during execution, and do not change CPUs once assigned.

</div>
</div>

### Ответ

<div class="lang-pair">
<input class="lang-sw" type="checkbox" id="p113-a"><label for="p113-a"></label>
<div class="lang-ru">

Зависит от назначения на два физических CPU: $20$, $25$, $30$ msec; если все три на одном CPU — до $35$ msec. HT не даёт true parallelism.

</div>
<div class="lang-en">

It depends on placement onto the two physical CPUs: $20$, $25$, or $30$ msec; if all three run on one CPU — up to $35$ msec. Hyperthreading is not true parallelism.

</div>
</div>

### Resources

- Milestone: [[OS Tutorial 1 - введение]]
- Resources: [[OS_Tutorial01.pdf]]
- AtomicNotes: [[Hyperthreading scheduling]]
