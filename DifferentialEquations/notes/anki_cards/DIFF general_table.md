№
1
Question;
In this course, a differential equation relates an unknown function to what else?
Answer;
its derivatives
Explanation
Rates of change are derivatives, so models of changing quantities become DEs. Not every equation with a function is a DE — the derivatives of the unknown must appear.

---
№
2
Question;
A good mathematical model must be simple enough for what?
Answer;
the problem to be solvable
Explanation
First of two properties: simplify until the math can be solved. The second property is useful accuracy of predictions, asked separately.

---
№
3
Question;
Besides being solvable, a good mathematical model must predict the real outcome with what?
Answer;
useful accuracy
Explanation
Not a perfect copy of nature — accuracy that is useful in practice. If predictions miss observations, revise the assumptions, do not fake the answer.

---
№
4
Question;
If a model's predictions disagree with physical observations, what must be revised?
Answer;
the underlying assumptions
Explanation
Keep changing simplifying assumptions until agreement is satisfactory. The DE is a consequence of those assumptions.

---
№
5
Question;
ODE vs PDE: an ODE is a DE whose unknown depends on how many independent variables?
Answer;
one
Explanation
Ordinary = one independent variable (e.g. Q(t) in an RLC circuit). Several independent variables make a PDE (e.g. u(x,t)).

---
№
6
Question;
PDE vs ODE: a PDE is a DE whose unknown depends on how many independent variables?
Answer;
several
Explanation
Example in the lecture: heat equation for u(x,t) in a rod. Two unknowns of one variable t would be a system of ODEs, not a PDE.

---
№
7
Question;
The 1D heat equation uses u(x,t). Why is it a PDE, not an ODE?
Answer;
two independent variables
Explanation
u depends on space x and time t. Partial derivatives appear: u_t = alpha u_xx. Thermal diffusivity alpha is a coefficient, not a second unknown function of t only.

---
№
8
Question;
What is the order of a differential equation?
Answer;
order of the highest derivative
Explanation
Count the highest derivative that appears, not the number of terms and not the degree of a nonlinearity. Duffing is second order because of x-double-dot, even with an x^3 term.

---
№
9
Question;
Why is the Duffing equation a second-order ODE?
Answer;
highest derivative is x-double-dot
Explanation
Duffing: x-double-dot + k x + x^3 = B cos t. The cubic term makes it nonlinear; it does not raise the order.

---
№
10
Question;
Write the explicit form of a first-order ODE solved for the derivative.
Answer;
dx/dt = f(t, x)
Explanation
This is the form used for direction fields and isoclines: the right-hand side is the slope at (t,x).

---
№
11
Question;
In a linear ODE, the coefficients a_i and the free term g may depend on which variable?
Answer;
only t
Explanation
Standard form: a_n(t) x^(n) + ... + a_0(t) x = g(t). They must not depend on x or on derivatives of x. Unknown and derivatives enter to the first power only.

---
№
12
Question;
The Duffing equation is nonlinear because of which term?
Answer;
x^3
Explanation
x-double-dot + k x + x^3 = B cos t. If it were only k x and a forcing, it could still be linear; the cube of the unknown breaks linearity.

---
№
13
Question;
The Lotka–Volterra system is nonlinear because of which kind of term?
Answer;
products y1 y2
Explanation
Prey–predator: y1' = a y1 − b y1 y2, y2' = c y1 y2 − d y2. The products of the two unknowns make the system nonlinear.

---
№
14
Question;
A linear ODE is called homogeneous when the free term g(t) equals what?
Answer;
0
Explanation
Every term then involves the unknown or its derivatives. Nonhomogeneous means g(t) ≠ 0. The trivial solution x ≡ 0 solves only the homogeneous linear equation.

---
№
15
Question;
The trivial solution x ≡ 0 solves a linear ODE only in which case?
Answer;
homogeneous (g = 0)
Explanation
If g(t) ≠ 0, plugging x ≡ 0 leaves g(t) = 0, a contradiction. Do not apply this slogan to nonlinear systems.

---
№
16
Question;
Newton's law of cooling T' = −r(T − Ta) is nonhomogeneous because of which extra term after expanding?
Answer;
r Ta
Explanation
Rewrite: T' + r T = r Ta. The right-hand side does not depend on T. That is the linear meaning of nonhomogeneous, not 'the cup sits in a room'.

---
№
17
Question;
The RLC equation for Q(t) is nonhomogeneous when the impressed voltage E(t) is what?
Answer;
not zero
Explanation
L Q'' + R Q' + Q/C = E(t). If E(t) = 0 the linear ODE is homogeneous.

---
№
18
Question;
Lecture calls Lotka–Volterra homogeneous in the sense of no external forcing. Is that the same as linear g(t)=0?
Answer;
no
Explanation
No forcing term, but the system is nonlinear (products y1 y2). Linear homogeneity is a statement about g(t) in the linear form, which this system does not have.

---
№
19
Question;
A system X' = F(t, X) is autonomous when the right-hand side depends on t how?
Answer;
not explicitly
Explanation
Laws may still depend on the state X. Autonomous means F = F(X), no clock in the formula. Lotka–Volterra as written is autonomous.

---
№
20
Question;
Normal form of a system of n first-order ODEs: each equation is solved for what?
Answer;
the first derivative
Explanation
x_i' = f_i(t, x1, ..., xn). Vector form: X' = F(t, X). This is not a PDE: each unknown is still a function of one variable t.

---
№
21
Question;
On a direction field, the slope of the segment at a grid point (ti, xj) equals what?
Answer;
f(ti, xj)
Explanation
For x' = f(t,x) the derivative is the tangent slope, so you can draw the field without solving the ODE. All segments have the same length; only the angle changes.

---
№
22
Question;
On a direction field, what is equal for every segment, with only the angle changing?
Answer;
length
Explanation
Fixed length L; slope (angle) equals f at that point. L must be smaller than the grid spacing so segments do not overlap.

---
№
23
Question;
Under standard existence and uniqueness, how many integral curves pass through each point of the domain?
Answer;
exactly one
Explanation
The field shows local behaviour, not one already-chosen trajectory. An initial condition picks which curve of the family.

---
№
24
Question;
When drawing a direction field, the segment length L must be smaller than what?
Answer;
the grid spacing
Explanation
Smaller than both Δt and Δx so segments neither overlap nor cross. Too coarse a grid can also mislead.

---
№
25
Question;
Does a direction field give a numerical value of the solution at a chosen time?
Answer;
no
Explanation
Qualitative picture: behaviour, equilibria. Accuracy depends on grid density. No substitute for an explicit formula or a numerical solver if you need a number.

---
№
26
Question;
On a direction field, an equilibrium (steady-state) solution appears as segments that are what?
Answer;
horizontal
Explanation
Slope zero: f = 0, the unknown does not change. Example: falling object with v' = 9.8 − v/5 has horizontal marks at v = 49 m/s.

---
№
27
Question;
For v' = 9.8 − v/5, what is the equilibrium velocity in m/s?
Answer;
49
Explanation
Set 9.8 − v/5 = 0 → v = 49. Matches vmax = mg/k with m = 10 kg, k = 2 kg/s. Below 49 slopes are positive; above 49, negative. All solutions tend to 49 as t → ∞.

---
№
28
Question;
An isocline of x' = f(t,x) is the curve on which f(t,x) equals what?
Answer;
a constant C
Explanation
Along that curve every direction-field segment has the same slope C. An isocline is not an integral curve; solutions cross isoclines, changing slope.

---
№
29
Question;
Is an isocline the same object as an integral curve?
Answer;
no
Explanation
Isocline: f(t,x) = C, constant slope of the field. Integral curve: actual solution graph, tangent to the field. You walk from isocline to isocline to sketch a solution.

---
№
30
Question;
Who introduced the notation dy/dx still used today?
Answer;
Leibniz
Explanation
Lecture: Newton’s Principia (1687) for mechanics; the term “differential equation” in 1676; Leibniz published calculus first and introduced dy/dx.

---
№
31
Question;
In which year was the term “differential equation” introduced, according to the lecture?
Answer;
1676
Explanation
Historical fact from Chapter 1. Separate from Leibniz’s dy/dx notation and from Newton 1687.

---
№
32
Question;
For linear drag Fd = −k v, the terminal velocity vmax equals what combination of m, g, k?
Answer;
mg/k
Explanation
From v' = g − (k/m)v, as t → ∞ the exponential dies and v → mg/k. That is the balance mg = k v, not the impact speed on the ground.

---
№
33
Question;
In the Malthusian model, the net growth rate r is which combination of birth and death coefficients?
Answer;
α − β
Explanation
N' = (α − β)N. If α, β are constant, r = α − β and N' = r N. This is a first-order linear homogeneous ODE.

---
№
34
Question;
Malthusian model: if r > 0, the population N(t) does what?
Answer;
grows exponentially without bound
Explanation
N(t) = N0 exp(r(t − t0)). The lecture lists hares without predators, bacteria in nutrient medium — and also the limitation: resources are finite, logistic later.

---
№
35
Question;
Malthusian model: if r < 0, the population N(t) does what?
Answer;
decays exponentially to zero
Explanation
Same exponential solution. If r = 0 the population stays constant — that is a separate fact.

---
№
36
Question;
Newton cooling: the rate constant r equals αS divided by what product?
Answer;
c ρ V
Explanation
r = α S / (c ρ V) > 0. α heat-transfer coefficient, S surface, c specific heat, ρ density, V volume. Larger r → faster pull toward Ta.

---
№
37
Question;
Falling object: write v' for gravity mg and linear drag −k v (mass m).
Answer;
g - (k/m)v
Explanation
Newton II: m v' = mg − k v, then divide by m. First-order linear ODE. Terminal speed is a different card (mg/k).

---
№
38
Question;
Falling object with Fd = −k v: formula for terminal velocity vmax.
Answer;
mg/k
Explanation
Limit of v(t) as t → ∞, not impact speed. With m = 10 kg, k = 2 kg/s this is 49 m/s, the equilibrium of the direction field.

---
№
39
Question;
Malthus: write the ODE for N(t) with net growth rate r.
Answer;
N' = rN
Explanation
r = α − β. Linear homogeneous first-order. Solution is the exponential asked on another card.

---
№
40
Question;
Malthus N' = rN with N(t0) = N0: write N(t).
Answer;
N0 exp(r(t-t0))
Explanation
Separation of variables. r > 0 unbounded growth; r < 0 decay to 0; r = 0 constant — those signs are theory cards.

---
№
41
Question;
Newton cooling, lumped body, no internal sources: write T' in terms of r, T, Ta.
Answer;
-r(T-Ta)
Explanation
Heat balance: c ρ V T' = −α S (T − Ta), r = αS/(cρV). Nonhomogeneous because of r Ta.

---
№
42
Question;
Newton cooling: write r using α, S, c, ρ, V.
Answer;
αS/(cρV)
Explanation
Positive. Depends on the object and the heat-transfer conditions. Not the ambient temperature Ta.

---
№
43
Question;
Direction field of x' = 1: write the family of integral curves.
Answer;
x = t + C
Explanation
Slope is 1 at every point; all segments parallel. Initial condition picks C (vertical shift).

---
№
44
Question;
Direction field of y' = y/x (origin excluded): write the integral curves.
Answer;
y = Cx
Explanation
Slope y/x is the slope of the ray from the origin. Field suggests the form without integrating. Origin is not in the domain.

---
№
45
Question;
Isoclines of x' = sqrt(x^2+t^2): write the Cartesian equation of an isocline of slope C.
Answer;
x^2 + t^2 = C^2
Explanation
Circles centred at the origin, radius C. C = 0 is the origin (degenerate). At (0,0) the ODE is not differentiable. Isocline ≠ solution curve.

---
№
46
Question;
For v' = 9.8 − v/5, at which v (m/s) are the direction-field segments horizontal?
Answer;
49
Explanation
dv/dt = 0. Below 49, slopes positive; above 49, negative. All solutions tend to this equilibrium as t → ∞.

