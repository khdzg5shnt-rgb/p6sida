# R02: the state projection and the pressure dictionary

Date: 3 October 2026 (Asia/Shanghai; 2 October UTC). All logarithms below are natural. These calculations check the interface of R01 with existing definitions. They are not claimed as new general entropy principles.

## 1. What was rechecked in R01

Use the labelled alphabet A = {0,...,m−1}, 1 < q ≤ m, the digits

$$
v_j=q-1-\frac{2(q-1)j}{m-1},
\qquad f_j(s,z)=(R(s),[R(s)/s](qz+sv_j)),
$$

with the smooth extension at s = 0. Here R is the radial diffeomorphism used in R01, 0 < R(s) < s on (0,1], and ρ = R′(0) > 0. The common constraint is Q = {(s,z): 0 ≤ s ≤ 1, |z| ≤ s}. At positive radius y = z/s satisfies y⁺ = qy + v_j, independently of s.

For a word w of length n, its viable normalized initial interval is

$$
I_w=\psi_{w_0}\cdots\psi_{w_{n-1}}([-1,1]),
\qquad \psi_j(y)=(y-v_j)/q.
$$

Each inverse branch maps [-1,1] into itself. Consecutive branch intervals meet because their left endpoints differ by 2(q−1)/(q(m−1)) ≤ 2/q. Thus they cover [-1,1]; the same holds at every depth n. All I_w have length 2q^{−n}. Nested inverse images show that membership in I_w is equivalent to feasibility at every time 0,...,n, not just at time n.

An inclusion-minimal subcover of the depth-n intervals has at most 2qⁿ+2 members. Indeed, if its sorted left endpoints are a_i, then a_{i+2} > a_i + 2q^{−n}; otherwise the middle interval is redundant. Count the two parities separately. A single word covers area q^{−n} of Q, since its vertical section at radius s has length 2sq^{−n}. Consequently, for every positive-area compact K ⊂ Q,

$$
|K|q^n\le r_{\rm inv}(n,K,Q)\le2q^n+2.
$$

This proves the actual time limit log q without assuming an interior viability margin.

For outer and tracking counts, the radial product bounds give Rⁿ(s)/s ≤ C_η(ρ+η)ⁿ uniformly and Rⁿ(s)/s ≥ c_{η,s₀}(ρ−η)ⁿ on s ≥ s₀ > 0. A normalized grid for the scale [q(ρ+η)]^k gives the upper rate max{0,log(q(ρ+η))}. For tracking, add a finite radial net: equicontinuity of the iterates R^k makes its size independent of n. At the final time a fixed input has vertical slope qⁿRⁿ(s)/s; the bounded vertical projection of Q^ε and Fubini give the lower rate log(q(ρ−η)) on a positive-area part of K. Nonnegativity and η ↓ 0 give, at every fixed ε > 0, the common time limit

$$
\max\{0,\log(\rho q)\}.
$$

The outer lower bound applies to tracking because closeness to a feasible reference keeps the actual trajectory in Q^ε. This argument does not impose feasibility on the actual tracking trajectory.

The series Y_q(u) = −Σ_{k≥0} v_{u_k}/q^{k+1} is uniformly convergent. A bounded normalized orbit forces its initial value to be Y_q(u). Thus H_{q,R}(u,s) = (u,(s,sY_q(u))) is a homeomorphism from Σ_m × [0,1] onto the entire forward lift, conjugating its map to σ × R. Radial conjugacies are obtained shell by shell from [R(1),1]; their endpoint definitions agree and extend continuously to zero. At positive radius an entire state trajectory determines every label, since its successive normalized coordinates determine v_{u_k}. At radius zero all inputs have the same state trajectory. The abstract trajectory factor is therefore the quotient that collapses Σ_m × {0} to one point.

Uniform radial collapse gives zero state-trajectory entropy; the equicontinuous radial coordinate gives zero input-fiber entropy. The full input shift persists at the apex. Finally, invariance and the nonnegative function s−R(s) force every invariant lift measure onto the apex. The family is exactly ν × δ_apex, with ν shift invariant, and the input factor is a measure isomorphism on each such support. Its conditional KS entropy is zero.

**Audit outcome.** No substantive error was found in the R01 realization or diagram separation theorem under these definitions. This is a manual derivation check. The theorem concerns abstract conjugacies of trajectory systems; it does not preserve their presentations by an initial-state coordinate map. That qualification is essential.

## 2. A concrete failure of the initial-state identification

Fix m = 2 and use the same R(s) = arsinh(s) for q₁ = 2 and q₂ = 3/2. Take

$$
u=(0,1,1,1,\ldots),\qquad u'=(1,0,0,0,\ldots).
$$

Since v₀ = q−1 and v₁ = −(q−1), summing the geometric series gives

$$
Y_q(u)=\frac{2-q}{q},\qquad Y_q(u')=-\frac{2-q}{q}.
$$

In the q₁ model, H_{q₁,R}(u,1) and H_{q₁,R}(u′,1) have the same initial state (1,0). The input-preserving lift conjugacy H_{q₂,R}H_{q₁,R}^{−1} sends them to lift points with initial states (1,1/3) and (1,−1/3). Hence this conjugacy does not descend to a single map of initial states. In particular, the induced trajectory conjugacy is not coordinatewise application of a state homeomorphism. It preserves distinct entire trajectories while changing which trajectories start at the same point.

This does not refute invariance under control-system conjugacy. It explains why that established invariance statement and the R01 diagram theorem concern different data.

Let p_i be the initial-state projection of lift Λ_i. If an input-preserving lift isomorphism Ψ and a homeomorphism h:Q₁→Q₂ instead satisfy

$$
p_2\Psi=h p_1,
$$

then, for every word w,

$$
h(V_w^1)=V_w^2,
\qquad V_w^i=p_i(\Lambda_i\cap\pi_i^{-1}[w]).
$$

To justify the identification, every finite viable prefix can be continued from its final state by controlled invariance; full-shift inputs allow the concatenation. Thus V_w^i is exactly its finite-prefix feasible initial set. Apply Ψ and its inverse to obtain the displayed equality. Covering K by these sets is equivalent to covering h(K), so every exact finite-horizon count is equal. Restoring p_i recovers this covering problem directly. It does not by itself provide a new effective formula or variational principle.

With q fixed and R changed, the radial state homeomorphism (s,sy) ↦ (h(s),h(s)y) preserves all feasible controlled transitions and their exact counts. It need not conjugate trajectories that leave Q. Outer and tracking counts use those ambient trajectories. An input-preserving controlled conjugacy between neighborhoods of two compact constraints, mapping one constraint and initial set to the other, preserves the outer and tracking entropies defined by letting the tolerance decrease to zero. Choose a small compact tube inside each domain, use uniform continuity of the conjugacy and inverse to compare tolerances, and transfer each finite catalogue. The tolerance changes are independent of n; equality of counts at the same fixed tolerance is not claimed. The R01 radial map asserts only a homeomorphism on Q, not this neighborhood conjugacy.

## 3. Pressure on minimum-cardinality catalogues

The relevant indexed passages of Nie–Wang–Huang (2022) use a pressure formed by maximizing weights over minimum-cardinality spanning families, and then define a dual entropy on probabilities on input values. Their complete original was not acquired. The following finite-alphabet calculation states its own conventions and proves its assertions without relying on an unread theorem of that paper. It is an application of existing pressure duality, not a proposed upgrade theorem.

Let N_n be the least number of length-n words whose feasible initial sets cover Q, and let C_n be the finite nonempty collection of such minimum-cardinality word families. For g ∈ ℝ^m define

$$
P_q(g)=\limsup_{n\to\infty}\frac1n
\log\max_{C\in\mathcal C_n}
\sum_{w\in C}\exp\left(\sum_{k<n}g_{w_k}\right).
$$

Taking prefixes identifies minimum-cardinality input catalogues with these word families: duplicate prefixes are redundant, and every word has an infinite extension. This is the maximum over smallest catalogues. It is not the usual infimum of weighted sums over all spanning catalogues.

The previous count proves P_q(0) = log q. Furthermore,

$$
|P_q(g)-P_q(f)|\le\|g-f\|_\infty,\qquad
P_q(g+c\mathbf1)=P_q(g)+c.
$$

Both follow from termwise exponential bounds at each n. P_q is monotone and convex: each finite-n log-sum-exp is convex, its finite maximum is convex, and the limsup inequality preserves the convexity inequality. All values are finite because P_q(0) is finite and the Lipschitz bound applies.

For p in the probability simplex Δ_m define

$$
H_q(p)=\inf_{g\in\mathbb R^m}\{P_q(g)-p\cdot g\}.
$$

An individual H_q(p) is allowed to equal −∞; no general nonnegativity is being asserted. Translation by P_q(g) shows that this infimum also equals inf{p·f : P_q(−f)=0}: take f = P_q(g)1−g, and conversely take g = −f.

We have

$$
\max_{p\in\Delta_m}H_q(p)=P_q(0)=\log q.\tag{1}
$$

Here is the finite-dimensional proof. A supporting hyperplane to the epigraph of the finite continuous convex function P_q at (0,P_q(0)) yields p with P_q(g) ≥ P_q(0)+p·g. Its coefficient in the vertical direction is strictly positive: a zero coefficient would give a nonzero linear functional bounded on all ℝ^m. Normalizing that coefficient yields the stated support inequality. Monotonicity applied to −t e_i implies p_i ≥ 0. Applying the translation identity to c1 for positive and negative c implies Σ_i p_i = 1. Thus p ∈ Δ_m, the support inequality gives H_q(p) ≥ P_q(0), and evaluation at g = 0 gives the reverse inequality. That evaluation also bounds H_q for every other p, proving (1).

Consequently, changing q from 2 to 3/2 changes the function H_q on the same simplex Δ₂, even though the invariant lift measures are unchanged. Otherwise their maxima in (1) would agree. All Bernoulli input marginals p occur among those invariant lift measures; knowing which measures exist supplies none of the pressure values used to define H_q.

## 4. An explicit binary calculation

For q = m = 2, the depth-n intervals I_w have disjoint interiors and cover [-1,1]. Every word is necessary to cover an interior point of its interval. Therefore every minimum catalogue has exactly one prefix of each of the 2ⁿ words. The weighted sum is forced:

$$
\sum_{w\in\{0,1\}^n}\exp\left(\sum_{k<n}g_{w_k}\right)
=(e^{g_0}+e^{g_1})^n,
\qquad P_2(g)=\log(e^{g_0}+e^{g_1}).
$$

Put p = (t,1−t). If z_i = e^{g_i}/(e^{g_0}+e^{g_1}), then

$$
P_2(g)-p\cdot g
=-t\log z_0-(1-t)\log z_1
=-t\log t-(1-t)\log(1-t)+D(p\Vert z).
$$

The last term is nonnegative. For 0 < t < 1, take z = p to attain equality. At either endpoint take the appropriate limiting sequence of positive z. With 0 log 0 = 0 this proves

$$
H_2(t,1-t)=-t\log t-(1-t)\log(1-t).
$$

At t = 1/2 its value is log 2. Choose even the invariant input measure that assigns mass 1/2 to each of the alternating sequences 0101... and 1010.... Its input-value marginal is (1/2,1/2), while its ordinary KS entropy and that of its apex lift are zero. The conditional KS entropy over input is also zero. The dual quantity H₂ is nevertheless log 2. Its argument is a probability on input values; it is not the ordinary entropy of either invariant process. This example makes the domain distinction explicit.

## 5. The all-time hypothesis is a genuine obstruction

The cone Q is a forward constraint. It has no positive-radius full-time feasible state. If s₀ > 0 admitted a backward radial orbit in [0,1], its radii R^{−n}(s₀) would increase to a limit ℓ ∈ (0,1] with R(ℓ) = ℓ, contrary to strict radial decrease. Its all-time state core is therefore the apex, which has zero area. This prevents applying the positive-volume all-time hyperbolic results directly to a positive-area K in the cone. For R = arsinh there is also a neutral derivative at the apex. The finite discrete alphabet does not satisfy the connected-input hypothesis of Kawan v5.

Failure of these hypotheses establishes nonapplicability, not novelty or importance. It also does not make the general achievability question in Kawan v5 a P6 result: P6 supplies no proof interface for positive internal fiber complexity in those all-time hyperbolic sets.

## 6. Result and limit of this round

The R01 separation survives the audit with the abstract-trajectory qualification. The explicit projection collision identifies the information it omits. The pressure calculation explains why a control measure entropy can remain positive when every conditional KS entropy of the feasible lift vanishes. These are useful clarifications and applications of known definitions and elementary convex duality. They do not establish a new important general formula. No new upgrade proof interface was selected in R02.
