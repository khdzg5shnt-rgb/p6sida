# R39: nondegenerate transients and precision–reliability transfer

2026-10-08 (UTC). Adopted repository baseline:
1d1ad60befd0278bc255ba57a2ef21b9c25a1ca8.

## 1. Statement, objects, and scope

Fix \(a_0,a_1\in(0,1)\), \(a_0+a_1=1\), \(a_0\ne a_1\), and
\(\beta>1\). Put \(r_i=a_i^\beta\). Let \(F_0,F_1:\mathbb R^2\to
\mathbb R^2\) be \(C^2\) maps, fixing the origin, with

\[
DF_0(0)=\begin{pmatrix}r_0&0\\r_0a_1/a_0&r_0/a_0\end{pmatrix},
\qquad
DF_1(0)=\begin{pmatrix}r_1&0\\-r_1a_0/a_1&r_1/a_1\end{pmatrix}.
\tag{39.1}
\]

The triangle \(Q=\{(s,z):0\le s\le1,\ |z|\le s\}\) is controlled
invariant: at every \(x\in Q\) at least one \(F_i x\) lies in \(Q\).
There are fixed \(\Lambda\ge1\), \(\theta\in(0,1)\) such that

\[
V(s,z)=\max\{\Lambda|s|,|z|\},\qquad V(F_i x)\le\theta V(x)
\quad(x\in\mathbb R^2,\ i=0,1).
\tag{39.2}
\]

This is contraction towards the origin, not contraction of the
distance between arbitrary pairs of states. Assume additionally

\[
\det DF_i(x)\ne0\quad(x\in Q,\ i=0,1).
\tag{39.3}
\]

No global injectivity, global inverse, triangular formula, radius
autonomy, exact state-dependent power identity, or assigned coding
is assumed.

Let \(\Omega=\{0,1\}^{\mathbb N}\), let \(F_u^k\) denote composition
of the first \(k\) inputs, and let \(\mu\) be area on \(Q\). Since
\(\operatorname{area}(Q)=1\), it is already a probability measure.
For \(u\in\Omega\), \(n\ge0\), \(\delta>0\), define the actual set

\[
A_u(n,\delta;Q)=
\{x\in Q:\operatorname{dist}(F_u^k x,Q)<\delta
                  \text{ for every }0\le k\le n\}.
\tag{39.4}
\]

All distances are Euclidean. Trajectories may leave and reenter
\(Q\); every intermediate constraint in (39.4) is retained. Write
\(r_e(n,\delta;Q)\) for the least size of a finite catalogue
\(\mathcal U\subset\Omega\) with
\(\mu(\bigcup_{u\in\mathcal U}A_u(n,\delta;Q))\ge1-e\).
This is a choice of an input for each actual initial state, not a
causal communication or feedback capacity. Successful subsets may
vary with \(n\); they are not the fixed compact sets in the manuscript.

Use natural logarithms and \(0\log0=0\). Define

\[
\begin{split}
H_b(p)&=-p\log p-(1-p)\log(1-p),\\
\chi(p)&=-p\log a_0-(1-p)\log a_1,\\
I_a(p)&=\chi(p)-H_b(p),\qquad h=H_b(a_0)=\chi(a_0),\\
S(\gamma)&=\max_{0\le p\le1}H_b(p)
                 \min\{1,\gamma/[\beta\chi(p)]\},\\
L_a(\alpha)&=\max_{I_a(p)\le\alpha}H_b(p).
\end{split}
\tag{39.5}
\]

**Theorem 39.1 (noncritical probability transfer).** For every fixed
system satisfying (39.1)–(39.3), every finite \(\gamma\ge0\),
\(\alpha>0\), and every pair of positive sequences with

\[
\delta_n\longrightarrow0,\quad -\log\delta_n/n\longrightarrow\gamma,
\qquad
e_n\longrightarrow0,\quad -\log e_n/n\longrightarrow\alpha,
\tag{39.6}
\]

one has

\[
\boxed{\displaystyle
\lim_{n\to\infty}\frac1n\log r_{e_n}(n,\delta_n;Q)
=\min\{S(\gamma),L_a(\alpha)\}.}
\tag{39.7}
\]

The constants below depend on the fixed system and, where indicated,
a fixed run bound. They do not depend on \(n,\delta_n,e_n\) or the
particular word. No common constant over all permitted systems is
asserted. Condition (39.3) is sufficient; necessity is not claimed.
R38 shows that replacing it merely by null critical sets is
insufficient for a universal theorem.

## 2. Dependency check and local geometry

The complete adopted proofs were restored, rather than relying on
previous passing reports: R37's linear stopping/probability argument,
R33's finite-transient and fixed-loss area proof, and the manuscript's
local graph, bounded-run, and full-cover stopping proofs. No adopted
error was found. In particular, terminal images need not fill the
angular interval, complete feasible sections can be empty or single
points, and a change between feasible codes is not a true exit.
The following local facts are recorded with their derivation because
they are used in the new probability comparison.

Set \(a_*=\min a_i\), \(a^*=\max a_i\), \(r_*=\min r_i\),
\(r^*=\max r_i\). Write, for \(s>0\), \(|y|\le1\),

\[
R_i(s,y)=F_i^s(s,sy)/s,\qquad
T_i(s,y)=F_i^z(s,sy)/(sR_i(s,y)),
\]

and
\(L_0(y)=(y+a_1)/a_0,\ L_1(y)=(y-a_0)/a_1\).
Taylor's integral formula and the \(C^2\) bound on a fixed
neighbourhood of the origin give finite \(B\) and small \(\rho>0\)
such that

\[
\begin{split}
&R_i\ge r_*/2,\quad |R_i-r_i|\le Bs,\quad
 |\log(R_i/r_i)|\le Bs,\\
&|\partial_s\log R_i|\le B,\quad
 |\partial_y\log R_i|\le Bs,\\
&|T_i-L_i|\le Bs,\quad |\partial_sT_i|\le B,\quad
 |\partial_yT_i-1/a_i|\le Bs .
\end{split}
\tag{39.8}
\]

For example, if \(L\) bounds both second derivatives on
\(\overline B(0,2)\), the manuscript's choices
\(B=10^4(1+L)/r_*^3\) and

\[
0<\rho\le\min\left\{\tfrac14,\frac{r_*}{8(1+L)},
 \frac{1-r^*}{8B},\frac{1/a^*-1}{16B},
 \frac1{16B},\frac{a_*}{16B}\right\}
\tag{39.9}
\]

suffice. These are derived bounds, not new dynamical assumptions.
Put \(\bar r=r^*+B\rho<1\) and
\(\widehat r=r^*+2B\rho<1\). On a feasible local trajectory,
\(s_j\le\bar r^j s_0\). Viability and the other branch's strict
outward image give
\(T_0(s,-1)\ge-1,\ T_1(s,1)\le1\). Each branch has one angular
cut. The two allowed intervals cover \([-1,1]\) and have at most
\(O(s)\) overlap; their endpoints may be sent strictly inward.

For a radial graph \(s=S(y)\), \(|S'/S|\le1\), put \(k=S'/S\).
Its image under input \(i\) has angular derivative and logarithmic
radial slope

\[
J_i=\partial_yT_i+\partial_sT_i S'
       =1/a_i+O(BS)>0,\qquad
k_{\rm new}=
\frac{k+(\partial_s\log R_i)S'+\partial_y\log R_i}{J_i}.
\tag{39.10}
\]

The numerator is at most \(1+2B\rho\) and the denominator at least
\(1/a^*-2B\rho\), so \(|k_{\rm new}|\le1\). Starting with a flat
initial radius, induction applies the next cut to the actual current
interval. Extending its radial graph constantly outside that interval
checks monotonicity of the next cut without asserting any onto image.
Consequently the complete feasible initial section \(I_w(s_0)\)
for a word \(w\) is a closed interval, possibly empty, a point, or
with truncated terminal image. All intermediate constraints have
been imposed in this construction.

Let
\(\lambda_w=\prod_{j=1}^{|w|}a_{w_j}\) and
\(P_w=\prod_{j=1}^{|w|}r_{w_j}=\lambda_w^\beta\).
Summing (39.8) and (39.10) along geometrically decreasing radii
gives, on every feasible section,

\[
C_R^{-1}s_0P_w\le s_{|w|}\le C_Rs_0P_w,\qquad
C_A^{-1}\lambda_w^{-1}\le\frac{dY_w}{dy_0}
                                      \le C_A\lambda_w^{-1},
\tag{39.11}
\]

with \(C_R=\exp(B\rho/(1-\bar r))\) and
\(C_A=\exp(4B\rho/(1-\bar r))\). In the angular bound one uses
\(|a_iJ_i-1|\le2Bs_j\) and then
\(|\log(a_iJ_i)|\le4Bs_j\). These are independent product
comparisons; matching is used only to identify \(P_w=\lambda_w^\beta\).

Integrating over the actual terminal interval, and then using the
physical Jacobian \(s\) of \((s,y)\mapsto(s,sy)\), gives

\[
|I_w(s)|\le2C_A\lambda_w,\qquad
|\mathcal I_w|\le C_A\rho^2\lambda_w,\qquad
\mathcal I_w=\{(s,sy):0<s\le\rho,\ y\in I_w(s)\}.
\tag{39.12}
\]

There is no lower length bound here. Empty, singleton and truncated
sections remain in covers; singleton sections contribute no area.

For later use, the old first-true-exit estimate is also verified.
If prefix \(w\) is feasible and the next prescribed step first
leaves \(Q\), distance less than \(\delta\) requires
\((|z'|-s')_+<2\delta\). Its output radius is at least a fixed
multiple of \(s_0P_w\). Monotonicity of the next angular map and
(39.11) bound its initial-angle band by
\(C\delta\lambda_w/(s_0P_w)\). Integration gives physical area
\(C\delta\lambda_w/P_w\). A cut need not lie inside the actual
terminal image. Later reentry cannot remove the constraint at that
first exit. This is the arbitrary-input estimate already used by
R33; it is not a new probability-discard argument.

## 3. Whole-triangle finite-transient probability domination

Choose once and for all an integer \(J\) such that
\(\theta^J\sup_Q V\le\rho\). For a finite word \(w\), let
\(D_w=\{x\in Q:F_{w|k}x\in Q,\ 0\le k\le|w|\}\), and
\(D_\varnothing=Q\). These sets are compact.

**Lemma 39.2.** There is a finite \(K_J\), uniform over
\(1\le|w|\le J\), such that every Lebesgue measurable \(B_0\subset
\mathbb R^2\) satisfies

\[
\mu(D_{w^-}\cap F_w^{-1}B_0)\le K_J |B_0|.
\tag{39.13}
\]

Consequently, if \(\mathcal V\) is any family of words of a common
tail length \(N\), then

\[
\mu\{x:\text{some exactly feasible prefix is }\sigma v,\
       |\sigma|=J,\ v\in\mathcal V\}
\le C_0\sum_{v\in\mathcal V}\lambda_v,
\tag{39.14}
\]

with \(C_0=\max\{1,2^J K_J C_A\rho^2\}\), independent of \(N\)
and of the family.

*Proof.* Compactness and (39.3) give
\(d_0=\min_{i,x\in Q}|\det DF_i(x)|>0\). At each
\(x\in D_{w^-}\), all inputs to the derivatives in \(DF_w(x)\)
are in \(Q\), even if the last output is outside \(Q\).
Thus \(|\det DF_w(x)|\ge d_0^{|w|}>0\). Cover this compact set
by finitely many inverse charts of \(F_w\), with compact closures
inside regular charts. On each chart change of variables bounds
the pulled-back area by its finite inverse determinant supremum
times \(|B_0|\). Summing the finitely many chart bounds and taking
the maximum over the finitely many words proves (39.13). Chart
overlap only increases this upper bound. Every inverse branch
meeting \(D_{w^-}\) is included; global injectivity is unnecessary.

An exactly feasible \(\sigma\) sends \(D_\sigma\) into
\(Q\cap\{s\le\rho\}\). If its continuation \(v\) is feasible,
the endpoint lies in \(\mathcal I_v\), except possibly the origin.
The pullback of the origin has zero area by (39.13).
Apply (39.13) to \(F_\sigma\) and (39.12), then sum over the at
most \(2^J\) prefixes and over \(v\). This proves (39.14). \(\square\)

For any fixed input, the first true exit during these first \(J\)
steps also has area at most \(J K_J C_Q\delta\), with, for example,
\(C_Q=2(2+2\sqrt2)+3\pi\), by applying (39.13) to
\(Q_\delta\setminus Q\). **This area is not charged to the failure
budget \(e_n\)**: it could be much larger than that budget. The
reliable upper construction below uses exact feasible prefixes,
and the lower construction imposes the physical first-error margin.

Lemma 39.2 gives domination of actual word-region probabilities
by reference weights. It does not assert that the regions form a
partition, that their probabilities equal \(\lambda_v\), or that
a selected strategy is optimal. Its whole-\(Q\) constant replaces
R33's constant on a compact window of a prescribed fixed area loss.

## 4. Two genuine catalogue upper bounds

### 4.1 Exponential reliability with exact feasible prefixes

Fix \(\varepsilon>0\) and \(n>J\), and put \(N=n-J\).
Keep all length-\(n\) words \(\sigma v\) with \(|\sigma|=J\),
\(|v|=N\), whose tail zero frequency \(p\) satisfies
\(I_a(p)\le\alpha+\varepsilon\). Empty feasible regions can be
omitted. Append any infinite continuation. Every kept region is
exactly feasible through time \(n\), hence is contained in its
actual set (39.4) for every positive tolerance.

For any state not covered, viability supplies an exactly feasible
prefix of length \(n\); every such prefix must have a discarded
tail. By (39.14) and the elementary type inequality
\(\binom Nj\le\exp[NH_b(j/N)]\), failure probability is at most

\[
C_0\sum_{I_a(j/N)>\alpha+\varepsilon}
        \binom Nj e^{-N\chi(j/N)}
\le C_0(N+1)e^{-N(\alpha+\varepsilon)}<e_n
\tag{39.15}
\]

for all sufficiently large \(n\). The catalogue size is at most

\[
2^J(N+1)\exp[N L_a(\alpha+\varepsilon)].
\tag{39.16}
\]

Let \(n\to\infty\), then \(\varepsilon\downarrow0\).
Continuity of \(L_a\) (proved in Section 7) gives
\(\limsup n^{-1}\log r_{e_n}\le L_a(\alpha)\).
Both original and transported probabilities have been compared to
uniform *physical* area; no transported-measure equivalence is
substituted for this bound.

### 4.2 Full-state stopping cover, with all-time tails

Put \(M=\max\{1,4\sqrt2\Lambda C_R\rho\}\). After the initial
exactly feasible \(J\) inputs, follow an exact feasible input until
either its reference product first satisfies \(P_w\le\delta_n/M\)
or the remaining horizon \(N\) is reached. Keep all realised
prefix/leaf pairs, including singleton and boundary states.

Before stopping the trajectory is exactly in \(Q\). At a threshold
leaf, (39.11) gives
\(s_{|w|}\le C_R\rho\delta_n/M\), and, while feasible,
\(V\le\Lambda s\). Append the same input \(0^\infty\) to every
threshold leaf. By (39.2), every later state's Euclidean norm is
at most \(\sqrt2 V\le\delta_n/4\); its distance from \(Q\) is
strictly less than \(\delta_n\). A horizon leaf is exactly feasible
through time \(n\). This construction covers every actual state,
including the origin. No leaf is declared necessary or optimal.

For all reference leaves of length \(\ell\le N\), the logarithmic
angular cost satisfies

\[
\ell\chi(p)\le\frac{-\log\delta_n+\log M}{\beta}+c_{\max},
\qquad c_{\max}=-\log a_*.
\tag{39.17}
\]

For a threshold leaf this follows from its parent and the bounded
last increment. For a horizon leaf that has not stopped it follows
from its strict below-threshold cost. Counting all lengths and
types, the number of leaves is at most

\[
(n+1)^2\exp[nS(\Gamma_n)],\qquad
\Gamma_n=\frac{-\log\delta_n+\log M+\beta c_{\max}}{n}
\longrightarrow\gamma.
\tag{39.18}
\]

Indeed \(\ell/n\le\min\{1,\Gamma_n/[\beta\chi(p)]\}\) for
each such type. The finite transient contributes at most \(2^J\).
Continuity of \(S\) yields

\[
\limsup_n n^{-1}\log r_{e_n}(n,\delta_n;Q)
\le \min\{S(\gamma),L_a(\alpha)\}.
\tag{39.19}
\]

The two constructions are separate alternatives; no compatibility
of two selected catalogues is presumed.

## 5. An old fixed-mass lower bound suffices on the low side

For completeness, the adopted fixed-window estimate from R33
Lemma 33.5 / manuscript Theorem 2.5 has the following matched form.
One can choose a fixed compact \(T\subset Q\) with area \(>3/4\)
such that for every \(0<\varepsilon<h\), all inputs, \(n>J\),
and \(0\le m\le n-J\),

\[
\mu(T\cap A_u(n,\delta;Q))
\le C_T\delta+C_\varepsilon\left[
 e^{-(h-\varepsilon)m}
 +\delta e^{((\beta-1)h+2\varepsilon)m}\right].
\tag{39.20}
\]

Here \(T\) is selected once, before \(\varepsilon,n,\delta\) and
the input. The dependency check recovers its proof: atypical
complete feasible word regions have summable area by (39.12) and
the Bernoulli type weights; Borel–Cantelli gives typicality for
every feasible coding outside one null set. Remove its finitely
many feasible transient pullbacks, use Egorov and compact inner
approximation once, and apply finite inverse charts on that window.
Typical products bound exact survival; the first-true-exit bands
from Section 2 give the geometric sum of local exit areas. Early
exits give \(C_T\delta\). No full-image cylinder, single specified
coding, or later nonreentry is assumed. This is the old fixed-loss
result; it is used here only for a fixed positive successful mass.

Write \(q_n=-\log\delta_n\) and choose
\[
m_n=\min\{n-J,\lfloor q_n/(\beta h+\varepsilon)\rfloor\}.
\]
Then \(\delta_n\le e^{-(\beta h+\varepsilon)m_n}\) and
(39.20) is at most a fixed multiple of
\(e^{-(h-\varepsilon)m_n}\). A catalogue successful on \(1-e_n\)
area covers more than \(1/2\) area inside \(T\) eventually.
The union bound therefore implies, after \(\varepsilon\downarrow0\),

\[
\liminf_n n^{-1}\log r_{e_n}(n,\delta_n;Q)
\ge\min\{h,\gamma/\beta\}.
\tag{39.21}
\]

Since \(S(\gamma)=\gamma/\beta\) when \(\gamma\le\beta h\),
and \(L_a(\alpha)\ge h\), this settles the whole low side,
including its endpoint. For \(\gamma=0\), (39.18) and \(r_e\ge1\)
settle the limit without requiring exponential decay of \(\delta_n\).
The fixed loss used in this *lower* bound is never substituted for
the exponentially small failure budget in an upper bound.

## 6. Positive-area regions forcing arbitrary approximate inputs

The existing bounded-run realisation gives individual states. A
probability lower bound needs positive-area sets, together with
wrong-control margins throughout every point of those sets.

**Lemma 39.3 (uniform thickening of physical words).** For every
integer \(L\ge2\) there are \(\tau_L,E_L>0\), depending only on
\(L\) and the fixed system, with this property. For every common
length \(m\) and every family \(\mathcal W\) of distinct words of
length \(m\), each having an infinite extension with runs at most
\(L\), there are pairwise disjoint measurable physical regions
\(E_w\subset Q\), \(w\in\mathcal W\), such that

\[
\mu(E_w)=\tau_L\lambda_w.
\tag{39.22}
\]

Every point of \(E_w\) is exactly feasible under \(w\). If
\(n\ge m\) and \(2\delta<E_LP_w\), any input whose actual set
\(A_u(n,\delta;Q)\) meets \(E_w\) must have prefix \(w\).
The implication includes all points of \(E_w\), not just its
central shadowing trajectory.

*Proof: uniform shadowing on a radius band.* Fix an infinite
bounded-run extension \(v\). The inverse reference maps
\(f_0(y)=a_0y-a_1,\ f_1(y)=a_1y+a_0\) give a unique bounded
reference orbit \(y^0\). Every shift encounters the opposite
digit within \(L+1\) places. The identities
\(f_0(y)+1=a_0(y+1)\) and
\(1-f_1(y)=a_1(1-y)\) yield

\[
|y_k^0|\le1-d_L,\qquad d_L=2a_*^{L+1}>0.
\tag{39.23}
\]

For a candidate sequence
\(\|y-y^0\|_\infty\le d_L/4\), and a starting radius
\(s\in(0,r_L]\), define
\(s_{k+1}=s_kR_{v_{k+1}}(s_k,y_k)\).
The radii decrease at least by \(\bar r\) in this recursion.
The scalar radial map has \(s\) derivative bounded by
\(\widehat r<1\), and \(y\) derivative bounded by \(Bs^2\).
Therefore

\[
\sup_k|s_k(y)-s_k(\widetilde y)|
\le C_s r_L^2\|y-\widetilde y\|_\infty,\qquad
C_s=B/(1-\widehat r).
\tag{39.24}
\]

For the same candidate sequence and two initial radii,
\(\sup_k|s_k(s,y)-s_k(s',y)|\le |s-s'|\), by scalar
contraction at each step. Let \(e_i=T_i-L_i\) and define

\[
(\mathcal B_s y)_k
=f_{v_{k+1}}(y_{k+1})
 -a_{v_{k+1}} e_{v_{k+1}}(s_k(s,y),y_k).
\tag{39.25}
\]

Choose a single positive \(r_L\le\rho\), before choosing \(v\),
so small that

\[
\begin{split}
a^*B r_L&\le(1-a^*)d_L/8,\\
a^*B(r_L+C_s r_L^2)&<(1-a^*)/2,\\
B(1+a^*/a_*)r_L&\le a_*d_L/(4a^*).
\end{split}
\tag{39.26}
\]

Then (39.25) maps the closed sequence ball into itself and has
uniform Lipschitz constant
\(\kappa_L\le a^*+a^*B(r_L+C_s r_L^2)<1\).
Its fixed point \(y^v(s)\) satisfies the actual angular recursion,
with
\(|y_k^v(s)|\le1-\Delta_L\), where
\(\Delta_L=3d_L/4\). Moreover (39.24) and the radial dependence
on initial radius give

\[
\|y^v(s)-y^v(s')\|_\infty
\le\frac{a^*B}{1-\kappa_L}|s-s'|.
\tag{39.27}
\]

In particular the initial-angle centre is a continuous function of
radius. This derives, rather than assumes, a whole radius band of
physical trajectories.

When the chosen digit is zero, its next angle is at most
\(1-3d_L/4\). From (39.8) its current angle is at most
\(a_0-a_1-3a_0d_L/4+a_0Bs_k\); hence the other output is at
most
\(-1-3a_0d_L/(4a_1)+B(1+a_0/a_1)s_k\).
For chosen digit one the symmetric bound is
\(1+3a_1d_L/(4a_0)-B(1+a_1/a_0)s_k\).
By (39.26) both wrong-control excesses are at least

\[
d'_L=a_*d_L/(2a^*)>0.
\tag{39.28}
\]

These assertions hold uniformly for every \(0<s\le r_L\).
They extend the already verified point-shadowing argument without
using a global inverse of either actual map.

*Proof: thickening and all intermediate constraints.* Choose one
such extension \(v(w)\) for each \(w\), and write \(y_w(s)\)
for its initial-angle centre. Put
\(K=1/a_*+3B\rho\) and choose

\[
0<\epsilon_L\le
\min\{1/(2C_A),\Delta_L/(4C_A),d'_L/(4KC_A)\}.
\tag{39.29}
\]

Define the physical region

\[
E_w=\{(s,sy):r_L/2\le s\le r_L,\
               |y-y_w(s)|\le\epsilon_L\lambda_w\}.
\tag{39.30}
\]

To check that the entire interval in (39.30) is feasible, fix its
radius. On the component between its centre and any feasible
angle, the derivative bound (39.11), for each prefix \(w|j\),
implies

\[
|Y_{w|j}(y)-Y_{w|j}(y_w(s))|
\le C_A\epsilon_L\,\lambda_w/\lambda_{w|j}
\le D,\qquad D=C_A\epsilon_L.
\tag{39.31}
\]

If the complete interval \(I_w(s)\) ended inside the proposed
interval, some prefix constraint, or the initial constraint,
would reach an angular endpoint. But the centre stays at distance
\(\Delta_L\) from both endpoints, and \(D\le\Delta_L/4\).
This is impossible by (39.31) and continuity. Positive radii
remain below \(\rho<1\), so no radial constraint can terminate
the interval instead. Thus the entire thickened interval lies in
the complete feasible section. This argument is valid for
truncated terminal images; no full-image assumption is inserted.

At each prefix, both the centre and the thickened state lie on
the same radial image graph of logarithmic slope at most one.
Equation (39.31) gives
\(|\log(s_j(y)/s_j(y_w))|\le D\), and, since \(D\le1/2\),
\(|s_j(y)-s_j(y_w)|\le2\rho D\).
The other angular map consequently changes by at most

\[
(1/a_*+B\rho)D+B(2\rho D)\le KD\le d'_L/4.
\]

Its wrong-control excess is still at least \(d'_L/2\), while
the selected prefix remains inside its boundaries. This proves
the required all-point wrong-control margin.

Continuity (39.27) makes (39.30) measurable. Since its initial
angular interval has full width \(2\epsilon_L\lambda_w\),
the physical Jacobian gives

\[
\mu(E_w)=2\epsilon_L\lambda_w
                \int_{r_L/2}^{r_L}s\,ds
=\frac{3\epsilon_L r_L^2}{4}\lambda_w.
\tag{39.32}
\]

Set \(\tau_L=3\epsilon_L r_L^2/4\). If two equal-length words
had a common point in their regions, at their first difference
one of the two inputs would be a wrong control for that point,
although both words were feasible. Hence the regions are
pairwise disjoint.

Finally let an arbitrary input first differ from \(w\) at
position \(j\le m\). Before that step its physical trajectory
is the exactly feasible \(w\)-trajectory. By (39.11) its radius
is at least \(C_R^{-1}(r_L/2)P_{w|j-1}\), and hence at least
\(C_R^{-1}(r_L/2)P_w\). The wrong output radius is at least
\(r_*/2\) times that radius, and its angular excess is at least
\(d'_L/2\). Therefore

\[
|z_j|-s_j\ge E_LP_w,\qquad
E_L=\frac{r_L r_*d'_L}{8C_R}>0.
\tag{39.33}
\]

Either \(z-s\) or \(-z-s\), each with Euclidean Lipschitz
constant \(\sqrt2\), is positive by this amount, so distance
from \(Q\) is at least \(E_LP_w/\sqrt2>\delta\) when
\(2\delta<E_LP_w\). Constraint (39.4) is violated at that
time. Later reentry does not repair it. This proves the lemma.
\(\square\)

The proof constructs subsets of actual feasible regions. It does
not identify them with strategy cylinders, nor bound every
feasible cylinder below by its reference length.

## 7. Rare-type probability lower bound and critical values

Suppose \(c=\gamma/\beta>h\). Fix an interior zero frequency
\(p\) satisfying the strict inequalities

\[
\chi(p)<c,\qquad I_a(p)<\alpha .
\tag{39.34}
\]

For large fixed \(L\), choose \(j_L/L\to p\), with
\(1\le j_L\le L-1\). Take all length-\(L\) blocks starting with
zero, ending with one, and having \(j_L\) zeros. Their number is
\(M_L=\binom{L-2}{j_L-1}\). Every concatenation, extended by
repeating one allowable block, has runs at most \(L\).

Put

\[
B_L=L^{-1}\log M_L,\quad
\chi_L=\chi(j_L/L),\quad I_L=\chi_L-B_L.
\]

Elementary binomial type bounds imply
\(B_L\to H_b(p)\), \(\chi_L\to\chi(p)\), \(I_L\to I_a(p)\).
For clarity, \(\binom Nj\le e^{NH_b(j/N)}\) follows by taking
the corresponding term of the binomial probability sum. At
parameter \(j/N\), its \(j\)-th term is a mode and at least
\(1/(N+1)\); this gives the reverse bound
\(\binom Nj\ge e^{NH_b(j/N)}/(N+1)\). Apply these with
\(N=L-2,j=j_L-1\). The endpoints \(j=0,N\) have value one
and obey the same conventions.

Fix \(L\) large enough that
\(\beta\chi_L<\gamma\), \(I_L<\alpha\). For
\(k=\lfloor n/L\rfloor\), \(m=Lk\), there are \(M_L^k\)
distinct concatenated words. All their regions from Lemma 39.3
have the same mass and radial scale:

\[
\mu(E_w)=\tau_L e^{-\chi_Lm},\qquad
P_w=e^{-\beta\chi_Lm}.
\tag{39.35}
\]

Since (39.6) gives
\(n^{-1}\log[E_L e^{-\beta\chi_Lm}/(2\delta_n)]
\to\gamma-\beta\chi_L>0\), the prefix-forcing conclusion
holds for all sufficiently large \(n\).

A single input can therefore cover points from at most one such
region. A catalogue of \(R\) inputs covers at most
\(R\tau_Le^{-\chi_Lm}\) area of their union. Successful
coverage of \(1-e_n\) area forces

\[
\begin{split}
R&\ge M_L^k-\frac{e_n}{\tau_L e^{-\chi_Lm}}\\
 &=M_L^k\left(1-\frac{e_n}{\tau_L e^{-I_Lm}}\right).
\end{split}
\tag{39.36}
\]

The parenthesis tends to one, since \(\alpha>I_L\).
Thus \(\liminf n^{-1}\log r_{e_n}\ge B_L\).
First the horizon limit is taken for fixed \(L\); then let
\(L\to\infty\), still with the strict inequalities (39.34).
This proves

\[
\liminf_n n^{-1}\log r_{e_n}
\ge \sup_{\chi(p)<c,\ I_a(p)<\alpha}H_b(p)
\quad(c>h).
\tag{39.37}
\]

The right side has a simple exact evaluation, already present in
the classical optimization underlying R37. Relabel the digits so
that \(a=a_*<1/2\), and let \(q\) be the frequency of the
smaller branch. Put

\[
c_b=-\log(1-a),\quad d=\log[(1-a)/a]>0,\quad
\chi(q)=c_b+dq,\quad c_s=\chi(1/2),\quad J_a=I_a(1/2)>0.
\]

One has \(I_a(q)\ge0\), with equality only at \(q=a\).
The ratio \(H_b(q)/\chi(q)\) is increasing up to \(a\) and
decreasing afterwards. Indeed the numerator of its derivative is

\[
(c_b+d)\log(1-q)-c_b\log q,
\]

which has strictly negative derivative and vanishes at \(q=a\).
It follows that

\[
S(\beta c)=
\begin{cases}
c,&0\le c\le h,\\
H_b((c-c_b)/d),&h<c<c_s,\\
\log2,&c\ge c_s.
\end{cases}
\tag{39.38}
\]

For the middle case, if \(\chi(q)\le c\), then
\(q\le(c-c_b)/d<1/2\), and its entropy is bounded by that at
the endpoint. If \(\chi(q)>c\), the decreasing ratio after
that endpoint gives the same bound. The other two cases follow
from \(H_b/\chi\le1\), the value at \(a\), and the value at
\(1/2\). Boundary frequencies have zero entropy and cannot
improve any of these maxima.

If \(0<\alpha<J_a\), there is a unique \(q_\alpha\in(a,1/2)\)
with \(I_a(q_\alpha)=\alpha\), and
\(L_a(\alpha)=H_b(q_\alpha)\). If \(\alpha\ge J_a\), set
\(q_\alpha=1/2\) and \(L_a(\alpha)=\log2\).
These facts follow from strict convexity of relative entropy and
the monotonicity of entropy on \([0,1/2]\). They also prove
continuity of \(L_a\), including \(\alpha=J_a\).

For \(c>h\), set
\(q_c=\min\{1/2,(c-c_b)/d\}>a\). Every
\(a<q<\min\{q_c,q_\alpha\}\) satisfies (39.34).
Letting \(q\) approach that endpoint in (39.37) gives

\[
\liminf_n n^{-1}\log r_{e_n}
\ge H_b(\min\{q_c,q_\alpha\})
=\min\{S(\gamma),L_a(\alpha)\}.
\tag{39.39}
\]

Together with (39.19) and (39.21), this proves Theorem 39.1.
The value \(c=h\) is obtained by the fixed-mass argument, not
by imposing an unjustified strict type gap there. The transitions
\(c=c_s\) and \(\alpha=J_a\) use approximation from below by
strict types. Integer rounding changes \(m\) by less than fixed
\(L\); the transient changes \(N\) by fixed \(J\). All constants
disappear after division by \(n\). The strict gaps in (39.15)
and (39.35)–(39.36) absorb arbitrary \(o(n)\) fluctuations in
both sequences in (39.6). This includes every finite positive
reliability exponent, all finite precision exponents, and
\(\gamma=0\).

## 8. What has and has not been proved

1. Lemma 39.2 transports *uniform physical probability* through
   all finite feasible transient branches with a fixed constant
   on all of \(Q\). It requires no \(e_n\)-dependent window.
   The local word-area inequality gives a probability domination,
   not equality of actual word probabilities.
2. Lemma 39.3 turns the previously available point witnesses into
   disjoint positive-area regions, with mass \(\tau_L\lambda_w\),
   each forcing an arbitrary successful approximate input while
   its physical radial scale exceeds the tolerance. This is the
   additional lower-probability connection needed for reliability.
3. The formula, binomial types, relative-entropy optimization,
   inverse function theorem, change of variables, and summable
   local distortion are existing tools. Theorem 39.1 is a proved
   structural extension of the project's linear R37 conclusion,
   not a new source-coding formula or pressure method.
4. The condition is nonvacuous (the matched linear maps satisfy it).
   The existing inward-boundary example in manuscript Section 8.1
   also satisfies it: its positive \(g(s)\) gives triangular
   maps with nonzero determinant, while its prescribed boundary
   images provide the already proved obstruction to a simultaneous
   \(Q\)-preserving conjugacy to the matched linear pair.
   Applying this theorem there is a corollary, not a new example
   theorem. No nonconjugacy claim is made for every member or for
   unrestricted coordinate changes.
5. R38's fixed counterexample has a null critical set and falls
   outside (39.3). It proves that the null-critical hypothesis
   alone cannot guarantee reliability transfer. This theorem
   proves a sufficient positive condition. The two results do
   not classify every system with critical points.
6. No unresolved mathematical interface remains in (39.7).
   The full nonlinear finite-horizon constant sandwich of R37
   Lemma 37.2 is neither assumed nor asserted; independent
   constructions and probability lower bounds prove the limit.
   Neither the usual full-\(Q\) spectrum nor the fixed-initial-set
   theorems require correction. The unique R36 manuscript is
   unchanged; R37–R39 remain research results pending a separately
   authorised integration.

The actual literature scope and its formal-version limits are in
[SOURCES.md](SOURCES.md). Independent publication value increases
through a positive reliability-transfer criterion complementing
R38's obstruction, but this is not a certification of priority,
JDE main-target competitiveness, or a journal quartile.
