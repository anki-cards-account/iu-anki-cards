**Мини-словарь:**
- OS — слой ПО: простая модель машины + управление ресурсами.
- kernel / user mode — два режима CPU: полный доступ vs subset инструкций.
- system call (TRAP) — вход из user mode в ядро.
- multiplexing — разделение ресурса во времени или в пространстве.

### Концепт

Путеводитель **Operating Systems, lection 1 — введение**: что такое ОС, два режима, две роли ОС, поколения, железо (CPU, память, диск, I/O, шины), загрузка, зоопарк ОС.

Книга слайдов: Tanenbaum & Bos, *Modern Operating Systems*, 4th ed., главы 1.1–1.4 и 1.8.

```text
железо (CPU, RAM, disk, I/O, bus)
  → BIOS / POST / boot loader
  → kernel (kernel mode): драйверы, таблицы, процессы
  → user programs (user mode) ─TRAP→ сервисы ОС
  → ресурсы делят time/space multiplexing
```

### Карта лекции

#### Что такое ОС и режимы
- [[Operating System]] — слой: чистая модель + управление ресурсами
- [[Kernel mode]] — полный доступ к hardware и любая инструкция
- [[User mode]] — subset инструкций, I/O запрещён
- [[System call]] — TRAP в ядро за услугой ОС

#### Две роли ОС
- [[Extended Machine]] — top-down: абстракции (диск = блоки)
- [[Resource Manager]] — bottom-up: orderly allocation
- [[Multiplexing]] — time (CPU, printer) vs space (memory, disk)

#### История
- [[History of OS]] — 1st–5th generations: от «No OS» до mobile / CP/M / timesharing

#### Процессоры
- [[CPU instruction cycle]] — fetch → decode → operands → execute → write
- [[CPU registers]] — general, PC, SP, PSW (в т.ч. mode)
- [[Instruction pipeline]] — 3 стадии и superscalar
- [[Multithreading]] — HT, не true parallelism
- [[Multicore]] — несколько полных ядер, GPU, true parallelism

#### Память и диск
- [[Memory hierarchy]] — регистры → кэш → RAM → disk
- [[Cache]] — линии 64 B, hit ≈ 2 такта, вопросы eviction
- [[Memory types]] — RAM, ROM, EEPROM, flash, CMOS
- [[Hard disk]] — геометрия HDD; seek + latency + transfer

#### I/O, шины, загрузка
- [[Device driver]] — controller + driver в ядре; port space / MMIO / IN OUT
- [[IO transfer]] — busy waiting, interrupt (+ vector), DMA
- [[Bus]] — shared/parallel/serial, DDR/PCIe/USB, Plug and Play
- [[Booting]] — BIOS → POST → CMOS boot device → sector → secondary loader → kernel

#### Типы ОС
- [[OS Zoo]] — mainframe, server, multiprocessor, PC, handheld, embedded, sensor, RT, smart card

### Sources
- [[OS_Lecture01.pdf]] — Lecture 1: Introduction to Operating Systems; Week 01; Ch. 1.1–1.4 & 1.8
- Практика к этой главе: [[OS Tutorial 1 - введение]], [[OS_Tutorial01.pdf]]
- Tanenbaum & Bos, Modern Operating Systems, 4th edition, 2013 (основа слайдов)
