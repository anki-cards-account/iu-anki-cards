### Формулировка

<div class="lang-pair">
<input class="lang-sw" type="checkbox" id="p110-q"><label for="p110-q"></label>
<div class="lang-ru">

- Что такое kernel mode?
- Чем kernel mode отличается от user mode?
- Как два режима помогают проектировать операционную систему?

</div>
<div class="lang-en">

- What is kernel mode?
- What is the difference between kernel and user mode?
- Explain how having two distinct modes aids in designing an operating system.

</div>
</div>

### Ответ

<div class="lang-pair">
<input class="lang-sw" type="checkbox" id="p110-a"><label for="p110-a"></label>
<div class="lang-ru">

Kernel mode — полный доступ к hardware, любая инструкция и любой адрес; crash валит PC. User mode — только subset инструкций, I/O и управление машиной запрещены; crash recoverable. Два режима изолируют приложения от ядра: услуга ОС только через [[System call]] (TRAP).

</div>
<div class="lang-en">

Kernel mode: full access to hardware, any instruction, any memory address; a crash takes down the PC. User mode: only a subset of instructions; I/O and machine-control instructions are forbidden; a crash is recoverable. Two modes isolate applications from the kernel: OS services only through a [[System call]] (TRAP).

</div>
</div>

### Resources

- Milestone: [[OS Tutorial 1 - введение]]
- Resources: [[OS_Tutorial01.pdf]]
- AtomicNotes: [[Kernel mode]]; [[User mode]]; [[System call]]
