**Мини-словарь:**
- OS zoo — классификация ОС по «какой компьютер / какая нагрузка».
- hard real-time — абсолютная гарантия, что действие случится к дедлайну.
- soft real-time — сорвать дедлайн иногда можно: плохо, но без permanent damage.
- JVM (на smart card) — интерпретатор в ROM карты; на карту качают Java applets.

Milestone: [[OS Lection 1 - введение]]

### Концепт

Не существует одной «ОС вообще». Mainframe живёт пачками I/O-джобов, микроволновка не ставит Steam, датчик в поле считает милливатты. На экзамене — **тип + чем занят + пример из слайда**.

### Под капотом

Типы со слайдов и чем они отличаются:

**Mainframe OS** (OS/390, OS/360). Room-sized машины в data centers. Заточены под **много jobs сразу**, почти все с **огромным I/O**. Сервисы:

- **batch** — рутинные jobs **без** interactive user;
- **transaction-processing** — много мелких запросов;
- **timesharing** — много удалённых пользователей сразу (например, query большой БД).

Связь с историей: timesharing появился в 3rd generation ([[History of OS]]).

**Server OS** — большие PC / workstations / даже mainframes; много пользователей **по сети**, sharing hardware и software. Примеры: Solaris, FreeBSD, Linux, Windows Server (на одном слайде ещё UNIX, Windows 2000).

**Multiprocessor OS** — несколько CPU в одной системе: parallel computers, multicomputers, multiprocessors. Сейчас и PC/ноутбуки — small-scale multiprocessors. Linux, Windows. Связь: [[Multicore]].

**Personal Computer OS** — FreeBSD, Linux, Mac OS X, Windows (на обзорном слайде ещё Windows 98, XP, Mac OS).

**Handheld** — раньше PDA, сейчас mobile: Android, iOS. Это 5th generation ([[History of OS]]).

**Embedded** — компьютеры в приборах, которые **не думают компьютерами** и **не принимают user-installed software**: microwave, MP3, TV, cars. Embedded Linux, QNX, VxWorks.

**Sensor-node** — у узла CPU, RAM, ROM и датчики; связь друг с другом и base station **wireless**. TinyOS.

**Real-time** (пример QNX):

- **hard** — **absolute guarantees**, действие к сроку;
- **soft** — пропуск редкого дедлайна допустим, без permanent damage.

**Smart card** — самые маленькие ОС, CPU на credit-card. Java-oriented: в ROM **интерпретатор JVM**, applets скачиваются и интерпретируются.

Не путать embedded «не ставят софт пользователя» и PC, куда ставят что угодно.
