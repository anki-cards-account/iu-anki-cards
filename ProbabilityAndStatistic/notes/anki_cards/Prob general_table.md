№
1
Question;
Probability theory is the branch of mathematics that analyses what kind of phenomena?
Answer;
random phenomena
Explanation
Central objects: random experiments, outcomes, events, and the likelihood of those events. Not a recipe for relative frequency alone.

---
№
2
Question;
The sample space S is the set of what?
Answer;
all possible outcomes
Explanation
Of a random experiment. Finite (coin, die), countably infinite (emails per hour), or uncountable (voltage, failure time, R^3).

---
№
3
Question;
Can the same physical experiment be described by more than one sample space?
Answer;
yes
Explanation
Die: S1 = {1,...,6} vs S2 = {even, odd}. S1 carries more information. Choosing S is part of the model.

---
№
4
Question;
An event A occurs when the outcome ω stands in which relation to A?
Answer;
ω ∈ A
Explanation
Naive lecture definition: an event is any subset A ⊆ S. On R, not every subset need be measurable; that is why F is a σ-algebra.

---
№
5
Question;
Empirical probability of A is the proportion of times A occurs in a large number of what?
Answer;
repeated trials
Explanation
P(A) ≈ (times A occurred) / (number of trials). As n → ∞ the relative frequency is said to stabilize to the true probability. 510 heads in 1000 tosses ≈ 0.51.

---
№
6
Question;
The intersection A ∩ B is the event of outcomes that belong to A and B in which way?
Answer;
common to both
Explanation
Both events occur. Die even and >3: {4,6}. Not the product of probabilities (independence is not in this lecture).

---
№
7
Question;
The union A ∪ B contains outcomes that belong to A or B or what?
Answer;
both
Explanation
At least one of the two events occurs, not exclusive or. Die even or >3: {2,4,5,6}.

---
№
8
Question;
The complement of A relative to S is the set of elements of S that are what?
Answer;
not in A
Explanation
A' or A^c: the event that A does not occur. Complement depends on the chosen S.

---
№
9
Question;
Two events are mutually exclusive (disjoint) when their intersection is what?
Answer;
empty
Explanation
A ∩ B = ∅: they have no outcomes in common, so they cannot occur together. Not the same as independence.

---
№
10
Question;
De Morgan: the complement of A ∩ B equals what?
Answer;
A' ∪ B'
Explanation
Lecture identity 8: (A ∩ B)' = A' ∪ B'. The dual (A ∪ B)' = A' ∩ B' is a separate card.

---
№
11
Question;
De Morgan: the complement of A ∪ B equals what?
Answer;
A' ∩ B'
Explanation
Lecture identity 9. Also (A')' = A, A ∪ A' = S, A ∩ A' = ∅.

---
№
12
Question;
Kolmogorov axiom of non-negativity: for any event A, P(A) is at least what?
Answer;
0
Explanation
P(A) ≥ 0. Axioms say what a probability function is allowed to be, not how to count a coin.

---
№
13
Question;
Kolmogorov normalization: P of the sample space S equals what?
Answer;
1
Explanation
The certain event has probability 1: something in S must happen.

---
№
14
Question;
Kolmogorov countable additivity applies to a sequence of events that are pairwise what?
Answer;
disjoint
Explanation
If Ai ∩ Aj = ∅ for i ≠ j, then P(union Ai) = sum P(Ai). Overlapping events need inclusion-exclusion, not this axiom raw.

---
№
15
Question;
As a consequence of the axioms, P of the empty set equals what?
Answer;
0
Explanation
Property 1 in the lecture, not listed as an axiom. Used when mutually exclusive events make P(A ∩ B) = P(∅) = 0.

---
№
16
Question;
If A and A' are complementary, P(A) + P(A') equals what?
Answer;
1
Explanation
Proof: A ∪ A' = S and the two sets are disjoint, so 1 = P(S) = P(A) + P(A'). Equivalently P(A^c) = 1 − P(A).

---
№
17
Question;
Inclusion-exclusion for two events: P(A ∪ B) = P(A) + P(B) minus what?
Answer;
P(A ∩ B)
Explanation
P(A)+P(B) counts the intersection twice; subtract once. If disjoint, that term is 0.

---
№
18
Question;
If A and B are mutually exclusive, P(A ∪ B) equals which sum?
Answer;
P(A) + P(B)
Explanation
Corollary: A ∩ B = ∅ so P(A ∩ B) = 0. This is finite additivity for n = 2, not independence.

---
№
19
Question;
Classical P(A) = n/N requires that the N outcomes be what?
Answer;
equally likely
Explanation
Limitation stated in the lecture. A loaded die (even twice as likely as odd) is not this regime.

---
№
20
Question;
Geometric probability: P(A) is measure(A) divided by what?
Answer;
measure(S)
Explanation
Length, area, or volume according as S sits in R, R^2, or R^3. Outcomes equally likely in the geometric sense. Not a point count n/N.

---
№
21
Question;
A σ-algebra on S must contain S, be closed under complements, and be closed under what unions?
Answer;
countable unions
Explanation
The three axioms of F. Pair (S, F) is a measurable space. Not every subset of S need lie in F.

---
№
22
Question;
A probability space is which triple?
Answer;
(S, F, P)
Explanation
Sample space, σ-algebra of events, probability measure on F. Measurable space is only (S, F).

---
№
23
Question;
The trivial (minimal) σ-algebra on a nonempty set X is which pair of sets?
Answer;
{∅, X}
Explanation
Smallest possible F. The power set 2^X is the maximal one. For a proper nonempty A: {∅, A, A^c, X}.

---
№
24
Question;
If A ⊆ B, monotonicity says P(A) compared with P(B) is what?
Answer;
≤
Explanation
Property 4: A ⊆ B ⇒ P(A) ≤ P(B). Union bound is a different inequality and does not need disjointness.

---
№
25
Question;
The union bound says P of a union is at most the sum of the P(Ai), even if the events are not what?
Answer;
disjoint
Explanation
Property 5. Equality needs disjointness (additivity). The bound can be strictly larger than 1; it is still valid as an inequality.

---
№
26
Question;
Inclusion-exclusion for three events: after subtracting the three pairwise intersections, what must be added back?
Answer;
P(A ∩ B ∩ C)
Explanation
P(A∪B∪C) = sum of singles − sum of pairs + triple. The triple was subtracted too often.

---
№
27
Question;
Fair coin twice: P(at least one head). Four equally likely outcomes.
Answer;
3/4
Explanation
S = {HH, HT, TH, TT}, each 1/4. A = {HH, HT, TH}. Includes HH, excludes only TT.

---
№
28
Question;
Loaded die, even twice as likely as odd. Weight w on each odd face. What is w?
Answer;
1/9
Explanation
Three odd (w) and three even (2w): 9w = 1. Then P(E) for E = {1,2,3} is a different card (4/9).

---
№
29
Question;
Loaded die as above. E = {1,2,3}. P(E) = ?
Answer;
4/9
Explanation
1/9 + 2/9 + 1/9. Not 3/6: outcomes are not equally likely.

---
№
30
Question;
Same loaded die. A even, B divisible by 3. P(A ∪ B) = ?
Answer;
7/9
Explanation
A∪B = {2,3,4,6}: 2/9+1/9+2/9+2/9. P(A∩B) is the next card.

---
№
31
Question;
Same loaded die. A even, B divisible by 3. P(A ∩ B) = ?
Answer;
2/9
Explanation
A∩B = {6}, even, weight 2/9. Not 1/6.

---
№
32
Question;
Class of 53 equally likely students, 25 industrial. P(industrial) = ?
Answer;
25/53
Explanation
Classical n/N. Civil-or-electrical is 18/53, a different card.

---
№
33
Question;
Same class: 8 civil and 10 electrical. P(civil or electrical) = ?
Answer;
18/53
Explanation
18 of 53. Majors do not overlap in the statement.

---
№
34
Question;
P(A)=0.8, P(B)=0.6, P(A∩B)=0.5. P(at least one offer) = ?
Answer;
0.9
Explanation
0.8+0.6−0.5. Not 1.4 and not 0.5.

---
№
35
Question;
Fair dice pair. P(total 7 or 11) = ?
Answer;
2/9
Explanation
P(7)=6/36=1/6, P(11)=2/36=1/18, mutually exclusive, sum 2/9.

---
№
36
Question;
Mechanic: P(3)=0.12, P(4)=0.19, and the rest given. P(at least 5 cars) = ?
Answer;
0.69
Explanation
Complement: 1 − (0.12+0.19) = 1 − 0.31. Not P(exactly 5)=0.28.

---
№
37
Question;
Alice–Bob, 60 min window, wait 15 min, uniform independent. P(meet) = ?
Answer;
7/16
Explanation
Areas 3600 and 1575. Two triangles of leg 45: 2025 non-meeting. 1575/3600 = 7/16 = 0.4375. Not 15/60.

