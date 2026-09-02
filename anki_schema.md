# IU Exam — схема Anki

Два **note type** (два clone), не два Card template в одном типе.

Поля одинаковые у обоих:

```
Kind
Question
Answer
Explanation
Milestone
AtomicNotes
```

Порядок: сначала тутор Theory, потом Problem.

---

# Тутор 1 — IU Exam Theory

Карточка: увидел вопрос → перевернул → вопрос + объяснение + Milestone + атомы. **Ничего печатать не надо.** Короткий `Answer` на обороте не рисуем — ответ уже внутри Explanation.

Это **первый** тип. Problem потом клонируется отсюда.

## Зачем отдельный тип

В Anki: **note type** = набор полей. **Cards** = как нарисовать одну карточку из этих полей.

Один clone Basic = один note type. Не добавляй второй Card template внутрь Theory: Anki начнёт штамповать по две карточки на каждую заметку.

## Шаг 1 — создать тип

1. Anki → **Tools** → **Manage Note Types**.
2. **Add** → **Clone: Basic** → OK.
3. Имя: `IU Exam Theory` → OK.

Если тип `IU Exam` уже есть — открой его, **Rename** в `IU Exam Theory`. Не создавай третий.

## Шаг 2 — поля

В Manage Note Types выбери `IU Exam Theory` → **Fields**.

Оставь или переименуй первое поле в `Kind`. Добавь остальные **Add**, порядок сверху вниз строго такой:

```
Kind
Question
Answer
Explanation
Milestone
AtomicNotes
```

Полей `Sources` и `Resource` **нет**. Если они уже есть — удали (сначала убери `{{Sources}}` / `{{Resource}}` из Cards, иначе Anki не даст удалить).

Лишние поля Basic (`Front`, `Back`), если остались — удали, когда все новые уже есть (Anki не даст удалить, если на них ссылается шаблон: сначала поправь Cards, потом удали).

Что в поле:

- `Kind` — всегда `theory`
- `Question` — вопрос (лицо и оборот)
- `Answer` — короткий ответ (для Excel и для Problem type-in; на обороте отдельным блоком не рисуем)
- `Explanation` — обширный разбор
- `Milestone` — wikilink Milestone, `[[OS Lection 1 - введение]]`
- `AtomicNotes` — атомы, без которых на вопрос не ответить: `[[Kernel mode]]; [[System call]]`

Close.

Anki пишет `there is no field called '…'` — поле не создано **в этом** note type. Сначала Add / Rename в Fields, потом Cards. Problem не наследует новые поля от Theory: добавь `AtomicNotes` в оба типа.

## Шаг 3 — окно Cards (Front / Back / Styling)

Выбери `IU Exam Theory` → **Cards**.

Сверху выпадающий список — это **Card 1**, единственный шаблон. Переименовывать не обязательно.

Слева три пункта — три места, куда вставлять текст:


| Куда кликнуть      | Что это            |
| ------------------ | ------------------ |
| **Front Template** | лицо карточки      |
| **Back Template**  | оборот             |
| **Styling**        | CSS на оба стороны |


Справа preview. Внизу **Save**.

### Front Template — вставь целиком, сотри старое

```html
<div class="question">{{Question}}</div>
```

### Back Template — вставь целиком, сотри старое

```html
<div class="question">{{Question}}</div>
<hr>
<div class="explanation">{{Explanation}}</div>
<div class="meta"><span class="label">Milestone</span> {{Milestone}}</div>
<div class="meta"><span class="label">Atoms</span> {{AtomicNotes}}</div>
```

На обороте Theory нет `{{type:Answer}}`: печатать нечего, строка сверки была бы пустой. Нет и жирного `{{Answer}}`.

### Styling — вставь целиком, сотри старое

```css
.card { font-family: sans-serif; font-size: 20px; text-align: left; }
.question { text-align: center; }
.explanation { margin: 0.8em 0; white-space: pre-wrap; }
.meta { margin-top: 0.8em; font-size: 0.85em; opacity: 0.85; }
.label { font-weight: bold; margin-right: 0.4em; }
#typeans { margin: 0.6em auto; }
```

**Save** → закрой Cards.

## Шаг 4 — проверка

**Add** → вверху Type = `IU Exam Theory`. Заполни Question / Answer / Explanation / Milestone / `AtomicNotes` → Preview. Лицо = вопрос по центру, оборот = вопрос + Explanation + Milestone + атомы. Поля ввода на лице нет.

---

# Тутор 2 — IU Exam Problem

Карточка: вопрос + **напечатать короткий ответ** (число, формула, «через 20 msec»). Оборот: вопрос, сверка набора, объяснение, Milestone, атомы. Жирный повтор `{{Answer}}` не рисуем.

Сначала должен существовать `IU Exam Theory` (тутор 1 выше).

## Зачем не Card 2 внутри Theory

Если в одном note type нажать Add Card Type, Anki из **каждой** заметки сделает две карточки (с печатью и без). Для задач нужен **отдельный clone**.

## Шаг 1 — клонировать Theory

1. **Tools** → **Manage Note Types**.
2. Выдели `IU Exam Theory` (не Basic).
3. **Add** → **Clone: IU Exam Theory** → OK.
4. Имя: `IU Exam Problem` → OK.

Поля уже скопированы. Не трогай Fields, если порядок такой:

```
Kind
Question
Answer
Explanation
Milestone
AtomicNotes
```

В Excel для этих карт `Kind` = `problem`.

## Шаг 2 — окно Cards

Выбери `IU Exam Problem` → **Cards**.

Снова три пункта слева: **Front Template**, **Back Template**, **Styling**.

Меняется **только Front** (плюс на обороте `{{type:Answer}}` для сверки набора — это не второй текст ответа, а зелёное/красное сравнение). Styling тот же.

### Front Template — вставь целиком (это единственное отличие лица)

```html
<div class="question">{{Question}}</div>
<br>
{{type:Answer}}
```

`{{type:Answer}}` — поле, куда ты печатаешь. Сверяется с полем `Answer`, не с Explanation.

### Back Template — вставь целиком

```html
<div class="question">{{Question}}</div>
{{type:Answer}}
<hr>
<div class="explanation">{{Explanation}}</div>
<div class="meta"><span class="label">Milestone</span> {{Milestone}}</div>
<div class="meta"><span class="label">Atoms</span> {{AtomicNotes}}</div>
```

`{{type:Answer}}` на обороте — сверка набора (зелёное/красное). Это не второй абзац ответа; отдельный `{{Answer}}` не ставь.

### Styling — должен быть таким

```css
.card { font-family: sans-serif; font-size: 20px; text-align: left; }
.question { text-align: center; }
.explanation { margin: 0.8em 0; white-space: pre-wrap; }
.meta { margin-top: 0.8em; font-size: 0.85em; opacity: 0.85; }
.label { font-weight: bold; margin-right: 0.4em; }
#typeans { margin: 0.6em auto; }
```

## Шаг 3 — проверка

**Add** → Type = `IU Exam Problem`. Question = «За сколько закончатся три процесса?», Answer = `20 msec`, Explanation / Milestone / `AtomicNotes` заполни. Preview: на лице вопрос по центру и строка ввода, на обороте вопрос + сверка + Explanation + Milestone + атомы.

## Импорт

- Теория → note type `IU Exam Theory`, колода например `OS::Tutorial 1`.
- Задачи → note type `IU Exam Problem`, та же или соседняя подколода.
- Родительская колода `OS` схему не хранит, только сгруппирует учёбу.

