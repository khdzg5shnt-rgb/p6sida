# R05: a tolerance–horizon law on the nonlinear forward cone

3 October 2026. Natural logarithms; rates are nat/step. This is one bounded proof advance within route A. It keeps the actual initial states, all controlled transitions, and the Euclidean ambient metric. It is not a formula from an abstract lift or a measure/pressure duality.

The new result is Theorem 5.1 below. Its exact-entropy ingredient already occurs in the original manuscript; §2 rederives that ingredient rather than assuming the R01 audit correct. The tolerance sequence and its complete rate law are new to the project. Priority and publication assessment are separate questions, recorded in REPORT.md and SOURCES.md.

## 1. Complete assumptions, counts and statement

Let q>1, let U be a nonempty finite subset of R, and suppose that for some η>0

$$
\forall y\in[-1,1]\ \exists v\in U:\quad |qy+v|\leq1-2\eta. \tag{1.1}
$$

All inputs in $U^{\mathbb N_0}$ are admissible. Let R:R→R be an increasing C∞ diffeomorphism with R(0)=0 and 0<R(s)<s for 0<s≤1. Set ρ=R′(0)∈(0,1], t(s)=R(s)/s for s≠0 and t(0)=ρ. For each v∈U let P_v:R²→R be C∞, with P_v(0,0)=0 and DP_v(0,0)=0, and assume

$$
\kappa:=\max_{v\in U}\sup_{x\in\mathbb R^2}
 \max\{|P_v(x)|,\|DP_v(x)\|,\|D^2P_v(x)\|\}
 <\min\{\eta,q/2\}. \tag{1.2}
$$

Derivative norms are Euclidean operator norms. Define

$$
f_v(s,z)=\left(R(s),t(s)[qz+sv+P_v(s,z)]\right),\qquad
Q=\{(s,z):0\leq s\leq1,\ |z|\leq s\},\quad p=(0,0). \tag{1.3}
$$

Let φ be the forward solution under these maps. For a compact K⊂Q of positive two-dimensional Lebesgue measure and δ>0, put

$$
Q^\delta=\{x:\operatorname{dist}_2(x,Q)<\delta\},
$$

$$
r(n,\delta;K)=\min\left\{|C|: C\subset U^{\mathbb N_0}\text{ finite},
\ \forall x\in K\ \exists u\in C\
\forall k\in\{0,\ldots,n\}: \varphi(k,x,u)\in Q^\delta\right\}. \tag{1.4}
$$

There are n control symbols and n+1 constrained states. The same tolerance δ is used at every time in a given horizon n. It is allowed to change when n changes. The actual trajectories in (1.4) may leave Q.

Write r_E(n;K) for the same count with exact Q in place of Q^δ. Finite U and controlled invariance ensure all these counts are finite. Minima may be taken over length-n prefixes.

**Theorem 5.1 (complete tolerance–horizon law).** Under (1.1)–(1.3), for every compact positive-area K⊂Q and every positive sequence δ_n with δ_n→0 and

$$
\lim_{n\to\infty}\frac{-\ln\delta_n}{n}=\gamma\in[0,\infty],
$$

the following actual time limit exists:

$$
\lim_{n\to\infty}\frac{\ln r(n,\delta_n;K)}n
=\Psi_{\alpha,c}(\gamma)
:=\max_{0\leq a\leq1}\{a\alpha-(ac-\gamma)_+\},
\qquad \alpha=\ln q,\quad c=-\ln\rho. \tag{1.5}
$$

For γ=∞ the positive-part term is understood as zero. Equivalently,

$$
\Psi_{\alpha,c}(\gamma)=
\begin{cases}
\alpha,&c=0,\\
\min\{\alpha,\alpha-c+\gamma\},&0<c\leq\alpha,\\
\alpha\min\{1,\gamma/c\},&c>\alpha.
\end{cases} \tag{1.6}
$$

This includes γ=0, γ=c and the critical case ρq=1. In particular, every vanishing subexponential tolerance has rate (α−c)_+, and every tolerance with decay exponent γ≥c has the exact rate α. No monotonicity of δ_n is needed.

The theorem concerns ambient constraint tolerance, not trajectory tracking with shrinking tolerance. For the latter, approximating the initial states at time zero would already impose an additional covering cost; no tracking analogue of (1.5) is asserted.

## 2. Independently recovered ingredients from the original

### 2.1 Smoothness, viability and radial estimates

The identity t(s)=∫₀¹R′(θs)dθ makes t smooth and positive. For a fixed s and v, the map z↦qz+sv+P_v(s,z) has derivative at least q−κ>0 and tends to the respective infinities as z→±∞. It is a bijection with smooth inverse. First recovering s=R^{-1}(s′), and then this inverse, proves that f_v is a global smooth diffeomorphism.

Taylor's formula gives

$$
|P_v(s,sy)|\leq\kappa s^2\quad(0<s\leq1,\ |y|\leq1),
\qquad |\partial_zP_v(s,z)|\leq\kappa\sqrt{s^2+z^2}. \tag{2.1}
$$

The second inequality follows by integrating D²P_v from the origin; also |∂_zP_v|≤κ globally. At positive radius, s_k=R^k(s) and

$$
y_{k+1}=qy_k+u_k+P_{u_k}(s_k,s_ky_k)/s_k. \tag{2.2}
$$

Choose u_k by (1.1). The last term has absolute value at most κs_k≤κ<η, so |y_{k+1}|≤1−η. The apex is fixed for every input. Thus Q is controlled invariant. Every finite viable prefix can be extended in Q, and every viable time-k state lies in R^k(1)Q.

The decreasing sequence R^n(1) has a fixed-point limit, necessarily zero. Monotonicity makes this convergence a uniform bound for all initial radii in [0,1]. For 0<ξ<ρ,

$$
\frac{R^k(s)}s\leq C_\xi(\rho+\xi)^k\quad(0<s\leq1),
\qquad
\frac{R^k(s)}s\geq d_{\xi,s_0}(\rho-\xi)^k
\quad(s_0\leq s\leq1). \tag{2.3}
$$

Indeed R(r)/r→ρ at zero, all radii enter a fixed small interval after one common finite time, and the product of these ratios gives (2.3). The finite initial products extend continuously at zero for the upper bound; on [s₀,1] their minimum is positive for the lower bound. Constants do not depend on k, the input, or δ_n.

### 2.2 Exact upper rate on the whole cone

Fix a block length N. Cover [-1,1] by at most C_ηq^N intervals of radius (η/4)q^{-N}, with centers in [-1,1] and C_η independent of N. From each center choose a length-N unperturbed word using (1.1) at each step; its positive-time reference ratios lie in [-1+2η,1−2η].

Choose a_N>0 with κa_N∑_{j=0}^{N−1}q^j≤η/4. If the initial radius is at most a_N, applying the word of a nearby center to (2.2) gives, as long as the perturbed ratios are feasible,

$$
|y_k-c_k|\leq q^k(\eta/4)q^{-N}
             +\kappa a_N\sum_{j=0}^{k-1}q^j
\leq\eta/2,\qquad 0\leq k\leq N.
$$

Induction justifies its own premise: at every positive step the reference has margin 2η and the error is at most η/2. These same finite words therefore work for every radius ≤a_N.

Choose N₀ with R^{N₀}(1)≤a_N. All |U|^{N₀} words give a finite catalogue for this transient; viability guarantees a suitable word for each initial state. Afterward concatenate the block catalogue, since radii keep decreasing. A prefix of the last block handles the remainder. Hence, for n≥N₀,

$$
r_E(n;Q)\leq |U|^{N_0}(C_\eta q^N)^{\lceil(n-N_0)/N\rceil}.
$$

Its upper exponential rate is ≤ln q+N^{-1}ln C_η. Let N→∞:

$$
\limsup_{n\to\infty}n^{-1}\ln r_E(n;Q)\leq\alpha. \tag{2.4}
$$

In particular, for each e>0 there is D_e<∞ such that r_E(m;Q)≤D_e exp[(α+e)m] for every integer m≥0. This follows from (2.4), absorbing finitely many horizons into D_e.

### 2.3 Exact lower rate and the role of positive area

For a fixed radius s>0 and a word, all vertical solution maps are strictly increasing. The initial z-values feasible in Q through time n form an interval. On it, the chain rule gives

$$
\partial_z Z_n(s,z,u)=\frac{R^n(s)}s
 \prod_{j=0}^{n-1}[q+\partial_zP_{u_j}(s_j,z_j)]. \tag{2.5}
$$

Along feasible states |z_j|≤s_j≤R^j(1)→0. For any 0<ζ<q−1, all factors after one uniform finite time are ≥q−ζ; earlier factors are ≥q−κ. Thus the derivative in (2.5) is ≥A_ζ[R^n(s)/s](q−ζ)^n. Its final image has length ≤2R^n(s), so the initial interval has length ≤2s A_ζ^{-1}(q−ζ)^{-n}. Fubini bounds the area covered by one word by a constant times (q−ζ)^{-n}. Covering positive-area K requires ≥B_{K,ζ}(q−ζ)^n words. Let ζ↓0 and combine with (2.4):

$$
\lim_{n\to\infty}n^{-1}\ln r_E(n;K)
=\lim_{n\to\infty}n^{-1}\ln r_E(n;Q)=\alpha. \tag{2.6}
$$

This is the recovered original result, not an R05 novelty claim. It fails as a uniform conclusion for arbitrary zero-area K, for example K={p}.

## 3. New lower bound: test every intermediate time

Choose s₀>0 such that K₀=K∩{s≥s₀} has positive area. Such a truncation exists because {s=0} has zero area.

Fix n and a word of length n. At a fixed initial radius s∈[s₀,1], let J_{n,s,u} be the initial z-values in [-s,s] whose actual trajectory lies in Q^{δ_n} through all times 0,…,n. It is an interval, possibly empty or a singleton: Q^{δ_n} is convex, its vertical sections are intervals, and every Z_j is strictly increasing. This also ensures that the derivative estimate is valid between any two of its points.

An outer-feasible state at time j satisfies

$$
|z_j|<s_j+2\delta_n. \tag{3.1}
$$

To see this, choose a point (r,w)∈Q within δ_n of it. Then |s_j−r|<δ_n, |z_j−w|<δ_n and |w|≤r.

For any fixed 0<ζ<q−1, choose d>0 with κ√10 d<ζ. Take N_ζ with R^{N_ζ}(1)≤d, and then n large enough that δ_n≤d. For j≥N_ζ, (3.1) gives s_j≤d, |z_j|≤3d, so |∂_zP_{u_j}|≤κ√10 d<ζ. Earlier factors are bounded below by q−κ globally. Therefore a constant A_ζ>0, independent of n, s and the word, gives for every 0≤k≤n

$$
\partial_z Z_k(s,z,u)\geq
A_\zeta\frac{R^k(s)}s(q-\zeta)^k
\quad\text{on }J_{n,s,u}. \tag{3.2}
$$

At time k its image lies in a vertical interval of length at most 2R^k(s)+4δ_n. Integration of (3.2), and then the radial lower bound (2.3), yield

$$
|J_{n,s,u}|
\leq C_{\zeta,\xi,s_0}(q-\zeta)^{-k}
      [1+C_{\xi,s_0}\delta_n(\rho-\xi)^{-k}]. \tag{3.3}
$$

Open endpoints do not change the bound: apply the mean-value inequality to any two points and take their supremal separation. The finite-time feasible sets are Borel. Fubini over s₀≤s≤1, and the positive area of K₀, imply for all 0≤k≤n

$$
r(n,\delta_n;K)\geq
\frac{B_{\zeta,\xi,K}(q-\zeta)^k}
 {1+C_{\xi,s_0}\delta_n(\rho-\xi)^{-k}}. \tag{3.4}
$$

All constants are independent of n and k. This is an all-time analytic bound, not a finite numerical check.

For finite γ and any a∈[0,1], choose k=⌊an⌋. Since −ln δ_n/n→γ,

$$
\frac1n\ln[1+C_{\xi,s_0}\delta_n(\rho-\xi)^{-k}]
\longrightarrow (a[-\ln(\rho-\xi)]-\gamma)_+.
$$

Thus (3.4), followed by ζ↓0 and ξ↓0, proves

$$
\liminf_n n^{-1}\ln r(n,\delta_n;K)
\geq a\alpha-(ac-\gamma)_+.
$$

Take the maximum over a. For γ=∞ use k=n: δ_n(ρ−ξ)^{-n}→0, giving the lower bound α after ζ↓0. This establishes the lower side of (1.5), including ρ=1 and γ=0.

## 4. New upper bound: a feasible prefix followed by an arbitrary tail

The key point is that constraint tolerance is not shrinking tracking accuracy. No exponentially fine initial reference net is required here.

Assume first ρ<1. Fix a_r∈(ρ,1). In any fixed norm, all states feasible through time m have norm ≤C a_r^m by (2.3). At the common fixed apex,

$$
Df_v(p)=\begin{pmatrix}\rho&0\\ \rho v&\rho q\end{pmatrix}.
$$

For every L>ρq choose M≥1 sufficiently large. In the norm ‖(s,z)‖_M=max{M|s|,|z|}, the displayed matrices have operator norm at most ρq+ρmax_v|v|/M<L. Continuity of the derivatives and finiteness of U then give one convex ball around p on which every f_v is L-Lipschitz. Euclidean norm is at most √2 times this norm.

Take a minimal exact horizon-m catalogue for Q, and append to each of its words an arbitrary tail, for example a fixed repeated symbol. Every assigned actual trajectory is feasible through time m. At time m it has norm ≤C a_r^m. Since every f_v fixes p, its tail states satisfy

$$
\|\varphi(k,x,u)\|_M\leq C a_r^m L^{k-m},\qquad m\leq k\leq n, \tag{4.1}
$$

whenever the right-hand side is sufficiently small. This implication is justified by induction: if all bounds are smaller than the ball radius, the next Lipschitz application remains inside that same ball. In the choices below the bounds are ≤δ_n/(2√2), which tends to zero. Thus their Euclidean distance from p is ≤δ_n/2<δ_n, and those states lie in Q^{δ_n}, since p∈Q. Earlier states were already exactly feasible.

If L>1 choose

$$
m_n=\max\left\{N,\
\left\lceil\frac{n\ln L+\ln(2\sqrt2 C/\delta_n)}
 {\ln L-\ln a_r}\right\rceil\right\}. \tag{4.2}
$$

N is a fixed transient large enough for the local ball. When m_n≥n, use the exact horizon-n catalogue instead. Otherwise (4.1) is maximized at k=n and is ≤δ_n/(2√2). Using (2.4), and letting its e↓0,

$$
\limsup_n n^{-1}\ln r(n,\delta_n;K)
\leq\alpha\min\left\{1,\frac{\gamma+\ln L}{\ln L-\ln a_r}\right\}. \tag{4.3}
$$

If 0<L≤1, choose instead

$$
m_n=\max\left\{N,\
\left\lceil\frac{\ln(2\sqrt2 C/\delta_n)}{-\ln a_r}\right\rceil\right\}, \tag{4.4}
$$

again using the exact catalogue if m_n≥n. Now the maximum of (4.1) is at k=m_n, so

$$
\limsup_n n^{-1}\ln r(n,\delta_n;K)
\leq\alpha\min\{1,\gamma/[-\ln a_r]\}. \tag{4.5}
$$

These estimates also cover m_n/n→0: the uniform bound D_e exp[(α+e)m] established after (2.4) avoids any invalid replacement of a sublinear horizon by n.

If ρq>1, let L↓ρq and a_r↓ρ in (4.3). The denominator tends to α, giving min{α,α−c+γ}. If ρq=1, let L↓1 from above; c=α and (4.3) gives min{α,γ}. If ρq<1, take ρq<L<1 and let a_r↓ρ in (4.5), giving αmin{1,γ/c}.

When ρ=1, exact catalogues already give upper rate α for any δ_n. The lower bound in §3 is α, so this case is complete as well. For γ=∞ the same exact upper bound suffices. Upper and lower bounds agree, proving the actual limit in Theorem 5.1.

To obtain (1.6) directly from (1.5), split the maximization at a=γ/c when c>0. Before that point the expression is aα; after it the expression is a(α−c)+γ. Its maximum is at a=1 if α≥c, and at a=min{1,γ/c} if α<c.

## 5. Interpretation, explicit instances and scope

The endpoints agree with the recovered exact rate α and the original outer rate (α−c)_+. The new statement controls the whole diagonal limit, including arbitrary vanishing subexponential tolerances. Ordinary outer entropy takes the time limit at fixed δ first; Theorem 5.1 does not silently replace that definition.

For q=2, U={−3/2,0,3/2}, η=1/8, and

$$
P_v(s,z)=e_v\tanh(s)\tanh(z),\qquad\max_v|e_v|<1/64,
$$

(1.1)–(1.2) hold: the function and gradient are bounded and its Hessian norm is ≤3; the conservative bound 4max|e_v|<1/16 suffices. Nonzero coefficients give genuinely nonlinear controlled maps.

* R(s)=s/4: c=ln4>α=ln2, so Ψ(γ)=min{ln2,γ/2}.
* R(s)=3s/4: 0<c=ln(4/3)<α, so Ψ(γ)=min{ln2,ln(3/2)+γ}.
* R(s)=arsinh(s): c=0, so Ψ(γ)=ln2 for every γ≥0.

In the first instance, δ_n=2^{-n} has γ=ln2 and rate (ln2)/2. Looking only at the terminal time would give the weaker lower bound max{0,ln(1/2)+γ}=0. The controlling lower-bound time is approximately n/2. This exposes a real intermediate-time constraint, rather than relabeling a terminal unstable-eigenvalue formula.

The assumptions evade the R04 atomic initial-set mechanism through positive area and uniform vertical-section bounds. They do not restore a fixed-measure variational principle. They evade the R01 lost-projection mechanism by retaining actual feasible initial sets and ambient trajectories. They do not restart either rejected universal lift formula or common-input chaos claim.

No unrestricted structural stability, genuine control-set theorem, varying first jet, nontriangular radial dynamics, general multidimensional formula, or coding/data-rate theorem is proved. The shrinking-tolerance tracking problem is also left open. None of these extensions is counted as a result or automatically started.
