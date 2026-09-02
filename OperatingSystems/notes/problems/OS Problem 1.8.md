### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>Одна из причин, почему GUI долго не принимали — стоимость железа, которое их поддерживает.</p><ul><li>Сколько video RAM нужно для монохромного текстового экрана 25 строк × 80 колонок?</li><li>Сколько для bitmap 1200 × 900 пикселей, 24-bit color?</li><li>Какова была цена этой RAM в ценах 1980 (5 $/KiB)?</li><li>Сколько это стоит сейчас?</li></ul></div><div class="lang-en"><p>One reason GUIs were initially slow to be adopted was the cost of the hardware needed to support them.</p><ul><li>How much video RAM is needed to support a 25-line × 80-row character monochrome text screen?</li><li>How much for a 1200 × 900-pixel 24-bit color bitmap?</li><li>What was the cost of this RAM at 1980 prices (5 $/KiB)?</li><li>How much is it now?</li></ul></div></div>

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>Считаем framebuffer: сколько байт, чтобы лежал <i>один</i> кадр. Текст: клетка = 1 байт → 25×80 = <b>2000 байт</b> ≈ 2 KiB → в 1980 при 5 $/KiB это <b>10 $</b>.</p><p>Картинка: 24 бита = 3 байта на пиксель → 1200×900×24 бит = <b>3 240 000 байт</b>. На слайде перевод KB→KiB через 1.024 даёт <b>15 820 $</b> в ценах 1980.</p><p>Смысл пары: текст копеечный, GUI — люкс. «Сколько сейчас» на слайде-ответе <b>не посчитано</b> (в источнике нет числа). Вывод формул: <a class="internal-link" data-href="Framebuffer" href="Framebuffer">Framebuffer</a>.</p></div><div class="lang-en"><p>Count the framebuffer: bytes for <i>one</i> frame. Text: one cell = 1 byte → 25×80 = <b>2000 bytes</b> ≈ 2 KiB → at 5 $/KiB in 1980 that is <b>$10</b>.</p><p>Bitmap: 24 bits = 3 bytes per pixel → 1200×900×24 bits = <b>3,240,000 bytes</b>. The slide converts KB→KiB via 1.024 and gets <b>$15,820</b> at 1980 prices.</p><p>Point of the pair: text is cheap, GUIs were luxury. “How much now” is <b>not computed</b> on the answer slide. Derivation: <a class="internal-link" data-href="Framebuffer" href="Framebuffer">Framebuffer</a>.</p></div></div>

$$
25 \times 80 = 2000\ \text{bytes}
$$

$$
1200 \times 900 \times 24\ \text{bit} = 3\,240\,000\ \text{bytes}, \quad \frac{3240\ \mathrm{KB}}{1.024}\times 5 = \$15\,820
$$

### Resources

- Milestone: [[OS Tutorial 1 - введение]]
- Resources: [[OS_Tutorial01.pdf]]
- AtomicNotes: [[Framebuffer]]
