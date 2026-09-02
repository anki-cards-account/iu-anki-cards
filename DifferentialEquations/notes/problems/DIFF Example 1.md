### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>Объект массы m падает под действием силы тяжести mg (g = 9.8 м/с²) и силы сопротивления Fd = −kv, пропорциональной скорости v (k — коэффициент сопротивления, кг/с). Запишите ODE для v(t), его решение с v(0) = v0 и терминальную скорость.</p></div><div class="lang-en"><p>An object of mass m falls under gravity mg (g = 9.8 m/s²) and a drag force Fd = −kv proportional to velocity v (k is the drag coefficient in kg/s). Write the ODE for v(t), the solution with v(0) = v0, and the terminal velocity.</p></div></div>

$$
m\frac{dv}{dt}=mg-kv,\qquad
\frac{dv}{dt}=g-\frac{k}{m}v,\qquad
v(t)=\frac{mg}{k}+C\exp\left(-\frac{k}{m}t\right),\qquad
v_{\max}=\frac{mg}{k}
$$

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p><b>Коротко:</b> m v' = mg − kv, или v' = g − (k/m)v. Решение v(t) = mg/k + C exp(−(k/m)t), C из v(0)=v0. При t→∞ скорость → vmax = mg/k.</p><p><b>Почему так:</b> второй закон Ньютона: сумма сил равна массе на ускорение. Вес вниз, линейный drag против скорости. Это линейное ODE первого порядка.</p><p><b>Путаница:</b> терминальная скорость — не «скорость в момент удара о землю», а предел v(t) на бесконечном времени, когда mg уравновешен kv. Подробнее: <a class="internal-link" data-href="Falling object" href="Falling object">Falling object</a>.</p></div><div class="lang-en"><p><b>Short:</b> m v' = mg − kv, or v' = g − (k/m)v. Solution v(t) = mg/k + C exp(−(k/m)t), with C from v(0)=v0. As t→∞, v → vmax = mg/k.</p><p><b>Why:</b> Newton’s second law: net force equals mass times acceleration. Weight down, linear drag against velocity. A first-order linear ODE.</p><p><b>Mix-up:</b> terminal velocity is not “speed at impact”. It is the limit of v(t) as t→∞, when mg balances kv. See <a class="internal-link" data-href="Falling object" href="Falling object">Falling object</a>.</p></div></div>

$$
\lim_{t\to\infty} v(t)=\frac{mg}{k}
$$

### Resources

- Milestone: [[DIFF Lection 1 - введение]]
- Resources: [[DE_Lecture01.pdf]]
- AtomicNotes: [[Falling object]]; [[Linear ODE]]; [[Equilibrium solution]]
