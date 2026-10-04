# R17: the sharp common-cost boundary in the matched family

4 October 2026 (UTC). Natural logarithms. This is a unified corollary of the R15–R16 proof methods, with the parameter-dependent controlled comparison verified below. The boundary statement and its simultaneous quantifiers are new to the project; no new counting or pressure mechanism is claimed.

## 1. Object, attribution, and complete statement

Fix
\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,\quad \beta>1,
\]
\[
F_0(s,z)=(a_0^\beta s,a_0^{\beta-1}(z+a_1s)),\qquad
F_1(s,z)=(a_1^\beta s,a_1^{\beta-1}(z-a_0s)),
\]
\[
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad \operatorname{area}(Q)=1.
\]
All infinite binary inputs are allowed. For nonempty compact \(K\subset Q\), keep
\[
r(n,\delta;K)=\min\{|\mathcal C|:\mathcal C\subset\{0,1\}^{\mathbb N}
\text{ finite},\
\forall x\in K\ \exists u\in\mathcal C\ \forall k=0,\ldots,n:\
\operatorname{dist}_2(\varphi(k,x,u),Q)<\delta\}. \tag{1}
\]
This is the actual initial-state catalogue with Euclidean ambient distance. One tolerance is imposed throughout each horizon. The selected inputs may leave and reenter \(Q\).

Write
\[
a_{\min}=\min(a_0,a_1),\quad a_{\max}=\max(a_0,a_1),\qquad
H(p)=-p\ln p-(1-p)\ln(1-p),
\]
with \(0\ln0=0\), and set
\[
h=H(a_0),\qquad
\chi(p)=-p\ln a_0-(1-p)\ln a_1,\qquad \gamma_*=\beta h.
\]
Thus \(\chi(a_0)=h\).

**Theorem 17.1 (sharp boundary for common cost).**

(a) For every fixed positive-area compact \(K\subset Q\), every finite \(0\le\gamma\le\gamma_*\), and every positive sequence \(\delta_n\to0\) with
\[
-\ln\delta_n/n\longrightarrow\gamma,
\]
the limit exists and is \(\gamma/\beta\). This is R15 Theorem 15.1, including equality at the boundary.

(b) For every \(\varepsilon\in(0,1)\), there exists one compact \(K_\varepsilon\subset Q\) with
\[
\operatorname{area}(K_\varepsilon)>1-\varepsilon,
\]
such that for every finite \(\gamma>\gamma_*\), and every sequence with the stated exponent,
\[
\lim_{n\to\infty}\frac{\ln r(n,\delta_n;K_\varepsilon)}n=h
<
\liminf_{n\to\infty}\frac{\ln r(n,\delta_n;Q)}n. \tag{2}
\]
The same \(K_\varepsilon\) works for all these exponents, all their tolerance sequences, and all horizons. It may depend on the fixed system and \(\varepsilon\). It contains the vertex and can have empty interior.

An explicit sufficient lower gap is as follows. Put
\[
\Delta=\chi(1/2)-h=(a_0-\tfrac12)\ln(a_0/a_1)>0,
\]
\[
\theta_\gamma=\min\left\{\tfrac12,\frac{\gamma/\beta-h}{2\Delta}\right\},
\qquad
p_\gamma=(1-\theta_\gamma)a_0+\theta_\gamma/2.
\]
Then
\[
\liminf_n n^{-1}\ln r(n,\delta_n;Q)
\ge H(p_\gamma)>h. \tag{3}
\]
This is a lower bound, not an exact full-\(Q\) rate formula or a claim that its limit has been established here.

Consequently \(\gamma_*\) is exactly the boundary of the finite precision exponents at which every positive-area compact initial set has a common cost in this family. At each larger exponent the single set in (b) and \(Q\) already give a strict separation. This does not classify all positive-area sets into two cost types.

**What follows from earlier work.** Part (a) is unchanged R15. The construction and upper count for a fixed typical compact set, and its arbitrary-input area lower bound, use R15 §3.2 and R16 §5. They already give the first equality in (2) for every high exponent, once the choice of the set is made before \(\gamma\). R16's theorem statement alone only covers one system and one exponent; it cannot simply be substituted for (b). The one interface requiring an explicit parameter check is its midpoint comparison. Lemma 17.2 supplies that check. After it, a type arbitrarily close to \(a_0\), in the direction of \(1/2\), proves (3). These are consequences of the existing methods, not an additional core mechanism.

## 2. Full feasible intervals and arbitrary tails

For \(s>0\), use \(y=z/s\) only as a calculation coordinate. The actual state remains \((s,z)\). The angle maps and inverse branches are
\[
T_0(y)=(y+a_1)/a_0,\quad T_1(y)=(y-a_0)/a_1,\qquad
B_0(y)=a_0y-a_1,\quad B_1(y)=a_1y+a_0.
\]
With \(\xi=a_0-a_1\), the one-step feasible domains are \([-1,\xi]\) and \([\xi,1]\), each mapped onto \([-1,1]\). Assign a tie to 0 for the natural coding. At the vertex both inputs fix the state.

For a word \(w=w_1\cdots w_l\), define \(\lambda_w=\prod_{j=1}^l a_{w_j}\) and \(\lambda_\varnothing=1\). Its complete exact feasible interval is
\[
I_w=B_{w_1}\circ\cdots\circ B_{w_l}([-1,1]),\qquad |I_w|=2\lambda_w. \tag{4}
\]
Indeed \(I_{iv}=I_i\cap T_i^{-1}(I_v)=B_i(I_v)\); this identity retains all intermediate constraints. At any fixed depth these closed intervals cover \([-1,1]\) with disjoint interiors. After \(w\) the actual radius is \(s\lambda_w^\beta\), and the angle-map slope is \(\lambda_w^{-1}\).

There is a common contracting norm for all inputs, including infeasible ones. For example take
\[
M=1+\max_{i=0,1}
\frac{a_i^{\beta-1}a_{1-i}}{1-a_i^{\beta-1}},\qquad
\|(s,z)\|_M=\max\{M|s|,|z|\}.
\]
The operator norm of \(F_i\) is at most
\[
\max\{a_i^\beta,\ a_i^{\beta-1}+a_i^{\beta-1}a_{1-i}/M\}.
\]
Its maximum over \(i\) is a constant \(L<1\), by \(\beta>1\) and the strict choice of \(M\). Also \(\|x\|_2\le\sqrt2\|x\|_M\). Set \(C_0=2\sqrt2M\).

## 3. The controlled comparison for all fixed parameters

For \(n\ge1\) and \(0<t<1\), stop every binary branch at the first word with \(\lambda_w\le t\), or at depth \(n\) if no earlier crossing occurs. Let \(\mathcal L(n,t)\) be this finite complete prefix-free leaf family, and \(N(n,t)\) its cardinality. A depth-\(n\) crossing is counted as one terminal leaf, not twice. Every leaf satisfies
\[
\lambda_{w^-}>t,\qquad \lambda_w>a_{\min}t. \tag{5}
\]
Here \(w^-\) removes the last letter. These inequalities hold for terminal leaves too, since all their proper prefixes precede a crossing. The corresponding closed intervals cover the whole angle range and have disjoint interiors.

**Lemma 17.2 (parameter-dependent witness comparison).** Set
\[
B=\left\lceil1+a_{\min}^{-\beta}\right\rceil.
\]
For every \(n\ge1\) and \(0<\delta<1\),
\[
\frac{N(n,\delta^{1/\beta})}{1+Bn}
\le r(n,\delta;Q)
\le N\left(n,(\delta/C_0)^{1/\beta}\right). \tag{6}
\]
The constants depend on the fixed system only. No uniformity as parameters approach their excluded endpoints is asserted.

**Proof.** For the lower bound put \(t=\delta^{1/\beta}\). Choose the midpoint \(y_w\) of every stopped interval, and the actual witness \(x_w=(1,y_w)\in Q\). By (5), every interval length is greater than \(2a_{\min}t\). Ordered midpoints of disjoint-interior intervals are consequently separated by more than \(2a_{\min}t\), even when their depths differ.

Fix any length-\(n\) input \(u\). There is at most one leaf which is a prefix of \(u\). For every other witness covered by \(u\), let \(j\le |w|\) be the first disagreement between \(u\) and \(w\). Let \(a=u_1\cdots u_{j-1}\), \(i=u_j\), and \(b_a=T_a^{-1}(\xi)\). The midpoint lies strictly in the opposite feasible child of \(I_a\). Since \(T_0(\xi)=1\) and \(T_1(\xi)=-1\), the state at that disagreement satisfies
\[
|y_j|-1=\frac{|y_w-b_a|}{a_i\lambda_a},\qquad
s_j=(a_i\lambda_a)^\beta. \tag{7}
\]
All preceding controls agree with an exact feasible prefix. No feasibility after this disagreement has been assumed.

A necessary condition for \((s_j,z_j)\in Q^\delta\), with \(s_j\ge0\), is
\[
|z_j|-s_j<2\delta. \tag{8}
\]
To see this compare both coordinates with a point of \(Q\) at Euclidean distance less than \(\delta\). Equations (7)–(8) imply
\[
|y_w-b_a|
<\frac{2\delta}{(a_i\lambda_a)^{\beta-1}}
<2a_{\min}^{1-\beta}t. \tag{9}
\]
The last inequality uses \(\lambda_a>t\), since \(a\) is a proper prefix of the stopped leaf, and \(\beta>1\). This calculation is the precise matching of the first-deviation band with the stopped interval scale; it is valid for either branch and every allowed \(\beta\).

For fixed \(u,j\), the center and the side of this band are fixed. Its length is less than \(2a_{\min}^{1-\beta}t\). The midpoint spacing bounds its count by \(1+a_{\min}^{-\beta}\), hence by \(B\). Summing over \(j\le n\), and adding the one possible prefix leaf, gives at most \(1+Bn\) witnesses for any input. Any catalogue covering all actual states of \(Q\) must cover them, proving the lower bound. Subsequent reentry into \(Q\) cannot remove the necessary constraint at time \(j\).

For the upper bound use all leaves at \(t=(\delta/C_0)^{1/\beta}\), each followed by one fixed infinite tail. A terminal leaf is exactly feasible at every required time. At an earlier stopping time the state has \(|z|\le s\le\lambda_w^\beta\le\delta/C_0\), so its \(M\)-norm is at most \(M\delta/C_0\). Every later input contracts this norm. The entire remaining trajectory is at Euclidean distance at most \(\delta/2\) from the origin in \(Q\), strictly inside the required open neighborhood. The leaf intervals include all shared endpoints and boundary rays; the vertex is fixed. This proves (6). ∎

This proof generalizes R16 Lemma 16.2, and retains the R06 first-deviation architecture. It does not assume a natural stopping tree is an optimal catalogue. The lower estimate tests arbitrary approximate inputs and gives the required zero-rate loss. Constant changes in the upper threshold are not, by themselves, asserted to prove an exact rate for \(N\).

## 4. One fixed compact set for every high exponent

Under normalized angular Lebesgue measure, an assigned natural prefix \(w\) has probability \(\lambda_w\), by (4); shared endpoints and their iterated preimages are countable. Thus the digits have product weights \(a_0,a_1\). If \(p\) is the zero frequency in a word of length \(k\), its type probability is at most
\[
\exp[-kD(p\Vert a_0)],\qquad
D(p\Vert a_0)=p\ln(p/a_0)+(1-p)\ln((1-p)/a_1).
\]
The binomial bound used here follows from
\(\binom{k}{kp}\le \exp(kH(p))\).
Since \(D''(p)=1/[p(1-p)]\ge4\), \(D(p\Vert a_0)\ge2(p-a_0)^2\). Summing the at most \(k+1\) types proves summability for every fixed frequency deviation. Borel–Cantelli, with a countable sequence of deviations, gives zero frequency tending to \(a_0\) almost everywhere.

Apply Egorov and inner regularity once to choose compact \(E_\varepsilon\subset(-1,1)\), avoiding the countable boundary set, with
\[
|E_\varepsilon|>2(1-\varepsilon),
\]
on which the frequency convergence is uniform. All these choices precede any \(\gamma\), tolerance sequence, or horizon. Define
\[
K_\varepsilon=\{(s,sy):0\le s\le1,\ y\in E_\varepsilon\}. \tag{10}
\]
It is the continuous image of a compact set and includes the vertex. The physical Jacobian is \(s\), so its area is \(|E_\varepsilon|/2>1-\varepsilon\). Boundary preimages are dense because the maximum depth-\(k\) interval length is \(2a_{\max}^k\to0\); hence this construction can have empty interior.

For every \(\eta>0\), all length-\(n\) natural prefixes realized on \(E_\varepsilon\), for sufficiently large \(n\), have zero frequency within \(\eta\) of \(a_0\). Their number is at most
\[
(n+1)\exp\left(n\max_{\substack{p\in[0,1]\\|p-a_0|\le\eta}}H(p)\right). \tag{11}
\]
Use these words as exact length-\(n\) prefixes, each extended to an infinite input. They cover every point of (10) at all times through \(n\), for every \(\delta>0\). Taking rates and then \(\eta\downarrow0\) gives
\[
\limsup_n n^{-1}\ln r(n,\delta_n;K_\varepsilon)\le h \tag{12}
\]
for every positive tolerance sequence, without an exponent restriction.

For completeness, the R15 arbitrary-input area bound gives the matching lower rate on this very same set. Let \(p_k(y)\) denote the length-\(k\) natural control prefix of \(y\). Uniform frequency convergence implies, for every \(0<\zeta<h\), a constant \(D_\zeta\ge1\) with
\[
D_\zeta^{-1}e^{-(h+\zeta)k}\le
\lambda_{p_k(y)}\le D_\zeta e^{-(h-\zeta)k}
\quad(y\in E_\varepsilon,\ k\ge0). \tag{13}
\]
For any input \(u\), let \(V(n,\delta,u)\) be its actual all-time admissible initial subset of \(Q\). Agreement with the natural code through \(m\le n\) occupies at most one interval of cone area \(D_\zeta e^{-(h-\zeta)m}\). At the first difference \(j\le m\), for arbitrary initial radius \(s>0\), (7)–(8) give a band of angular length at most
\[
\frac{2\delta}{s(a_{u_j}\lambda_{u_1\cdots u_{j-1}})^{\beta-1}}.
\]
Integrating against \(s\,ds\) cancels \(1/s\), so its area is at most
\(2\delta a_{\min}^{1-\beta}\lambda_{u_1\cdots u_{j-1}}^{1-\beta}\).
If this difference class meets (10), its common prefix is realized on \(E_\varepsilon\), and (13) bounds the product below. Sum the resulting geometric progression to obtain
\[
\operatorname{area}(K_\varepsilon\cap V(n,\delta,u))
\le C_\zeta\left[
e^{-(h-\zeta)m}+\delta e^{(\beta-1)(h+\zeta)m}\right]. \tag{14}
\]
The constant is independent of \(u,n,m,\delta\). Empty difference classes contribute zero. Boundary states remain covered by the exact upper catalogue, and the vertex has zero area only for this lower estimate.

Now fix any finite \(\gamma>\beta h\), and any tolerance sequence of exponent \(\gamma\). For every sufficiently small
\[
0<\zeta<\min\{h,\gamma/\beta-h\},
\]
we eventually have \(\delta_n e^{\beta(h+\zeta)n}\le1\). With \(m=n\), (14) is at most \(2C_\zeta e^{-(h-\zeta)n}\). Summing areas over any catalogue spanning the positive-area set gives
\[
r(n,\delta_n;K_\varepsilon)\ge
\frac{\operatorname{area}(K_\varepsilon)}{2C_\zeta}e^{(h-\zeta)n}. \tag{15}
\]
Let \(\zeta\downarrow0\) and combine with (12). The resulting limit is \(h\).

The set in (10) has not changed during this argument. The auxiliary \(\zeta\) and the time from which (15) applies can depend on \(\gamma\) and the sequence; this is compatible with the simultaneous quantifier in Theorem 17.1. No common positive gap as \(\gamma\downarrow\beta h\) has been used.

## 5. Full-cone strict separation at every high exponent

Fix \(\gamma>\beta h\). The explicit \(\Delta,\theta_\gamma,p_\gamma\) in §1 satisfy
\[
0<\theta_\gamma\le1/2,\qquad
\chi(p_\gamma)=h+\theta_\gamma\Delta
\le h+\tfrac12(\gamma/\beta-h)<\gamma/\beta. \tag{16}
\]
Since \(a_0\ne1/2\), \(p_\gamma\) lies strictly between \(a_0\) and \(1/2\). The strict increase of binary entropy toward \(1/2\) implies
\[
H(p_\gamma)>H(a_0)=h. \tag{17}
\]

Put \(t_n=\delta_n^{1/\beta}\) and \(T_n=-\ln t_n\), so \(T_n/n\to\gamma/\beta\). Choose integers \(j_n\) with \(j_n/n\to p_\gamma\). Every length-\(n\) word of this zero type has total product cost
\[
-\ln\lambda_w=n\chi(j_n/n)<T_n
\]
for all sufficiently large \(n\), by (16). All increments \(-\ln a_i\) are positive; consequently no earlier prefix can cross \(T_n\). All such words are terminal leaves of \(\mathcal L(n,t_n)\).

The elementary type bounds are
\[
\frac{\exp(nH(j/n))}{n+1}\le\binom nj\le\exp(nH(j/n)). \tag{18}
\]
For \(0<j<n\), use the binomial distribution with parameter \(j/n\): its mass at \(j\) is a mode (check the two adjacent mass ratios), hence lies between \(1/(n+1)\) and 1. The endpoint cases are immediate. This proves (18) without an asymptotic or numerical approximation.

By Lemma 17.2 and these terminal leaves,
\[
r(n,\delta_n;Q)\ge
\frac{\binom n{j_n}}{1+Bn}
\ge\frac{\exp(nH(j_n/n))}{(n+1)(1+Bn)}. \tag{19}
\]
Taking the lower rate gives (3), then (17) and §4 prove (2).

The argument only requires convergence of \(-\ln\delta_n/n\). It covers nonmonotone sequences and arbitrary subexponential perturbations. It does not impose exact feasibility on an optimal approximate catalogue.

Part (a) follows from the verified R15 bounds
\[
\min\{h,\gamma/\beta\}
\le\liminf n^{-1}\ln r(n,\delta_n;K)
\le\limsup n^{-1}\ln r(n,\delta_n;K)
\le\min\{\ln2,\gamma/\beta\}. \tag{20}
\]
Specifically, R15 §3.2 retains a fixed positive-area typical portion of any given \(K\), applies the same (14) with
\(m=\min\{n,\lfloor-\ln\delta/[\beta(h+\zeta)]\rfloor\}\),
and then lets \(\zeta\downarrow0\). Its upper bound is the full-time stopping catalogue of §2–3, counted using the sum of its relative interval lengths. These steps include \(\gamma=\beta h\) and \(\gamma=0\). For \(\gamma\le\beta h\), (20) matches at \(\gamma/\beta\). Theorem 17.1 is complete. ∎

## 6. What the boundary explains and what it does not

Matching balances angular interval length \(\lambda_w\) with radial size \(\lambda_w^\beta\). The first-deviation band then has the same order as a stopped interval. Arbitrary approximate controls cannot discard an exponential number of the full-cone witnesses.

For every exponent just above \(\beta h\), words with a frequency slightly closer to \(1/2\) than \(a_0\) are still unstopped at time \(n\). They are more numerous than the typical prefixes. Their total angular mass is at most \(\exp(n[H(p)-\chi(p)])=\exp[-nD(p\Vert a_0)]\), up to the type specification. They can therefore be rare in area while forcing more controls when every point of \(Q\) must be covered. One uniformly typical compact set excludes all fixed deviations eventually, which is why one choice works for every high exponent.

The project now has a sharp precision boundary in its existing unequal-width matched linear family, rather than an isolated high-precision example. The full-\(Q\) lower gap, general constants, and simultaneous fixed-set assertion were not stated as completed results in R15–R16. Their proofs require no new mechanism beyond the verified transfer of those arguments. The appropriate attribution is a unified corollary with a checked controlled geometric lemma.

No exact high-precision spectrum for full \(Q\), general initial-set classification, perturbation theorem, overlap theorem, or nonlinear extension is claimed. R09–R14 remain paused. The unique existing paper is unchanged. Repeating parameter changes or optimizing another type-count constant in this same class would have limited additional value; any later research must justify an independently useful new mathematical obstruction, rather than count another round as an upgrade.
