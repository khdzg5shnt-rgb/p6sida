# R26 — The precision boundary with vanishing feasible overlap

5 October 2026 UTC. Verified starting main:
`0fa6593538b2110eb5ea8eb9fa516cf424f2ef51`.
The unique paper is unchanged. This note proves the fixed R26 target;
it does not resume the constant-overlap problem of R09–R14.

## 1. Fixed class, physical catalogue, and statement

Fix \(a_0,a_1>0\), \(a_0+a_1=1\), \(a_0\ne a_1\), and \(\beta>1\).
Write
\[
A=\min a_i,\qquad a^+=\max a_i,\qquad d=-\log a^+>0,
\qquad h=-\sum_i a_i\log a_i.
\]
All logarithms are natural. Fix a smooth cutoff \(0\le\kappa\le1\),
equal to one on \(\overline B(0,3/2)\), with support contained in
the **open** ball \(B(0,7/4)\). For an explicit choice fixed before
the argument, let
\[
E(v)=\begin{cases}e^{-1/v}&v>0,\\0&v\le0,\end{cases}\qquad
\kappa(x)=\frac{E(169/64-|x|^2)}
 {E(169/64-|x|^2)+E(|x|^2-9/4)}.
\tag{1}
\]
The denominator is positive everywhere. Its support is the closed
ball of radius \(13/8<7/4\), and it is one on the required inner
ball. This is the existing cutoff construction with a smaller fixed
outer radius: the old radius-\(7/4\) construction has support touching
that sphere and would not literally satisfy the new open-ball
condition. No subsequent cutoff change is used. The proof also works
for any one cutoff satisfying the stated conditions.

Set the finite, fixed derivative bound
\[
C_\kappa=\max\{1,\max_{|\alpha|\le2}
                  \|\partial^\alpha(s\kappa)\|_\infty\},
\quad C=1+C_\kappa,
\quad
\boxed{\nu_0=\frac1C\min\left\{
 \frac{A}{1000},\frac{(\beta-1)d}{4(1+2/A)}\right\}>0.}
\tag{2}
\]
Thus the threshold depends only on the fixed parameters and cutoff.
Finiteness of \(C_\kappa\) follows from smooth compact support, not a
dynamical or catalogue hypothesis.

Fix \(0<\nu<\nu_0\), \(0<u<\nu\), and
\(\eta,\xi_0,\xi_1\in C^\infty_c(B(0,2))\), all zero at the origin,
with every partial derivative of order zero, one, or two bounded
globally by \(\nu\). Define at the actual input state
\[
\omega=us\kappa,\quad
P_0=a_0+\eta+\omega,\quad P_1=a_1-\eta+\omega,
\quad R_i=a_i^\beta e^{\xi_i},
\]
\[
\widetilde F_0(s,z)=
 \left(sR_0,\frac{R_0}{P_0}[z+(1-P_0)s]\right),\quad
\widetilde F_1(s,z)=
 \left(sR_1,\frac{R_1}{P_1}[z-(1-P_1)s]\right).
\tag{3}
\]
The transverse coefficient is \(1-P_i\), not the other \(P\).
No identity \(R_i=P_i^\beta\) is required.

Retain the actual planar set and ordinary area
\[
Q=\{0\le s\le1,\ |z|\le s\},\qquad \operatorname{area}(Q)=1.
\]
All infinite binary inputs \(v\) are allowed. If \(x_j^v\) is the
actual trajectory, put
\[
V(n,\delta,v)=\{x\in Q:
 \operatorname{dist}_2(x_j^v,Q)<\delta\quad(0\le j\le n)\}.
\]
\(r(n,\delta;K)\) is the minimum number of such inputs covering the
nonempty compact \(K\subset Q\). An input can be assigned to each
actual initial state independently. A trajectory may exit and
reenter \(Q\), subject to every displayed tolerance constraint. None
of the calculation coordinates below changes this object or metric.
A precision sequence means \(\delta_n>0\), \(\delta_n\to0\), and
\(-\log\delta_n/n\to\gamma<\infty\); monotonicity is not required.

**Theorem 26.1.** Every system (3) under (2) consists of global smooth
diffeomorphisms, has the matched linear first jets at its common fixed
origin, drives every bounded initial set uniformly exponentially to
the origin under all inputs, and makes \(Q\) controlled invariant.
Its two complete feasible branches have positive internal overlap
at every positive initial radius. They cannot be simultaneously
conjugated to the paper's no-internal-overlap class by an ambient
homeomorphism preserving \(Q\), even with an interchange of labels.

For each fixed positive-area compact \(K\subset Q\) and each finite
precision exponent \(\gamma\ge0\),
\[
\min\{h,\gamma/\beta\}\le
\liminf_n\frac{\log r(n,\delta_n;K)}n
\le\limsup_n\frac{\log r(n,\delta_n;K)}n
\le\min\{\log2,\gamma/\beta\}.
\tag{4}
\]
In particular the rate is \(\gamma/\beta\) for
\(0\le\gamma\le\beta h\).

For each \(\zeta\in(0,1)\), one fixed compact \(K_\zeta\subset Q\)
of area greater than \(1-\zeta\) can be chosen before all finite
\(\gamma>\beta h\), their precision sequences, and horizons, so that
simultaneously
\[
\lim_n\frac{\log r(n,\delta_n;K_\zeta)}n=h
<\liminf_n\frac{\log r(n,\delta_n;Q)}n.
\tag{5}
\]
The compact set may depend on the fixed system and \(\zeta\).
The strict gap may depend on \(\gamma\). No high-side full-\(Q\)
exact spectrum or limit is claimed.

The new actual-catalogue interface is §§5–8. The complete intervals
overlap; the no-overlap stopping-witness spacing proof in R24 cannot
be copied. Instead we control **all feasible prefixes** on physical
typical sets and construct physical bounded-run witnesses on which
any first alternative input has a quantitative infeasibility margin.

## 2. Global inverse, first jets, and all-input tails

Let \(\mu=C\nu\). Each \(P_i-a_i\), with all its derivatives through
order two, is bounded by \(\mu\), vanishes at zero, and has support in
\(B(0,2)\). Each \(\xi_i\) obeys the same bounds. Put
\[
p_-=A-\mu,\quad p_+=1-p_-,\quad
r=e^\mu(a^+)^\beta,\quad
t=\frac{e^\mu(a^+)^{\beta-1}}{1-\mu/A}.
\]
Globally \(P_i\in[p_-,p_+]\), \(R_i\le r\), and \(R_i/P_i\le t\).
Since \(\mu<A/1000\) and (2) holds,
\[
\log t\le-(\beta-1)d+(1+2/A)\mu
 <-\tfrac34(\beta-1)d<0,\qquad
\log r<-\tfrac34\beta d<0.
\tag{6}
\]
Here \(-\log(1-\mu/A)\le2\mu/A\), and
\(\mu<\beta d/4\). Thus \(0<r,t<1\).
For
\[
M=\frac{1+t}{1-t},\quad
\|(s,z)\|_*=\max(M|s|,|z|),\quad
L_*=\max\{r,2t/(1+t)\}<1,
\]
the coefficient of the cross term in (3) is at most \(t\), giving
on the **entire plane**
\[
\|\widetilde F_i x\|_*\le L_*\|x\|_*.
\tag{7}
\]
This is contraction towards the origin, not an assertion of pairwise
contraction. It proves the claimed uniform convergence and controls
every later time in an appended tail, including times outside \(Q\).

Let
\[
\mathsf A_0=
 \begin{pmatrix}a_0^\beta&0\\a_0^{\beta-1}a_1&a_0^{\beta-1}\end{pmatrix},
\quad
\mathsf A_1=
 \begin{pmatrix}a_1^\beta&0\\-a_1^{\beta-1}a_0&a_1^{\beta-1}\end{pmatrix}.
\]
For \(\sigma_0=-1,\sigma_1=1\), use the shear
\(J_i(s,z)=(s,z-\sigma_i s)=(s,v)\), with both shear norms less
than two. Directly from \(1-P_i\) in (3),
\[
J_i\widetilde F_iJ_i^{-1}(s,v)=(sR_i,vR_i/P_i),
\quad J_i\mathsf A_iJ_i^{-1}
       =\operatorname{diag}(a_i^\beta,a_i^{\beta-1}).
\]
This identity does **not** require \(P_0+P_1=1\).
For \(g_i=\mathsf A_i^{-1}\widetilde F_i-\mathrm{id}\), therefore
\[
J_i g_i=(s\alpha_i,v\vartheta_i),\qquad
\alpha_i=e^{\xi_i}-1,\quad
\vartheta_i=e^{\xi_i}a_i/P_i-1.
\]
The function \(g_i\) vanishes off \(B(0,2)\). On its support,
\(|s|\le2\), \(|v|\le2\sqrt2\), and
\[
|\alpha_i|\le e^\mu\mu,\quad
\|\nabla\alpha_i\|_2\le e^\mu\sqrt2\mu,
\]
\[
|\vartheta_i|\le e^\mu\mu(1+1/p_-),\quad
\|\nabla\vartheta_i\|_2
 \le2e^\mu\sqrt2\mu(1+1/p_-).
\]
The derivative of the two displayed components, followed by \(J_i^{-1}\),
is consequently bounded by
\[
\|Dg_i\|_2\le
2e^\mu\mu[(1+2\sqrt2)+(8+\sqrt2)(1+1/p_-)]
<200\mu/A<1/5.
\tag{8}
\]
For the coarse bound use \(e^\mu<3\), \(p_->A/2\), \(A\le1/2\).
The bound is global. For every target \(b\),
\(x\mapsto\mathsf A_i^{-1}b-g_i(x)\) is a contraction of the
complete Euclidean plane, hence has one fixed point. In addition
\(D\widetilde F_i=\mathsf A_i(I+Dg_i)\) is invertible everywhere.
The local smooth inverse theorem gives a smooth global inverse.
Positivity of \(P_i\) proves global smoothness already. Since all
perturbation values vanish at zero, differentiation of (3) gives
\(D\widetilde F_i(0)=\mathsf A_i\); perturbation derivatives at zero
need not vanish.

## 3. Actual overlap and complete moving intervals

Use only calculation coordinates \(y=z/s\) for \(s>0\), and write
\(\mathcal P_i(s,y)=P_i(s,sy)\), \(W_i(s,y)=\xi_i(s,sy)\).
The one-step equations are
\[
S=s a_i^\beta e^{W_i},\qquad
Y=\sigma_i+(y-\sigma_i)/\mathcal P_i.
\tag{9}
\]
On \(0<s\le1, |y|\le1\),
\[
|\mathcal P_i-a_i|,|W_i|\le2\mu s,\quad
|(\mathcal P_i)_s|,|(W_i)_s|\le2\mu,\quad
|(\mathcal P_i)_y|,|(W_i)_y|\le\mu s.
\tag{10}
\]
These follow from the actual derivatives and vanishing values.
On \(Q\), \(\kappa=1\) since \(\sqrt2<3/2\). Hence
\(\mathcal P_0+\mathcal P_1=1+2us\).

At a fixed radius define
\[
f_s(y)=y-2\eta(s,sy),\qquad \theta=2a_0-1,
\qquad f_s(\theta_\pm(s))=\theta\pm2us.
\]
Its derivative lies in \([1-2\nu s,1+2\nu s]\).
From (9), the complete one-step feasible domains are exactly
\[
I_0(s)=[-1,\theta_+(s)],\qquad
I_1(s)=[\theta_-(s),1].
\tag{11}
\]
The roots are strictly in \((-1,1)\): the corresponding separating
functions have opposite endpoint signs because \(0<P_i<1\).
The radial condition causes no additional restriction, since \(S\le rs<1\).
Their overlap width satisfies the actual estimate
\[
\frac{4us}{1+2\nu s}
\le\theta_+(s)-\theta_-(s)
\le\frac{4us}{1-2\nu s}.
\tag{12}
\]
The physical fibre width is \(s\) times this width, thus of order
\(us^2\). These are angular margins, not a uniform positive Euclidean
inward distance. The vertex is fixed, and (11) gives controlled
invariance while retaining both choices in the overlap.

For a complete parent image graph \(s=S(y)\) with
\(k=S'/S\), \(|k|\le1\), define
\[
A_i=(\mathcal P_i)_s S'+(\mathcal P_i)_y,
\quad B_i=(W_i)_s S'+(W_i)_y,
\quad q_i=1-(y-\sigma_i)A_i/\mathcal P_i.
\]
Equation (10) gives \(|A_i|,|B_i|\le3\mu S\). Differentiating the
actual equations (9) on this graph gives
\[
\frac{dY}{dy}=q_i/\mathcal P_i,
\qquad k_{\rm new}=\mathcal P_i(k+B_i)/q_i.
\tag{13}
\]
Here \(B_i\) is independent of \(A_i\). We have
\(|q_i-1|\le6\mu S/\mathcal P_i\). Moreover
\[
\mathcal P_i(1-\mathcal P_i)\ge A/4
>9\mu S\ge(3\mathcal P_i^2+6)\mu S,
\]
so \(q_i>0\) and
\(\mathcal P_i(1+3\mu S)/(1-6\mu S/\mathcal P_i)<1\).
Thus \(|k_{\rm new}|<1\).

There are now **two** separating functions on the graph:
\[
\Delta_0(y)=y-2\mathcal P_0(S(y),y)+1,
\quad \Delta_1(y)=y+2\mathcal P_1(S(y),y)-1.
\tag{14}
\]
Both have derivative at least \(1-6\mu S>0\), with opposite
endpoint signs. Their unique roots are ordered, because
\(\Delta_1-\Delta_0=4uS>0\).
Control 0 is feasible to the left of its root, and control 1 to the
right of its root; these two closed domains overlap. Each restricted
map (9) is increasing onto the full angular interval \([-1,1]\),
and (13) preserves the radial graph cone on its image.

Starting from \(S\equiv s_0\), induction proves that every finite
word \(w\) has a nondegenerate **closed complete** feasible initial
interval \(I_w(s_0)\), imposing every intermediate constraint.
Its terminal angular map is increasing onto \([-1,1]\) and its radial
graph satisfies the same cone. Endpoints depend smoothly on \(s_0>0\)
by the positive derivatives in (14). A complete prefix-free family
covers the whole fibre but generally does **not** partition it.
No deterministic strategy cylinder has been substituted for \(I_w\).

Let \(D_i=Q\cap\widetilde F_i^{-1}(Q)\). By (11)–(12),
\(D_0\cap D_1\) has nonempty ambient interior within \(0<s<1, |z|<s\). In every paper no-internal-overlap model the same
intersection has empty interior. A simultaneous ambient conjugacy
\(H\) preserving \(Q\) and satisfying the identities on \(Q\) and
the needed one-step images would give
\(H(D_0\cap D_1)=D'_0\cap D'_1\), also after label interchange.
Homeomorphisms preserve interior, a contradiction. This excludes
that \(Q\)-preserving simultaneous reduction for **every** \(u>0\)
here. It does not exclude coordinate changes which change the
constraint set or unrelated unconstrained equivalences.

## 4. Derived radial, angular, and physical area comparisons

For \(w=w_1\cdots w_l\), put \(\lambda_w=\prod_{j=1}^l a_{w_j}\)
and \(\lambda_\varnothing=1\). Fix
\[
B_P=\frac{2\mu}{p_-(1-r)},\quad B_R=\frac{2\mu}{1-r},
\quad C_R=e^{B_R},\quad d_0=6\mu/p_-<1,
\]
\[
B_q=\frac{6\mu}{p_-(1-d_0)(1-r)},\qquad C_A=e^{B_P+B_q}.
\]
On a complete feasible trajectory, \(s_j\le r^j s_0\).
Summing (10) and (13), using
\(|\log q_i|\le|q_i-1|/(1-d_0)\), gives
\[
\left|\sum\log(P_{w_{j+1}}(x_j)/a_{w_{j+1}})\right|\le B_P,
\quad\left|\sum\xi_{w_{j+1}}(x_j)\right|\le B_R,
\quad\sum|\log q_{w_{j+1}}|\le B_q.
\]
Consequently
\[
C_R^{-1}s_0\lambda_w^\beta\le s_l\le C_Rs_0\lambda_w^\beta,
\quad C_A^{-1}\lambda_w^{-1}
 \le\partial_{y_0}Y_{w,s_0}\le C_A\lambda_w^{-1}.
\tag{15}
\]
Neither product is assumed independent of the actual initial angle.
Since the complete image is \([-1,1]\),
\[
2C_A^{-1}\lambda_w\le|I_w(s_0)|\le2C_A\lambda_w.
\tag{16}
\]
Let the actual strip be
\[
\mathcal A_w=
 \{(s_0,s_0y_0):0<s_0\le1,\ y_0\in I_w(s_0)\}\cup\{0\}.
\]
Integration with the actual Jacobian \(s_0\,ds_0dy_0\) proves
\[
C_A^{-1}\lambda_w\le\operatorname{area}(\mathcal A_w)
\le C_A\lambda_w.
\tag{17}
\]
Finite-word endpoint graphs and the vertex have area zero, by
Fubini. Closed endpoints remain in all covers. Bounds (15)–(17)
hold for each complete word, not only words selected by one code;
overlaps cause no change in these single-strip bounds.

## 5. First genuinely infeasible time for any approximate input

Set
\[
\ell_- =\min_i\frac{a_i^\beta e^{-\mu}}{a_i+\mu}>0,
\qquad C_b=\frac{2C_R C_A}{\ell_-(1-6\mu)}.
\]
**Lemma 26.2.** If any input \(v\) covers \(x\in Q\) at tolerance
\(\delta\) through \(n\), and its first actual state outside \(Q\)
occurs at \(j\le n\), then its prefix \(a=v|_{j-1}\) is exactly
feasible. At each initial radius \(s_0>0\), the initial angles with
this property lie on one side of the appropriate boundary
\(b_{a,v_j}(s_0)\in I_a(s_0)\), within width
\[
C_b\delta\lambda_a^{1-\beta}/s_0.
\tag{18}
\]
For a fixed input and time their physical area is at most
\(C_b\delta\lambda_a^{1-\beta}\).

**Proof.** Until time \(j-1\), the actual state lies on the complete
parent graph. Its initial radius satisfies \(s_0>0\), and its radius
there is \(S\ge C_R^{-1}s_0\lambda_a^\beta\). The boundary is the
pullback of the unique zero of the relevant function in (14).
Control 0 is truly infeasible exactly when \(\Delta_0>0\); control
1 exactly when \(\Delta_1<0\). No radial upper-bound violation is
possible on this first step, since \(R_i<1\).
At this time the exact physical excess is
\[
|z_j|-s_j=S(R_{v_j}/P_{v_j})|\Delta_{v_j}(Y)|.
\tag{19}
\]
The global ratio is at least \(\ell_-\). Euclidean membership in
\(Q^\delta\) implies \( |z_j|-s_j<2\delta\): compare with a point
of \(Q\) at distance less than \(\delta\). Meanwhile (13)–(15) give
\[
\frac{d}{dy_0}\Delta_{v_j}(Y_{a,s_0}(y_0))
\ge(1-6\mu)C_A^{-1}\lambda_a^{-1}.
\]
The mean value theorem proves (18). The wrong input determines one
side of this root. Multiplication by \(s_0\,ds_0\) and integration
over \(0<s_0\le1\) proves the physical area bound without a radial
cutoff. A later reentry cannot remove this necessary constraint at
time \(j\). No cone is imposed on the approximate trajectory after
that time. The fixed vertex never has such a time. QED.

There is deliberately no assertion that the first difference from
a prescribed code is infeasible. Such an assertion would be false
in the interior overlap. Lemma 26.2 starts at the actual first exit.

## 6. Uniform physical typicality across all feasible codes

For each \(m\ge1\) and \(e>0\), the area of states possessing even
one feasible length-\(m\) word whose zero frequency differs from
\(a_0\) by at least \(e\) is at most
\[
C_A(m+1)e^{-2e^2m}.
\tag{20}
\]
Indeed, it is a union of complete strips \(\mathcal A_w\). By (17)
its area is at most \(C_A\sum_w\lambda_w\) over those words, without
any disjointness requirement. For a type with \(j\) zeros, \(t=j/m\),
\(\binom mj\le e^{mH_b(t)}\), so its Bernoulli weight is at most
\(e^{-mD(t\Vert a_0)}\). The binary relative entropy has zero value
and derivative at \(a_0\), and second derivative
\(1/[t(1-t)]\ge4\). Therefore \(D(t\Vert a_0)\ge2(t-a_0)^2\),
also at endpoint types by continuity. Summing at most \(m+1\) types
proves (20). No independence of actual state-dependent digits is
assumed.

Define \(f_m(x)\) as the largest frequency deviation among **all**
feasible length-\(m\) words at the actual point \(x\). Feasibility is
nonempty by controlled invariance, and \(f_m\) is measurable because
there are finitely many closed strips. Borel–Cantelli for a countable
sequence of positive \(e\downarrow0\) proves \(f_m(x)\to0\) for
area-almost every \(x\in Q\). In particular this assertion is uniform
over possible codes at that point, not merely for one selected code.

Egorov's theorem and compact inner approximation give, for every
positive-area compact \(K\subset Q\), a positive-area compact
\(T\subset K\) on which \(f_m\to0\) uniformly. On \(Q\), for each
\(\zeta>0\), one may choose \(T_\zeta\) with area \(>1-\zeta\).
These sets may avoid the null vertex and finite-word endpoint graphs;
the vertex will be explicitly restored. They are chosen once before
all precision exponents and sequences. Since
\(-\log\lambda_w/m=\chi(\#0(w)/m)\), where
\[
\chi(t)=-t\log a_0-(1-t)\log a_1,\quad \chi(a_0)=h,
\]
uniform convergence implies that for every \(0<e<h\) there exists
one \(D_e\ge1\) such that
\[
D_e^{-1}e^{-(h+e)m}\le\lambda_w\le D_e e^{-(h-e)m}
\tag{21}
\]
whenever \(T\cap\mathcal A_w\ne\varnothing\), \(|w|=m\ge0\).
The finitely many early times are absorbed into \(D_e\). The same
fixed \(T\) works for every \(e\). This statement includes every
possible exactly feasible prefix of an approximate input until its
first true exit, resolving its otherwise unknown repeated choices
and their different remaining budgets on \(T\).

For any input \(v\), any \(0\le m\le n\), split its covered part of
\(T\) into exact feasibility through \(m\), or first true exit at
\(1\le j\le m\). The first part lies in the single strip
\(\mathcal A_{v|m}\), and if nonempty has area at most
\(C_A D_e e^{-(h-e)m}\). Each nonempty exit part has a feasible
prefix \(a=v|_{j-1}\) meeting \(T\). Lemma 26.2 and (21) give its
area at most
\(C_bD_e^{\beta-1}\delta e^{(\beta-1)(h+e)(j-1)}\).
The geometric sum proves, with a fixed \(A_e<\infty\), uniformly in
the input, horizon, tolerance, and stopping choice \(m\),
\[
\boxed{\operatorname{area}(T\cap V(n,\delta,v))
 \le A_e\left[e^{-(h-e)m}
              +\delta e^{(\beta-1)(h+e)m}\right].}
\tag{22}
\]
For \(m=0\) enlarge \(A_e\) if necessary. This is a real-catalogue
loss estimate: it applies to every approximate input even if it
switches within overlaps repeatedly or reenters after exiting.
It is not a restatement of an unknown coding-count factor.

For \(0<\delta<1\), take
\[
m=\min\left\{n,
 \left\lfloor\frac{-\log\delta}{\beta(h+e)}\right\rfloor\right\}.
\]
Then the second term in (22) is at most \(e^{-(h+e)m}\), and any
catalogue covering \(K\) must cover \(T\). Thus
\[
r(n,\delta;K)\ge
 \frac{\operatorname{area}(T)}{2A_e}e^{(h-e)m}.
\tag{23}
\]
For every precision sequence, taking lower rates and then
\(e\downarrow0\) gives the lower bound in (4), including the critical
exponent. The case \(\gamma=0\) also follows from \(r\ge1\).

## 7. Full stopping tails and one compact set for every high exponent

Let \(\mathcal L(n,t)\) stop each reference binary branch at its
first word with \(\lambda_w\le t\), or at depth \(n\). For
\(0<t<1\), elementary parent-child addition
\(\lambda_{w0}+\lambda_{w1}=\lambda_w\) proves
\[
\sum_{w\in\mathcal L(n,t)}\lambda_w=1,
\qquad\lambda_w>At,
\qquad\#\mathcal L(n,t)\le(At)^{-1}.
\tag{24}
\]
These are reference counting weights, not physical probabilities and
not an assumption that this tree is necessary or optimal.

For every physical initial point choose any exactly feasible input
until its reference stopping leaf. The complete prefix-free cover
in §3 ensures the associated leaf covers that state through its
whole prefix; a depth-\(n\) leaf needs no later constrained time.
Append to every leaf the same tail \(0^\infty\). An earlier stopped
leaf has terminal radius at most \(C_Rt^\beta\), lies in \(Q\), and
has adapted norm at most \(MC_Rt^\beta\). With
\[
C_0=2\sqrt2 MC_R,\qquad
t=(\delta/C_0)^{1/\beta},
\]
the entire appended tail remains in Euclidean norm at most
\(\delta/2\), by (7). It therefore satisfies every later tolerance
constraint, even when it leaves \(Q\). Closed endpoints and the
vertex are covered. Hence for \(0<\delta<1\)
\[
r(n,\delta;Q)\le
\#\mathcal L\bigl(n,(\delta/C_0)^{1/\beta}\bigr)
\le(C_0^{1/\beta}/A)\delta^{-1/\beta}.
\tag{25}
\]
Using all exactly feasible length-\(n\) prefixes also gives \(r\le2^n\).
These bounds prove the upper side of (4). They match (23) when
\(\gamma\le\beta h\), establishing the requested low-side rate for
every fixed positive-area compact set and every precision sequence.

Choose once the uniformly all-code-typical compact \(T_\zeta\) from
§6, and set \(K_\zeta=T_\zeta\cup\{0\}\). For any \(e>0\) and all
sufficiently large \(n\), all feasible words meeting \(T_\zeta\)
have zero frequency within \(e\) of \(a_0\). Their total number is
at most
\[
(n+1)\exp\left(n\max_{|t-a_0|\le e,\,0\le t\le1}H_b(t)\right).
\]
Use all those words as exact length-\(n\) prefixes, extended
arbitrarily, and one input for the vertex. This covers \(K_\zeta\)
for **every** tolerance. Continuity of \(H_b\), followed by
\(e\downarrow0\), gives upper rate \(h\). Its lower rate is \(h\)
for every finite \(\gamma>\beta h\) by (23). Thus the same fixed
compact set has the accurate high-side rate in (5), before the
exponent, sequence, and time are specified.

## 8. The overlap mechanism and strict full-Q cost

An overlap choice at a state \((s,sy)\in Q\), \(s>0\), has
\(\Delta_0\in[-4us,0]\), \(\Delta_1=\Delta_0+4us\in[0,4us]\).
After choosing 0 it gives
\[
0\le1-Y_0=-\Delta_0/P_0\le4us/p_-,
\]
and after choosing 1 it gives
\(0\le Y_1+1=\Delta_1/P_1\le4us/p_-\).
Control 0 cannot be feasible at a state whose distance from \(+1\)
is less than \(2p_-\); control 1 cannot be feasible at a state whose
distance from \(-1\) is less than \(2p_-\). Repeated 1 multiplies
distance from \(+1\) by \(1/P_1\le1/p_-\), and repeated 0 does the
same from \(-1\). Therefore, if
\[
4us\,p_-^{-k}<2p_- \quad(k\ge1),
\tag{26}
\]
an overlap choice of 0 must be followed by at least \(k\) consecutive
1's in any exact continuation; an overlap choice of 1 by at least
\(k\) consecutive 0's. This includes boundary choices. The guaranteed
waiting length tends to infinity as \(s\downarrow0\).
At larger radii (26) need not hold. We do not infer a global optimal
catalogue comparison from pointwise coding multiplicity or waiting
alone.

**Lemma 26.3 (physical bounded-run witnesses).** Let \(L\ge3\) and
\(1\le j\le L-1\). Let \(\mathcal B\) be all length-\(L\) words
starting with 0, ending with 1, and containing \(j\) zeros. Put
\[
M_L=\binom{L-2}{j-1},\quad
\chi_L=\chi(j/L),\quad b_L=(\log M_L)/L.
\]
For every precision sequence with \(\gamma>\beta\chi_L\),
\[
\liminf_n\frac{\log r(n,\delta_n;Q)}n\ge b_L.
\tag{27}
\]

**Proof.** Every infinite concatenation of blocks from \(\mathcal B\)
has no constant-symbol run of length \(L\): each block has both
symbols and block boundaries are \(1|0\). In every \(L\) successive
positions both symbols occur.

At any positive fixed initial radius \(s_*\), its complete feasible
prefix intervals are nonempty, closed, nested, and, by (16), have
diameters at most \(2C_A(a^+)^m\to0\). Their intersection is a
single angle. Thus each infinite block concatenation specifies an
**actual planar initial state** and an exact all-time feasible
trajectory. This constructs physical points before using them as
catalogue witnesses; a symbolic set is not substituted for \(Q\).

At any time along this trajectory, a 0 occurs within the next \(L\)
inputs. At its source feasibility of 0 gives
\(1-y\ge2(1-P_0)\ge2p_-\). Moving backwards through the preceding
1's multiplies this distance by their \(P_1\)'s, each at least
\(p_-\). Similarly the next 1 and preceding 0's give a lower-bound
distance from \(-1\). In particular, with the conservative constant
\[
d_L=2p_-^{L+1}>0,
\]
all actual angles at all times satisfy
\[
-1+d_L\le y_k\le1-d_L.
\tag{28}
\]
Choose one fixed physical radius
\[
0<s_*\le\min\{1/2,\ p_-d_L/(8u)\}.
\tag{29}
\]
Its whole feasible trajectory has \(s_k\le s_*\), so
\(4us_k\le p_-d_L/2\). If its prescribed next input is 0, its
actual next angle obeys (28), and therefore at the source
\[
\Delta_0=P_0(Y_0-1)\le-p_-d_L,
\quad\Delta_1=\Delta_0+4us_k\le-p_-d_L/2.
\]
Thus the alternative input 1 is genuinely infeasible, with
\(|\Delta_1|\ge e_L:=p_-d_L/2\). If the prescribed input is 1,
then \(\Delta_1=P_1(Y_1+1)\ge p_-d_L\), and
\(\Delta_0=\Delta_1-4us_k\ge e_L\); alternative 0 is genuinely
infeasible. Every such physical point therefore has a unique exact
input, and distinct infinite block concatenations give distinct
points. This uniqueness is proved only for these witnesses, not
assumed for all of \(Q\).

Every full block has the same reference product
\(\exp(-L\chi_L)\). For any prefix of length \(m\),
\[
-\log\lambda_{v|m}\le\chi_L m+C_L,
\qquad C_L=L\max_i(-\log a_i).
\tag{30}
\]
Indeed the completed blocks give the first term and the at most
\(L-1\) remaining symbols contribute at most \(C_L\).
If an arbitrary approximate input first differs from the witness
at time \(t\le n\), it follows the same actual exact trajectory
until \(t-1\). Equations (15), (19), (28)–(30) give at that time
\[
|z_t|-s_t\ge E_L e^{-\beta\chi_L n},\qquad
E_L=C_R^{-1}s_*e^{-\beta C_L}\ell_-e_L>0.
\tag{31}
\]
Since \(\gamma>\beta\chi_L\), eventually
\(2\delta_n<E_L e^{-\beta\chi_L n}\), for every precision sequence
of that exponent, including its arbitrary subexponential factors.
The necessary Euclidean tolerance condition at time \(t\) fails.
A subsequent reentry cannot help. Consequently every input covering
a witness through \(n\) must agree with all its first \(n\) inputs.

For \(k=\lfloor n/L\rfloor\), take every word in \(\mathcal B^k\)
and extend it by one fixed block repeated forever. The construction
gives \(M_L^k\) distinct actual points on the same radius \(s_*\),
all in \(Q\), whose first \(n\) inputs are distinct. Each catalogue
input can cover at most one. Hence
\[
r(n,\delta_n;Q)\ge M_L^{\lfloor n/L\rfloor}
\]
for all sufficiently large \(n\). This proves (27). QED.

To finish the strict high-side bound, fix any \(\gamma>\beta h\).
Because \(a_0\ne1/2\),
\[
\Delta=\chi(1/2)-h
 =(a_0-1/2)\log(a_0/a_1)>0.
\]
Choose
\[
\alpha=\min\{1/2,(\gamma/\beta-h)/(2\Delta)\}>0,
\qquad p=(1-\alpha)a_0+\alpha/2.
\]
Then \(\beta\chi(p)<\gamma\), and strict concavity of binary entropy
gives \(H_b(p)>h\). Choose \(j_L/L\to p\). For the block family
above,
\[
\frac1L\log\binom{L-2}{j_L-1}\longrightarrow H_b(p),
\qquad\chi(j_L/L)\longrightarrow\chi(p).
\tag{32}
\]
For completeness, writing \(q=(j_L-1)/(L-2)\), the elementary type
bounds
\[
\frac{e^{(L-2)H_b(q)}}{L-1}
\le\binom{L-2}{j_L-1}\le e^{(L-2)H_b(q)}
\]
prove (32). The lower bound follows because \(j_L-1\) is a mode of
the binomial law with parameter \(q\), hence has probability at least
\(1/(L-1)\); the upper bound follows because its probability is at
most one. These are analytic inequalities, not finite enumeration.

Choose **one finite** \(L,j_L\), before the precision sequence, with
\(b_L>h\) and \(\beta\chi_L<\gamma\). Lemma 26.3 then proves
\[
\liminf_n\frac{\log r(n,\delta_n;Q)}n\ge b_L>h.
\tag{33}
\]
The auxiliary witness family and its positive radius may depend on
\(\gamma\), which does not change \(Q\). In contrast, \(K_\zeta\)
was already fixed in §7 and works simultaneously for all high-side
exponents and sequences. Equations (4), (25), and (33) prove
Theorem 26.1 with the stipulated full quantifiers. QED.

## 9. What the result does and does not use

- The threshold (2) simultaneously supports global inverses, contraction,
  positive branches, the actual moving graph cone, both separate products,
  and the first-infeasibility band. No accumulated error, area comparison,
  catalogue rate, or necessary stopping tree was placed in the hypotheses.
- The new catalogue estimates are (22) and (27)/(31). Repeated exact
  choices cannot evade (22), since **all** feasible prefixes meeting \(T\)
  satisfy (21). On the bounded-run physical witnesses, (31) prevents
  **any** alternative approximate input up to the horizon. This handles
  remaining budgets without a strategy-optimality assumption.
- The no-overlap midpoint spacing and the universal \(1+Bn\) lower
  comparison of R24 Proposition 24.4 are not established for this class.
  They are unnecessary for the boundary target proved here. Neither
  pointwise subexponential coding multiplicity nor a full stopping-tree
  optimum is claimed.
- The graph/cone estimates, summable distortion, binomial types,
  Borel–Cantelli, Egorov, compact inner approximation, and stopping
  weight identity are classical tools. Their overlap-specific physical
  connection is proved above; the earlier disjoint proof alone did not
  supply it. The strict gap uses the already known entropy mechanism
  after the new bounded-run first-infeasibility estimate.
- The fixed cutoff, small global derivative class, matched first jets,
  positive \(u\), and this particular vanishing overlap remain restrictions.
  This is not a theorem for every rate of vanishing overlap, for constant
  overlap, or for arbitrary nonlinear control systems.
- The requested boundary has no remaining unproved lemma in this note.
  Exact high-side full-\(Q\) rates and optimality of the whole overlapping
  stopped cover remain undetermined and are not required or automatically
  assigned as a second research task.
