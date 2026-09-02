**Мини-словарь:**
- busy waiting (polling) — драйвер крутит цикл, пока устройство не закончит; CPU занят ожиданием.
- interrupt — устройство само сигналит о конце; ОС может заняться другой работой.
- interrupt vector — кусок памяти: номер устройства → адрес interrupt handler.
- DMA (Direct Memory Access) — чип гоняет биты между memory и контроллером **без постоянного участия CPU**.

Milestone: [[OS Lection 1 - введение]]

### Концепт

Три способа I/O — три ответа на вопрос «кто сторожит окончание передачи». CPU в цикле (глупо, но просто), устройство орёт прерыванием (CPU свободен), отдельный DMA-чип возит байты сам (CPU программирует и забывает).

### Под капотом

Три способа (после того как [[Device driver]] стартовал операцию):

**1. Busy waiting**

Драйвер стартует I/O и сидит в tight loop, **polling** устройство. Минус: **CPU занят опросом**, пока устройство не закончит.

**2. Interrupt**

Драйвер стартует устройство и просит **interrupt when finished**. ОС блокирует caller при необходимости и ищет другую работу. Когда контроллер видит конец transfer, генерирует interrupt. Номер устройства может быть индексом в памяти к адресу handler — это **interrupt vector**.

Шаги на слайде: старт I/O → interrupt → dispatch to handler → return к user program. Участники: CPU, interrupt controller, disk controller, disk drive.

**3. DMA**

DMA-чип контролирует поток битов **memory ↔ controller** без постоянной опеки CPU. CPU **программирует** DMA (что и куда), отпускает. По завершении DMA вызывает **interrupt** (дальше как в п. 2).

Цепочка на слайде: CPU programs DMA → DMA request transfer to memory → data transferred → interrupt when done.

Связано: без [[Kernel mode]] драйвер не стартует устройство. Диск как цель — [[Hard disk]].
