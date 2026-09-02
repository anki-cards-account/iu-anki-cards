**Мини-словарь:**
- batch system — пачка задач без интерактива у машины.
- multiprogramming — в памяти несколько задач, CPU переключается, пока одна ждёт I/O.
- timesharing — много пользователей делят машину в интерактиве.
- spooling — буферизация I/O (например, печать) на диск, чтобы CPU не простаивал.

Milestone: [[OS Lection 1 - введение]]

### Концепт

История ОС — это история «кто стоит у машины и как делят железо». От ламп без ОС до смартфонов. На экзамене ждут поколения, железо и **что появилось в ОС**, а не биографию Тьюринга.

### Под капотом

| Поколение | Годы (лекция) | Железо / системы | ОС и программы |
|---|---|---|---|
| 1st | 1945–1955 | vacuum tubes, plug boards; Colossus (Turing), ENIAC (Mauchley) | **No OS**; mechanical language; медленно, огромно, кондиционер, жрут электричество, мало storage |
| 2nd | 1955–1965 | transistors, batch / mainframes; core memory; magnetic tapes & disks | **First OS**; machine language & assembly; меньше, меньше тепла и электричества |
| 3rd, part 1 | 1965–1971 | integrated circuits; SSI & MSI; Honeywell-6000, PDP, IBM-360 и 370/168, TDC-316 | high-level languages; малое потребление |
| 3rd, part 2 | 1971–1980 | microprocessors; LSI & VLSI; RAID; portable computers | data communication; быстрые памяти; parallel processing, VR, multimedia (как область применения) |
| 3rd (сводка слайда) | 1965–1980 | IC + batch/mainframes | **multiprogramming, spooling, timesharing**; пример IBM System/360 |
| 4th | 1980–1990 | personal computers после LSI; Intel 8080 + 8-inch floppy | первый disk OS: **CP/M**; IBM PC, Gates (запрос ОС) |
| 5th | 1990–present | mobile computers | (слайд почти пустой: эпоха мобильных) |

На экзамене часто спрашивают: первое поколение **без ОС**; второе — **первая ОС + batch**; третье — **multiprogramming / timesharing**; четвёртое — **PC и CP/M**.

Связано: типы современных ОС — [[OS Zoo]] (в т.ч. timesharing у mainframe).
