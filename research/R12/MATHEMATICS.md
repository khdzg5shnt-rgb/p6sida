# R12: actual endpoint budgets and bounded incidence with an optimal cover

4 October 2026 (Asia/Shanghai). Natural logarithms. This is one bounded attack on the same fixed-policy comparison as R11. The requested comparison remains **unresolved**. The completed result is an endpoint-budget interface with a proved constant incidence bound, not a proof that the residual budgets have subexponential cost.

## 1. Fixed objects and the single interface

Retain exactly
\[
q=2-2^{-20},\quad \rho_0=1/4,\quad \rho_1=1/256,\qquad
F_0(s,z)=(\rho_0s,\rho_0(qz+qs/2)),\quad
F_1(s,z)=(\rho_1s,\rho_1(qz-qs/2)).
\]
The actual initial set is
\[
K=Q=\{0\le s\le1,\ |z|\le s\}.
\]
All binary inputs remain allowed. The genuine catalogue assigns a control to each actual initial state and uses the Euclidean environment distance at every time \(0,\ldots,n\), with tolerance \(2^{-n}\); exits and returns are allowed. The auxiliary exact stopping problem below has not replaced these original quantifiers. Its relation to that genuine problem is R09's proved comparison \(H=\kappa/2\), not an assumption that the approximate controls follow a policy.

Set
\[
T_0(y)=qy+q/2,\quad T_1(y)=qy-q/2,\quad
c(w)=\#_0(w)+4\#_1(w),\qquad b=1/q-1/2.
\]
For a word \(w=w_1\cdots w_l\), write \(T_w=T_{w_l}\circ\cdots\circ T_{w_1}\) and retain the complete feasible interval
\[
I_w=[-1,1]\cap\bigcap_{k=1}^l
T_{w_1\cdots w_k}^{-1}([-1,1]).
\]
Every intermediate constraint is present. Let \(N_m\) be the minimum number of cost-at-least-\(m\) words whose intervals cover all \([-1,1]\). A minimum can be normalized at first cost crossing:
\[
m\le c(w)\le m+3,\qquad \lceil m/4\rceil\le |w|\le m. \tag{1}
\]
Empty intervals are discarded. Fix any such minimizing family \(\mathcal W_m\), with \(|\mathcal W_m|=N_m\). All assertions below are uniform over the choice of this family.

Use only the authorized selector
\[
\pi_0(y)=0\ (y\le b),\qquad \pi_0(y)=1\ (y>b),\qquad
f(y)=T_{\pi_0(y)}(y).
\]
It is exactly feasible on the whole interval, including the tie:
\[
T_0([-1,b])=[-q/2,1],\qquad T_1((b,1])=(1-q,q/2]\subset[-1,1].
\]
Let \(p_l(y)\) be its first \(l\) inputs and \(C_v=\{y:p_{|v|}(y)=v\}\). These actual cylinders are intervals, possibly half-open or singletons. They satisfy \(C_v\subset I_v\); they are not identified with \(I_v\).

Let \(\mathcal P_m\) denote the actual first-cost-\(m\) policy words on \([-1,1]\), and \(G_m=|\mathcal P_m|\). For an interval \(E\subset[-1,1]\), define \(G_d(E)\) in the same way from actual starting points in \(E\). Set \(G_0(E)=1\) for nonempty \(E\), and \(G_d(\varnothing)=0\). All actual boundary itineraries count.

For \(w\in\mathcal W_m\), \(l=|w|\), and each realized \(v=p_l(y)\) on \(I_w\), define
\[
E_{w,v}=T_v(I_w\cap C_v),\qquad d_{m,v}=(m-c(v))_+.
\]
The endpoint interval retains its actual open or closed ends. It is not enlarged to \([-1,1]\). Define the residual count using only prefixes which have not already stopped:
\[
R_m(\mathcal W_m)=
\sum_{w\in\mathcal W_m}
\ \sum_{\substack{|v|=|w|,\ I_w\cap C_v\ne\varnothing\\c(v)<m}}
G_{m-c(v)}(E_{w,v}). \tag{2}
\]
Each term is an actual continuation count, not a conjectural covering rate.

We use the already proved R11 estimate, independently checked at the used steps:
\[
\forall\eta>0\ \exists A_\eta<\infty\
\forall l\ge1\ \forall J\subset[-1,1]\text{ interval},\quad
|J|\le2q^{-l}\ \Longrightarrow\
\#\{p_l(y):y\in J\}\le A_\eta e^{\eta l}. \tag{3}
\]
Here and below \(|J|\) is interval length; an included singleton has length zero but still has an itinerary. The uniform fixed-block proof, not its finite data at one block length, establishes (3). It is not reproved or claimed as a new R12 result.

**Theorem 12.1 (optimal-cover incidence and actual residual budgets).**

(a) For every \(m\ge1\), every normalized minimizing cover \(\mathcal W_m\), and every word \(a\) with \(c(a)\ge m\),
\[
\#\{w\in\mathcal W_m:I_w\cap I_a\ne\varnothing\}\le3. \tag{4}
\]
Empty \(I_a\) gives zero. Thus every actual cylinder \(C_u\) of a word \(u\in\mathcal P_m\) meets at most three intervals of \(\mathcal W_m\), including intersections at boundaries.

(b) For every \(\eta>0\), every \(m\ge1\), and every such minimizing cover,
\[
0\le R_m(\mathcal W_m)\le3G_m,\qquad
G_m\le R_m(\mathcal W_m)+A_\eta e^{\eta m}N_m. \tag{5}
\]
Consequently, for every choice of minimizing covers,
\[
\lim_{m\to\infty}\frac1m
\ln\left(1+\frac{R_m(\mathcal W_m)}{N_m}\right)=g-\kappa, \tag{6}
\]
where \(g=\lim_m\ln G_m/m\) and \(\kappa=\lim_m\ln N_m/m\) are the existing R11 and R09 rates. In particular, the requested comparison is equivalent to
\[
\ln\left(1+R_m(\mathcal W_m)/N_m\right)=o(m). \tag{7}
\]
Unlike R11's maximum-deficit or full-interval residual conditions, (7) is necessary as well as sufficient. It has **not** been established.

(c) For every nonempty interval \(E\subset[-1,1]\), every integer \(d\ge1\), and every \(\eta>0\),
\[
\frac{|E|}{2}q^{\lceil d/4\rceil}
\le G_d(E)\le
A_\eta e^{\eta d}\left(1+\frac{|E|}{2}q^d\right). \tag{8}
\]
For each fixed \(w\), its realized length-\(|w|\) pieces satisfy the exact length identity
\[
\sum_v |E_{w,v}|=q^{|w|}|I_w|\le2. \tag{9}
\]
Define the two explicit endpoint moments, with the same unstopped indices as (2),
\[
M_m^-=\sum_{w,v:\,c(v)<m}|E_{w,v}|q^{\lceil(m-c(v))/4\rceil},
\qquad
M_m^+=\sum_{w,v:\,c(v)<m}|E_{w,v}|q^{m-c(v)}. \tag{10}
\]
For all \(\eta,\zeta>0\),
\[
\frac12 M_m^-\le R_m
\le A_\eta e^{\eta m}
\left(A_\zeta e^{\zeta m}N_m+\frac12 M_m^+\right). \tag{11}
\]
These are actual quantitative length-budget estimates. For example:

- if \(M_m^+/N_m\) is subexponential, the requested comparison follows;
- if \(M_m^-/N_m\ge e^{am}\) for some \(a>0\) and infinitely many \(m\), then \(g-\kappa\ge a\), and the comparison is false.

Neither hypothesis in these examples has been proved for minimizing covers. The two moment conditions are not declared equivalent to each other or to (7).

## 2. A replacement proof of the constant three

A minimizing cover is irredundant. In particular, no one of its nonempty intervals is contained in another: otherwise its word could be removed while all actual ratios remain covered, contradicting minimality.

Therefore its intervals can be ordered as
\[
I_j=[\alpha_j,\beta_j],\qquad
\alpha_1<\cdots<\alpha_{N_m},\quad
\beta_1<\cdots<\beta_{N_m}. \tag{12}
\]
Equal left or right endpoints would also imply containment and are excluded. This applies to closed feasible intervals, including any hypothetical singleton; no boundary is deleted.

Suppose a legal interval \(I_a\), \(c(a)\ge m\), meets four distinct cover intervals \(I_{j_1},I_{j_2},I_{j_3},I_{j_4}\), with increasing indices. The set
\[
I_{j_1}\cup I_a\cup I_{j_4}
\]
is an interval, since \(I_a\) meets both outer intervals. Its left endpoint is at most \(\alpha_{j_1}\), and its right endpoint at least \(\beta_{j_4}\). By (12), it therefore contains both \(I_{j_2}\) and \(I_{j_3}\).

Remove the two middle words and add \(a\), keeping every other word, including the outer two. The new catalogue covers the whole \([-1,1]\), consists of cost-at-least-\(m\) words, and has at most \(N_m-1\) words. If \(a\) was already present, its size is smaller still. Its coverage uses the complete intervals, so all intermediate controlled constraints of the new assignment hold. One may normalize \(a\) at first crossing if desired; that enlarges its feasible interval and does not increase cardinality. This contradicts the definition of \(N_m\), proving (4).

This is a minimum-cover replacement argument, an existing interval method. The cost threshold matters: inserting a word of smaller cost would not yield the contradiction. The result does not say that the fixed policy itself is a minimizing cover.

## 3. The actual endpoint count and all stopping times

For each \(w\in\mathcal W_m\), let
\[
P_m(I_w)=\{u\in\mathcal P_m:C_u\cap I_w\ne\varnothing\}.
\]
Every policy stopping word has an actual initial witness, and the minimizing cover covers every such witness. Conversely, \(C_u\subset I_u\), with \(c(u)\ge m\); (4) permits at most three cover intervals to meet \(C_u\). Counting the pairs \((w,u)\) gives the exact incidence bounds
\[
G_m\le\sum_{w\in\mathcal W_m}|P_m(I_w)|\le3G_m. \tag{13}
\]
Open policy endpoints cause no exception: a nonempty intersection with \(C_u\) is also an intersection with the closed full feasible interval \(I_u\).

Fix \(w\), \(l=|w|\). Split \(P_m(I_w)\) according to whether its stopping time is greater than \(l\) or at most \(l\).

For the first part, the length-\(l\) prefix is one uniquely determined realized word \(v\) with \(c(v)<m\). If \(y\in I_w\cap C_v\), its actual endpoint is \(x=T_v(y)\in E_{w,v}\). Its first-cost-\(m\) policy word is exactly \(v\) followed by the first-cost-\((m-c(v))\) policy word from \(x\). Conversely, every such continuation from \(E_{w,v}\) has a unique initial preimage under the affine map \(T_v\), lying in \(I_w\cap C_v\). It follows the same policy through the entire prefix and suffix, and first crosses \(m\) at the claimed time.

This is a bijection of distinct words for a fixed \(v\). Different length-\(l\) words \(v\) give different completed words. Thus
\[
\#\{u\in P_m(I_w):|u|>l\}
=\sum_{\substack{|v|=l,\ I_w\cap C_v\ne\varnothing\\c(v)<m}}
G_{m-c(v)}(E_{w,v}). \tag{14}
\]
There is no common-suffix substitution between different controls or endpoints.

Let \(B_m\) be the sum, over \(w\), of the counts with stopping time at most \(|w|\), with stopping ancestors deduplicated within each \(w\). Every such ancestor is the first-cost-\(m\) ancestor of some realized length-\(|w|\) prefix. Since
\(\operatorname{diam}I_w\le2q^{-|w|}\), (3) and (1) imply
\[
B_m\le\sum_w A_\eta e^{\eta|w|}
\le A_\eta e^{\eta m}N_m. \tag{15}
\]
This is an upper bound; different longer prefixes may have the same stopping ancestor and are not assumed to give distinct ancestors.

Equations (13)--(15) give
\[
G_m\le R_m+B_m\le3G_m,
\]
and therefore (5). Points on the switch threshold, on the boundary of a feasible interval, or in singleton policy pieces participate in these exact word counts. All newly used times are exactly feasible under the policy. Nothing has been inferred from the final endpoint alone.

## 4. Why the refined residual criterion is an equivalence

Put \(\gamma=g-\kappa\ge0\). The existing rates imply
\(\ln(G_m/N_m)/m\to\gamma\). From \(R_m/N_m\le3G_m/N_m\),
\[
\limsup_m m^{-1}\ln(1+R_m/N_m)\le\gamma. \tag{16}
\]
If \(\gamma=0\), the logarithm is nonnegative and (16) proves (6).

If \(\gamma>0\), choose any \(0<\eta<\gamma\). For every sufficiently small \(\xi>0\) with \(\eta<\gamma-\xi\), eventually
\[
G_m/N_m\ge e^{(\gamma-\xi)m}.
\]
By (5),
\[
R_m/N_m\ge e^{(\gamma-\xi)m}-A_\eta e^{\eta m}
\ge\tfrac12e^{(\gamma-\xi)m}
\]
for all sufficiently large \(m\). Let \(\xi\downarrow0\). Together with (16) this proves (6), uniformly over whatever minimizing family is chosen at each \(m\).

The equivalence (7) follows. More directly, if \(R_m/N_m\) is subexponential, (5), with an arbitrarily small \(\eta\), implies that \(G_m/N_m\) is subexponential. The reverse implication follows from \(R_m\le3G_m\).

A possible positive exponential residual burden is thus not caused by exponentially many duplicate appearances of a policy stopping word in a minimizing cover. That duplication has a proved constant bound. This conclusion uses optimality of the exact cover and is absent from the arbitrary-cover bound of R11.

## 5. Quantitative continuation bounds on the actual endpoint intervals

For the lower bound in (8), each first-cost-\(d\) policy suffix \(a\) has length
\[
|a|\ge\lceil d/4\rceil,
\]
because no input costs more than four. Its actual cylinder is contained in \(I_a\), and the last map has slope \(q^{|a|}\), so
\[
\operatorname{diam}C_a\le\operatorname{diam}I_a
\le2q^{-|a|}\le2q^{-\lceil d/4\rceil}.
\]
These cylinders cover all actual points of \(E\). Finite subadditivity of interval length gives the lower bound in (8). For an actual singleton the lower bound is zero, but its itinerary still counts.

For the upper bound, cover the closed hull of \(E\) by
\[
k\le1+\frac{|E|}{2}q^d
\]
closed intervals of length at most \(2q^{-d}\), all within \([-1,1]\). A nonempty singleton uses one interval. Each policy orbit crosses cost \(d\) by its \(d\)-th input, because every input costs at least one. Hence its stopping word is the ancestor of its length-\(d\) prefix. Applying (3) to each short interval,
\[
G_d(E)\le k A_\eta e^{\eta d}.
\]
Adding endpoints to obtain an upper cover only adds possible itineraries; it does not remove the actual boundary ones. This proves (8), with the same uniform constant from (3).

For (9), the sets \(I_w\cap C_v\) form a finite disjoint partition of \(I_w\), including all point assignments. Every affine \(T_v\) at this length has the same slope \(q^{|w|}\). Therefore the sum of their image lengths, whether or not different images overlap, is exactly \(q^{|w|}|I_w|\). The last complete feasible constraint gives \(|I_w|\le2q^{-|w|}\). The endpoint images have not been treated as disjoint.

Finally the number of unstopped pairs \((w,v)\) is at most
\[
\sum_w\#\{p_{|w|}(y):y\in I_w\}
\le A_\zeta e^{\zeta m}N_m. \tag{17}
\]
Each \(d=m-c(v)\) is at most \(m\). Sum (8), use (17), and obtain (11).

If \(M_m^+/N_m\) is subexponential, divide (11) by \(N_m\) and let \(\eta,\zeta\) be arbitrarily small. Then (7) holds. If \(M_m^-/N_m\ge e^{am}\) infinitely often, (11) and (5) give \(G_m/N_m\ge e^{am}/6\) on that sequence, and the existing rate limit gives \(\gamma\ge a\). These are conditional consequences, not verified assertions about optimal covers. This completes Theorem 12.1. ∎

## 6. The exact unresolved step

The attack removes an unbounded-overcount explanation for the *refined actual endpoint* sum and proves how endpoint length can suppress, or fail to suppress, a remaining budget:

- an endpoint of size \(O(q^{-d})\) contributes only subexponentially in \(d\) by (8), even if \(d\) is large;
- a positive-length endpoint contributes at least \((|E|/2)q^{\lceil d/4\rceil}\);
- singleton and boundary contributions remain in the unit term and actual word counts.

What is not proved is a deficit-dependent squeezing or distribution estimate on the actual \(E_{w,v}\) of a minimizing cover. The identity (9) bounds their total length by two per word, but does not give the budget-weighted bound in (10). It is therefore insufficient.

R11's trajectory identity was checked algebraically:
\[
c(p_l(y))-c(w)=\frac{3(q-1)}q\sum_{k=1}^{l-1}
(y_k^\pi-y_k^w)-\frac3q(y_l^\pi-y_l^w).
\]
Feasibility bounds each summand but supplies neither its sign nor a sublinear cumulative bound. R10's cost difference 57 and nonzero endpoint shift do not settle this accumulation. Neither shortcut closes (7); their failures are not counterexamples to the requested comparison.

The single minimum unresolved assertion, now with duplication and already-stopped terms controlled, is
\[
\ln(1+R_m(\mathcal W_m)/N_m)=o(m).
\]
It is equivalent to the original comparison, not assumed as a structural hypothesis. A bound on the explicit positive-budget endpoint moment \(M_m^+\) would suffice; its failure alone would not disprove the comparison. A positive exponential lower moment would disprove it, but none has been constructed.

The round proves neither \(g=\kappa\) nor \(g>\kappa\), and does not evaluate \(\kappa\). R09's existence of the genuine precision-cost rate and its two distinct bounds remain unchanged. No new pressure root, finite-state assumption, coding restriction, strategy, parameter or model has been introduced.

## 7. Dependencies and contribution boundary

The used R11 proofs are exact policy feasibility and cylinders, the diameter bound, the uniform fixed-block estimate, and the existing rate of \(G_m\). The R09 interval definition, threshold normalization, full-time genuine-to-exact comparison and rate of \(N_m\) were restored at their actual dependency steps; no affecting error was found. R10's full forced-block and mixed-cover proof was read for the rejected cost shortcut; its common-tail counterexample is not reused as a new result.

The new project interface is the cost-threshold replacement bound (4), the exact endpoint residual bijection (14), and their quantitative combination (5), (8), (11). Minimum interval-cover exchanges, interval-length counting, fixed-block multiplicity and subadditivity are existing methods; no general originality or all-literature priority is claimed.

This is a limited technical advance over R11, not a new main rate theorem or a basis to raise the journal-tier assessment of the unchanged stage paper. It gives a necessary-and-sufficient residual criterion and explicit scale tests, but leaves their dynamical content on minimizing covers unresolved. No independent publication value for this interface alone is established.
