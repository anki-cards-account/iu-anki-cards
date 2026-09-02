**Мини-словарь:**
- pipeline — конвейер: разные стадии разных инструкций идут одновременно.
- superscalar — несколько execute-unit'ов: можно запускать больше одной инструкции за такт (через holding buffer).

Milestone: [[OS Lection 1 - введение]]

### Концепт

Как заводской конвейер: пока одна инструкция execute, следующая уже decode, третья — fetch. Superscalar — несколько таких линий плюс буфер. Это **не** несколько ядер и **не** hyper-threading.

### Под капотом

На слайде (Tanenbaum Fig. 1.7):

- **Three-stage pipeline:** Fetch Unit → Decode Unit → Execute Unit. Стадии [[CPU instruction cycle]] перекрываются.
- **Superscalar CPU:** несколько fetch/decode/execute плюс **holding buffer** — CPU может иметь больше одного исполнительного тракта.

Это ускорение **одного** ядра за счёт параллелизма стадий/инструкций. Настоящий параллелизм нескольких полных процессоров — [[Multicore]]. Переключение двух потоков на одном ядре — [[Multithreading]] (не true parallelism).
