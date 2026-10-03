# R06: control-dependent contraction and the geometry of precision cost

3 October 2026. Natural logarithms; rates are nat/step. One main theorem is proved below. Its symbolic counting ingredients are classical; the substantive interface is the comparison with catalogues of actual, possibly off-constraint trajectories, and the resulting failure of positive-area universality. No pressure duality, fixed-measure variational principle, or data-rate implementation theorem is claimed.

## 1. System, quantifiers, and one main theorem

Let $0<\rho_0,\rho_1<1/2$. Take the finite control alphabet $U=\{0,1\}$, with $v_0=1$, $v_1=-1$, and all sequences in $U^{\mathbb N_0}$ admissible. On the actual ambient state space $\mathbb R^2$, define the linear, hence $C^\infty$, diffeomorphisms

$$
F_i(s,z)=(\rho_i s,\rho_i(2z+v_i s)),\qquad
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad o=(0,0). \tag{1.1}
$$

Controls change the radial contraction as well as the feasible branch. The coordinate $y=z/s$, used only when $s>0$, is a calculation device, not a replacement of the ambient metric or of the initial-state projection.

For compact $K\subset Q$, let $r(n,\delta;K)$ be the least cardinality of a finite set $C\subset U^{\mathbb N_0}$ such that

$$
\forall x\in K\ \exists u\in C\ \forall k\in\{0,\ldots,n\}:
\operatorname{dist}_2(\varphi(k,x,u),Q)<\delta. \tag{1.2}
$$

Thus there are $n$ input symbols and $n+1$ constrained states. The same positive tolerance is used at every time of one horizon. The assigned actual trajectory is allowed to leave $Q$. Let $r_E(n;K)$ denote the corresponding exact count with membership in $Q$.

Write

$$
\alpha=\ln2,\quad c_i=-\ln\rho_i,\quad
\bar c=(c_0+c_1)/2,\quad c_{\min}=\min_i c_i>\alpha,
$$

and $c_{\max}=\max_i c_i$, $\rho_{\min}=\min_i\rho_i$, $\rho_{\max}=\max_i\rho_i$.

$$
H(p)=-p\ln p-(1-p)\ln(1-p),\qquad
\chi(p)=pc_0+(1-p)c_1,\quad 0\ln0=0,
$$

$$
F(\gamma)=\max_{0\le p\le1}H(p)\min\{1,\gamma/\chi(p)\},\qquad
G(\gamma)=\alpha\min\{1,\gamma/\bar c\}. \tag{1.3}
$$

For $\gamma=\infty$, both minima in (1.3) are interpreted as one.

**Theorem 6.1 (precision spectrum and failure of positive-area universality).** For the system (1.1):

1. $Q$ is controlled invariant. Every trajectory from a bounded set converges to $o$ uniformly over all inputs. For every compact positive-area $K\subset Q$, the exact time limit is $\lim_n n^{-1}\ln r_E(n;K)=\alpha$, while the ordinary outer invariance rate is zero.
2. For every compact $K\subset Q$ with nonempty interior in $\mathbb R^2$, and every sequence $\delta_n>0$ such that $\delta_n\to0$ and $-n^{-1}\ln\delta_n\to\gamma\in[0,\infty]$, the actual limit exists and equals
   $$\lim_{n\to\infty}n^{-1}\ln r(n,\delta_n;K)=F(\gamma). \tag{1.4}$$
3. For every $\varepsilon\in(0,1)$ there is a compact set $K_\varepsilon\subset Q$ of area greater than $(1-\varepsilon)\operatorname{area}(Q)$ such that, for **every** tolerance sequence in part 2, the actual limit instead equals
   $$\lim_{n\to\infty}n^{-1}\ln r(n,\delta_n;K_\varepsilon)=G(\gamma). \tag{1.5}$$
   The set is chosen independently of $\gamma$ and of the tolerance sequence.
4. If $\rho_0\ne\rho_1$, then $F(\gamma)>G(\gamma)$ for every $0<\gamma\le c_{\min}$. The family cannot be simultaneously transformed into the common-first-jet family of R05 by a fixed local $C^1$ diffeomorphism, or even by a fixed local bi-Lipschitz state conjugacy to that smooth family, taking apex to apex and respecting the control labels up to permutation.

The usefulness is a precise boundary on initial-set assumptions: positive area, sufficient for a common precision law in R05, is insufficient after feasible branches carry different contractions. Nonempty interior is sufficient in this class. This is not a statement that every positive-area set without interior has law $G$, nor a characterization of all compact initial sets.

The system class is planar and linear with binary branches and uniform ambient contraction. It is not an unrestricted nonlinear extension of R05. In particular, the binary alphabet here has no strict inward margin, so R05 Theorem 5.1 is not literally being applied to this alphabet.

## 2. Actual dynamics and recovered exact endpoints

For a finite word $w=w_1\cdots w_k$, set

$$
A_w=\prod_{j=1}^k\rho_{w_j},\qquad S(w)=-\ln A_w,
\qquad A_\varnothing=1.
$$

Starting from $(s,sy)$ with $s>0$, the ratios satisfy $y_{j+1}=2y_j+v_{u_j}$ and the radius after the word is $sA_w$. The inverse ratio branches $b_i(y)=(y-v_i)/2$ map $[-1,1]$ onto $[-1,0]$ and $[0,1]$. Consequently the interval

$$
I_w=b_{w_1}\circ\cdots\circ b_{w_k}([-1,1])
$$

has length $2^{1-k}$, and consists exactly of the initial ratios feasible through that word. Length-$k$ intervals partition $[-1,1]$ with disjoint interiors; shared endpoints cause no counting or measure difficulty. This proves controlled invariance, including the fixed apex. It also shows why the fastest control cannot simply be chosen everywhere: away from branch boundaries only one first control is exactly feasible.

Choose $M\ge1$ sufficiently large that

$$
L=\rho_{\max}(2+1/M)<1,
\qquad \|(s,z)\|_M=\max\{M|s|,|z|\}. \tag{2.1}
$$

Both matrices have operator norm at most $L$ in this norm. Therefore arbitrary products contract globally, uniformly over all inputs. Also $\|x\|_2\le\sqrt2\|x\|_M$.

Each exact word covers a cone slice whose area is

$$
\int_0^1 s\,|I_w|\,ds=2^{-n}
$$

at horizon $n$. All $2^n$ words cover $Q$, so for positive-area $K$

$$
\operatorname{area}(K)2^n\le r_E(n;K)\le2^n. \tag{2.2}
$$

For any fixed $\delta>0$, follow an exact prefix of a sufficiently large fixed length $m$. Its endpoint has $M$-norm at most $M\rho_{\max}^m$. Choose this less than $\delta/(2\sqrt2)$ and append any fixed input tail. Equation (2.1) keeps that entire tail in the $\delta$-ball about $o$. Thus $r(n,\delta;Q)\le2^m$ for all $n\ge m$, proving the ordinary outer rate zero. These exact/outer endpoints are recovered ingredients, not the R06 novelty claim.

## 3. Decisive interface: stopping prefixes versus true catalogues

For an integer $n\ge1$ and $0<t<1$, stop each binary path at the first prefix $w$ for which $A_w\le t$, or at depth $n$ if that has not happened earlier. Let $\mathcal L(n,t)$ be this complete prefix-free set of leaves and $N(n,t)=|\mathcal L(n,t)|$. Set $N(0,t)=1$ when needed. For $n\ge1$, every leaf satisfies

$$
A_{w^-}>t,\qquad A_w>\rho_{\min}t,\qquad |w|\le n. \tag{3.1}
$$

Leaves of depth less than $n$ have $A_w\le t$. The dyadic intervals of all leaves, including terminal leaves, cover $[-1,1]$ and have disjoint interiors.

### 3.1 Upper bound, including the entire tail

Put $C_0=2\sqrt2M$. For each leaf of $\mathcal L(n,\delta/C_0)$ use its exact prefix and append a fixed tail. If it stops before $n$, the endpoint has norm at most $M\delta/C_0=\delta/(2\sqrt2)$; (2.1) keeps every subsequent actual state within Euclidean distance $\delta/2$ of $o\in Q$. A leaf reaching depth $n$ is already exactly feasible for the whole horizon. Hence, for all sufficiently small $\delta$,

$$
r(n,\delta;K)\le r(n,\delta;Q)\le N(n,\delta/C_0). \tag{3.2}
$$

No feedback choice during a tail and no approximation of initial states is hidden in this catalogue.

### 3.2 Lower bound: an off-constraint word covers only $O(n)$ witnesses

Fix a radius $s_*\in(0,1]$ and use leaves of $\mathcal L(n,t)$ with $t=\delta/s_*<1$. For each leaf $w$ choose its midpoint $y_w\in I_w$ and the actual point $x_w=(s_*,s_*y_w)$.

Any state with radius $r\ge0$ in $Q^\delta$ satisfies

$$
|z|<r+2\delta. \tag{3.3}
$$

Indeed a point $(r',z')\in Q$ within Euclidean distance $\delta$ has $|r-r'|<\delta$, $|z-z'|<\delta$ and $|z'|\le r'$.

Consider any length-$n$ input word $u$, without requiring it to be exactly feasible. At most one leaf is a prefix of $u$. For every other leaf witness covered by $u$ in the sense of (1.2), let $j\le |w|$ be the first position where $u$ and $w$ differ, and let $a=u_1\cdots u_{j-1}$. The midpoint $b_a$ of $I_a$ separates its two children. Since $y_w$ lies in the opposite child from $u_j$, application of the wrong branch gives

$$
|y_j|-1=2^j|y_w-b_a|.
$$

The actual radius at this time is $s_*A_a\rho_{u_j}$. By (3.3), the witness must lie in a one-sided band of width at most

$$
b_j=\frac{2\delta}{s_*2^j A_a\rho_{\min}}. \tag{3.4}
$$

Every leaf in that opposite child has length bounded below by

$$
|I_w|=|I_a|2^{-(|w|-|a|)}
\ge |I_a|\frac{A_w}{A_a}
>\frac{2^{2-j}\rho_{\min}\delta}{s_* A_a}
=:\ell_j. \tag{3.5}
$$

Here the first inequality uses each $\rho_i<1/2$ and the second uses (3.1). For disjoint-interior intervals of lengths at least $\ell_j$, their midpoints are separated by at least $\ell_j$. Thus at most $1+b_j/\ell_j\le1+(2\rho_{\min}^2)^{-1}$ such witnesses can lie in the band (3.4). Summing over $j=1,\ldots,n$, there is a constant $B$ depending only on $\rho_0,\rho_1$ such that one actual input word covers at most $1+Bn$ leaf witnesses.

In particular, taking $s_*=1$ gives

$$
\frac{N(n,\delta)}{1+Bn}\le r(n,\delta;Q)
\le N(n,\delta/C_0). \tag{3.6}
$$

This is the main control-geometric step. It does not assume that approximate controls follow the natural coding. It explicitly bounds their possible advantage by looking at their first wrong feasible branch.

### 3.3 Every initial set with interior contains a full descendant tree

If $K$ has nonempty interior, choose $s_*>0$ and a fixed dyadic interval $I_a$ such that the whole segment $\{(s_*,s_*y):y\in I_a\}$ lies in $K$. An open ball inside $K\subset Q$ supplies a segment with fixed positive $s$, and a sufficiently small dyadic interval lies inside its ratio interval.

Let $d=|a|$. For small enough $\delta$, $t=\delta/s_*<A_a$. The leaves of $\mathcal L(n,t)$ descending from $a$ are precisely $a$ followed by the leaves of $\mathcal L(n-d,t/A_a)$. All their witnesses lie in $K$. The same first-mismatch bound applies even when $u$ disagrees with $a$, and yields

$$
\frac{N(n-d,\delta/(s_*A_a))}{1+Bn}
\le r(n,\delta;K)\le N(n,\delta/C_0) \tag{3.7}
$$

for $n\ge d$ and sufficiently small $\delta$. All constants and the prefix $a$ are independent of $n$ and of the tolerance sequence.

## 4. Complete asymptotic count of the stopped tree

We prove directly that, for every $t_n\to0$ with $T_n=-\ln t_n$ and $T_n/n\to\gamma\in[0,\infty]$,

$$
\lim_{n\to\infty}\frac{\ln N(n,t_n)}n=F(\gamma). \tag{4.1}
$$

This is an elementary finite-alphabet type calculation, not a new pressure theorem. For a word of length $k$ with $j$ zeros and $p=j/k$, its cost is $k\chi(p)$ and there are $\binom{k}{j}$ such words. The standard binomial bounds are

$$
\frac{e^{kH(j/k)}}{k+1}\le\binom{k}{j}\le e^{kH(j/k)}. \tag{4.2}
$$

For completeness, apply the binomial distribution with parameter $p=j/k$. The mass at $j$ is $\binom{k}{j}e^{-kH(p)}$, at most one. It is a mode (the ratio of adjacent masses verifies this), so its mass is at least $1/(k+1)$. The endpoint cases $j=0,k$ are immediate. This proves (4.2).

Suppose first $0<\gamma<\infty$. A leaf stopping at depth $k<n$ has

$$
T_n\le k\chi(j/k)<T_n+c_{\max}, \tag{4.3}
$$

whereas every terminal leaf of depth $n$ has $n\chi(j/n)<T_n+c_{\max}$. There are at most $(n+1)^2$ choices of length and type. For an upper bound, sum (4.2) over these eligible types, even if some of their words are not leaves. Along a maximizing subsequence set $k/n\to a$ and $j/k\to p$. In the stopped case, (4.3) implies $a\chi(p)=\gamma$ and the normalized log count is at most $aH(p)$. In the terminal case $a=1$ and $\chi(p)\le\gamma$, giving at most $H(p)$. Both bounds are at most $F(\gamma)$. Compactness supplies such subsequences; the polynomial number of types contributes $o(1)$ after dividing the logarithm by $n$.

For the lower bound fix $p\in[0,1]$ and $0<a<\min\{1,\gamma/\chi(p)\}$. At depth $k_n=\lfloor an\rfloor$, choose $j_n/k_n\to p$. For large $n$, every word of that type has total cost less than $T_n$. Its prefixes have smaller costs, so it has not stopped. Distinct such words have disjoint sets of descendant leaves. Consequently

$$
N(n,t_n)\ge\binom{k_n}{j_n},\qquad
\liminf_n n^{-1}\ln N(n,t_n)\ge aH(p).
$$

Let $a$ increase to the displayed minimum, and then maximize over $p$. This proves (4.1), including equality cases in the threshold without any arithmetic assumption on $c_0/c_1$.

If $\gamma=0$, every leaf stops by depth at most $\lceil T_n/c_{\min}\rceil+1$, or by the earlier horizon. Therefore $1\le N(n,t_n)\le2^{\min\{n,\lceil T_n/c_{\min}\rceil+1\}}$, giving zero rate. If $\gamma=\infty$, eventually $T_n>nc_{\max}$, so no path stops early and $N(n,t_n)=2^n$.

Fixed multiplicative changes to $t_n$ and a fixed change of the horizon do not change the limiting exponent $\gamma$ or (4.1). Applying this observation to (3.7) proves (1.4), for arbitrary sequences with the stated exponent, without monotonicity assumptions.

## 5. Arbitrarily large-area compact sets with a smaller law

### 5.1 A uniformly typical compact ratio set

For a non-dyadic $y\in(-1,1)$ let its natural feasible coding be $i_1(y)i_2(y)\cdots$. Under normalized Lebesgue measure on $[-1,1]$, these digits are independent and take each value with probability $1/2$, because each length-$k$ cylinder has measure $2^{-k}$. Thus

$$
\frac{S_k(y)}k:=\frac1k\sum_{j=1}^k c_{i_j(y)}\longrightarrow\bar c
\quad\text{for Lebesgue-almost every }y. \tag{5.1}
$$

One elementary justification is the Chernoff bound for the number of zeros: its moment generating function gives probability at most $2e^{-2k\eta^2}$ of a deviation greater than $\eta$ from frequency $1/2$. This follows from $\cosh t\le e^{t^2/2}$ and optimization in $t$. Summability and Borel–Cantelli for $\eta=1/m$, $m\ge1$, prove (5.1). Removing the countable dyadic set does not change the measure.

By Egorov's theorem and inner regularity of Lebesgue measure, for any prescribed arbitrarily small loss of measure there is a compact $E\subset(-1,1)$, containing no dyadic points, on which (5.1) is uniform. These standard measure-theoretic existence theorems impose no desired covering rate. For every $\zeta>0$, uniform convergence and the finitely many early times imply a constant $C_\zeta\ge1$ such that

$$
C_\zeta^{-1}e^{-(\bar c+\zeta)k}
\le A_k(y)\le C_\zeta e^{-(\bar c-\zeta)k}
\quad(y\in E,\ k\ge0). \tag{5.2}
$$

Choose $s_0\in(0,1)$ and put

$$
K_E=\{(s,sy):s_0\le s\le1,\ y\in E\}. \tag{5.3}
$$

This is compact, and the Jacobian of $(s,y)\mapsto(s,sy)$ is $s$, so its area is $(1-s_0^2)|E|/2$. Taking $s_0^2<\varepsilon/2$ and $|E|>2(1-\varepsilon/2)$ gives area greater than $1-\varepsilon$, while $\operatorname{area}(Q)=1$. Its interior is empty: every ratio interval contains a dyadic point absent from $E$.

### 5.2 Upper bound using actual feasible prefixes

Fix $0<\zeta<\bar c-\alpha$. At depth $m$ there are at most $2^m$ natural prefixes meeting $E$. Use them as the exact prefix catalogue for $K_E$. By (5.2), every assigned endpoint has norm at most $MC_\zeta e^{-(\bar c-\zeta)m}$. With $T=-\ln\delta$, choose

$$
m=\min\left\{n,\left\lceil
\frac{T+\ln(2\sqrt2MC_\zeta)}{\bar c-\zeta}
\right\rceil\right\}. \tag{5.4}
$$

If $m<n$, append any fixed tail; (2.1) bounds every tail state by $\delta/2$ in Euclidean distance from $o$. If $m=n$, the catalogue is exact for the required horizon. Therefore

$$
\limsup_n n^{-1}\ln r(n,\delta_n;K_E)
\le\alpha\min\{1,\gamma/(\bar c-\zeta)\}. \tag{5.5}
$$

### 5.3 Uniform lower bound for every approximate input

Let $u$ be an arbitrary length-$n$ word and fix $s\in[s_0,1]$. Among ratios in $E$ whose actual states under $u$ satisfy (1.2), consider any $m\le n$. Those agreeing with $u$ through position $m$ lie in a single interval of length $2^{1-m}$. All remaining covered ratios first disagree at some $j\le m$.

At that first disagreement the prefix $a=u_1\cdots u_{j-1}$ is still the natural feasible one. Equation (5.2) bounds $A_a$ below uniformly. The same wrong-branch calculation (3.3)–(3.4), with $s\ge s_0$, places such ratios in a one-sided band of length at most

$$
C'_{\zeta,s_0}\delta\,2^{-j}e^{(\bar c+\zeta)(j-1)}.
$$

There is only one band for each $j$ and fixed $u$, regardless of how many points it covers. Summing this geometric progression, using $\bar c+\zeta>\alpha$, shows that the length of all covered ratios in $E$ is at most

$$
C''_{\zeta,s_0}\left[2^{-m}
 +\delta e^{(\bar c+\zeta-\alpha)m}\right]. \tag{5.6}
$$

This bound is uniform in $s,u,n,m,\delta$. The ratio sets may depend on $s$, but integrating their lengths against $s\,ds$ gives the same bound, up to a constant, for the actual area of $K_E$ covered by this input. All finite-time constraint sets are Borel by continuity, so Fubini applies.

For $\delta<1$ choose

$$
m=\min\{n,\lfloor T/(\bar c+\zeta)\rfloor\}. \tag{5.7}
$$

Then $\delta e^{(\bar c+\zeta)m}\le1$, and (5.6) is at most a constant times $2^{-m}$. Positive area of the fixed $K_E$ now implies

$$
r(n,\delta;K_E)\ge b_{\zeta,K_E}2^m,
\qquad
\liminf_n n^{-1}\ln r(n,\delta_n;K_E)
\ge\alpha\min\{1,\gamma/(\bar c+\zeta)\}. \tag{5.8}
$$

The cases $m=0$, $\gamma=0$, and $\gamma=\infty$ obey the same bounds. Letting $\zeta\downarrow0$ in (5.5) and (5.8) proves (1.5) for this single set and all tolerance sequences in the theorem. This proof never restricts the optimizing catalogue to natural codes.

## 6. Strict difference and impossibility of a fixed regular coordinate reduction

Let $D>0$ solve $\rho_0^D+\rho_1^D=1$. With $p_* =\rho_0^D$ and $1-p_* =\rho_1^D$, nonnegativity of relative entropy gives

$$
D\chi(p)-H(p)
=p\ln\frac p{p_*}+(1-p)\ln\frac{1-p}{1-p_*}\ge0,
$$

with equality at $p=p_*$. Hence $\max_p H(p)/\chi(p)=D$. This is a classical entropy/similarity-dimension identity, not an R06 priority claim. For $0\le\gamma\le c_{\min}$,

$$
F(\gamma)=D\gamma,\qquad G(\gamma)=\frac\alpha{\bar c}\gamma. \tag{6.1}
$$

If $c_0\ne c_1$, strict AM–GM gives

$$
\rho_0^{\alpha/\bar c}+\rho_1^{\alpha/\bar c}
>2\exp\left(-\frac\alpha{\bar c}\frac{c_0+c_1}{2}\right)=1.
$$

The left side decreases strictly with its exponent, so $D>\alpha/\bar c$. This proves the strict gap. Both spectra equal $\alpha$ for $\gamma\ge\bar c$, because $H(1/2)=\alpha$ and $H(p)\le\alpha$.

For example, take $\rho_0=1/4$, $\rho_1=1/16$ and $\delta_n=2^{-n}$. If $\phi=(1+\sqrt5)/2$, then $D=\ln\phi/\ln4$, since $\phi^{-1}+\phi^{-2}=1$. Therefore

$$
\lim_n\frac{\ln r(n,2^{-n};Q)}n=\frac{\ln\phi}{2}
\quad>\quad
\lim_n\frac{\ln r(n,2^{-n};K_\varepsilon)}n=\frac{\ln2}{3}. \tag{6.2}
$$

The inequality follows exactly from $\phi^3=2\phi+1>4$, not from a numerical experiment. Both initial sets have exact rate $\ln2$ and ordinary outer rate zero. The gap is visible only when precision and horizon vary together. Moreover the nearly full-area examples have the same law as the common-contraction rate with $c=\bar c$, while the whole cone has a strictly higher low-precision slope.

To exclude a coordinate relabeling, note first that $DF_i(o)$ has eigenvalues $\rho_i,2\rho_i$. In the common-first-jet model of R05, each control derivative at the apex has the same pair $\rho,\rho q$. A fixed $C^1$ coordinate change conjugates every derivative by the same invertible matrix, so the unequal pairs here cannot become those common pairs.

The obstruction also holds for a local bi-Lipschitz state conjugacy to a $C^1$ target family. We give the needed argument rather than assuming differentiability of the conjugacy. If a contracting linear map $A$ is locally conjugate by a bi-Lipschitz $h$, $h(0)=0$, to a $C^1$ map $g$, then

$$
\operatorname{spr}(Dg(0))=\operatorname{spr}(A). \tag{6.3}
$$

Choose an $A$-invariant small ball in an adapted norm on which the conjugacy holds. On its image, $g^k=hA^kh^{-1}$ has Lipschitz constant at most a fixed constant times $\|A^k\|$. Its derivative at zero is $(Dg(0))^k$, so the spectral-radius formula gives $\operatorname{spr}(Dg(0))\le\operatorname{spr}(A)<1$. Conversely, for each small $\eta>0$, an adapted norm and continuity of $Dg$ give a small invariant ball on which $g$ is Lipschitz with constant at most $\operatorname{spr}(Dg(0))+\eta<1$. Apply $h^{-1}g^kh$ to points in its preimage and use the bi-Lipschitz constants. This bounds $\|A^kx\|$ by a fixed constant times $[\operatorname{spr}(Dg(0))+\eta]^k\|x\|$ near zero. Linearity of $A^k$ extends the bound to its operator norm. Taking $k$th roots and then $\eta\downarrow0$ proves (6.3).

Apply (6.3) separately to the two labels. Their spectral radii are $2\rho_0\ne2\rho_1$, whereas the smooth R05 family has common spectral radius $\rho q$. Simultaneous reduction is impossible. This argument concerns regular changes of the actual state coordinates; arbitrary singular homeomorphisms need not preserve positive area or exponential precision and are not claimed to be excluded. It completes Theorem 6.1.

## 7. What remains outside the theorem

The R05 proof was rechecked at the four interfaces actually needed here: all-time constraints, tolerance depending on the horizon, uniform lower section bounds, and an exact prefix followed by a controlled tail. No correction of R05 was required. Its common radial estimate cannot simply be carried over to (1.1); the replacement is the first-mismatch estimate and the contraction-weighted stopping tree.

The construction is distinct from the R04 countable/atomic initial-set obstruction: $K_\varepsilon$ has arbitrarily nearly full two-dimensional area; there is no fixed-probability variational assertion to refute. Nor is (1.4) inferred from a bare abstract lift. Every lower-bound witness and every upper-bound prefix has its actual state projection and ambient constraint checked.

All branch contractions being less than $1/2$ is used twice: arbitrary tails contract in (2.1), and dyadic cylinder length dominates the contraction product in (3.5). The formula is not established after dropping that restriction. For example the same binary cone with $(\rho_0,\rho_1)=(3/4,1/4)$ still has contracting radii and exact feasible coding, but the present proof does not determine $\lim_n n^{-1}\ln r(n,2^{-n};Q)$. Equation (3.5) can fail along descendants containing many zero symbols, and an arbitrary tail no longer contracts. That is one precise possible next problem, not a second attempted theorem or a claimed counterexample in this round.

No robustness under nonlinear perturbations, overlapping feasible branches, classification for every positive-area initial set, or larger-journal significance follows from this proof. Publication priority and the strength of this bounded mechanism result are assessed separately in REPORT.md and SOURCES.md.
