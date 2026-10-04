# R16: high-precision splitting in the fixed geometrically matched system

4 October 2026 (UTC). Natural logarithms. The one requested splitting proposition is proved, with limits and exact constants for every tolerance sequence of exponent ln 4. No other system or precision exponent is classified.

## 1. Actual object and the main theorem

The state space is the actual Euclidean plane. All infinite binary inputs are allowed. Keep
\[
F_0(s,z)=(s/9,z/3+2s/9),\qquad
F_1(s,z)=(4s/9,2z/3-2s/9),
\]
\[
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad \operatorname{area}(Q)=1.
\]
For a compact nonempty initial set K contained in Q, the catalogue is
\[
r(n,\delta;K)=\min\{|\mathcal C|:\mathcal C\subset\{0,1\}^{\mathbb N}
\text{ finite},\quad
\forall x\in K\ \exists u\in\mathcal C\ \forall k=0,\ldots,n:\
\operatorname{dist}_2(\varphi(k,x,u),Q)<\delta\}. \tag{1}
\]
There is one tolerance for the entire horizon. Approximate trajectories may leave and return to Q; the catalogue is not required to use an exact coding or a feedback policy.

Set
\[
H(p)=-p\ln p-(1-p)\ln(1-p),\quad 0\ln0=0,
\]
\[
h=H(1/3)=\ln3-\tfrac23\ln2,\qquad
p_* =\frac{\ln(4/3)}{\ln2},\qquad h_*=H(p_*).
\]

**Theorem 16.1 (the requested high-precision split).** For every positive sequence satisfying
\[
\delta_n\longrightarrow0,\qquad -\frac{\ln\delta_n}{n}\longrightarrow\ln4,
\]
the full-cone limit exists and equals
\[
\lim_{n\to\infty}\frac{\ln r(n,\delta_n;Q)}n=h_*. \tag{2}
\]
For every epsilon in (0,1), there is one compact K_epsilon contained in Q, with positive area and
\[
\operatorname{area}(K_\varepsilon)>1-\varepsilon,
\]
such that, for **every** sequence with the same stated exponent,
\[
\lim_{n\to\infty}\frac{\ln r(n,\delta_n;K_\varepsilon)}n=h<h_*. \tag{3}
\]
The set is chosen independently of the tolerance sequence and of every horizon. It can have empty interior and includes the cone vertex. Both limits are proved; the requested liminf/limsup inequality follows.

The system is precisely the R15 matching example with a_0=1/3, a_1=2/3 and beta=2. Thus this result proves that its matching condition does not eliminate initial-set splitting at all precisions. It does not prove a maximal common-cost interval or a necessary and sufficient structural classification.

## 2. Recovered exact geometry and full-time tails

For s>0, use y=z/s only for calculation. The angular maps and inverse branches are
\[
T_0(y)=3y+2,\quad T_1(y)=(3y-1)/2,
\]
\[
B_0(y)=(y-2)/3,\quad B_1(y)=(2y+1)/3.
\]
Their exact feasible domains are [-1,-1/3] and [-1/3,1]. Each maps onto [-1,1]. A tie can be assigned to control 0. The vertex is fixed by both inputs.

For a word w, write
\[
\lambda_w=\prod_j a_{w_j},\qquad a_0=1/3,\ a_1=2/3,
\quad \lambda_\varnothing=1.
\]
Its complete feasible interval, requiring every intermediate state to remain feasible, is
\[
I_w=B_{w_1}\circ\cdots\circ B_{w_l}([-1,1]),\qquad
|I_w|=2\lambda_w. \tag{4}
\]
Indeed, I_{iv}=I_i intersect T_i^{-1}(I_v)=B_i(I_v). These intervals partition [-1,1] with disjoint interiors at every depth. After w, the actual radius is s lambda_w^2 and the ratio-map slope is lambda_w^{-1}.

In the actual sup norm, the two matrix operator norms are at most 5/9 and 8/9. Thus arbitrary input products contract with common bound L=8/9, and the Euclidean norm is at most sqrt(2) times the sup norm. This verifies the R15 complete-tail argument directly for this example; no arbitrary tail is assumed feasible before its size is controlled.

## 3. The decisive comparison with arbitrary approximate controls

For 0<t<1 and n>=1, let L(n,t) be the complete prefix-free tree of words stopped at the first product lambda_w<=t, or at depth n if no earlier crossing has occurred. Let N(n,t) be its number of leaves. Every leaf satisfies
\[
\lambda_{w^-}>t,\qquad \lambda_w>t/3. \tag{5}
\]
The first inequality includes terminal leaves, whose proper prefixes have not crossed. The leaf intervals have disjoint interiors and cover all of [-1,1], with their actual endpoints retained.

**Lemma 16.2 (a real-catalogue stopping comparison).** For every n>=1 and 0<delta<1,
\[
\frac{N(n,\sqrt\delta)}{1+10n}
\le r(n,\delta;Q)
\le N\left(n,\sqrt{\frac{\delta}{2\sqrt2}}\right). \tag{6}
\]

**Proof of the lower bound.** Put t=sqrt(delta). For every stopped leaf w choose its interval midpoint y_w and the actual state x_w=(1,y_w), which belongs to Q. By (5), all the intervals have length greater than 2t/3. The midpoints of any two such disjoint-interior intervals are separated by more than 2t/3.

Fix any length-n input u, whether or not it is exactly feasible for its covered initial states. At most one stopped leaf is a prefix of u. For every other covered witness, let j<=|w| be the first input where u differs from w, and let a=u_1...u_{j-1}. Define the unique dividing point
\[
b_a=T_a^{-1}(-1/3).
\]
The witness is in the opposite feasible child of I_a from the chosen input i=u_j. At the first disagreement,
\[
|y_j|-1=\frac{|y_w-b_a|}{a_i\lambda_a},\qquad
s_j=(a_i\lambda_a)^2. \tag{7}
\]
These identities follow from the affine slopes and from T_0(-1/3)=1, T_1(-1/3)=-1. They do not impose feasibility after the disagreement.

A necessary condition for an actual state (s_j,z_j) in Q^delta, with s_j>=0, is
\[
|z_j|-s_j<2\delta. \tag{8}
\]
Compare both coordinates with a point of Q less than delta away. Combining (7) and (8), any covered witness must lie in the one-sided band
\[
|y_w-b_a|<\frac{2\delta}{a_i\lambda_a}<6t. \tag{9}
\]
Here lambda_a>t because a is a proper prefix of a stopped leaf, and a_i>=1/3. For a fixed u and j the band center and side are fixed. Its length is less than 6t. The midpoint separation gives at most 1+6t/(2t/3)=10 witnesses in that band. Hence any arbitrary input covers at most 1+10n leaf witnesses.

Any catalogue spanning Q must cover every actual witness. Summing this bound over its inputs proves the left inequality of (6). The input can reenter Q later; it still had to satisfy (8) at its first wrong branch. No midpoint is substituted for the initial-state coverage requirement: the points are necessary witnesses belonging to the full physical Q.

**Proof of the upper bound.** Use every leaf at t=sqrt(delta/(2sqrt(2))) as an exact prefix, followed by a fixed infinite tail. A depth-n leaf is feasible at all required times. For an earlier leaf, its exact endpoint has sup norm at most lambda_w^2<=delta/(2sqrt(2)). Every later input contracts the sup norm by at most 8/9. The entire tail is therefore at Euclidean distance at most delta/2 from the origin in Q. The leaf intervals cover every initial ratio, both boundary rays and shared endpoints; the vertex is fixed. This proves the right inequality and the whole lemma. ∎

This is the one new decisive interface. It bounds the possible advantage of arbitrary approximate inputs without assuming that the stopped tree is an optimal catalogue. Its first-deviation architecture is inherited from R06; the estimate is re-established for the actual unequal-width, matched branches of R15.

## 4. Stopped counting at the one requested exponent

We prove only the count needed for (6): if t_n->0 and -ln(t_n)/n->tau=ln2, then
\[
\lim_n\frac{\ln N(n,t_n)}n=H(p_*). \tag{10}
\]
This is classical type counting applied after the real-catalogue comparison. It is not a new pressure principle.

For a length-k word with zero frequency p, its product cost is
\[
-\ln\lambda_w=k\chi(p),\qquad
\chi(p)=\ln(3/2)+p\ln2. \tag{11}
\]
The equation chi(p_*)=tau gives the constant in the theorem. Since
\[
\chi(1/3)=H(1/3)<\ln2,\qquad
\chi(1/2)=\ln(3/\sqrt2)>\ln2,
\]
we have
\[
1/3<p_*<1/2. \tag{12}
\]
The first strict inequality follows from the strict maximum of H at 1/2; the second numerical inequality is exactly 9>8. In particular H(p_*)>H(1/3), giving the desired strict gap without numerical fitting.

For p in (0,1), the sign of the derivative of H(p)/chi(p) is the sign of
\[
U(p)=\ln3\,\ln(1-p)-\ln(3/2)\,\ln p.
\]
Its derivative is -ln3/(1-p)-ln(3/2)/p<0, and U(1/3)=0. Thus H/chi is strictly decreasing on [p_*,1), and by continuity
\[
\tau\frac{H(p)}{\chi(p)}\le H(p_*)\quad(p\ge p_*). \tag{13}
\]
Also H(p)<=H(p_*) for p<=p_*, since p_*<1/2.

For completeness, for every k and integer j in [0,k],
\[
\frac{e^{kH(j/k)}}{k+1}\le {k\choose j}\le e^{kH(j/k)}. \tag{14}
\]
With binomial parameter j/k, the mass at j equals the middle expression times e^{-kH(j/k)}. It is a mode, as verified by the adjacent-mass ratios; it is therefore between 1/(k+1) and 1. The endpoint cases are immediate.

Write T_n=-ln(t_n). A stopped leaf of depth k<n has total cost in [T_n,T_n+ln3), since the last increment is at most ln3. A terminal leaf of depth n has total cost less than T_n+ln3. There are at most (n+1)^2 length/type pairs. Their counts are bounded above by (14), even if not every word of such a type is a leaf.

Along a subsequence maximizing this bound, in the stopped case let k/n->alpha and j/k->p. The positive threshold ensures alpha>0, and
\[
\alpha\chi(p)=\tau,\qquad \chi(p)\ge\tau.
\]
Consequently p>=p_* and the normalized logarithmic count is at most alpha H(p)=tau H(p)/chi(p)<=H(p_*), by (13). In the terminal case k=n and chi(p)<=tau in the limit, so p<=p_* and the bound is again H(p_*). Compactness and the polynomial number of types prove the upper half of (10).

For its lower half, fix 1/3<p<p_*. At depth n choose j_n/n->p. Since chi(p)<tau, all words of this type have total cost less than T_n for large n. Every proper-prefix cost is smaller, so all these words are terminal leaves. Hence N(n,t_n)>={n choose j_n}. Equation (14) gives a lower rate at least H(p). Let p increase to p_* to obtain (10).

The argument uses only the limiting threshold exponent. It permits nonmonotone sequences and arbitrary o(n) perturbations of -ln(t_n). Both thresholds in (6) have exponent ln2 whenever -ln(delta_n)/n->ln4. The factor 1+10n contributes zero rate. Equations (6) and (10) therefore prove (2).

## 5. One near-full-area compact initial set for all tolerance sequences

Under normalized Lebesgue measure on [-1,1], natural exact branch digits have probabilities a_0=1/3 and a_1=2/3: the measure of a word interval is lambda_w by (4). Boundary points and their preimages form a countable set. R15 §3.2's elementary binomial estimate and Borel--Cantelli prove that the zero frequency tends to 1/3 almost everywhere.

Egorov and inner regularity now give one compact E_epsilon contained in (-1,1), avoiding all these boundary points, such that
\[
|E_\varepsilon|>2(1-\varepsilon)
\]
and the zero-frequency convergence is uniform on E_epsilon. This choice is made before any tolerance sequence. Define the actual compact set
\[
K_\varepsilon=\{(s,sy):0\le s\le1,\ y\in E_\varepsilon\}. \tag{15}
\]
It includes the vertex. The physical Jacobian is s, so its area is |E_epsilon|/2>1-epsilon. It has empty interior: preimages of the dividing point are dense, since the maximum depth-k interval length is 2(2/3)^k, and E_epsilon avoids them.

### 5.1 Exact prefixes provide the upper bound

For every eta>0 and sufficiently large n, each actual natural prefix appearing on E_epsilon has zero frequency within eta of 1/3. Its number is at most
\[
(n+1)\exp\left(n\max_{|p-1/3|\le\eta}H(p)\right), \tag{16}
\]
where the maximum is restricted to p in [0,1]. This is (14) summed over the allowable types. Use each such word as an exact length-n prefix of an infinite control. Every assigned point of K_epsilon remains in Q at every time through n. The vertex is feasible for any of them. Thus this catalogue is valid for every positive delta, and by continuity of H,
\[
\limsup_n n^{-1}\ln r(n,\delta_n;K_\varepsilon)\le h. \tag{17}
\]
This upper catalogue covers the whole fixed K_epsilon; it is not a measure-almost-everywhere coverage claim.

### 5.2 The arbitrary-input area bound supplies the matching lower bound

Uniform frequency convergence and (11) give, for every 0<zeta<h, one constant D_zeta>=1 with
\[
D_\zeta^{-1}e^{-(h+\zeta)k}
\le\lambda_{p_k(y)}\le D_\zeta e^{-(h-\zeta)k}
\quad(y\in E_\varepsilon,\ k\ge0). \tag{18}
\]
The finitely many early times are absorbed in the constant. This is a dynamical frequency property, not an assumed covering estimate.

The actual first-deviation band of R15 §3.1, integrated using the physical Jacobian, has area at most 2 delta a_min^{-1} lambda_prefix^{-1} when beta=2. Applying (18) to a common prefix, and summing the resulting geometric progression, reproduces R15 (17) on the fixed actual K_epsilon:
\[
\operatorname{area}(K_\varepsilon\cap V(n,\delta,u))
\le C_\zeta\left[e^{-(h-\zeta)m}+\delta e^{(h+\zeta)m}\right]
\quad(0\le m\le n). \tag{19}
\]
This holds for every input u. Agreement through m occupies one exact interval with area at most D_zeta e^{-(h-zeta)m}. A first difference at j<=m is constrained at that time by the same one-sided band as R15 (10); (18) bounds its prefix product below, and integration cancels the factor 1/s. All later reentry is permitted but cannot remove this earlier necessary condition. Thus (19) also covers initial points arbitrarily close to the vertex.

Because ln4>2h, every tolerance sequence in the theorem satisfies delta_n e^{2hn}<=1 for all sufficiently large n. Take m=n in (19). Every input then covers area at most 2C_zeta e^{-(h-zeta)n}. Any catalogue spanning the positive-area K_epsilon consequently has
\[
r(n,\delta_n;K_\varepsilon)\ge
\frac{\operatorname{area}(K_\varepsilon)}{2C_\zeta}
e^{(h-\zeta)n}. \tag{20}
\]
Let zeta decrease to zero and combine with (17). This proves (3). The set, its frequency property and all constants were fixed before the sequence; only the time from which the bound applies may depend on that sequence. The all-sequence quantifier is therefore proved. Theorem 16.1 is complete. ∎

## 6. Mechanism, inherited methods, and limits

R15's matching balances physical radial shrinkage with inverse angular lengths. It gives one cost for every positive-area compact initial set at lower precision. At the present higher precision, a finite horizon truncates the scale stopping. The full cone must include words whose zero frequency is near p_*, while the fixed near-full-area set has uniformly typical frequency 1/3. Equation (6) prevents arbitrary approximate controls from removing an exponential number of the full-cone witnesses.

These exceptional types can occupy very little angular measure despite their many prefixes: a depth-n type of frequency p has total relative angular length {n choose np} exp(-n chi(p)), at most exp(n[H(p)-chi(p)]). At p=p_*, chi(p_*)=ln2>H(p_*). The uniformly typical compact set excludes a neighborhood of these frequencies for all sufficiently large depths, while retaining arbitrarily nearly full physical area. This explains the coexistence of (2) and (3).

Products, type counts, Egorov, stopped scales and local packing are classical. R06 already used first-deviation witnesses and typical sets for equal-width branches. The project-level increment is their checked transfer to the same unequal-width matching system, with a full-time real-catalogue comparison and a fixed-set all-sequence split. It establishes a substantive limit of R15's sufficient condition; it does not introduce a new thermodynamic formalism.

No proof gap remains in the one stated theorem. The round does not classify other precision exponents or parameters, overlapping/nonlinear systems, or all positive-area initial sets. It does not solve or resume the paused R09--R14 fixed-policy comparison. Publication priority and contribution strength remain separate from the self-contained proof and are assessed in REPORT.md and SOURCES.md. The existing paper is unchanged.
