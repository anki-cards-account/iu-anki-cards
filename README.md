# IU Anki Cards — заметки 2 курса, 1 семестр

Это **хранилище курса**, не «папка со слайдами». Цель: по лекциям Innopolis University собрать ответы, которые можно сказать на экзамене, и те же факты положить в Anki.

Репозиторий: [anki-cards-account/iu-anki-cards](https://github.com/anki-cards-account/iu-anki-cards). Локально это vault Obsidian (`2Year_1semester_notes`).

## Зачем это нужно

Слайд с Moodle сам по себе не закрывает экзамен: в нём много воды, нумерации «как на паре» и дыр («сверху вниз» — от кого к кому?). Здесь материал **сжимается в факты** и режется на атомы.

После чтения заметки не должно оставаться «это что значит?». Карточка Anki — уже не конспект лекции, а **один устный вопрос**. Правка объяснения в заметке не обязана пересобирать колоду, если формулировка Question стабильна.

## Что лежит в репо

Шесть предметов (седьмую папку не заводим):

| Папка | Префикс | Колода Anki |
|---|---|---|
| `OperatingSystems/` | OS | `Inno_2course_1semester::OperatingSystems` |
| `DifferentialEquations/` | DIFF | `Inno_2course_1semester::Differential Equations` |
| `ProbabilityAndStatistic/` | Prob | `Inno_2course_1semester::ProbaStat` |
| `IntroToAI/` | IAI | `Inno_2course_1semester::IntroToAI` |
| `IntroToOptimization/` | ITO | `Inno_2course_1semester::IntroToOptimization` |
| `Physics/` | Physic | `Inno_2course_1semester::Physics` |

Внутри предмета:

```
<Subject>/
  notes/                 ← Milestone: карта одной лекции / туториала
  notes/atomic/          ← одна тема = один файл
  notes/problems/        ← один вопрос источника (задача, Example)
  notes/anki_cards/      ← таблица карточек (xlsx) + соседний .md
  sources/               ← PDF/видео с Moodle
```

В корне: [`anki_schema.md`](anki_schema.md) — как устроены note type в Anki (туторы Theory и Problem). Схему в папки предметов не копируем.

**Сейчас в vault уже есть** конспекты и карточки по OS (лекция 1 + туториал 1), дифференциальным уравнениям (глава 1 / введения) и Probability and Statistics (Lecture 1: Foundations). Остальные предметы — те же папки, материал появится по мере лекций.

## Как читать заметки

- Текст на русском, имена атомарных файлов — English термин (`Kernel mode.md`, `Sample space.md`).
- Wikilink без `.md`: `[[Kernel mode]]`.
- Математика только `$...$` / `$$...$$`.
- **Milestone** — оглавление лекции, не полный конспект.
- **Atomic** — один экзаменационный вопрос / одна узкая тема.
- **Problem / Example** — формулировка и ответ на *этот* вопрос источника, с переключателем ru/en.

Цепочка обычной работы: PDF в `sources/` → Milestone + атомы (+ problems, если в PDF есть задачи) → карточки Anki → markdown-копия таблицы рядом с xlsx.

## Anki: два тутора

Карточки экзамена живут в двух **note type** (два клона Basic), не в двух шаблонах одной заметки.

Полная пошаговая инструкция — тутор в репозитории:

**[anki_schema.md](https://github.com/anki-cards-account/iu-anki-cards/blob/main/anki_schema.md)** — «IU Exam»: поля, HTML лица/оборота, CSS.

Кратко, что делает каждый тутор:

1. **IU Exam Theory** — увидел вопрос, перевернул, читаешь объяснение + ссылки на Milestone и атомы. Печатать ничего не надо. Поле `Kind` = `theory`.
2. **IU Exam Problem** — клон Theory; на лице ещё строка ввода `{{type:Answer}}` (число, формула, короткое имя). `Kind` = `problem`.

Одинаковые поля у обоих: `Kind`, `Question`, `Answer`, `Explanation`, `Milestone`, `AtomicNotes`.

Качество формулировок — правила SuperMemo «20 rules of formulating knowledge» (одна карточка = один факт, без списков на одну карту): [Twenty rules of formulating knowledge](https://www.supermemo.com/en/blog/twenty-rules-of-formulating-knowledge).

Таблицы карточек: `<Milestone>_anki_cards.xlsx` на связку лекция+атомы и общий `<Prefix> general_table.xlsx` на предмет. Рядом те же имена с расширением `.md` (удобно читать в git без Excel).

Чтобы залить колоду, Anki должен быть открыт (AnkiConnect / MCP). Без Anki таблицы всё равно лежат в `notes/anki_cards/`.

## Чего в git нет

Локальные правила Cursor, скрипты skills и пароль Moodle **не публикуются**: `.cursor/`, `*.local.env`. Их нет в этом репозитории специально.
