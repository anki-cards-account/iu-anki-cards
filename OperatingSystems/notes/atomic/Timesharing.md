**Мини-словарь:**
- multiprogramming — на одном компьютере одновременно размещены несколько программ (CPU не простаивает, пока одна ждёт).
- time-sharing — вычислительные ресурсы делят **несколько пользователей одновременно** (интерактив).

Milestone: [[OS Tutorial 1 - введение]]
Problem: [[Problem 1.3]]

### Концепт

Multiprogramming — про **несколько программ в машине**. Time-sharing — про **нескольких людей за раз**. Все time-sharing системы — multiprogramming, но не наоборот: можно грузить пачку jobs без интерактива.

### Под капотом

Ответ туториала (problem 1.3):

- **Multiprogramming** = allocation of multiple programs on one computer **simultaneously**.
- **Time-sharing** = sharing of computing resources among **several users at the same time**.
- **Все** timesharing-системы суть multiprogramming-системы, **но не все** multiprogramming-системы — timesharing.

Не путать с [[Multiplexing]]: там оси time vs space (CPU/принтер vs память/диск). Time-sharing — частный случай разделения CPU во времени между **пользователями**. История: timesharing в 3rd generation ([[History of OS]]), сервис mainframe ([[OS Zoo]]).
