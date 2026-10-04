# R18 — Identical local dynamics do not determine the global precision boundary

Date: 2026-10-04 UTC. Baseline: `9fb4b4fdea97ca1d6d756ebcdf7f8122994034e3`.

## 1. Fixed question, one candidate, and precise conclusion

We select one globally C∞ class: state-dependent angular saturation. No second candidate or alternative attack is used. The parameter range is fixed throughout:

\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,
\quad \beta>1,\quad 0<\sigma<1/2.
\]

Write \(\rho_i=a_i^\beta\), \(h_a=-a_0\ln a_0-a_1\ln a_1>0\), and let \(A_i\) be the R15–R17 linear maps

\[
A_0(s,z)=(\rho_0s,a_0^{\beta-1}(z+a_1s)),\qquad
A_1(s,z)=(\rho_1s,a_1^{\beta-1}(z-a_0s)).
\]

The constraint is the same physical triangle
\(Q=\{0\le s\le1,\ |z|\le s\}\), whose area is one. All binary infinite inputs are allowed. For maps \(G_i\), define

\[
r_G(n,\delta;K)=\min\{|\mathcal C|:
\mathcal C\subset\{0,1\}^{\mathbb N},\quad
\forall x\in K\ \exists u\in\mathcal C\ \forall k\in\{0,\ldots,n\},
\operatorname{dist}_2(G_{u_{k-1}}\cdots G_{u_0}x,Q)<\delta\}.
\]

At \(k=0\) the composition is the identity. The control is assigned to the actual initial state; no sampled or symbolic initial set replaces it. Trajectories may leave and reenter Q. Statements below remain valid if the neighbourhood is defined using ≤ instead of <.

**Theorem 18.1 (global collapse obstruction despite identical local dynamics).** There are explicit C∞ maps \(G_0,G_1:\mathbb R^2\to\mathbb R^2\) with these parameters such that:

1. Each map agrees exactly with \(A_i\) on an open neighbourhood of the origin, so all derivatives there agree. Every input converges exponentially to the common origin, uniformly on bounded initial sets.
2. Every initial state in Q has an infinite exactly feasible input.
3. The fixed compact set \(K_\sigma=\{(s,z)\in Q:s\ge2\sigma\}\) has area \(1-4\sigma^2\), contains interior, and satisfies \(r_G(n,\delta;K_\sigma)=1\) for every \(n\ge0\) and \(\delta>0\).
4. For every sequence \(\delta_n\to0\) with finite \(-\ln\delta_n/n\to\gamma\ge0\),
\[
\min\{h_a,\gamma/\beta\}\le
\liminf_n\frac{\ln r_G(n,\delta_n;Q)}n
\le\limsup_n\frac{\ln r_G(n,\delta_n;Q)}n
\le\min\{\ln2,\gamma/\beta\}.
\tag{18.1}
\]
In particular, when \(0\le\gamma\le\beta h_a\), the full-Q limit exists and equals \(\gamma/\beta\).
5. No injective coordinate change on a neighbourhood containing Q can conjugate both maps to the R17 invertible linear maps, even after swapping the input labels.

Thus for every finite \(\gamma>0\), full Q and the same fixed \(K_\sigma\) have strictly different costs (a positive full-Q lower rate versus zero). First-order matching is insufficient to transfer R17's universal positive-area low-precision law. In fact, agreement on a whole origin neighbourhood is insufficient. At \(\gamma=0\), all nonempty compact subsets of Q have rate zero by (18.1) and monotonicity. No exact full-Q high-precision spectrum is asserted.

The maps are globally noninjective and have zero Jacobian in a saturation region. They are locally invertible near the origin. This theorem does **not** disprove a transfer theorem for maps locally invertible throughout Q, nor assert that global injectivity alone suffices for such a theorem.

## 2. Construction and feasible geometry

Let \(e(t)=0\) for \(t\le0\) and \(e(t)=\exp(-1/t)\) for \(t>0\). Set

\[
\psi(s)=\frac{e(s-\sigma)}{e(s-\sigma)+e(2\sigma-s)}.
\]

The denominator is everywhere positive. The standard flat function e gives \(\psi\in C^\infty(\mathbb R)\), \(0\le\psi\le1\), \(\psi=0\) for \(s\le\sigma\), and \(\psi=1\) for \(s\ge2\sigma\). Define on all of \(\mathbb R^2\)

\[
G_0(s,z)=\left(\rho_0s,
(1-\psi(s))a_0^{\beta-1}(z+a_1s)-\psi(s)\rho_0s\right),
\tag{18.2}
\]
\[
G_1(s,z)=\left(\rho_1s,
(1-\psi(s))a_1^{\beta-1}(z-a_0s)+\psi(s)\rho_1s\right).
\tag{18.3}
\]

There is no division by s in these definitions. They are C∞ at the origin and equal the linear maps whenever \(s\le\sigma\). No nonzero state with s>0 is sent to the origin in finite time: its radial coordinate remains strictly positive.

For checking feasibility only, take \(s>0\), \(y=z/s\in[-1,1]\), \(t=\psi(s)\), and \(\xi=a_0-a_1\). The output ratios are

\[
U_0(s,y)=(1-t)(y+a_1)/a_0-t,\quad
U_1(s,y)=(1-t)(y-a_0)/a_1+t.
\]

If \(t<1\), imposing \(-1\le U_i\le1\) gives the complete one-step feasible branches

\[
J_0(s)=[-1,\min\{1,\xi+2a_0t/(1-t)\}],
\quad
J_1(s)=[\max\{-1,\xi-2a_1t/(1-t)\},1].
\tag{18.4}
\]

Indeed, for branch 0 the lower inequality is \(y\ge-1\), and the upper is \(y\le\xi+2a_0t/(1-t)\); the other branch is analogous. At t=1, \(U_0=-1\) and \(U_1=1\), so both branches allow all y. Since \(J_0\) contains \([-1,\xi]\) and \(J_1\) contains \([\xi,1]\), their union covers every ratio at every radius. The radial outputs remain in [0,1]. At s=0 the only Q state is the fixed origin. Recursively selecting a feasible branch proves exact controlled invariance, including both endpoints, for an infinite input.

Crucially this is a new physical branch geometry, not the old symbolic partition inserted by assumption. In the saturation region a single branch covers the whole angular interval.

## 3. All-input convergence and the zero-cost positive-area set

Write \(R_0(s,z)=(\rho_0s,-\rho_0s)\) and \(R_1(s,z)=(\rho_1s,\rho_1s)\). Then
\(G_i(x)=(1-\psi(s))A_ix+\psi(s)R_ix\).
Choose

\[
M=1+\max_i\frac{a_i^{\beta-1}a_{1-i}}{1-a_i^{\beta-1}},
\quad \|x\|_M=\max\{M|s|,|z|\}.
\]

In this norm,
\[
\|A_i\|\le\max\{\rho_i,a_i^{\beta-1}+a_i^{\beta-1}a_{1-i}/M\}<1,
\qquad \|R_i\|\le\rho_i<1.
\]

Convexity of the norm yields a constant L<1 independent of x and i with
\(\|G_i(x)\|_M\le L\|x\|_M\). Consequently every input satisfies
\(\|\varphi_G(k,x,u)\|_2\le\sqrt2 L^k\|x\|_M\), even off Q. This is a uniform bound toward the origin; it is not a claim of a global Lipschitz contraction between arbitrary pairs of points, which would require controlling \(\psi'\).

Direct substitution, at all radii, gives

\[
G_0(s,-s)=(\rho_0s,-\rho_0s),\qquad
G_1(s,s)=(\rho_1s,\rho_1s).
\tag{18.5}
\]

For every x in \(K_\sigma\), (18.2) sends x in one step to the lower ray. Equation (18.5) then keeps every subsequent iterate under the single input \(0^\infty\) inside Q. Time zero is already in Q. Hence this input is exactly feasible simultaneously for all x in the compact K, every horizon, and every precision. Nonemptiness of K implies the catalogue cannot have cardinality zero, proving cardinality exactly one. Its area is \(\int_{2\sigma}^1 2s\,ds=1-4\sigma^2\).

For example, \(\sigma=1/8\) gives one fixed set of area 15/16. By selecting a smaller σ when constructing a system, one can make this area arbitrarily close to one. This latter observation changes the system with σ: it is **not** a claim that one fixed system has zero-cost sets of arbitrarily near-full area. The fixed \(K_\sigma\) already simultaneously serves all precision sequences in the theorem.

## 4. Arbitrary approximate controls on the unaffected core

Take \(c=\sigma/2\) and \(Q_c=\{0\le s\le c,\ |z|\le s\}\). Its area \(c^2\) is positive. For every input, whether feasible or not, the first coordinate is

\[
s_k=s_0\prod_{j<k}\rho_{u_j}\le c<\sigma.
\]

Thus \(\psi(s_k)=0\) at every time, irrespective of the z coordinate. The complete G trajectory from each x in \(Q_c\) is exactly the corresponding A trajectory, including trajectories that leave and reenter Q. Both catalogues use the same ambient Q, not the smaller core as constraint. Therefore

\[
r_G(n,\delta;Q_c)=r_A(n,\delta;Q_c)
\quad\text{for all }n,\delta>0.
\tag{18.6}
\]

The actually required R15 dependence is its arbitrary-approximate-control area bound, typical positive-area intersection, and Theorem 15.1 lower bound (4), proved in §§3–4 there. Applied to this fixed positive-area core, it yields

\[
\liminf_n n^{-1}\ln r_A(n,\delta_n;Q_c)
\ge\min\{h_a,\gamma/\beta\}.
\]

Monotonicity and (18.6) prove the lower bound in (18.1). This uses a pointwise equality of full trajectories; no uncontrolled first-deviation error or unproved bounded-distortion property is assumed. No subsequent reentry can reduce the inherited lower bound.

## 5. Finite feasible prelude and the complete-tail upper bound

Set \(\rho_{\max}=\max_i\rho_i<1\) and choose a fixed integer t with \(\rho_{\max}^t\le\sigma\). Every exactly feasible length-t prefix from Q ends in Q with s≤σ. From then on, for all later inputs, its dynamics is exactly linear.

For n≥t, take any linear catalogue for full Q, horizon n−t, and precision δ. Concatenate each of its inputs with every binary prefix of length t. For each actual x, choose an exactly feasible prefix provided by (18.4), and then a linear catalogue input assigned to the actual resulting state. The first t times are exactly feasible and the remaining n−t times satisfy the same Euclidean δ-neighbourhood constraint. All endpoints and boundary states are included. Consequently

\[
r_G(n,\delta;Q)\le 2^t r_A(n-t,\delta;Q)
\le2^t C_U\delta^{-1/\beta},\qquad 0<\delta<1.
\tag{18.7}
\]

The last inequality is R15 (20), whose stopped exact prefix followed by a uniformly contracting arbitrary tail proves every intermediate-time constraint. Its constant is independent of horizon and precision; no limit at a shifted critical exponent is being assumed. Exact controlled invariance also gives \(r_G(n,\delta;Q)\le2^n\), using all length-n prefixes with arbitrary infinite extensions. Taking upper limits proves (18.1). The lower and upper bounds match for \(\gamma\le\beta h_a\), including the critical equality and all sequences with that limiting exponent.

Together with §3 this proves strict full-Q versus K separation at every finite positive γ, under the original all-sequence and all-time quantifiers.

## 6. No global coordinate reduction; the precise obstruction

At each fixed s>2σ, two distinct z coordinates give the same \(G_i(s,z)\). If an injective coordinate map H conjugated this G_i to an invertible linear A_j on a domain containing Q and its images, equal G images would give equal A_jH images, hence equal H images and equal initial states, a contradiction. Thus no simultaneous homeomorphism, C¹ diffeomorphism, or bi-Lipschitz coordinate reduction of this type exists. Locally near zero the identity is already an exact reduction; this is why local equivalence does not settle the global cost.

More quantitatively, the triangular Jacobian satisfies

\[
\det DG_i(s,z)=(1-\psi(s))a_i^{2\beta-1}.
\tag{18.8}
\]

It vanishes in the saturation region, and the angular derivative is \((1-\psi(s))/a_i\). A full angular interval is collapsed to an invariant boundary ray in one step. R17's high-radius witness spacing or first-wrong-branch geometry therefore cannot be inferred from the common first jet: all such high-radius witnesses in this region are covered by the same exact input, at every precision. Uniform all-input convergence does not prevent this collapse.

An elementary general implication clarifies the necessary exclusion: if a fixed positive-area compact K can be sent by one exactly feasible finite prefix into a set on which one fixed infinite input stays feasible, then K has catalogue size at most one for every horizon and precision (short horizons use that same prefix). Such a K is incompatible with a positive universal rate for all positive-area compact initial sets. Finite collections of such channels likewise give a uniform finite bound. This finite-catalogue observation is an existing method, not a new main theorem. Here it is realized with globally C∞ binary maps, the same all-input limit and exactly unchanged local dynamics, while a positive-cost core remains.

R18 therefore supplies a rigorous exclusion reason, not a nonlinear transfer theorem. A transfer claim must control global feasible geometry and rule out this finite-time positive-area collapse into a zero-cost channel. Global local invertibility rules out (18.8)'s mechanism but has not been proved sufficient. The noncollapsing nonlinear case remains unresolved and is not attacked in this round. ∎

## 7. Dependency and contribution boundary

Freshly checked dependencies: R15's full-time upper catalogue and arbitrary approximate-input lower area bound for every fixed positive-area compact K; R16–R17 comparison and fixed-set quantifiers were recovered to identify the transfer target. This proof needs no general high-precision formula, R09–R14 optimal-strategy assertion, or new pressure root. R17's linear theorem is not contradicted: its globally matching geometry is absent in the saturation region.

Noninjective finite-catalogue mechanisms have direct antecedents in Chen–Zhong (2024), detailed in SOURCES.md. The project increment is the explicit smooth realization showing that even all local jets and all-input convergence fail to determine the global positive-area precision boundary. It has modest exclusion value; it does not independently establish an improved publication tier or a general smooth noncollapsing theory.
