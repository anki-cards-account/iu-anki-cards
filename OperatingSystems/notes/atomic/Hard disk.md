**Мини-словарь:**
- platter — пластина HDD.
- track — окружность на пластине; segment — дуга на track.
- sector — адресуемый кусок дорожки (плюс partition/boot — в [[Booting]]).
- seek time — физическая установка головки на нужную дорожку.
- rotation delay (latency) — ожидание, пока нужный сектор доедет до головки.
- transfer time (data rate) — время собственно чтения/записи данных.

Milestone: [[OS Lection 1 - введение]]

### Концепт

HDD — грампластинка с роботом-иглой: сначала доехать головкой (seek), дождаться оборота (latency), потом качать биты (transfer). Поэтому диск в [[Memory hierarchy]] на миллисекундах, а RAM — на наносекундах.

### Под капотом

**Геометрия multi-platter HDD:** platters, actuator arm, read/write head, track, segment (дуга на track), sector.

**Время read/write** складывается из трёх частей:

1. **Seek time** — физическое позиционирование головки.
2. **Rotation delay (latency)** — пока диск довернётся в нужную позицию.
3. **Transfer time (data rate)** — чтение или запись данных.

Связь с ОС как абстракцией диска: [[Extended Machine]] (блоки, не головки). Загрузка с диска: [[Booting]] (boot sector). Шина до диска: [[Bus]] (SCSI, SATA).
