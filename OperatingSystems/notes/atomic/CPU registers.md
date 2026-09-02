**Мини-словарь:**
- register — сверхбыстрая ячейка **внутри** CPU.
- program counter (PC) — адрес **следующей** инструкции для fetch.
- stack pointer (SP) — указатель на текущий стек в памяти.
- PSW (Program Status Word) — флаги результата сравнений, приоритет CPU, режим (kernel/user) и прочие control bits.

Milestone: [[OS Lection 1 - введение]]

### Концепт

Регистры — карман процессора: переменные и промежуточные результаты не гоняют по шине в RAM. PC — «где мы в программе»; PSW — «в каком мы мире» (в том числе kernel vs user).

### Под капотом

Внутри CPU есть регистры для ключевых переменных и временных результатов:

- **General registers** — переменные и temporary results.
- **Program counter** — адрес **next instruction** для fetch ([[CPU instruction cycle]]).
- **Stack pointer** — текущий stack в memory.
- **PSW** — биты результатов comparison, CPU priority, **mode (kernel or user)**, другие control bits.

Режим в PSW — аппаратная основа [[Kernel mode]] / [[User mode]]. Без смены PSW system call не переключил бы привилегии.
