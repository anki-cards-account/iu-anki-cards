### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>Модель Мальтуса: нет лимитирующих факторов, скорость роста популяции пропорциональна её размеру. Запишите уравнение для N(t), смысл r = α − β и решение через N0 = N(t0). Что будет при r > 0, r < 0, r = 0?</p></div><div class="lang-en"><p>Malthusian model: no limiting factors, the growth rate of the population is proportional to its size. Write the equation for N(t), the meaning of r = α − β, and the solution via N0 = N(t0). What happens if r > 0, r < 0, r = 0?</p></div></div>

$$
\frac{dN}{dt}=(\alpha-\beta)N=rN,\qquad
N(t)=N_0\exp\bigl(r(t-t_0)\bigr)
$$

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p><b>Коротко:</b> N' = rN, r = α − β (рождаемость минус смертность). N(t) = N0 exp(r(t−t0)). r>0 — неограниченный экспоненциальный рост; r<0 — спад к нулю; r=0 — константа.</p><p><b>Почему так:</b> dN/dt пропорционально N. При постоянных α, β их разность — одна константа r. Разделение переменных даёт экспоненту. Это линейное однородное ODE первого порядка.</p><p><b>Путаница:</b> модель не утверждает, что так живут все популяции навсегда: ресурсы конечны, логистику лекция обещает позже. «Люди в стране» в списке примеров — про применимость идеи, не про демографический закон. Подробнее: <a class="internal-link" data-href="Malthusian model" href="Malthusian model">Malthusian model</a>.</p></div><div class="lang-en"><p><b>Short:</b> N' = rN, r = α − β (birth minus death). N(t) = N0 exp(r(t−t0)). r>0 unbounded exponential growth; r<0 decay to zero; r=0 constant.</p><p><b>Why:</b> dN/dt is proportional to N. With constant α, β their difference is one constant r. Separation of variables gives the exponential. A first-order linear homogeneous ODE.</p><p><b>Mix-up:</b> the model does not claim every population does this forever: resources are finite; logistic growth comes later. “People in a country” is an applicability example, not a demographic law. See <a class="internal-link" data-href="Malthusian model" href="Malthusian model">Malthusian model</a>.</p></div></div>

### Resources

- Milestone: [[DIFF Lection 1 - введение]]
- Resources: [[DE_Lecture01.pdf]]
- AtomicNotes: [[Malthusian model]]; [[Linear ODE]]; [[Homogeneous ODE]]
