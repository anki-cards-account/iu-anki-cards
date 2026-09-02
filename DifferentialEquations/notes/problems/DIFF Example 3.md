### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>Чашка жидкости нагрета до T0 и остывает до температуры среды Ta. Выведите ODE для T(t) из закона Ньютона для охлаждения и баланса тепла, укажите охлаждающую константу r.</p></div><div class="lang-en"><p>A cup of liquid is heated to T0 and cools toward the ambient temperature Ta. Derive the ODE for T(t) from Newton’s law of cooling and the heat balance, and state the cooling rate constant r.</p></div></div>

$$
dQ=\alpha S(T-T_a)\,dt,\qquad
dQ=c\rho V\,dT,\qquad
\frac{dT}{dt}=-r(T-T_a),\qquad
r=\frac{\alpha S}{c\rho V}
$$

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p><b>Коротко:</b> T' = −r(T − Ta), где r = αS / (c ρ V) > 0. Линейное неоднородное ODE первого порядка.</p><p><b>Почему так:</b> за dt уходит тепло αS(T−Ta) dt. То же тепло меняет внутреннюю энергию: c ρ V dT. Нет внутренних источников, температура тела одна. Знак минус: тепло уходит, T падает, если T > Ta.</p><p><b>Путаница:</b> неоднородность — из постоянного слагаемого r Ta (перепись T' + r T = r Ta), не из того что «чай в чашке». Lumped temperature — не «в чашке нет градиента в жизни», а допущение модели. Подробнее: <a class="internal-link" data-href="Newton's law of cooling" href="Newton's law of cooling">Newton's law of cooling</a>.</p></div><div class="lang-en"><p><b>Short:</b> T' = −r(T − Ta), with r = αS / (c ρ V) > 0. A first-order linear nonhomogeneous ODE.</p><p><b>Why:</b> in time dt the heat leaving is αS(T−Ta) dt. The same heat changes internal energy: c ρ V dT. No internal sources; one temperature for the whole body. Minus sign: heat leaves, so T falls when T > Ta.</p><p><b>Mix-up:</b> nonhomogeneous because of the constant r Ta (rewrite T' + r T = r Ta), not because “tea is in a cup”. Lumped temperature is a modelling assumption, not a claim that real cups have zero gradient. See <a class="internal-link" data-href="Newton's law of cooling" href="Newton's law of cooling">Newton's law of cooling</a>.</p></div></div>

### Resources

- Milestone: [[DIFF Lection 1 - введение]]
- Resources: [[DE_Lecture01.pdf]]
- AtomicNotes: [[Newton's law of cooling]]; [[Linear ODE]]; [[Homogeneous ODE]]
