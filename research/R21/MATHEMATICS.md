# R21: mismatched radial powers and loss of a common low-precision cost

5 October 2026. Baseline `782edf83d79d1765c1e6eb5b90f0a7951aecdb54`. All logarithms are natural. This proves the single system and proposition authorized for R21. No statement about the paused overlapping system is used.

## 1. System, actual catalogue, and theorem

Fix
\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,
\qquad \beta_0,\beta_1>1,\quad \beta_0\ne\beta_1,
\]
\[
0<\epsilon<\frac{a_{\min}}{4(\beta_++1)},\qquad
a_{\min}=\min_i a_i,\quad \beta_- =\min_i\beta_i,
\quad \beta_+=\max_i\beta_i.
\]
On the entire plane define
\[
p_0(s)=a_0+\epsilon\frac{s}{1+s^2},\qquad
p_1(s)=a_1-\epsilon\frac{s}{1+s^2},
\]
\[
G_0(s,z)=\bigl(sp_0(s)^{\beta_0},p_0(s)^{\beta_0-1}[z+p_1(s)s]\bigr),
\quad
G_1(s,z)=\bigl(sp_1(s)^{\beta_1},p_1(s)^{\beta_1-1}[z-p_0(s)s]\bigr).
\tag{1}
\]
Every infinite binary input is allowed. Keep
\[
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad \operatorname{area}(Q)=1.
\]
For a nonempty compact \(K\subset Q\), \(r_G(n,\delta;K)\) is the minimum cardinality of a finite catalogue \(\mathcal U\subset\{0,1\}^{\mathbb N}\) of infinite inputs such that
\[
\forall x\in K\ \exists u\in\mathcal U\ \forall k=0,\ldots,n:
\operatorname{dist}_2(G_u^kx,Q)<\delta.
\tag{2}
\]
The input is assigned to the actual planar state. Approximate trajectories may leave and reenter \(Q\). A single tolerance applies throughout each horizon; there is no constraint between integer times. All boundary states are included.

Put
\[
\rho_i=a_i^{\beta_i},\quad \rho_{\min}=\min_i\rho_i,
\quad \rho_{\max}=\max_i\rho_i,\quad
\gamma_0=-\log\rho_{\max},
\]
\[
h=-\sum_i a_i\log a_i,\qquad
\chi=-\sum_i a_i\log\rho_i,\qquad
\rho_0^D+\rho_1^D=1\quad(D>0).
\tag{3}
\]
In particular \(0<\rho_i<a_i<1\), \(\chi>h>0\), and \(\chi\ge\gamma_0>0\). The root \(D\) is unique because the left side is continuous and strictly decreasing from 2 to 0.

**Theorem 21.1.** Both maps (1) are global \(C^\infty\) diffeomorphisms. All inputs take bounded sets uniformly exponentially to the common origin, and \(Q\) is controlled invariant. For every \(\zeta\in(0,1)\) there is one compact \(K_\zeta\subset Q\), with
\[
\operatorname{area}(K_\zeta)>1-\zeta,
\]
such that for every \(\gamma\in(0,\gamma_0)\) and every positive sequence \(\delta_n\to0\) satisfying \(-\log\delta_n/n\to\gamma\),
\[
\lim_{n\to\infty}\frac{\log r_G(n,\delta_n;Q)}n=\gamma D,
\qquad
\lim_{n\to\infty}\frac{\log r_G(n,\delta_n;K_\zeta)}n
=\gamma\frac h\chi<\gamma D.
\tag{4}
\]
The compact set is chosen before the exponent, sequence, and horizon. No monotonicity of the sequence is required. For every other fixed positive-area compact \(K\subset Q\) the proof also gives the lower bound \(\liminf n^{-1}\log r_G(n,\delta_n;K)\ge\gamma h/\chi\) in this range; it does not classify all such sets.

## 2. Dynamics and two distinct products

Set
\[
\underline p=a_{\min}-\epsilon/2>0,\quad
\overline p=\max_i a_i+\epsilon/2<1,\quad r=\overline p^{\beta_-}<1.
\]
For \(f(s)=s/(1+s^2)\), \(|f|\le1/2\) and \(|sf'(s)|\le1/2\). The radial map \(g_i(s)=sp_i(s)^{\beta_i}\) has derivative
\[
g_i'(s)=p_i(s)^{\beta_i-1}[p_i(s)+\beta_i s p_i'(s)]>0,
\]
since the bracket is at least \(a_{\min}-(\beta_++1)\epsilon/2>0\). As \(|s|\to\infty\), \(p_i(s)\to a_i\), so \(g_i\) is onto \(\mathbb R\). Recovering \(s\) from the first output and then \(z\) from the second gives a smooth global inverse, with
\[
\det DG_i(s,z)=p_i(s)^{2\beta_i-2}[p_i(s)+\beta_i s p_i'(s)]>0.
\]
All powers are smooth because \(p_i\) is strictly positive globally.

Choose \(M\ge1\) with \(M>r/(1-\overline p^{\beta_--1})\). In the norm \(\|(s,z)\|_*=\max\{M|s|,|z|\}\),
\[
\|G_i(s,z)\|_*\le L\|(s,z)\|_*,\qquad
L=\max\{r,\overline p^{\beta_--1}+r/M\}<1.
\tag{5}
\]
Indeed \(|s'|\le r|s|\) and \(|z'|\le\overline p^{\beta_--1}|z|+r|s|\). This applies on the entire plane, including off-constraint states. It is a bound toward the origin, not a pairwise Lipschitz assertion.

For \(s>0\), use \(y=z/s\) only for calculations. Write \(\xi(s)=p_0(s)-p_1(s)\). The angular maps and inverses are
\[
T_{0,s}(y)=\frac{y+p_1(s)}{p_0(s)},\quad
T_{1,s}(y)=\frac{y-p_0(s)}{p_1(s)},\quad
B_{0,s}(y)=p_0(s)y-p_1(s),\quad
B_{1,s}(y)=p_1(s)y+p_0(s).
\]
Their complete one-step feasible domains are \([-1,\xi(s)]\) and \([\xi(s),1]\), respectively. They cover \([-1,1]\), and the radius decreases. Assign ties to branch 0. This gives an exact infinite feasible code \(c(x)\) for every actual state, with the vertex covered separately.

For a word \(w=w_1\cdots w_l\), let \(s_0=s\), \(s_j=g_{w_j}(s_{j-1})\), and define
\[
\lambda_w=\prod_j a_{w_j},\quad R_w=\prod_j\rho_{w_j},
\quad P_w(s)=\prod_j p_{w_j}(s_{j-1}),
\quad \mathcal R_w(s)=\prod_jp_{w_j}(s_{j-1})^{\beta_{w_j}}.
\tag{6}
\]
Empty products equal 1. The actual radius is \(s_l=s\mathcal R_w(s)\), and \(s_j\le r^js\). **There is no common identity \(\mathcal R_w=P_w^\beta\) in the mismatched case.**

For \(0\le s\le1\),
\[
|\log p_i(s_j)-\log a_i|\le\epsilon s_j/\underline p.
\]
Summing the geometric series and, separately, multiplying each summand by its actual exponent proves
\[
C_P^{-1}\lambda_w\le P_w(s)\le C_P\lambda_w,
\quad C_R^{-1}R_w\le\mathcal R_w(s)\le C_R R_w,
\tag{7}
\]
where
\[
C_P=\exp\frac{\epsilon}{\underline p(1-r)},\qquad C_R=C_P^{\beta_+}.
\]
These constants hold uniformly in the word, its length, and the initial radius. They are derived from the maps, not assumed as covering or distortion hypotheses.

Let \(I_w(s)\) be the closed interval of initial angles feasible at **all** intermediate times for \(w\). Recursion gives
\[
I_{iv}(s)=B_{i,s}(I_v(g_i(s))),\quad I_\varnothing(s)=[-1,1],
\qquad |I_w(s)|=2P_w(s).
\tag{8}
\]
The recursion includes the first constraint because \(B_{i,s}([-1,1])\) is its full feasible domain. Every finite complete prefix-free leaf family gives a cover by these intervals with disjoint interiors on each actual radius. All shared endpoints are retained.

The corresponding physical strip \(Q_w=\{(s,sy):0<s\le1,y\in I_w(s)\}\cup\{0\}\) satisfies
\[
C_P^{-1}\lambda_w\le\operatorname{area}(Q_w)
=\int_0^1 2sP_w(s)\,ds\le C_P\lambda_w.
\tag{9}
\]
Every finite-word boundary is a continuous curve and has area zero; the union of these boundaries and the vertex is null. This is only used for area arguments, never to omit states from a full-set catalogue.

## 3. The decisive interface: relative spacing inside a common prefix

Let \(V(n,\delta,u)\) denote the actual states in \(Q\) satisfying (2) under one arbitrary input \(u\). It need not be exactly feasible. If the assigned exact code first differs from \(u\) at time \(j\), put \(a=u|_{j-1}\), \(i=u_j\), and
\[
b_a(s)=T_{a,s}^{-1}(\xi(s_{j-1})).
\]
The angular composition is affine and increasing with slope \(1/P_a(s)\). The wrong branch yields
\[
|y_j|-1=\frac{|y-b_a(s)|}{P_{ai}(s)},\qquad
s_j=s\mathcal R_{ai}(s).
\]
At a tie the excess is zero. Membership in \(Q^\delta\) at this time necessarily gives \(|z_j|-s_j<2\delta\), since \((s,z)\mapsto |z|-s\) is \(\sqrt2\)-Lipschitz. Consequently each first-difference class lies in a one-sided band
\[
|y-b_a(s)|<\frac{2\delta P_{ai}(s)}{s\mathcal R_{ai}(s)}
\le \frac{C_b\delta\lambda_a}{sR_a},
\qquad C_b=2C_P C_R\max_i\frac{a_i}{\rho_i}.
\tag{10}
\]
Its physical area is at most \(C_b\delta\lambda_a/R_a\), after multiplying by the Jacobian \(s\) and integrating in \(s\). No lower bound on the initial radius is assumed. Reentry at later times cannot erase this necessary constraint.

For \(0<t<1\), stop at the first word with \(R_w\le t\), or at depth \(n\) if no earlier crossing occurs. Let \(\mathcal L_R(n,t)\) be this finite complete prefix-free family and \(N_R(n,t)\) its size. Every leaf has
\[
R_{w^-}>t,\qquad R_w>\rho_{\min}t.
\tag{11}
\]
These bounds include terminal leaves which have not crossed. At a common proper prefix \(a\), every descendant leaf \(w=av\) has
\[
\lambda_v\ge R_v=R_w/R_a>\rho_{\min}t/R_a,
\]
because each \(a_i>\rho_i\). Hence at radius 1
\[
|I_w(1)|\ge2C_P^{-1}\lambda_w
>2C_P^{-1}\lambda_a\rho_{\min}t/R_a.
\tag{12}
\]
This is a **conditional** spacing estimate. The entire stopped tree need not have comparable angular widths. That is why the global matched-width spacing from R19 cannot simply be reused.

**Lemma 21.2 (comparison with arbitrary actual inputs).** With
\[
C_0=2\sqrt2 M C_R,\qquad
B=\left\lceil1+\frac{C_b C_P}{2\rho_{\min}}\right\rceil,
\]
for every \(n\ge1\) and \(0<\delta<1\),
\[
\frac{N_R(n,\delta)}{1+Bn}\le r_G(n,\delta;Q)
\le N_R(n,\delta/C_0).
\tag{13}
\]

**Proof.** For the lower bound use the actual states \((1,y_w)\), where \(y_w\) is the midpoint of \(I_w(1)\) for \(w\in\mathcal L_R(n,\delta)\). Each midpoint has assigned prefix \(w\): it lies strictly inside the leaf, so no earlier branch boundary can occur.

Fix any \(u\). At most one leaf is a prefix of \(u\). Every other covered witness first differs at some \(j\le |w|\le n\), and shares \(a=u|_{j-1}\). For fixed \(u,j\), all such leaves are descendants of this same \(a\). Their disjoint-interior intervals have lengths greater than
\(\ell=2C_P^{-1}\lambda_a\rho_{\min}\delta/R_a\), by (12). Any two of their ordered midpoints are separated by more than \(\ell\), even if other leaves intervene. On the other hand (10), at \(s=1\), confines the covered midpoints to one band of length at most \(C_b\delta\lambda_a/R_a\). It contains at most
\[
1+\frac{C_b\delta\lambda_a/R_a}{2C_P^{-1}\lambda_a\rho_{\min}\delta/R_a}
=1+\frac{C_b C_P}{2\rho_{\min}}\le B
\]
such witnesses. Sum over \(j\le n\) and include the one possible prefix leaf. An arbitrary input covers at most \(1+Bn\) actual witnesses, proving the lower bound. No condition has been imposed after its first difference other than the original all-time constraint.

For the upper bound use every leaf at \(t=\delta/C_0\) as an exact prefix, followed by one fixed infinite input tail. On every radius these leaf intervals cover all initial angles, including closed endpoints. A terminal depth-\(n\) leaf is exactly feasible throughout the horizon. An earlier leaf ends at \(|z_l|\le s_l\le C_Rt\), so its adapted norm is at most \(MC_Rt=\delta/(2\sqrt2)\). By (5), the **entire** remaining tail stays at Euclidean distance at most \(\delta/2\) from the origin in \(Q\). The vertex is fixed. This proves the upper bound. ∎

The proof architecture of the prefix-dependent spacing is already present in R06 §3.2 for equal-width linear branches. Here it is verified for unequal moving branches, distinct angular and radial products, and actual state-dependent intervals. It is not a new interval-packing principle or an assumed optimality of the exact tree.

## 4. Full-set rate below the first horizon cutoff

When every branch crosses before or at depth \(n\), write \(\mathcal L_R(t)\) and \(N_R(t)\) for the stopped family. This occurs if \(\lceil-\log t/\gamma_0\rceil\le n\), because \(R_w\le\rho_{\max}^{|w|}\). Replacing a parent by its two children preserves the sum of its \(D\)-weights; thus
\[
\sum_{w\in\mathcal L_R(t)}R_w^D=1.
\]
Every leaf now has \(\rho_{\min}t<R_w\le t\), yielding
\[
t^{-D}\le N_R(t)\le(\rho_{\min}t)^{-D}.
\tag{14}
\]
This is classical stopped-product counting, not a new pressure result.

If \(-\log\delta_n/n\to\gamma\in(0,\gamma_0)\), both thresholds \(\delta_n\) and \(\delta_n/C_0\) cross by \(n\) for all sufficiently large \(n\). Combining (13)–(14) gives
\[
\frac{\delta_n^{-D}}{1+Bn}\le r_G(n,\delta_n;Q)
\le \left(\frac{\rho_{\min}\delta_n}{C_0}\right)^{-D}.
\tag{15}
\]
The logarithm of the polynomial loss divided by \(n\) vanishes. This proves the first limit in (4) for every stated sequence, including arbitrary subexponential fluctuations.

## 5. One physical compact set before any precision choice

Write \(H(t)=-t\log t-(1-t)\log(1-t)\), with \(0\log0=0\). The assigned length-\(k\) cylinder is contained in \(Q_w\), with probability at most \(C_P\lambda_w\) under normalized physical area. For a type with zero frequency \(t=j/k\),
\[
\binom{k}{j}a_0^j a_1^{k-j}\le e^{-k I(t)},\qquad
I(t)=t\log(t/a_0)+(1-t)\log((1-t)/a_1)\ge2(t-a_0)^2.
\]
The first inequality follows from \(\binom{k}{j}\le e^{kH(t)}\), obtained by evaluating a binomial probability with parameter \(t\). The second follows from \(I''(t)=1/[t(1-t)]\ge4\), \(I(a_0)=I'(a_0)=0\). There are at most \(k+1\) types. Hence each fixed frequency deviation has area at most \(C_P(k+1)e^{-2\eta^2k}\), summable in \(k\). Borel–Cantelli for a countable sequence of deviations proves frequency convergence to \(a_0\) for area-almost every state. Independence of the moving digits is not assumed.

Remove the null boundary curves and vertex. Egorov's theorem and inner regularity give one compact \(T_\zeta\subset Q\) of area greater than \(1-\zeta\) with uniform frequency convergence. Choose it now, before any exponent, precision sequence, or horizon, and put \(K_\zeta=T_\zeta\cup\{0\}\).

For every \(0<\eta<h\) small enough that \(\chi-\eta>0\), there is \(A_\eta\ge1\) such that for all \(x\in T_\zeta\) and \(k\ge0\),
\[
A_\eta^{-1}e^{-(h+\eta)k}\le\lambda_{c_k(x)}\le A_\eta e^{-(h-\eta)k},
\quad
A_\eta^{-1}e^{-(\chi+\eta)k}\le R_{c_k(x)}\le A_\eta e^{-(\chi-\eta)k}.
\tag{16}
\]
These follow from the two affine functions of frequency, \(-k^{-1}\log\lambda\) and \(-k^{-1}\log R\); finitely many early times are absorbed in \(A_\eta\). The same compact set works for every auxiliary \(\eta\). The same construction supplies a positive-area compact typical portion of any fixed positive-area compact \(K\).

## 6. Area lower bound for every approximate input

For any such uniformly typical compact \(T\), any arbitrary \(u\), and \(0\le m\le n\), agreement through \(m\) occupies at most \(Q_{u|_m}\). If it meets \(T\), (9) and (16) bound its area by \(C_P A_\eta e^{-(h-\eta)m}\). At a first disagreement \(j\le m\), a nonempty class has common prefix \(a=u|_{j-1}=c_{j-1}(x)\) for some \(x\in T\). Equations (10) and (16) bound its area by
\[
C_b A_\eta^2\delta e^{(\chi-h+2\eta)(j-1)}.
\]
Since \(\chi-h>0\), summing this geometric progression proves
\[
\operatorname{area}(T\cap V(n,\delta,u))
\le A'_\eta\bigl[e^{-(h-\eta)m}+\delta e^{(\chi-h+2\eta)m}\bigr],
\tag{17}
\]
uniformly in \(u,n,m,\delta\). Empty classes do not contribute. Later disagreements are already in the agreement class through \(m\).

Take
\[
m=\min\{n,\lfloor-\log\delta/(\chi+\eta)\rfloor\}.
\]
Then \(\delta e^{(\chi+\eta)m}\le1\), so (17) is at most \(2A'_\eta e^{-(h-\eta)m}\). Any catalogue spanning \(T\) must cover its positive physical area. For \(\gamma<\gamma_0\le\chi\), this gives
\[
\liminf_n \frac{\log r_G(n,\delta_n;K_\zeta)}n
\ge\gamma\frac{h-\eta}{\chi+\eta}.
\tag{18}
\]
Let \(\eta\downarrow0\). Applying the same argument to a fixed typical portion of any positive-area \(K\) proves the extra lower bound stated after the theorem. The Jacobian cancellation in (10) is why no positive initial-radius lower bound is needed for this estimate.

## 7. A complete stopped upper catalogue on that same compact set

Use only leaves of \(\mathcal L_R(n,\delta/C_0)\) actually realized by assigned prefixes on \(T_\zeta\), each with the same fixed tail as in Lemma 21.2; add one input for the vertex. This covers every point of \(K_\zeta\) at all required times. For the exponents in (4), every leaf has crossed for all sufficiently large \(n\). Put \(T=-\log(\delta/C_0)\), \(c_{\max}=-\log\rho_{\min}\). A realized stopped word of length \(l\) obeys
\[
T\le-\log R_w<T+c_{\max},\qquad
(\chi-\eta)l-\log A_\eta\le-\log R_w.
\]
Therefore
\[
l\le\frac{T+c_{\max}+\log A_\eta}{\chi-\eta}.
\tag{19}
\]
Uniform frequency convergence on the already chosen \(T_\zeta\), and continuity of \(H\), imply that the number of realized length-\(l\) prefixes is at most
\(A''_\eta(l+1)e^{(h+\eta)l}\) for every \(l\); the finite early lengths are absorbed in \(A''_\eta\). Summing this bound over the lengths permitted by (19) yields
\[
\log r_G(n,\delta;K_\zeta)
\le \frac{h+\eta}{\chi-\eta}(T+c_{\max}+\log A_\eta)
+O_\eta(\log(1+T))+O_\eta(1)
\tag{20}
\]
for sufficiently large \(n\) along every stated precision sequence. In particular
\[
\limsup_n n^{-1}\log r_G(n,\delta_n;K_\zeta)
\le\gamma\frac{h+\eta}{\chi-\eta}.
\]
Let \(\eta\downarrow0\) and combine with (18). The second limit in (4) follows. Neither the compact set nor its uniform frequency property has been changed when varying \(\eta\), \(\gamma\), or the precision sequence. Every finite horizon has a valid catalogue; the eventual crossing condition is used only to derive the asymptotic count.

## 8. Strict separation and the scoped matching criterion

Let \(b_i=\rho_i^D\), so \(b_0+b_1=1\). Relative entropy gives
\[
D\chi-h=\sum_i a_i\log\frac{a_i}{b_i}\ge0.
\tag{21}
\]
For completeness, concavity of \(\log\) gives \(\sum_i a_i\log(b_i/a_i)\le\log\sum_i b_i=0\), with equality only when \(b_i/a_i\) is constant, hence only when \(b_i=a_i\) for both labels. Equality in (21) would imply
\(a_i^{\beta_iD}=a_i\), thus \(\beta_iD=1\) for both \(i\). This is impossible when \(\beta_0\ne\beta_1\). Therefore \(D>h/\chi\), completing Theorem 21.1. The root and relative-entropy identity are classical tools, not the new controlled step.

**Corollary 21.3 (matching is necessary and sufficient within this family).** Enlarge (1) only by allowing \(\beta_0=\beta_1\), retaining all other stipulated assumptions. There exists a positive interval of exponents next to zero on which every fixed positive-area compact initial set shares the same rate, for every precision sequence with each exponent, **if and only if** \(\beta_0=\beta_1\).

**Proof.** If the exponents agree, the verified R19/R20 theorem gives the interval \(0<\gamma\le\beta h\), with rate \(\gamma/\beta\). If they differ, for every \(0<\gamma<\gamma_0\), (4) already separates \(Q\) from one fixed nearly full-area compact set. Every interval next to zero contains such an exponent, so the common-cost property fails. ∎

This is a criterion for the expressly given triangular family, not for all smooth invertible control systems. It does not claim separation at every larger exponent or a two-value classification of positive-area compacts.

A regular coordinate replacement cannot make (1) a common-exponent R19/R17 system. At the origin \(DG_i\) has ordered positive eigenvalues \(\rho_i<\rho_i/a_i\). A simultaneous \(C^1\) diffeomorphism preserves these spectra, allowing a label permutation. Comparing with a target \((a_i')^\beta<(a_i')^{\beta-1}\) forces \(a_i'=a_i\) and \(\beta=\log\rho_i/\log a_i=\beta_i\) for both labels, a contradiction. This is a standard derivative obstruction, not an extra research task or an assertion about all singular ambient homeomorphisms.

## 9. Mathematical attribution and limits

The one interface proved here is (13): a genuine arbitrary-input comparison with a radial stopping tree despite unequal moving angular widths. Its relative-prefix packing architecture comes from R06, while the derived summable state dependence, actual curved strips, physical typical sets, and full tail come from R19. The weighted stopping count, types, Egorov construction, and relative entropy are established methods. The new project conclusion is (4) and the matching necessity in Corollary 21.3, not a new pressure theory or a new general packing technique.

R19's single-product formula cannot be used after splitting the exponents. Keeping the two products in (6), and proving the conditional cancellation (10)–(12), closes that missing application. The theorem therefore has a checked proof beyond a bare parameter substitution, but its proof methods remain closely continuous with the earlier results. Independent priority is limited by the literature comparison in SOURCES.md; no quartile or TOP status is certified.

The range \(0<\gamma<\gamma_0\) was fixed in the authorized problem. No full higher-precision spectrum, general nonlinear necessary-and-sufficient classification, or overlapping-strategy optimality is asserted. The unique manuscript is unchanged. ∎
