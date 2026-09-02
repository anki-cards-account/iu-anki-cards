### Формулировка
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p>P(оффер A)=0.8, P(оффер B)=0.6, P(оба)=0.5. Какова вероятность хотя бы одного оффера от этих двух компаний?</p></div><div class="lang-en"><p>P(offer from A)=0.8, P(offer from B)=0.6, P(both)=0.5. What is the probability of at least one offer from these two companies?</p></div></div>

$$
P(A\cup B)=0.8+0.6-0.5=0.9
$$

### Ответ
<div class="lang-pair"><label class="lang-btn"><input class="lang-sw" type="checkbox"><span class="is-ru">ru</span><span class="is-en">en</span></label><div class="lang-ru"><p><b>Коротко:</b> 0.9. Additive rule: P(A ∪ B) = P(A)+P(B)−P(A ∩ B).</p><p><b>Почему так:</b> 0.8+0.6 уже дважды считает «оба оффера». Вычитаем 0.5 один раз.</p><p><b>Путаница:</b> не 0.8+0.6=1.4 (больше 1). Не 0.5 «только оба». «Хотя бы один» — объединение, не пересечение. Подробнее: <a class="internal-link" data-href="Inclusion-exclusion" href="Inclusion-exclusion">Inclusion-exclusion</a>.</p></div><div class="lang-en"><p><b>Short:</b> 0.9. Additive rule: P(A ∪ B) = P(A)+P(B)−P(A ∩ B).</p><p><b>Why:</b> 0.8+0.6 counts “both offers” twice. Subtract 0.5 once.</p><p><b>Mix-up:</b> not 0.8+0.6=1.4 (exceeds 1). Not 0.5 “only both”. “At least one” is the union, not the intersection. See <a class="internal-link" data-href="Inclusion-exclusion" href="Inclusion-exclusion">Inclusion-exclusion</a>.</p></div></div>

### Resources

- Milestone: [[Prob Lection 1 - основания]]
- Resources: [[Prob_Lecture01.pdf]]
- AtomicNotes: [[Inclusion-exclusion]]; [[Union of events]]
