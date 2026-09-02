### Формулировка

<div class="lang-pair">
<input class="lang-sw" type="checkbox" id="p115-q"><label for="p115-q"></label>
<div class="lang-ru">

В системе есть кэш, основная память (RAM) и диск; ОС использует виртуальную память. Доступ к слову: $1$ нс из кэша, $10$ нс из RAM, $10$ мс с диска.

Hit rate кэша $95\%$, hit rate RAM (после промаха кэша) $99\%$. Каково среднее время доступа к слову?

</div>
<div class="lang-en">

A computer system has cache memory, main memory (RAM) and disk, and an operating system that uses virtual memory. It takes $1$ nsec to access a word from the cache, $10$ nsec from the RAM, and $10$ ms from the disk.

If the cache hit rate is $95\%$ and main memory hit rate (after a cache miss) is $99\%$, what is the average time to access a word?

</div>
</div>

### Ответ

<div class="lang-pair">
<input class="lang-sw" type="checkbox" id="p115-a"><label for="p115-a"></label>
<div class="lang-ru">

$5001.445$ нс $= 5.001445\ \mu\mathrm{s}$

($0.95\times 1 + 0.05\times 0.99\times 10 + 0.05\times 0.01\times 10\,000\,000$).

</div>
<div class="lang-en">

$5001.445$ nsec $= 5.001445\ \mu\mathrm{s}$

($0.95\times 1 + 0.05\times 0.99\times 10 + 0.05\times 0.01\times 10\,000\,000$).

</div>
</div>

### Resources

- Milestone: [[OS Tutorial 1 - введение]]
- Resources: [[OS_Tutorial01.pdf]]
- AtomicNotes: [[Average access time]]
