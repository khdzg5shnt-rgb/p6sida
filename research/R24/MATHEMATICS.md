# R24 — Precision boundary under asymptotic matching

5 October 2026 UTC (6 October in Asia/Shanghai). Baseline main: `5ab1c5d5867d83e69608f35e5580ec17b755da17`.

## 1. Fixed class, actual object, and theorem

Fix
\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,\quad\beta>1,
\qquad A=\min_i a_i,\quad a^+=\max_i a_i,\quad d=-\log a^+>0.
\]
One explicit sufficient threshold for this entire function class is
\[
\boxed{\quad \nu_0=
\min\left\{\frac{A}{1000},
       \frac{(\beta-1)d}{4(1+2/A)}\right\}>0.\quad}
\tag{1}
\]
This is a sufficient bound, not an optimal threshold. Fix any
\(0<\nu<\nu_0\), and any three independent functions
\(\eta,\xi_0,\xi_1\in C^\infty_c(B(0,2))\) vanishing at the origin,
with every partial derivative of order zero, one, or two bounded in
absolute value by \(\nu\) on the whole plane. Put
\[
p_0=a_0+\eta,\quad p_1=a_1-\eta,
\qquad R_i=a_i^\beta e^{\xi_i},
\]
\[
F_0(s,z)=\left(sR_0,\frac{R_0}{p_0}(z+p_1s)\right),\qquad
F_1(s,z)=\left(sR_1,\frac{R_1}{p_1}(z-p_0s)\right).
\tag{2}
\]
All factors are evaluated at the input state. No relation
\(R_i=p_i^\beta\) is imposed.

Keep the physical set and its ordinary planar area:
\[
Q=\{0\le s\le1,\ |z|\le s\},\qquad \operatorname{area}(Q)=1.
\]
For every infinite binary input \(u\), let \(x_j^u\) be its actual
trajectory. Define
\[
V_F(n,\delta,u)=\{x\in Q:\operatorname{dist}_2(x_j^u,Q)<\delta
                         \text{ for all }j=0,\ldots,n\},
\]
and let \(r_F(n,\delta;K)\) be the minimum number of such inputs whose
sets cover a nonempty compact \(K\subset Q\). The assignment may depend
on the actual state; no exact coding is prescribed to a catalogue.
All inputs are allowed. Exits and reentries are allowed subject to
every displayed time constraint. Calculation coordinates below do not
change this set, metric, or measure.

Write \(h=-\sum_i a_i\log a_i\). A precision sequence is any positive
sequence \(\delta_n\to0\) with \(-\log\delta_n/n\to\gamma\), where
\(\gamma\) is finite and nonnegative; it need not be monotone.

**Theorem 24.1.** For every triple in the class above, the maps (2) are
global smooth diffeomorphisms with the prescribed matched first jets
at their common fixed origin. Every input drives bounded initial sets
uniformly exponentially to that origin, and \(Q\) is controlled
invariant. For every fixed positive-area compact \(K\subset Q\) and
every precision sequence of finite exponent \(\gamma\ge0\),
\[
\min\{h,\gamma/\beta\}\le
\liminf_n\frac{\log r_F(n,\delta_n;K)}n
\le\limsup_n\frac{\log r_F(n,\delta_n;K)}n
\le\min\{\log2,\gamma/\beta\}.
\tag{3}
\]
Consequently the rate exists and is \(\gamma/\beta\) for
\(0\le\gamma\le\beta h\).

For every \(\zeta\in(0,1)\), there is one fixed compact
\(K_\zeta\subset Q\) of area greater than \(1-\zeta\) such that,
simultaneously for every finite \(\gamma>\beta h\) and all its precision
sequences,
\[
\lim_n\frac{\log r_F(n,\delta_n;K_\zeta)}n=h
<\liminf_n\frac{\log r_F(n,\delta_n;Q)}n.
\tag{4}
\]
This compact set may depend on the fixed triple and \(\zeta\), but is
chosen before the exponent, sequence, and horizon. The strict gap need
not stay uniformly positive near \(\beta h\). No exact high-side full-Q
spectrum or limit is asserted.

The new proof interface is §§3–6: independent radial derivatives,
complete moving feasible intervals, physical wrong-branch bands, and
the real-catalogue comparison. The type/typical-set deductions in §7
are the R22 argument with these newly established premises. Section 8
checks that genuine instances are not simultaneous coordinate
corollaries of either previously adopted model class.

## 2. Global dynamics, inverse, first jets, and branches

Set
\[
p_-=A-\nu>0,\quad p_+=1-p_-,\qquad
r=e^\nu(a^+)^\beta,
\qquad t=\frac{e^\nu(a^+)^{\beta-1}}{1-\nu/A}.
\]
Both \(p_i\in[p_-,p_+]\) globally. Also \(R_i\le r\) and
\(R_i/p_i\le t\). Since \(\nu<A/2\),
\[
\log t\le-(\beta-1)d+(1+2/A)\nu
<-\tfrac34(\beta-1)d<0,
\qquad \log r< -\tfrac34\beta d<0.
\tag{5}
\]
Here \(-\log(1-\nu/A)\le2\nu/A\) was used. Choose
\[
M=\frac{1+t}{1-t}\ge1,\quad
\|(s,z)\|_*=\max(M|s|,|z|),\quad
L=\max\{r,2t/(1+t)\}<1.
\]
Because the coefficient of the cross term in the second component is
at most \(t\), on the ENTIRE plane
\[
\|F_i x\|_*\le L\|x\|_*.
\tag{6}
\]
This is contraction relative to the origin, not a claim of pairwise
contraction. It proves all-input convergence and later controls full
tails outside \(Q\).

For global invertibility, denote the matched linear first jet by
\[
\mathsf A_0=\begin{pmatrix}a_0^\beta&0\\a_0^{\beta-1}a_1&a_0^{\beta-1}\end{pmatrix},
\qquad
\mathsf A_1=\begin{pmatrix}a_1^\beta&0\\-a_1^{\beta-1}a_0&a_1^{\beta-1}\end{pmatrix}.
\]
With \(\sigma_0=-1,\sigma_1=1\), use the linear shear
\(J_i(s,z)=(s,z-\sigma_i s)=(s,v)\). Both
\(\|J_i\|_2,\|J_i^{-1}\|_2<2\). The input/output shear of (2) is
\[
(S,V)=(sR_i,vR_i/p_i),
\]
because \(p_0+p_1=1\). Thus for
\(g_i(x)=\mathsf A_i^{-1}F_i(x)-x\),
\[
J_i g_i(x)=\bigl(s\alpha_i(x),v\omega_i(x)\bigr),\quad
\alpha_i=e^{\xi_i}-1,\quad
\omega_i=e^{\xi_i}a_i/p_i-1.
\]
The function \(g_i\) vanishes outside \(B(0,2)\). On its support,
\(|s|\le2, |v|\le2\sqrt2\), and
\[
|\alpha_i|\le e^\nu\nu,\quad
\|\nabla\alpha_i\|_2\le e^\nu\sqrt2\nu,
\]
\[
|\omega_i|\le e^\nu\nu(1+1/p_-),\quad
\|\nabla\omega_i\|_2\le2e^\nu\sqrt2\nu(1+1/p_-).
\]
The last inequality uses \(a_i/p_i\le2\). The two row-gradient
estimates and the shear therefore give
\[
\|Dg_i\|_2
\le2e^\nu\nu\bigl[(1+2\sqrt2)+(8+\sqrt2)(1+1/p_-)\bigr]
<200\nu/A<1/5.
\tag{7}
\]
For the coarse last bound use \(e^\nu<3\), \(p_->A/2\),
\(A\le1/2\), and (1). The same bound is global since \(g_i=0\)
off its compact support. To solve \(F_i(x)=y\), the map
\(x\mapsto\mathsf A_i^{-1}y-g_i(x)\) is a contraction of the complete
Euclidean plane. It has exactly one fixed point. Moreover
\(DF_i=\mathsf A_i(I+Dg_i)\) is invertible everywhere. The local smooth
inverse theorem, together with this unique global preimage, proves a
global smooth inverse. Positivity of \(p_i\) already made (2) smooth.
The zero values of all three functions at the origin give
\(DF_i(0)=\mathsf A_i\) directly; their first derivatives need not
vanish.

For \(s>0\), write only in calculation coordinates
\[
y=z/s,\quad P_i(s,y)=p_i(s,sy),\quad W_i(s,y)=\xi_i(s,sy).
\]
Then
\[
S=s a_i^\beta e^{W_i(s,y)},\qquad
Y=\sigma_i+(y-\sigma_i)/P_i(s,y).
\tag{8}
\]
On \(0<s\le1, |y|\le1\), vanishing at zero and the derivative bounds
imply
\[
|P_i-a_i|,|W_i|\le2\nu s,\quad
|(P_i)_s|,|(W_i)_s|\le2\nu,\quad
|(P_i)_y|,|(W_i)_y|\le\nu s.
\tag{9}
\]
The separating function \(y-2P_0(s,y)+1\) has derivative at least
\(1-2\nu>0\), negative value at \(-1\), and positive value at \(1\).
Its unique zero \(\theta(s)\) gives the COMPLETE feasible domains
\([-1,\theta(s)]\) for 0 and \([\theta(s),1]\) for 1. Indeed these
are exactly \(-1\le Y\le1\), and \(0<S\le rs<1\) imposes no further
restriction. Both branches map their angular endpoints to \(-1,1\).
The vertex is fixed. Choosing 0 at the shared endpoint defines a Borel
natural exact code, proving controlled invariance.

## 3. Independent radial derivative and complete feasible intervals

**Lemma 24.2.** At every actual initial radius \(0<s_0\le1\), every
finite word \(w\) has a nondegenerate closed complete feasible initial
interval \(I_w(s_0)\). All intermediate times are imposed. Its terminal
angular map is increasing onto \([-1,1]\), and its terminal radial
graph \(s=S(y)\) obeys \(|S'/S|\le1\). Complete prefix-free families
partition the initial fibre, with shared endpoints included.

**Proof.** Suppose a parent graph has \(k=S'/S\), \(|k|\le1\). Set
\[
A_i=(P_i)_s S'+(P_i)_y,\qquad
B_i=(W_i)_s S'+(W_i)_y.
\]
By (9), \(|A_i|,|B_i|\le3\nu S\). Differentiating (8) along this
ACTUAL moving graph gives the replacement for the old matched formula:
\[
q_i=1-(y-\sigma_i)A_i/P_i,\qquad
\frac{dY}{dy}=q_i/P_i,\qquad
\boxed{\ k_{\rm new}=P_i(k+B_i)/q_i.\ }
\tag{10}
\]
There is no substitution \(B_i=\beta A_i/P_i\); those quantities are
independent. We have \(|q_i-1|\le6\nu S/P_i\), hence \(q_i>0\).
For cone invariance it suffices that
\[
P_i(1-P_i)>(3P_i^2+6)\nu S.
\]
Its left side is at least \(p_-(1-p_-)\ge A/4\), whereas its right
side is at most \(9\nu<A/4\). Therefore
\[
|k_{\rm new}|\le
\frac{P_i(1+3\nu S)}{1-6\nu S/P_i}<1.
\tag{11}
\]
On the same graph \(\Psi(y)=y-2P_0(S(y),y)+1\) has derivative at
least \(1-6\nu S>0\) and opposite endpoint signs. It splits the parent
once. On each feasible side (8) is increasing onto the whole
\([-1,1]\), and (11) preserves the cone on the output graph.

The original fibre has \(S\equiv s_0\), hence \(k=0\). Induction
proves the assertion for every word and every time, and splitting
parent intervals proves the prefix-free partition. Smooth dependence
of finite-word endpoints on \(s_0>0\) follows from the strictly
positive derivatives and the implicit function theorem. No cone or
interval structure was assumed as a hypothesis. QED.

## 4. Derived independent radial and angular products

For \(w=w_1\cdots w_\ell\), write \(\lambda_w=\prod_j a_{w_j}\).
Both the radial and angular products below depend on the actual initial
angle. Put
\[
B_P=\frac{2\nu}{p_-(1-r)},\quad
B_R=\frac{2\nu}{1-r},\quad C_R=e^{B_R},\quad
d_0=\frac{6\nu}{p_-}<1,
\]
\[
B_q=\frac{6\nu}{p_-(1-d_0)(1-r)},\qquad C_A=e^{B_P+B_q}.
\]
Along any complete feasible word \(s_j\le r^j s_0\). By (9) and (10),
\[
\left|\sum_j\log\frac{p_{w_{j+1}}(x_j)}{a_{w_{j+1}}}\right|\le B_P,
\quad \left|\sum_j\xi_{w_{j+1}}(x_j)\right|\le B_R,
\quad \sum_j|\log q_{w_{j+1}}|\le B_q.
\tag{12}
\]
The last bound follows from \(|\log q|\le|q-1|/(1-d_0)\).
Consequently the independent products yield
\[
C_R^{-1}s_0\lambda_w^\beta\le s_\ell\le C_Rs_0\lambda_w^\beta,
\qquad
C_A^{-1}\lambda_w^{-1}\le
\partial_{y_0}Y_{w,s_0}\le C_A\lambda_w^{-1}.
\tag{13}
\]
For the first estimate use
\(s_\ell=s_0\lambda_w^\beta\exp\sum_j\xi_{w_{j+1}}(x_j)\).
For the second use the chain rule \(\prod_j q_{w_{j+1}}/P_{w_{j+1}}\)
along the moving graphs. No shared radial trajectory is used.

Lemma 24.2 and (13) imply
\[
2C_A^{-1}\lambda_w\le|I_w(s_0)|\le2C_A\lambda_w.
\tag{14}
\]
For the physical complete feasible strip
\(\mathcal A_w=\{(s_0,s_0y):0<s_0\le1,y\in I_w(s_0)\}\cup\{0\}\),
integration against the actual Jacobian \(s_0\,ds_0\) gives
\[
C_A^{-1}\lambda_w\le\operatorname{area}(\mathcal A_w)
                         \le C_A\lambda_w.
\tag{15}
\]
Each finite-word boundary has zero area by its finite singleton fibre
sections and Fubini; their countable union and the vertex are null.
They remain present in the complete covers.

## 5. Arbitrary-input first deviation, including reentry

Define a positive global lower bound
\[
\ell_- =\min_{i=0,1}\frac{a_i^\beta e^{-\nu}}{a_i+\nu}>0,
\qquad C_b=\frac{2C_R C_A}{\ell_-(1-6\nu)}.
\]
**Lemma 24.3.** Suppose any input \(u\) covers
\(x=(s_0,s_0y_0)\) at tolerance \(\delta\) through time \(n\), and
first differs from its natural exact code at time \(j\le n\).
For the common prefix \(a=u|_{j-1}\) there is a separating point
\(b_a(s_0)\in I_a(s_0)\), independent of \(y_0\), such that
\[
|y_0-b_a(s_0)|\le
C_b\delta\lambda_a^{1-\beta}/s_0.
\tag{16}
\]
For fixed \(u,j\) all these states are on one side of that boundary,
with physical area at most \(C_b\delta\lambda_a^{1-\beta}\).

**Proof.** The common prefix is exactly feasible. On its full image
graph, let \(Y_*\) be the unique zero of
\(\Psi(Y)=Y-2P_0(S(Y),Y)+1\), and set
\(b_a=Y_{a,s_0}^{-1}(Y_*)\). For the wrong branch \(i=u_j\), (8) gives
the ACTUAL excess
\[
|Y_j|-1=|\Psi(Y)|/P_i,\qquad
|z_j|-s_j=S\frac{R_i}{P_i}|\Psi(Y)|.
\tag{17}
\]
The first-deviation point is still on the exact parent graph, so
\(S\ge C_R^{-1}s_0\lambda_a^\beta\). Globally \(R_i/P_i\ge\ell_-\).
A necessary condition for Euclidean membership in \(Q^\delta\) is
\(|z_j|-s_j<2\delta\): compare with a point \((\bar s,\bar z)\in Q\)
at distance less than \(\delta\), and use \(|\bar z|\le\bar s\).
Also
\[
\frac{d}{dy_0}\Psi(Y_{a,s_0}(y_0))
\ge(1-6\nu)C_A^{-1}\lambda_a^{-1}.
\]
These two lower bounds and the mean value theorem prove (16).
The wrong input fixes its side of the divider. Multiplying its
one-sided width by \(s_0\,ds_0\) cancels \(1/s_0\), proving the area
bound over all actual radii without a radial cutoff.

At a tie both excesses are zero, so the alternate branch is included.
Only the necessary constraint at this FIRST time was used. Reentry
later cannot remove it; no exact feasibility or cone assumption on the
later approximate trajectory has been made. QED.

## 6. Real stopping-catalogue comparison and complete tails

Let \(\mathcal L(n,t)\) stop each binary branch at its first word with
\(\lambda_w\le t\), or at depth \(n\) if no earlier crossing occurs.
Write \(N(n,t)=\#\mathcal L(n,t)\). It is a counting tree, not an
assumed optimal catalogue. Parent/child weight addition gives
\[
\sum_{w\in\mathcal L(n,t)}\lambda_w=1,\qquad
\lambda_w>A t,\qquad N(n,t)\le(At)^{-1}.
\tag{18}
\]
The strict weight lower bound also holds for capped leaves, since
each proper prefix precedes any crossing.

**Proposition 24.4 (the decisive comparison).** Fixed constants
\(B,C_0,C_U\) satisfy, for every \(n\ge1\) and \(0<\delta<1\),
\[
\boxed{\quad
\frac{N(n,\delta^{1/\beta})}{1+Bn}
\le r_F(n,\delta;Q)
\le N\bigl(n,(\delta/C_0)^{1/\beta}\bigr)
\le C_U\delta^{-1/\beta}.\quad}
\tag{19}
\]
Also \(r_F(n,\delta;Q)\le2^n\).

**Proof.** For the lower bound take the physical witnesses \((1,y_w)\)
at the midpoints of the complete intervals \(I_w(1)\) for the leaves
at \(t=\delta^{1/\beta}\). Their ordered successive gaps are greater
than \(2C_A^{-1}At\), by (14) and (18). Each midpoint has the natural
prefix \(w\), since it is interior to every ancestor interval.

An arbitrary input has at most one of these prefix-free leaves as a
prefix. Every other witness it covers first differs at some time
\(j\le n\), with the ONE common prefix \(a=u|_{j-1}\). This is a proper
prefix of the witness leaf, so \(\lambda_a>t\). Lemma 24.3 confines
these witnesses to a one-sided band at radius 1 of width at most
\(C_b\delta t^{1-\beta}=C_bt\). Its spacing permits at most
\[
B=\left\lceil1+\frac{C_A C_b}{2A}\right\rceil
\]
witnesses for that input and that time. Summing over times and adding
the possible prefix witness proves the lower bound in (19). This
counts all approximate inputs, not only naturally coded ones.

For the upper bound take \(t=(\delta/C_0)^{1/\beta}\), use all leaves
as exactly feasible prefixes, and append the SAME infinite tail,
say \(0^\infty\). Lemma 24.2 covers every actual radius and every
angle through the leaf, including all intermediate times and closed
endpoints. A capped depth-n leaf needs no further constrained time.
An earlier stopped leaf has terminal radius at most \(C_Rt^\beta\)
and lies in \(Q\), hence terminal adapted norm at most \(MC_Rt^\beta\).
With
\[
C_0=2\sqrt2 MC_R,\qquad C_U=C_0^{1/\beta}/A,
\]
the global bound (6) keeps the ENTIRE remaining tail within Euclidean
norm \(\delta/2\), strictly inside \(Q^\delta\) at every later time.
The vertex is fixed. Equation (18) proves the last inequality in
(19). Alternatively all exact length-n prefixes, extended
arbitrarily, give the \(2^n\) bound. QED.

The factor \(1+Bn\) is proved from physical spacing and the independent
radial first-deviation coefficient in (17). Product comparability
alone, or the entropy of one exact coding, would not prove (19).

## 7. Physical typical sets and all precision-sequence quantifiers

This section supplies the full deductions, with their R22/classical
attribution; it does not claim a new type-counting method.

Let \(c_k(x)\) be the natural first k inputs. Its assigned-code sets
are Borel and lie in \(\mathcal A_w\). By (15), the area of states
whose zero frequency at length k differs from \(a_0\) by at least
\(e>0\) is at most
\[
C_A(k+1)e^{-2e^2k}.
\tag{20}
\]
Indeed, for a type with \(j\) zeros, \(v=j/k\),
\(\binom{k}{j}\le e^{kH_b(v)}\), so its Bernoulli weight is at most
\(e^{-kD(v\Vert a_0)}\). The binary relative entropy has value and
first derivative zero at \(a_0\) and second derivative
\(1/[v(1-v)]\ge4\), giving \(D(v\Vert a_0)\ge2(v-a_0)^2\).
Summing at most \(k+1\) types proves (20), including endpoint types
by continuity. The actual digits have not been assumed independent.

Borel–Cantelli for countably many positive e gives zero frequency
\(a_0\) for physical area-almost every state. Remove the null finite
coding boundaries and the vertex. Egorov and inner regularity give a
compact positive-area \(T\subset K\), for every positive-area compact
K, on which the frequency converges uniformly. For each \(0<e<h\),
one fixed such T therefore has a constant \(D_e\ge1\) with
\[
D_e^{-1}e^{-(h+e)k}\le\lambda_{c_k(x)}
                  \le D_e e^{-(h-e)k}\quad(x\in T,k\ge0).
\tag{21}
\]
The finitely many early times are absorbed in \(D_e\). T is chosen
once, before e or any precision sequence. On Q it can be chosen with
area greater than \(1-\zeta\).

For any input u, any \(0\le m\le n\), and any \(\delta>0\), split its
covered part of T by agreement through m or first difference at
\(j\le m\). A nonempty agreement class has area at most
\(C_A D_e e^{-(h-e)m}\), by (15) and (21). In a nonempty first-difference
class its common word \(a=u|_{j-1}\) is a typical prefix of some point
of T. Lemma 24.3 and (21) bound its area by
\(C_b D_e^{\beta-1}\delta e^{(\beta-1)(h+e)(j-1)}\).
The geometric sum yields, uniformly in u,n,δ,m,
\[
\operatorname{area}(T\cap V_F(n,\delta,u))
\le A_e\left[e^{-(h-e)m}+\delta e^{(\beta-1)(h+e)m}\right].
\tag{22}
\]
Take, for \(\delta<1\),
\[
m=\min\left\{n,\left\lfloor\frac{-\log\delta}{\beta(h+e)}\right\rfloor\right\}.
\]
Then the second term in (22) is at most \(e^{-(h+e)m}\). Any catalogue
for K covers T, hence
\[
r_F(n,\delta;K)\ge\frac{\operatorname{area}(T)}{2A_e}e^{(h-e)m}.
\tag{23}
\]
For every sequence of exponent γ, passage to lower rates and then
\(e\downarrow0\) proves \(\min(h,\gamma/\beta)\). Equations (19) and
\(2^n\) give the two upper bounds in (3). They coincide with the lower
bound for \(\gamma\le\beta h\), including equality. For \(\gamma=0\),
\(r_F\ge1\) and the \(\delta^{-1/\beta}\) bound give rate zero.
Only the limit of \(-\log\delta_n/n\) was used, not monotonicity.

For the high side, select once a uniformly typical compact
\(T_\zeta\subset Q\) of area greater than \(1-\zeta\), and let
\(K_\zeta=T_\zeta\cup\{0\}\). Uniform frequency convergence says that,
for each e and all sufficiently large n, all length-n natural words
on \(T_\zeta\) have zero frequency within e of \(a_0\). Their number
is at most
\[
(n+1)\exp\left[n\max_{|v-a_0|\le e,\ 0\le v\le1}H_b(v)\right].
\]
Use these exact prefixes and arbitrary extensions, plus one input for
the vertex. They cover \(K_\zeta\) through n for EVERY tolerance.
Continuity of \(H_b\) gives upper rate h; (3) gives lower rate h for
every finite \(\gamma>\beta h\). This ONE K has rate h simultaneously
for every high exponent and its sequences.

For the strict full-Q lower bound, set
\[
\chi(v)=-v\log a_0-(1-v)\log a_1,\qquad
\Delta=\chi(1/2)-h=(a_0-1/2)\log(a_0/a_1)>0.
\]
For a given \(\gamma>\beta h\) choose
\[
\alpha=\min\{1/2,(\gamma/\beta-h)/(2\Delta)\}>0,\quad
v_\gamma=(1-\alpha)a_0+\alpha/2.
\]
Then \(\chi(v_\gamma)<\gamma/\beta\), while strict concavity gives
\(H_b(v_\gamma)>h\). Choose integers \(j_n/n\to v_\gamma\). All words
of length n with \(j_n\) zeros eventually have
\(\lambda_w=e^{-n\chi(j_n/n)}>\delta_n^{1/\beta}\), including any
subexponential factor in the sequence. Their proper prefixes have
still larger products, so they are capped leaves of the tree in
(19). The elementary lower type bound
\(\binom n j\ge e^{nH_b(j/n)}/(n+1)\) follows since j is a mode of
the binomial distribution with parameter j/n and has mass at least
\(1/(n+1)\). Thus (19) implies
\[
\liminf_n\frac{\log r_F(n,\delta_n;Q)}n
\ge H_b(v_\gamma)>h.
\tag{24}
\]
Only this lower bound depends on γ; K was already chosen. Equations
(3) and (24) prove Theorem 24.1 with all its quantifiers. QED.

## 8. Checking coordinate reduction: genuine independent instances

Zero perturbations and some other triples are old-model corollaries.
Nonlinearity by itself does not exclude conjugacy. The following
example, within the FIXED stipulated class, rules out that explanation
for a nonempty set of instances, even against the old R22 family.

**Proposition 24.5.** There are triples satisfying (1)–(2), with
\(R_i\ne p_i^\beta\), that admit no Q-preserving simultaneous ambient
homeomorphism to any previously adopted R22 matched feedback system
or any R17/R19/R21 radius-autonomous system (including label exchange).
In particular no fixed C¹ or bi-Lipschitz change of this kind works.
The conjugacy identities are required on all of Q and on a domain
containing Q and the needed one-step images. This is an existence
statement, not a nonconjugacy assertion for every triple.

**Proof.** Choose a smooth cutoff χ equal to one on the closed ball
of radius 3/2 and zero outside the ball of radius 7/4. It is compactly
supported in B(0,2). For an explicit construction use
\[
E(v)=\begin{cases}e^{-1/v}&v>0,\\0&v\le0,\end{cases}\quad
\chi(x)=\frac{E(49/16-|x|^2)}
                 {E(49/16-|x|^2)+E(|x|^2-9/4)}.
\]
Its denominator is positive everywhere. Put
\[
f(s,z)=\chi(s,z)\sin(4\pi z),\quad
C_f=\max\{1,\max_{|\alpha|\le2}\|\partial^\alpha f\|_\infty\},
\quad \bar\nu=1/4000,\quad u=\bar\nu/(2C_f),\quad d_1=u/64.
\]
These are fixed analytic choices, not results of finite enumeration.
Take \(\beta=2\), \(a_0=(1+d_1)/2\), \(a_1=(1-d_1)/2\),
\(\eta=0\), \(\xi_0=uf\), \(\xi_1=-uf\). They vanish at zero and
have the prescribed C² bounds at most \(\bar\nu/2\). For these a's,
\(A>0.49\), \(a^+<0.51\). The first member of the minimum in (1)
exceeds \(0.49/1000>\bar\nu\); the second also exceeds \(\bar\nu\)
(use \(-\log0.51>2/5\) and \(4(1+2/0.49)<24\)). Thus the triple
belongs to the proved class with \(\nu=\bar\nu\).

Let \(D_i=Q\cap F_i^{-1}Q\), \(J_i=F_i(D_i)\). Since p is constant,
the source angle for a terminal angle Y is
\[
y_0(Y)=a_0Y-a_1,\qquad y_1(Y)=a_1Y+a_0.
\]
All sources in Q lie in the region χ=1. At a fixed Y the output
radius from source radius s is
\(a_i^2s\exp[(-1)^i u\sin(4\pi s y_i(Y))]\).
Its s derivative is positive, since its bracket is at least
\(1-4\pi u>0\). Therefore J_i is exactly the radial region
\(0\le S\le U_i(Y)\), \(-1\le Y\le1\), where
\[
U_0(Y)=a_0^2e^{u\sin(4\pi y_0(Y))},\qquad
U_1(Y)=a_1^2e^{-u\sin(4\pi y_1(Y))}.
\]
The parts of \(\partial J_i\) in the interior of Q are precisely
these upper radial arcs for \(-1<Y<1\). They lie strictly below
the cap s=1. Their log-radius difference is
\[
\mathcal D(Y)=2\log\frac{1+d_1}{1-d_1}
             +2u\sin(2\pi(Y+d_1))\cos(2\pi d_1Y).
\tag{25}
\]
For \(d_1<1/2\), its positive constant term is at most
\(8d_1=u/8\). At the four ordered points
\(-3/4,-1/4,1/4,3/4\), \(\sin(2\pi Y)\) has signs +,−,+,− and
magnitude 1. The error of replacing the sine/cosine factor in (25)
by \(\sin(2\pi Y)\) is at most
\(2\pi d_1+2\pi^2d_1^2<1/4\). Hence \(\mathcal D\) has those four
alternating signs. It has at least three distinct zeros in the
interior. Its zero set on [-1,1] is finite: it is analytic on a
neighbourhood of that compact interval and is not identically zero.
Thus \(\partial J_0\cap\partial J_1\cap\operatorname{int}Q\) has a
finite number of points, at least three.

For every old R22 matched feedback system, the image of its feasible
source cap s=1 is increasing in radial size with Y for branch 0 and
decreasing for branch 1, when its feedback ε is positive. To see this
directly, its cap factors are
\(a_0+\epsilon y/(2+y^2)\) and
\(a_1-\epsilon y/(2+y^2)\), respectively;
\((y/(2+y^2))'=(2-y^2)/(2+y^2)^2>0\) on [-1,1]. Its cap angular maps
are increasing by the proved graph formula with initial slope zero.
The radial coordinate is the common positive power of that factor.
The two interior upper arcs consequently meet at most once. At ε=0,
they are distinct constant-radius arcs since the a's are unequal.

For the old radius-autonomous classes the feasible images are
truncated triangles of radii \(g_i(1)\). Their interior boundary arcs
are disjoint, or coincide in an entire arc if these two radii agree.
Neither case has a finite intersection of at least three points.

Any Q-preserving simultaneous ambient homeomorphism maps D_i and J_i
to the target feasible domains and images. It maps their boundaries
and the interior of Q bijectively, preserving the cardinality of this
intersection set. Label exchange does not change it. The new finite
intersection contradicts both old possibilities. Finally
\(p_i^\beta=a_i^2\) here, whereas \(R_i=a_i^2e^{\pm uf}\) is not that
constant on Q. This verifies both actual failure of instantaneous
matching and the stated exclusion of old-model reduction. QED.

This argument does not exclude changes that alter Q, individual rather
than simultaneous control conjugacies, or reduction to an unspecified
larger model class. The unrestricted theorem (3)–(4) does not require
this existence example or an exclusion for every triple.

## 9. Increment and limits

The precise new conclusion is that the adopted boundary survives a
whole directly checkable function class with INDEPENDENT radial and
branch-length perturbations. The identity \(R_i=p_i^\beta\) at each
state is unnecessary in this small compactly supported class. The
functions have matching VALUES at the origin; derivative smallness,
contraction and graph induction prove that their accumulated effects
are bounded, rather than assuming that bound. The controlled step is
(10)–(19), especially the independent coefficient in (17). Proposition
24.5 prevents interpreting the whole result as an old simultaneous
coordinate formula.

The classical nature of graph cones, summable distortion, contractions,
stopping, types, and typical compact sets is retained. Equation (10)
is an application of those tools, not a new general graph-transform
theory. After (19) and (22), the boundary deductions are project-internal
corollaries of the already established R22 counting argument, supplied
here in full to preserve quantifiers.

Remaining restrictions: fixed compact support and uniform derivative
smallness, the complementary two-branch angular form, matching first
jets, all-input contraction, positive-area physical initial sets, and
nonoverlapping complete feasibility. This does not repair the R18
collapse merely from a first jet, prove necessity in the feedback
class, or determine a high-side full-Q exact spectrum. The latter and
the paused R09–R14 problem were not attacked. There is no remaining
core lemma for the theorem stated in §1.
