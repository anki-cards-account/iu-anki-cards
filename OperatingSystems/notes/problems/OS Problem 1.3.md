### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>В чём разница между time-sharing и multiprogramming системами?</p></div><div class="lang-en"><p>What is the difference between time-sharing and multiprogramming systems?</p></div></div>

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p><b>Multiprogramming</b> — в одной машине <i>одновременно живут несколько программ</i>. Цель: пока одна ждёт диск, CPU крутит другую. Пользователей за экраном может не быть (пачка jobs).</p><p><b>Time-sharing</b> — ресурсы делят <i>несколько пользователей сразу</i>, обычно интерактивно. Каждый думает, что машина «его».</p><p><b>Следствие:</b> любая TS-система есть MP (несколько людей ⇒ несколько программ). Не любая MP есть TS: пакетная система крутит несколько jobs без интерактива.</p><p>Не путать с multiplexing (time vs space у одного ресурса). Разбор: <a class="internal-link" data-href="Timesharing" href="Timesharing">Timesharing</a>.</p></div><div class="lang-en"><p><b>Multiprogramming</b> — several programs reside on one computer <i>at the same time</i>. Goal: while one waits for disk, the CPU runs another. There need not be interactive users (a batch of jobs is enough).</p><p><b>Time-sharing</b> — computing resources are shared among <i>several users at the same time</i>, usually interactively. Each user thinks the machine is theirs.</p><p><b>Consequence:</b> every TS system is MP (several people ⇒ several programs). Not every MP system is TS: a batch system can run several jobs with no interactive users.</p><p>Do not confuse with multiplexing (time vs space for one resource). Details: <a class="internal-link" data-href="Timesharing" href="Timesharing">Timesharing</a>.</p></div></div>

### Resources

- Milestone: [[OS Tutorial 1 - введение]]
- Resources: [[OS_Tutorial01.pdf]]
- AtomicNotes: [[Timesharing]]
