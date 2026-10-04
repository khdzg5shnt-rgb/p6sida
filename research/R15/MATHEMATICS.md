# R15: radial contraction matched to feasible branch geometry

4 October 2026 (UTC). Natural logarithms. One sufficient criterion is proved. It prevents initial-set cost splitting in a specified precision range even though the controls have different radial contractions. It is not a classification of all precision exponents, an overlap theorem, or a solution of the paused R09–R14 policy comparison.

## 1. The one candidate and its full statement

Choose numbers
\[
a_0,a_1\in(0,1),\qquad a_0+a_1=1,\qquad \beta>1.
\]
On the actual Euclidean state space \(\mathbb R^2\), with all binary input sequences admissible, set
\[
F_0(s,z)=(a_0^\beta s,\ a_0^{\beta-1}(z+a_1s)),\qquad
F_1(s,z)=(a_1^\beta s,\ a_1^{\beta-1}(z-a_0s)). \tag{1}
\]
The constraint is the same physical cone
\[
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad \operatorname{area}(Q)=1.
\]
For every compact nonempty \(K\subset Q\), use the existing real catalogue:
\[
r(n,\delta;K)=\min\{|\mathcal C|:\mathcal C\subset\{0,1\}^{\mathbb N}
\text{ finite},\
\forall x\in K\ \exists u\in\mathcal C\ \forall k=0,\ldots,n:\
\operatorname{dist}_2(\varphi(k,x,u),Q)<\delta\}. \tag{2}
\]
The actual initial state is retained. A selected control may leave and return to \(Q\). The single tolerance of a horizon is imposed at every intermediate time, not only at its endpoint.

Put
\[
a_{\min}=\min_i a_i,\quad a_{\max}=\max_i a_i,\quad
h_a=-a_0\ln a_0-a_1\ln a_1>0.
\]

**Theorem 15.1 (a sufficient geometric matching criterion).** For (1):

(a) Both maps are smooth linear diffeomorphisms; \(Q\) is controlled invariant. Every trajectory from a bounded set converges to the origin uniformly over all binary inputs.

(b) For every compact \(K\subset Q\) with positive area and every positive sequence \(\delta_n\to0\) satisfying
\[
-\frac{\ln\delta_n}{n}\longrightarrow\gamma,\qquad
0\le\gamma\le\beta h_a,
\]
the actual limit exists and
\[
\lim_{n\to\infty}\frac{\ln r(n,\delta_n;K)}n=\frac{\gamma}{\beta}. \tag{3}
\]
No monotonicity of the sequence is required. The quantifier is over every fixed positive-area compact \(K\); \(K\) is not chosen as a function of \(n,\gamma\), or the tolerance sequence.

(c) More generally, for \(\gamma\in[0,\infty]\),
\[
\min\{h_a,\gamma/\beta\}
\le \liminf_n\frac{\ln r(n,\delta_n;K)}n
\le \limsup_n\frac{\ln r(n,\delta_n;K)}n
\le \min\{\ln2,\gamma/\beta\}. \tag{4}
\]
The usual value \(+\infty\) is used for \(\gamma/\beta\) at infinity. Outside the range in (b), (4) is only a pair of bounds.

The dynamical condition is directly checkable. The ratio inverse branch has relative interval length \(a_i\), while the radius contracts by \(\rho_i=a_i^\beta\). Equivalently,
\[
-\ln\rho_i=\beta\ln|T_i'|. \tag{5}
\]
This is a relation between two one-step dynamical quantities, not an assumption about a covering rate. If \(a_0\ne a_1\), the radial contractions are genuinely different. Only this one candidate is attacked; no necessary condition or complete dichotomy is claimed.

The significance of (3) is the quantifier over **all** positive-area compact initial sets, including every near-full-area set of empty interior. R06's unequal radial factors with equal-width feasible branches do not have this conclusion. The pressure-root value and the symbolic measure matching behind (5) are classical; the transfer to arbitrary ambient approximate controls is proved below.

## 2. Full feasibility and a common contracting norm

For \(s>0\), use \(y=z/s\) only as a calculation coordinate. Then
\[
T_0(y)=\frac{y+a_1}{a_0},\qquad
T_1(y)=\frac{y-a_0}{a_1}.
\]
With \(\xi=a_0-a_1\), their exact feasible domains are
\[
I_0=[-1,\xi],\qquad I_1=[\xi,1].
\]
Each branch maps its domain increasingly onto \([-1,1]\). Choose control 0 at \(y=\xi\), and otherwise the unique feasible branch. This gives an exactly feasible infinite control for every actual state in \(Q\), including the two boundary rays; the vertex is fixed by both controls.

The inverse branches
\[
B_0(y)=a_0y-a_1,\qquad B_1(y)=a_1y+a_0
\]
map \([-1,1]\) onto these domains. For a word \(w=w_1\cdots w_l\), put
\[
\lambda_w=\prod_{j=1}^l a_{w_j},\qquad \lambda_\varnothing=1.
\]
Its complete exact feasible interval, including every intermediate constraint, is
\[
I_w=B_{w_1}\circ\cdots\circ B_{w_l}([-1,1]),\qquad
|I_w|=2\lambda_w. \tag{6}
\]
This follows inductively from \(I_{ia}=I_i\cap T_i^{-1}(I_a)=B_i(I_a)\). The intervals at each depth partition \([-1,1]\) up to shared endpoints. On \(I_w\), the final ratio map has slope \(\lambda_w^{-1}\), and the physical radius after the word is
\[
s_w=s\lambda_w^\beta. \tag{7}
\]
Equations (6)–(7), not just a symbolic label, express the matching condition.

Write \(v_0=a_1/a_0,\ v_1=-a_0/a_1\). In the norm
\[
\|(s,z)\|_M=\max\{M|s|,|z|\},
\]
the operator norm of \(F_i\) is at most
\[
\max\{a_i^\beta,\ a_i^{\beta-1}+a_i^\beta|v_i|/M\}.
\]
Because \(a_i^{\beta-1}<1\), choose \(M\ge1\) so the maximum over both labels is \(L<1\). Also \(\|x\|_2\le\sqrt2\|x\|_M\). This proves (a), including all off-constraint inputs, and supplies the complete-tail bound used below.

## 3. The decisive estimate for arbitrary approximate controls

For a fixed word \(u\) of length \(n\), let
\[
V(n,\delta,u)=\{x\in Q:\operatorname{dist}_2(\varphi(k,x,u),Q)<\delta
\text{ for all }0\le k\le n\}.
\]
These are Borel sets. No exact feasibility of \(u\) is imposed.

### 3.1 First deviation and the physical area it can cover

A necessary condition for a state \((r,z)\in Q^\delta\), \(r\ge0\), is
\[
|z|-r<2\delta. \tag{8}
\]
Indeed compare both coordinates with a point of \(Q\) less than \(\delta\) away.

Compare \(u\) with the fixed exact coding of an initial ratio \(y\). Suppose its first different input is \(j\), and let \(a=u_1\cdots u_{j-1}\) be the shared prefix. Define
\[
t_a=T_a^{-1}(\xi).
\]
The common prefix map has slope \(\lambda_a^{-1}\). On the opposite feasible child, the wrong branch produces
\[
|y_j|-1=\frac{|y-t_a|}{a_{u_j}\lambda_a}. \tag{9}
\]
This identity also gives zero at a tied boundary point. The actual radius at that time is \(s(a_{u_j}\lambda_a)^\beta\). Combining (8)–(9), every such covered initial ratio belongs to the one-sided band
\[
|y-t_a|<
\frac{2\delta}{s(a_{u_j}\lambda_a)^{\beta-1}}. \tag{10}
\]
The center is fixed by \(u,j\), and all prior constraints were retained by the shared exact prefix. No later reentry can repair failure of (8) at this time.

The physical change of variables \((s,y)\mapsto(s,sy)\) has Jacobian \(s\). Therefore integrating the band length against \(s\,ds\), \(0<s\le1\), bounds its covered area by
\[
2\delta\,a_{\min}^{1-\beta}\lambda_a^{1-\beta}. \tag{11}
\]
The factor \(1/s\) in (10) cancels the Jacobian; there is no uniform-positive-radius assumption hidden here. The vertex has zero area but is included in all upper catalogues.

**Lemma 15.2 (finite-horizon area bound).** For all \(n\ge1,\ 0<\delta<1\), and all binary words \(u\),
\[
\operatorname{area}V(n,\delta,u)
\le a_{\max}^n+C_A\delta^{1/\beta},\qquad
C_A=1+\frac{2a_{\min}^{1-\beta}}{1-a_{\max}^{\beta-1}}. \tag{12}
\]

**Proof.** Set \(\theta=\delta^{1/\beta}\). Along the given word \(u\), let \(l\) be its first product crossing \(\lambda_{u_1\cdots u_l}\le\theta\), or \(n\) if there is no crossing through time \(n\). For each \(j\le l\), \(\lambda_{u_1\cdots u_{j-1}}>\theta\). Moreover,
\[
\sum_{j=1}^l\lambda_{u_1\cdots u_{j-1}}^{1-\beta}
\le \frac{\lambda_{u_1\cdots u_{l-1}}^{1-\beta}}
{1-a_{\max}^{\beta-1}}
\le\frac{\theta^{1-\beta}}{1-a_{\max}^{\beta-1}}. \tag{13}
\]
The first inequality follows by comparing earlier products with the last one; every extra factor contributes at most \(a_{\max}^{\beta-1}\) after raising to the exponent \(1-\beta\).

Ratios agreeing with \(u\) through \(l\) lie in \(I_{u_1\cdots u_l}\), whose cone area is \(\lambda_{u_1\cdots u_l}\le\theta+a_{\max}^n\). All remaining covered points have a first deviation \(j\le l\). Sum (11) and use (13). This gives (12). Boundaries lie either in the agreement set or in a band; none has been discarded from the control requirement. ∎

Consequently, for every positive-area compact \(K\),
\[
r(n,\delta;K)\ge
\frac{\operatorname{area}(K)}{a_{\max}^n+C_A\delta^{1/\beta}}. \tag{14}
\]
This is already a horizon-uniform geometric estimate. It does not assert that an optimal catalogue is a selected coding tree.

### 3.2 Typical products extend the matching range to \(\beta h_a\)

Under normalized Lebesgue measure on \([-1,1]\), the assigned branch digits are independent with probabilities \(a_0,a_1\): (6) gives the measure of every finite cylinder as \(\lambda_w\). Tie points and their preimages form a countable set, hence have zero measure.

For completeness, if \(p\) is the zero frequency at time \(k\), its probability is \(\binom{k}{kp}a_0^{kp}a_1^{k(1-p)}\). The elementary binomial upper bound gives at most
\[
e^{-kD(p\Vert a_0)},\quad
D(p\Vert a_0)=p\ln(p/a_0)+(1-p)\ln((1-p)/a_1).
\]
Since \(D''(p)=1/[p(1-p)]\ge4\) and its minimum is at \(a_0\), \(D(p\Vert a_0)\ge2(p-a_0)^2\). Summing at most \(k+1\) types makes each fixed frequency deviation summable in \(k\). Borel–Cantelli, then a countable sequence of deviations, proves
\[
-\frac{\ln\lambda_{p_k(y)}}k\longrightarrow h_a
\quad\text{for Lebesgue-almost every }y. \tag{15}
\]

Fix the given positive-area compact \(K\), with area \(A>0\). Egorov's theorem and inner regularity give one compact \(E\subset(-1,1)\), excluding the countable boundary set, with \(2-|E|<A\), on which (15) is uniform. The physical cone
\[
Q_E=\{(s,sy):0\le s\le1,\ y\in E\}
\]
is compact; it includes the vertex. Its missing area is \((2-|E|)/2<A/2\). Thus \(K'=K\cap Q_E\) is compact and has area \(>A/2\).

The set \(E\), and hence \(K'\), is fixed before any precision exponent or tolerance sequence. For every \(0<\zeta<h_a\), a constant \(D_\zeta\ge1\) absorbs the finitely many early times and gives
\[
D_\zeta^{-1}e^{-(h_a+\zeta)k}
\le \lambda_{p_k(y)}
\le D_\zeta e^{-(h_a-\zeta)k}
\quad(y\in E,\ k\ge0). \tag{16}
\]

Fix an arbitrary \(u,n,\delta\) and \(0\le m\le n\). The covered points of \(K'\) agreeing through \(m\), if any, lie in a cylinder of cone area at most \(D_\zeta e^{-(h_a-\zeta)m}\), by (16). A covered point first differing at \(j\le m\) has the actual common prefix of a point of \(E\), so (16) bounds \(\lambda_a\) below. Its band area (11) is at most
\[
C_\zeta\delta e^{(\beta-1)(h_a+\zeta)(j-1)}.
\]
Summing the geometric progression yields a constant independent of \(u,n,m,\delta\) such that
\[
\operatorname{area}(K'\cap V(n,\delta,u))
\le C'_\zeta\left[
e^{-(h_a-\zeta)m}
+\delta e^{(\beta-1)(h_a+\zeta)m}\right]. \tag{17}
\]
This is the same first-deviation estimate, now restricted to an actual positive-area subset of the arbitrary given \(K\), not a replacement of \(K\) by symbolic states.

For small \(\delta\), choose
\[
m=\min\left\{n,\left\lfloor
\frac{-\ln\delta}{\beta(h_a+\zeta)}
\right\rfloor\right\}.
\]
Then \(\delta e^{\beta(h_a+\zeta)m}\le1\); the second term of (17) is at most \(e^{-(h_a+\zeta)m}\). Summing the areas of the controls in any spanning catalogue proves
\[
r(n,\delta;K)\ge B_{\zeta,K}e^{(h_a-\zeta)m}
\quad\text{with }B_{\zeta,K}>0. \tag{18}
\]
For every tolerance sequence of exponent \(\gamma\in[0,\infty]\), (18) implies
\[
\liminf_n n^{-1}\ln r(n,\delta_n;K)
\ge(h_a-\zeta)\min\{1,\gamma/[\beta(h_a+\zeta)]\}.
\]
Let \(\zeta\downarrow0\). This gives the lower bound in (4), including the endpoint \(\gamma=\beta h_a\). At \(\gamma=0\), nonnegativity also supplies the trivial zero lower rate.

## 4. A full-time upper catalogue

Use the \(M,L\) of §2, and set \(C_0=2\sqrt2M\). Stop every exact binary branch at its first word with
\[
\lambda_w^\beta\le\delta/C_0,
\]
or at depth \(n\) if no earlier crossing occurs. For \(0<\delta<1\) this is a finite complete prefix-free tree. Every leaf satisfies
\[
\lambda_w>a_{\min}(\delta/C_0)^{1/\beta}.
\]
The disjoint-interior intervals of the leaves cover \([-1,1]\), so their relative lengths sum to one. Therefore
\[
|\mathcal L|\le a_{\min}^{-1}C_0^{1/\beta}\delta^{-1/\beta}. \tag{19}
\]
This stopping-scale count is classical.

Use each leaf as the exact prefix of one infinite control, followed by any fixed tail. If it reaches depth \(n\), all required times are exact. If it stops earlier, (7) gives endpoint norm at most \(M\delta/C_0\); every later input contracts the \(M\)-norm by \(L<1\). Thus at every remaining time the Euclidean norm is at most \(\delta/2\), strictly within \(Q^\delta\). All initial radii and all endpoints are included.

This proves
\[
r(n,\delta;K)\le r(n,\delta;Q)
\le C_U\delta^{-1/\beta},\qquad C_U=a_{\min}^{-1}C_0^{1/\beta}. \tag{20}
\]
The full length-\(n\) exact catalogue also gives \(r(n,\delta;Q)\le2^n\). Equations (18)–(20) prove (4). They match for \(0\le\gamma\le\beta h_a\), proving (3) and completing Theorem 15.1. ∎

For the smaller finite-horizon region \(\delta^{1/\beta}\ge a_{\max}^n\), (14) and (20) even bound the catalogue between fixed multiples of \(\delta^{-1/\beta}\), with no polynomial-in-\(n\) loss. This is a consequence of the proved area estimate, not an extra assumption.

## 5. A concrete comparison with the already proved splitting model

Choose
\[
a_0=1/3,\qquad a_1=2/3,\qquad \beta=2.
\]
Then
\[
F_0(s,z)=(s/9,\ z/3+2s/9),\qquad
F_1(s,z)=(4s/9,\ 2z/3-2s/9). \tag{21}
\]
The two radial factors are \(1/9\) and \(4/9\). Since
\[
\ln2<2\ln(3/2)\le2h_a,
\]
Theorem 15.1 gives, for every positive-area compact \(K\subset Q\),
\[
\lim_n n^{-1}\ln r(n,2^{-n};K)=\tfrac12\ln2. \tag{22}
\]
The first inequality is \(2<9/4\); the second follows from
\(h_a=\sum a_i\ln(1/a_i)\ge\ln(1/a_{\max})\).

In the R06 equal-width family with the **same** radial factors \(1/9,4/9\), the already proved theorem gives full-\(Q\) rate \(\frac12\ln2\), because
\[
(1/9)^{1/2}+(4/9)^{1/2}=1.
\]
Its fixed near-full-area compact sets instead have rate
\[
\frac{(\ln2)^2}{\ln(9/2)}<\tfrac12\ln2. \tag{23}
\]
Here \(\bar c=\ln(9/2)\); the strict inequality is \(9/2>4\). This is a consequence of R06, not a second newly attacked theorem.

Thus the radial factors, physical cone, precision sequence and full-\(Q\) rate can all stay the same while changing the feasible branch geometry removes the splitting at this precision. Unequal radial factors alone are not the mechanism. The criterion matches contraction to the actual angular cylinder widths, which makes first-deviation area and stopping scale compatible.

## 6. Coordinate reduction and precise limits of the result

For label \(i\), the eigenvalues at the origin are
\[
a_i^\beta,\qquad a_i^{\beta-1}.
\]
If \(a_0\ne a_1\), the two spectral radii are different. A fixed \(C^1\) state conjugacy fixing the origin and preserving control labels up to permutation cannot turn this class into the common-first-jet R05 family, whose control spectral radii coincide. The R06 family has eigenvalue ratio 2 for both labels, whereas here the ratios are \(1/a_0\) and \(1/a_1\). It therefore cannot give a simultaneous \(C^1\) reduction to R06 either.

This excludes these regular coordinate reductions; it does not assert a general theorem about arbitrary singular homeomorphisms. For \(a_0=a_1=1/2\), the model is precisely the equal-radial R06 case and is only an old corollary. The unequal-width, unequal-radial case is the new sufficient regime.

The proof does not treat overlapping feasible branches, nonlinear control-dependent contraction, or perturbations of (5). It does not prove that (5) is necessary, that it eliminates splitting at every precision, or that \(\beta h_a\) is the maximal universal range. At \(\gamma>\beta h_a\), (4) generally leaves a gap. The fixed-system comparison \(g=\kappa\) and the exact value of the paused R09 constant remain untouched.

The symbolic facts used here—product cylinders, typical frequencies, stopped scales and entropy/contraction relations—are existing methods. The new project-level result is their complete controlled realization in (12), (17)–(20), giving a directly checkable sufficient condition for universality over arbitrary positive-area compact sets with genuinely different radial factors. SOURCES.md records the exact external reading and its coverage limits; this proof is not a claim of all-literature priority or journal-level certification.

