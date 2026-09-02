### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>В системе есть кэш, основная память (RAM) и диск; ОС использует виртуальную память. Доступ к слову: 1 нс из кэша, 10 нс из RAM, 10 мс с диска.</p><p>Hit rate кэша 95%, hit rate RAM (после промаха кэша) 99%. Каково среднее время доступа к слову?</p></div><div class="lang-en"><p>A computer system has cache memory, main memory (RAM) and disk, and an operating system that uses virtual memory. It takes 1 nsec to access a word from the cache, 10 nsec from the RAM, and 10 ms from the disk.</p><p>If the cache hit rate is 95% and main memory hit rate (after a cache miss) is 99%, what is the average time to access a word?</p></div></div>

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>Не складывать 1+10+10 000 000 и делить на 3. Среднее — <i>взвешенная</i> сумма трёх непересекающихся случаев. 99% у RAM считаются <b>от промахов кэша</b> (это 5% всех обращений), не от всех подряд.</p><p>Кэш: 95% × 1 нс. RAM: 5% × 99% × 10 нс. Диск: 5% × 1% × 10 000 000 нс (10 мс = 10 000 000 нс). Итого <b>5001.445 нс</b> ≈ 5.001 мкс. Почти всё среднее даёт редкий диск (5000 нс).</p><p>Разбор символов: <a class="internal-link" data-href="Average access time" href="Average access time">Average access time</a>.</p></div><div class="lang-en"><p>Do not average 1+10+10,000,000. The mean is a <i>weighted</i> sum of three disjoint cases. The 99% RAM hit rate is among <b>cache misses</b> (5% of all references), not among all references.</p><p>Cache: 95% × 1 ns. RAM: 5% × 99% × 10 ns. Disk: 5% × 1% × 10,000,000 ns (10 ms = 10,000,000 ns). Total <b>5001.445 ns</b> ≈ 5.001 µs. Almost all of that is the rare disk term (5000 ns).</p><p>Symbols: <a class="internal-link" data-href="Average access time" href="Average access time">Average access time</a>.</p></div></div>

$$
T = 0.95\times 1 + 0.05\times 0.99\times 10 + 0.05\times 0.01\times 10\,000\,000 = 5001.445\ \mathrm{nsec}
$$

### Resources

- Milestone: [[OS Tutorial 1 - введение]]
- Resources: [[OS_Tutorial01.pdf]]
- AtomicNotes: [[Average access time]]
