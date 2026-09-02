**Мини-словарь:**
- multithreading (hyper-threading) — CPU хранит состояние **двух** (или более) потоков и переключается между ними за наносекунды.
- thread — поток выполнения; на слайде пул T0…T5 у приложений.

Milestone: [[OS Lection 1 - введение]]

### Концепт

Поток ушёл читать слово из памяти (долго). Обычный CPU стопорится. Hyper-threading: «у меня уже заряжен второй поток — переключаюсь». Это **экономия простоя**, не два полноценных ядра.

### Под капотом

**Multithreading / hyper-threading:**

- CPU держит **state of two different threads** и переключается за **nanoseconds**.
- Если процесс должен **read a word from memory** (долгая операция), multithreaded CPU переключается на **другой thread** и экономит время.
- Ключевая фраза лекции: **multithreading does not offer true parallelism**.

На схеме: обычный multithreading — один CPU, потоки по времени; HT — два logical processors (LP0/LP1), «2 threads per processor».

True parallelism — [[Multicore]] (несколько complete processors) и GPU с тысячами tiny cores. Конвейер внутри ядра — [[Instruction pipeline]].
