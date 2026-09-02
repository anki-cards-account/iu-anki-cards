**Мини-словарь:**
- differential equation (DE) — уравнение, связывающее неизвестную функцию и её производные.
- ODE / PDE — обычное vs уравнение в частных производных: одна независимая переменная vs несколько.
- direction field (slope field) — поле коротких отрезков со склоном $f(t,x)$.
- isocline — кривая постоянного склона $f(t,x)=C$.

### Концепт

Путеводитель **Differential Equations, lection 1 — введение**: зачем ДУ в моделях, как их классифицировать, как увидеть решения геометрически (поле направлений и изоклины), ещё не решая уравнение.

Курс: Maslovskaya, *Differential Equations for Engineers*, глава 1.

```text
реальность
  → упрощения → математическая модель (часто ДУ)
  → тип: ODE/PDE, порядок, система, linear/nonlinear, homogeneous/nonhomogeneous
  → геометрия 1-го порядка: direction field, isoclines, equilibrium
```

### Карта лекции

#### Модели и три сюжета
- [[Mathematical model]] — упрощения и два свойства «хорошей» модели
- [[Differential equation]] — производные = скорости изменения; язык моделей
- [[Falling object]] — Ньютон II + сопротивление $\propto v$, терминальная скорость
- [[Malthusian model]] — $N'=rN$, экспонента, пределы модели
- [[Newton's law of cooling]] — теплообмен → линейное ODE для $T(t)$

#### Классификация
- [[Ordinary differential equation]] — одна независимая переменная; против [[Partial differential equation]]
- [[Order of a differential equation]] — порядок старшей производной; явная форма 1-го порядка
- [[System of ODEs]] — нормальная форма, векторная запись, автономность
- [[Linear ODE]] — коэффициенты только от $t$; неизвестная и производные входят линейно
- [[Nonlinear ODE]] — не линейно: $x^3$, произведения $y_1 y_2$
- [[Homogeneous ODE]] — $g(t)=0$ vs неоднородное; ловушка «forcing» у Lotka–Volterra

#### Геометрия решений
- [[Direction field]] — склон в точке = $f(t,x)$ без формулы решения
- [[Equilibrium solution]] — горизонтальные отрезки, $v=49$ у падения
- [[Isocline]] — $f(t,x)=C$, экономная сборка поля направлений

### Problems
- [[DIFF Example 1]] — падающий объект
- [[DIFF Example 2]] — модель Мальтуса
- [[DIFF Example 3]] — остывание чашки
- [[DIFF Example 4]] — поле для $x'=1$
- [[DIFF Example 5]] — поле для $y'=y/x$
- [[DIFF Example 6]] — изоклины $\sqrt{x^2+t^2}$

### Sources
- [[DE_Lecture01.pdf]] — Chapter 1, FUNDAMENTALS OF DIFFERENTIAL EQUATIONS: INTRODUCTION; курс [F26] Differential Equations
