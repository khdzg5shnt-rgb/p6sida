# R13: a finite endpoint closure is unavailable

4 October 2026 (UTC). Natural logarithms. Baseline: `b0ac13287fa0be97d27d9f2ae7fa45ccca1f128f`.

**Outcome.** The fixed-policy comparison is unresolved. This note proves a new exclusion for this project's proposed endpoint reduction, using established intermediate beta-shift tools. It does not bound the residual ratio `R_m/N_m`, improve either rate bound, or supply a new publication-level main theorem.

## 1. Objects retained and the attempted reduction

Keep the prescribed system
\[
q=2-2^{-20},\quad \rho_0=1/4,\quad\rho_1=1/256,\qquad
F_i(s,z)=\bigl(\rho_i s,\rho_i(qz+q/2\,s-qi\,s)\bigr),\quad i=0,1.
\]
The actual initial set remains
\[
K=Q=\{0\le s\le1,\ |z|\le s\},\qquad \delta_n=2^{-n}.
\]
Every binary input is allowed; an actual initial state is assigned a control, and the Euclidean distance to `Q` is constrained at every time `0,...,n`, with exits and returns permitted. No policy restriction has been imposed on that problem.

For the existing exact stopping comparison, put
\[
T_i(y)=qy+q/2-qi,\quad c(w)=\#_0(w)+4\#_1(w),\quad
b=1/q-1/2,\quad f(y)=\begin{cases}T_0(y),&y\le b,\\T_1(y),&y>b.\end{cases}
\]
The complete feasible interval is
\[
I_w=[-1,1]\cap\bigcap_{k=1}^{|w|}T_{w_1\cdots w_k}^{-1}([-1,1]).
\]
`N_m` is its minimum cost-at-least-`m` cover of all `[-1,1]`; `G_m` counts all actual first-cost-`m` policy words, including boundary itineraries. A normalized minimum cover `W_m` has
\[
m\le c(w)\le m+3,\qquad \lceil m/4\rceil\le |w|\le m.
\]
For actual policy cylinders `C_v`, retain precisely
\[
E_{w,v}=T_v(I_w\cap C_v),\qquad
d_{m,v}=m-c(v)>0,
\]
and the R12 sum
\[
R_m=\sum_{w\in W_m}\ \sum_{\substack{|v|=|w|,\ I_w\cap C_v\ne\varnothing\\c(v)<m}}
G_{m-c(v)}(E_{w,v}).
\]
Open ends, closed ends and singletons remain actual; `C_v` is not replaced by `I_v`.

The attempted reduction was to synchronize the possible endpoint trajectories after a uniformly finite excursion, or encode all their continuations by an exact finite graph with edge costs `1,4`. The following proposition rules out those exact closures. It does **not** rule out inequalities, approximate finite-state bounds, or a direct infinite-state budget estimate.

## 2. One exclusion proposition

**Proposition 13.1 (core, nonmatching critical endpoints, and no exact finite graph).** Set
\[
J=[1-q,1],\qquad L=[-1,1-q),\qquad
h(y)=(y+q-1)/q,\qquad
\alpha=5/2-q-1/q.
\]
Then:

1. `f(J)` is contained in `J`, and `f^2([-1,1])` is contained in `J`. On `J`, `h f h^{-1}` is the left-continuous intermediate beta transformation of slope `q` and parameter `alpha`, with its threshold assigned digit `0`. In particular, every actual residual endpoint set `E_{w,v}` lies in `J` for `m>=5`.
2. Any exactly feasible trajectory which enters `L` has only input `0` available there and returns to `J` within at most two further inputs. From an initial ratio `y` in `J`, an exit is possible only by digit `1` at `-b<=y<b`. The returning blocks are `10` or `100`, as specified below, with costs `5` or `6`. Their return positions are not identified with the fixed-policy positions.
3. The two one-sided images of the policy threshold are `1` and `1-q`. For **all** finite binary words `u,v`, including the empty word and unequal lengths,
   \[
   T_u(1)\ne T_v(1-q). \tag{1}
   \]
   Neither critical endpoint has a repeated finite-time value under the policy. Thus a finite set of endpoints containing the threshold and closed under its appropriate one-sided forward images is impossible.
4. Neither the policy's complete finite-word language on `[-1,1]` nor its language on `J` can be represented exactly by a finite labelled graph. This includes word-preserving graphs equipped with the costs `1,4`; it does not exclude a finite formula for some coarser statistic.

This proposition is an exclusion result for a possible proof shortcut. Parts 1--2 alone yield no subexponential residual-budget bound.

### Proof: the actual core and excursions

We have `3/2<q<2`, and
\[
T_0([-1,b])=[-q/2,1],\qquad
T_1((b,1])=(1-q,q/2],
\]
so the policy is feasible everywhere. On its core,
\[
T_0([1-q,b])=[q(3/2-q),1],\qquad
T_1((b,1])=(1-q,q/2].
\]
The first lower endpoint satisfies
\[
q(3/2-q)-(1-q)=(2-q)(q-1/2)>0.
\]
Both images are therefore in `J`, with the actual tie `f(b)=1` retained.

Every point of `L` is below `-b`. Indeed `q-1>b` for the present `q`. Digit `1` would send it below `-1`, so an exactly feasible control must use digit `0` until it returns to `J`. If a first such step has not returned, the second does, since
\[
T_0^2(-1)=-q(q-1)/2>1-q,
\qquad
-q(q-1)/2-(1-q)=(q-1)(1-q/2)>0.
\]
The intermediate state is at least `-q/2>-1`; while a second step is needed its starting state is below `1-q`, and the second image is below `q(3/2-q)<1`. Thus the whole excursion is feasible and its return takes at most two inputs. This also proves `f^2([-1,1])` is contained in `J`. Since `|v|=|w|>=ceil(m/4)>=2` for `m>=5`, it proves the assertion about every actual `E_{w,v}`, without deleting endpoint states.

For `y` in `J`, digit `0`, whenever feasible, stays in `J`. Digit `1` is feasible only for `y>=-b`, and its image is below `1-q` exactly when `y<b`. Define
\[
e=-b(1-1/q)=-\frac{(q-1)(2-q)}{2q^2}.
\]
After an exit, the forced input `0` gives
\[
T_{10}(y)=q^2y-q(q-1)/2.
\]
It returns to `J` if and only if `y>=e`. Therefore the return is
\[
\begin{cases}
10,& e\le y<b,\\
100,&-b\le y<e,
\end{cases}\qquad
T_{100}(y)=q^3y-q^3/2+q^2/2+q/2. \tag{2}
\]
At `y=e`, the two-input block returns to the included left endpoint of `J`. At `y=b`, digit `1` lands directly at that endpoint and is not an exit. All intermediate constraints and these boundary cases are retained. Formula (2) follows from the trajectories, not from a presumption about optimal covers.

Since
\[
\alpha=\frac{(2-q)(q-1/2)}q,\qquad 0<\alpha<2-q,
\]
direct substitution gives
\[
h T_i h^{-1}(x)=qx+\alpha-i,
\qquad h(b)=\frac{1-\alpha}{q}.
\]
The branch at equality is `0` and maps to `1`, exactly the `T^-_{q,alpha}` convention. This identifies only the fixed selector on its invariant core. Arbitrary feasible controls may take the exits in (2), or select the other branch at the threshold, so the original optimal-cover problem has not become the fixed beta-shift problem.

### Proof: no exact endpoint synchronization

Put `A=2^20`, `B=2^21-1`. Then
\[
q=B/A,\quad B\text{ is odd},\qquad b=1/(2B).
\]
For a dyadic rational, use its denominator in lowest terms. From `1`, either first input gives `B/(2A)` or `3B/(2A)`, both with odd numerator and denominator `2^21`. If a later state has odd numerator over `2^k`, `k>=2`, adding either `1/2` or `-1/2` leaves an odd numerator, and multiplying by the odd `B` divided by `A` increases the denominator exponent by exactly `20`. Hence
\[
\operatorname{den}(T_u(1))=2^{20|u|+1}\quad (|u|\ge1). \tag{3}
\]
For the other endpoint, `1-q=(A-B)/A` already has odd numerator over `2^20`. The same induction yields
\[
\operatorname{den}(T_v(1-q))=2^{20(|v|+1)}\quad (|v|\ge0). \tag{4}
\]
The denominator exponents in (3) and (4) differ modulo `20`; the empty orbit of `1` has denominator `1` and also cannot match (4). This proves (1) for every pair of finite words, even before imposing feasibility. Within either policy orbit the exponents strictly increase, so no value repeats. A finite forward-closed endpoint set would force a repeat and is therefore impossible. In particular, allowing different suffixes or different elapsed times cannot **exactly** join these critical endpoints. This is not a statement about how many intervals an optimal cover needs.

### Proof: the full language has no finite graph

Let `a_l(S)` count the distinct actual policy prefixes of length `l` from `S`, where `S` is `[-1,1]` or `J`. Every nonempty actual cylinder is an interval, possibly half-open or a singleton. Because `T_v` has slope `q^l` and its image stays in `[-1,1]`, its length is at most `2q^{-l}`. These cylinders partition `S`, so
\[
a_l(S)\ge \frac{|S|}{2}q^l. \tag{5}
\]
Use only the independently checked R11 local multiplicity bound: for every `eta>0`, there is a uniform `A_eta` such that an interval of length at most `2q^{-l}` realizes at most `A_eta exp(eta l)` prefixes. Cover `S` by at most `1+q^l` such closed intervals. Boundary itineraries are included rather than discarded. Thus
\[
a_l(S)\le (1+q^l)A_\eta e^{\eta l},
\qquad
\lim_{l\to\infty}a_l(S)^{1/l}=q. \tag{6}
\]

For completeness, suppose a finite labelled graph represented exactly this language. The usual subset construction makes a finite deterministic automaton with the same distinct words, including its allowed initial states. Remove unreachable or nonproductive states. If `M` is its nonnegative integer transition matrix (counting labelled edges), word counts have the form of a finite matrix product. Their limsup exponential growth is the spectral radius of a reachable productive component with maximal spectral radius. This follows, for example, by decomposing the matrix into strongly connected components: powers have at most polynomial factors multiplying the maximal spectral radius, and a maximal component supplies the corresponding lower growth on a subsequence. Consequently (6) would make `q` an eigenvalue of an integer matrix. It would be a root of the monic integer polynomial `det(lambda I-M)`, hence an algebraic integer. A rational algebraic integer is an integer, whereas `q=B/A` is a noninteger rational. This is a contradiction.

The closure of actual infinite policy itineraries has the same finite-word language: a finite prefix cylinder in sequence space is both open and closed. It is shift invariant because the starting interval is policy invariant. In symbolic terminology this closure is not sofic, and in particular is not of finite type. This is the established algebraic obstruction for finite symbolic presentations, applied with the actual boundary convention. No finite enumeration has been used. This completes the proposition.

## 3. What this does and does not control

The core containment gives a fixed-size restriction `E_{w,v} subset J`, whose length is `q`, independent of the remaining budget. A return in at most two steps likewise bounds the cost of **one excursion**, not the cumulative cost difference between two different trajectories after their different return positions. Excursions can recur. Even the two critical endpoints cannot be reset exactly by arbitrary different finite suffixes.

These facts exclude an exact finite endpoint closure and an exact finite word-preserving cost graph. They do not estimate the distribution of `E_{w,v}` and `m-c(v)` over a minimizing `W_m`. They do not prove that large deficits occur, that they force narrow endpoints, or that the relevant endpoint moments are subexponential. They also do not exclude subexponential comparison by a method that keeps infinitely many actual endpoints.

The recovered R12 estimates remain available and unchanged:
\[
R_m\le3G_m,\qquad
G_m\le R_m+A_\eta e^{\eta m}N_m,\qquad
\lim_m\frac1m\ln(1+R_m/N_m)=g-\kappa.
\]
They are not re-established or claimed as R13 progress. This attack supplies **no new bound on `R_m/N_m`**, no strict positive rate gap, and no improvement of R09's bounds.

The one unresolved statement remains: for every `eta>0`, is `G_m<=exp(eta m)N_m` eventually? Its residual formulation still requires an actual optimal-cover budget estimate, not just nonmatching endpoint information. In particular, a failure of finite-state representation does not falsify that comparison.

## 4. Stop

Intermediate beta conjugacy, finite graph entropy, and rational-denominator arithmetic are existing methods. The project-specific addition is a proved reason not to close this endpoint attack by exact finite synchronization or a finite word graph. It is not claimed as a new main contribution or a result with independent publication value. No actual residual-budget control was obtained, so repeated attacks at this interface are paused. R14 is not authorized or started, and the unique paper and all earlier history remain unchanged.
