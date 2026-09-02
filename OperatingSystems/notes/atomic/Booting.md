**Мини-словарь:**
- BIOS (Basic Input Output System) — программа на материнской плате с low-level I/O software.
- POST (Power-On Self-Test) — проверка целостности, объёма RAM и базовых устройств.
- boot device — устройство, с которого грузится ОС; список кандидатов в CMOS.
- boot sector — первый сектор boot device; содержит программу, смотрящую partition table.
- secondary boot loader — грузится из **active partition**, затем читает ОС.

Milestone: [[OS Lection 1 - введение]]

### Концепт

Включение — не «сразу Linux». Сначала крошечная программа в ROM тестирует железо, выбирает диск, читает первый сектор, тот находит активный раздел, оттуда второй загрузчик тащит ОС, ОС подхватывает драйверы и рисует login. Цепочка хрупкая: сломай CMOS «boot disk» — не встанешь.

### Под капотом

Порядок с лекции:

1. Стартует **BIOS** (low-level I/O на parent board).
2. BIOS делает **POST**: integrity, сколько RAM, базовые устройства отвечают.
3. Сканирует **buses**, детектит устройства ([[Bus]]).
4. Выбирает **boot device**, перебирая список из **CMOS** ([[Memory types]]).
5. **Boot sector** (first sector boot device) читается в memory и **исполняется**. Обычно смотрит **partition table в конце boot sector** — какая partition **active**.
6. С active partition читается **secondary boot loader**. Он читает ОС с этого раздела и стартует её.
7. ОС **query BIOS** за configuration. Для каждого устройства проверяет, есть ли [[Device driver]].
8. Драйверы грузятся **в kernel**. ОС инициализирует таблицы, создаёт нужные background processes, стартует **login program или GUI**.

Bootstrap loader на части машин лежит в **ROM** ([[Memory types]]). Сама ОС после старта работает в [[Kernel mode]].
