**Мини-словарь:**
- tutorial — разбор задач по главе, не новый конспект лекции.
- multiprogramming / time-sharing — несколько программ vs несколько пользователей.

### Концепт

Путеводитель **Operating Systems, tutorial 1 — введение**: те же главы, что лекция 1, но в форме экзаменационных задач (определения, сравнение, расчёт). Пары, потом свои задачи однокурснику.

Книга: Tanenbaum & Bos MOS 4ed, Ch. 1.1–1.4 & 1.8. Теория: [[OS Lection 1 - введение]].

```text
вопрос «что это / сравни / посчитай»
  → две функции ОС, режимы, timesharing
  → VRAM, HT-расписание, среднее время доступа
```

### Карта лекции

#### Определения (уже были на лекции, формулировки туториала)
- [[Operating System]] — две функции: resource management + abstractions from bare metal
- [[Extended Machine]] / [[Resource Manager]] — те же две роли
- [[Kernel mode]] — полный hardware/memory; crash валит PC
- [[User mode]] — нет прямого железа; crash recoverable; [[System call]]

#### Сравнения
- [[Timesharing]] — vs multiprogramming: все TS суть MP, не наоборот
- [[Multiplexing]] — другая ось: time vs space
- [[Multithreading]] / [[Multicore]] — нужны для HT-задачи

#### Расчёт
- [[Framebuffer]] — текст 2000 B vs bitmap $3\,240\,000$ B, цена 1980
- [[Hyperthreading scheduling]] — 2 CPU $\times$ 2 threads, $P0/P1/P2$, итог 20…35 msec
- [[Average access time]] — cache 95% / RAM 99% after miss / disk → $5001.445$ nsec

### Problems

Отдельные файлы в `notes/problems/`. В файле задачи: Формулировка и Ответ — каждый со своим переключателем ru/en; Resources. Длинный разбор — в атомах.

- [[OS Problem 1.1]] — две функции ОС
- [[OS Problem 1.3]] — time-sharing vs multiprogramming
- [[OS Problem 1.8]] — video RAM / цена 1980
- [[OS Problem 1.10]] — kernel vs user, зачем два режима
- [[OS Problem 1.13]] — 2 CPU $\times$ 2 HT, три программы
- [[OS Problem 1.15]] — average access time cache/RAM/disk

Часть 2 туториала (придумать 3+2+1 задач однокурснику) — педагогика пары, не факты курса.

### Sources
- [[OS_Tutorial01.pdf]] — Tutorial 1 (OS): Introduction; Moodle Tutorial 01
- Tanenbaum & Bos, Modern Operating Systems, 4th ed., Ch. 1.1–1.4 & 1.8
