# R03 full-text audit: normalization, conjugacy, and coverage

3 October 2026 (Asia/Shanghai). Baseline: `791fd5f6a25ab193ecaff3860fc179e11ced2a1c`.

This addendum uses the supplied **complete journal original** of Nie–Wang–Huang (2022), denoted NWH, and the supplied original of Wang–Huang–Sun (2019), denoted WHS. NWH was read on all 31 PDF pages, including its proofs and supplementary remarks. Relevant formulas were checked against page images. This is a source and definition audit within route A, not a new upgrade route. No claim of first discovery of the corrections below is made.

## 1. The three measure domains

| Quantity | Argument and optimization | What remains in the definition |
|---|---|---|
| WHS lower/upper invariance entropy | An arbitrary Borel probability on the initial constraint; then an infimum over invariant partitions | Initial-state cylinders and their controlled realization |
| NWH pressure-derived entropy | A Borel probability on the compact space of **control values** | Pressure computed from minimum-cardinality feasible catalogues |
| Conditional KS entropy of a feasible lift | An invariant probability on the lift, conditioned on its input factor | The invariant dynamics of that lift and factor |

Neither WHS nor NWH requires its optimizing probability to be an invariant lift measure. NWH uses a supremum of weighted sums over **minimum-cardinality** spanning catalogues. It does not use the usual infimum of weighted sums over all spanning catalogues. Thus its convex duality does not give a variational theorem for that latter pressure, or for conditional KS entropy.

The binary pressure and WHS computations already proved in R02 and the earlier R03 record remain self-contained. Their natural logarithms must be specified when comparing them with the printed NWH formulas.

## 2. A normalization inconsistency in the printed NWH definitions

NWH p. 321 chooses `log = log_2` in discrete time. Its (2.1), p. 322, nevertheless uses the weights `exp(S_n f)`. Let

$$
P_e(f)=\limsup_{n\to\infty}\frac1n\ln
\sup_{\mathcal S\in\mathcal G_n}\sum_{u\in\mathcal S}e^{S_nf(u)},
\qquad P_{\rm pr}(f)=\frac{P_e(f)}{\ln2},
$$

where the catalogues in `G_n` have the least possible cardinality. The subscript `pr` means the printed discrete-time convention. For finite entropy,

$$
P_{\rm pr}(f+c)=P_{\rm pr}(f)+\frac{c}{\ln2}.
$$

**Proof.** Each weight is multiplied by `e^{nc}`. Supremum, logarithm, division by `n`, and limsup give the identity. It contradicts the unscaled `+c` in Lemma 2.3(2) as printed. This is not an OCR inference: PDF pages 4–5 were inspected visually.

There is also a direct failure of the printed variational formula on the P6 binary cone. R02 proves, by forcing one prefix of each binary word into every minimum catalogue, that

$$
P_e(f)=\ln(e^{f_0}+e^{f_1}),\qquad P_{\rm pr}(0)=1.
$$

NWH Definition 3.4 uses the zero-pressure level set:

$$
h_{\rm lev}(p)=\inf\{p_0g_0+p_1g_1:P_{\rm pr}(-g)=0\}.
$$

That level condition is `e^{-g_0}+e^{-g_1}=1`. Write `z_i=e^{-g_i}`. For `p=(t,1-t)`,

$$
-\sum_i p_i\ln z_i
=-\sum_i p_i\ln p_i+D(p\Vert z)
\ge-\sum_i p_i\ln p_i.
$$

Equality is attained when both `p_i` are positive by `z=p`; approximation by positive `z` treats the endpoints. Consequently

$$
\sup_p h_{\rm lev}(p)=\ln2\ne1=P_{\rm pr}(0).
$$

Thus Theorem 3.13 and Corollary 3.15, with all those printed conventions used simultaneously, fail even at zero potential. The other proposed dual formula (3.9) is not equivalent to Definition 3.4 under the mixed normalization: for every probability `mu`, constant potentials give

$$
\inf_f\{P_{\rm pr}(f)-\textstyle\int f\,d\mu\}
\le\inf_{c\in\mathbb R}\{P_{\rm pr}(0)+(1/\ln2-1)c\}=-\infty.
$$

This last statement concerns formula (3.9); it does **not** claim that every entropy in the actual level-set Definition 3.4 is minus infinity.

Two consistent repairs are available: use natural logarithms with the existing exponential weights, or use weights `2^{S_nf}` with binary logarithms and potentials measured in bits. This audit and P6 use the first convention. The repair is explicit; the printed theorem is not silently certified.

In addition, Definition 5.5 on p. 346 visibly omits the logarithm before the weighted sum. Its stated analogy with pressure requires inserting that logarithm. For example, a singleton constraint with one control and constant potential `c>0` has `p_n=e^{nc}`; the displayed `limsup p_n/n` is infinity, while a consistently defined pressure is finite. This supplementary formula is not used in P6 or in the counterexample below.

## 3. An explicit counterexample to the time-variant conjugacy equality

NWH Proposition 2.5 assumes a time-variant conjugacy and only

$$
\pi_n(Q)\subset\pi_0(Q).
$$

It concludes equality of pressures, hence equality of exact entropies at zero potential. The inverse-spanning assertion in its proof, p. 326, does not follow from that one-way inclusion. The following example satisfies the stated assumptions, with a positive-area initial set.

Let `X=R^2`, `U={-1,1}`, and let all input sequences be admissible. Set

$$
F_u(s,z)=(s,2z+su),\qquad
G_u(s,z)=\tfrac14F_u(s,z),
$$

$$
Q=[0,1]\times[-1,1],\qquad
K=\{(s,z):\tfrac12\le s\le1,\ |z|\le s\}.
$$

`K` is compact with area `3/4`; `Q` is compact, convex, and has nonempty interior. Both controlled maps are global smooth linear diffeomorphisms: their determinants are respectively `2` and `1/8`. Both systems are discrete-time continuous control systems with compact control-value space, shift-invariant full inputs, unrestricted concatenation, and the cocycle property. We use forward time; two-sided input functions can equally be supplied without changing any count.

Define `pi_n(x)=4^{-n}x` and take the control-value map `H=id`. Homogeneity of every `F_u` gives, for every initial state and input sequence,

$$
\varphi_G(n,x,u)=4^{-n}\varphi_F(n,x,u)
=\pi_n(\varphi_F(n,x,u)),\qquad \pi_0=\operatorname{id}.
$$

Each `pi_n` is a homeomorphism of the entire state space; the family is continuous in discrete time. The inverse relation also holds. Moreover,

$$
\pi_n(Q)=[0,4^{-n}]\times[-4^{-n},4^{-n}]\subset Q=\pi_0(Q).
$$

These are exactly the NWH conjugacy and set-inclusion conditions, with an induced input map that is a bijection.

### Counts for the source system

At a positive radius `s`, the normalized coordinate `y=z/s` evolves as

$$
y_{k+1}=2y_k+u_k.
$$

The inverse maps `(y-u)/2` send `[-1,1]` into itself and their two images cover it. Successively choosing viable branches proves that `(K,Q)` is admissible for `F`.

For a word `w=(u_0,...,u_{n-1})`, put

$$
B_w=\sum_{k=0}^{n-1}2^{n-1-k}u_k,\qquad
I_w=\left[\frac{-1-B_w}{2^n},\frac{1-B_w}{2^n}\right].
$$

The `2^n` different values of `B_w` are the odd integers between `-(2^n-1)` and `2^n-1`. Thus the intervals `I_w` tile `[-1,1]` with disjoint interiors. Membership in `I_w` is equivalent to normalized feasibility through time `n`: its final state is in `[-1,1]`, and applying the prescribed inverse branches backwards keeps all preceding states there.

Using all `2^n` words covers `K`, since the resulting actual coordinates satisfy `|z_k|<=s<=1`. Conversely the slice `{1} x [-1,1]` lies in `K`. On that slice every interior point of `I_w` requires the prefix `w`; no other prefix covers it. Every spanning catalogue must therefore contain all `2^n` distinct prefixes. Hence, for every `n>=1`,

$$
r_{\rm inv}^{F}(n,K,Q)=2^n.
$$

### Counts for the target system

For every `(s,z) in Q` and either input,

$$
0\le s/4\le1/4,\qquad |(2z+su)/4|\le3/4.
$$

Thus every input keeps the whole rectangle in `Q`; any single infinite input spans `K` for every horizon. The pair is admissible for `G`, and

$$
r_{\rm inv}^{G}(n,K,Q)=1.
$$

It follows, in natural units, that

$$
\boxed{h_{\mathrm{inv}}^{F}(K,Q)=\ln2,\qquad h_{\mathrm{inv}}^{G}(K,Q)=0.}
$$

In the printed binary units these values are `1` and `0`, so this failure is independent of the normalization problem in section 2.

For clarity, `Q` need not itself be controlled invariant for `F` (points at `s=0`, `z!=0` cannot be kept there). **The stated NWH Proposition 2.5 requires an admissible pair, not controlled invariance of all of Q.** The pair above meets that assumption. No claim about a genuine control set, a `K=Q` variant with extra assumptions, or chaos is made here.

### Pressures and the measure version

The forced prefixes give

$$
P_e^{F}(f)=\ln(e^{f(-1)}+e^{f(1)}),\qquad
P_e^{G}(f)=\max\{f(-1),f(1)\}.
$$

For the second identity the minimum catalogue has one member, any word is feasible, and a constant maximizing letter attains the supremum weight. The level-set Definition 3.4 is unchanged by multiplication of pressure by the positive factor `1/ln2`. Therefore, with `p=\tfrac12\delta_{-1}+\tfrac12\delta_1`, its two values are `ln2` and `0`, respectively. The first follows from the Gibbs calculation in section 2. For the second the level condition is `min g=0`, so every average is nonnegative and `g=0` attains zero. Since `H=id`, this also contradicts the equality in NWH Theorem 3.11 as stated.

### Correct boundary

Kawan (2013), Definition 2.4 and Proposition 2.13, printed pp. 56–57 (physical PDF pages 79–80), use this set inclusion for a **one-way** entropy inequality. Mapping a source-spanning catalogue gives a target-spanning one. Mapping a target-spanning catalogue back would require

$$
\pi_n^{-1}(\pi_0(Q))\subset Q,
$$

which is not implied by the forward inclusion. Our inverse maps are expanding, and precisely this condition fails.

A sufficient repair of the NWH equality is

$$
\pi_n(Q)=\pi_0(Q)\quad\text{for all }n\ge0.
$$

**Proof.** Under a time-variant conjugacy with the stated bijective induced input map, this equality makes `phi_F(k,x,u) in Q` equivalent to `phi_G(k,pi_0(x),H(u)) in pi_0(Q)` at each time. The corresponding spanning families and their inverses then have equal cardinalities. Minimum catalogues correspond bijectively; their weights agree after composing the potential with the control-value homeomorphism. Taking logarithms and limsup proves pressure equality. Pushing control-value probabilities through that homeomorphism transports the zero-pressure level sets, proving equality for the level-set entropies as well. A time-invariant state conjugacy satisfies the set equality automatically. This elementary repair is not claimed as a new major structure theorem.

## 4. The dual entropy must be allowed to equal minus infinity

Even after fixing units, the real-valued codomain in NWH Proposition 3.6 is too restrictive. This is already suggested by its Example 3.8, but the full infimum makes the issue explicit.

Take `X=R`, `U={a,b}`, `F_a(x)=x`, `F_b(x)=x+1`, and `K=Q={0}`. The only feasible prefix of length `n` is `a^n`. Hence in natural units `P_e(f)=f(a)` and the zero-pressure level condition is `g(a)=0`. For a control-value probability with `p(b)>0`, choosing `g(b)=-M` yields

$$
h_{\rm lev}(p)\le-Mp(b)\longrightarrow-\infty.
$$

For `p=delta_a` the value is zero. Thus the appropriate codomain for finite topological entropy is `[-infinity,h_inv]`, with minus infinity permitted. R02 already used this extended convention, so its calculation needs no reversal. One should not invoke a theorem with a real-valued hypothesis for every one of these probabilities without handling the extended values.

## 5. The part of pressure duality that does survive

Here is a self-contained verification of the relevant corrected assertion. It identifies what NWH already supplies conceptually and avoids depending on its disputed conjugacy assertion.

Let `U` be compact metric and let `P:C(U,R)->R` be finite, continuous, convex, monotone, and satisfy `P(f+c)=P(f)+c`. Natural-unit minimum-catalogue pressure has these properties whenever its zero-potential entropy is finite. Monotonicity and constant translation give its uniform Lipschitz bound. At each finite horizon, the logarithm of a weighted sum is convex, taking a supremum preserves convexity, and the limsup convexity inequality preserves it in the pressure limit.

For every probability `mu` define

$$
H(\mu)=\inf_{g\in C(U)}\left(P(g)-\int g\,d\mu\right)\in[-\infty,P(0)].
$$

Then

$$
H(\mu)=\inf\left\{\int a\,d\mu:P(-a)=0\right\},\qquad
P(f)=\max_{\mu\in\mathcal M(U)}\left(H(\mu)+\int f\,d\mu\right).
$$

**Proof of the first identity.** For any `g`, let `a=P(g)1-g`. Constant translation gives `P(-a)=0` and its integral is `P(g)-int g dmu`. Conversely every zero-level `a` is obtained by using `g=-a`. This identifies both infima, including minus infinity.

**Proof of the second identity.** The infimum gives `H(mu)+int f dmu<=P(f)` for every probability. To obtain equality, define the directional derivative

$$
d_f(g)=\lim_{t\downarrow0}\frac{P(f+tg)-P(f)}t.
$$

Convexity and the Lipschitz bound make this a finite sublinear functional with `|d_f(g)|<=||g||_infinity`. For subadditivity, apply convexity to `f+t(g+h)` as the midpoint of `f+2tg` and `f+2th` and pass to the limit. Positive homogeneity follows by a change of parameter. Constant translation gives `d_f(c1)=c`. Hahn–Banach extends `c1 -> c` to a linear functional `L` on `C(U)` dominated by `d_f`. It is bounded by the uniform norm. If `g>=0`, monotonicity gives `d_f(-g)<=0`, and consequently `L(g)>=0`. Also `L(1)=1`. Riesz representation therefore identifies `L` with a Borel probability `mu_f` on `U`.

The slope of a convex function on a ray is nondecreasing, so

$$
\int g\,d\mu_f=L(g)\le d_f(g)\le P(f+g)-P(f).
$$

Substituting `g=k-f` gives `P(k)-int k dmu_f >= P(f)-int f dmu_f` for every `k`. Taking the infimum and then using `k=f` proves `H(mu_f)=P(f)-int f dmu_f`. This proves the maximum formula. Upper semicontinuity and concavity of `H` also follow from its expression as an infimum of continuous affine functions, with extended values allowed.

This is established convex pressure duality, not a newly proposed general control variational principle. It verifies that the normalized pressure computation in R02 remains an application of the existing NWH approach. It gives no trajectory-realization theorem and no formula based only on invariant lift dynamics.

## 6. WHS proofs and their actual applicability

The added WHS review covered Propositions 4.4–4.6, Theorem 4.8, Propositions 4.11–4.12 and Theorem 4.13, Lemma 5.1 and the mass/cylinder mechanisms in Theorems 5.2–5.3, Proposition 6.1, Lemma 6.3 and Theorem 6.4, and Lemma 7.1 and Theorem 7.2, with the corresponding global corollaries. This is a review of the mechanisms affecting P6; it is not certification of every external dependency or every symbolic example in section 8.

The relevant checks are as follows.

* Fixed-partition cylinders form finite partitions at each depth and are nested or disjoint across depths. This supports the disjoint-selection argument in Lemma 5.1 and the mass bounds in section 5.
* Time grouping preserves cylinders, with denominator `N*tau` or `Nk*tau`. Refinement retains the assigned controls. The generator argument uses a common block time before comparing different partitions; it does not interchange infimum over partitions and supremum over probabilities without the stated generator condition.
* Theorem 4.8 uses a single bimeasurable bijection of actual states and both directions of controlled feasibility. Transported cylinders have the same probability. R01's abstract trajectory conjugacy with different `q` does not meet this condition.
* In the Frostman construction, clopen cylinders permit continuous test functions; in the packing construction, they permit passing cylinder masses through a weak limit and retaining nested branches. The compact initial set supplies compact support. The openness hypothesis is used in the proof, not added decoration.

The printed WHS proof has minor coefficient/notation omissions that must not be propagated. On p. 326, the cylinder bound from its weighted definition is

$$
\mu(Q_n(x,\mathcal C))\le c^{-1}e^{-\alpha\tau n},
$$

not the displayed bound without `tau`. On p. 328 the initial packing mass should consistently use `e^{-alpha*tau*m_1(x)}`, as the subsequent levels do. Both omissions were checked in page images. In the construction, the next minimum horizon can be chosen strictly larger than the previous maximum using Lemma 7.1; this makes the claimed unbounded subsequence explicit. These are repairs in the displayed derivations, not new entropy principles. This audit does not assert that the printed proofs are literally correct without them.

Under the WHS compactness and clopen hypotheses, the weighted Frostman repair can be checked directly: normalize the weighted covering functional on continuous functions by its positive value on `1`; Hahn–Banach and positivity give a probability; openness lets one bound the mass of a cylinder by its one-cylinder cover cost `e^{-alpha*tau*n}`. In the packing construction, nested clopen cylinders carry descendant masses within the product of factors `1+2^{-i}`. The finite measures then have bounded mass on the compact initial set, a weak limit preserves every such cylinder mass, and the increasing selected depths yield the local upper-entropy bound. These checks recover precisely the uses of units, compactness, and openness at issue here. They do not remove those hypotheses for the P6 cone.

The earlier R03 calculation used `tau=1` for its explicit binary partition and its all-partitions lower bound used the correct denominator `N*tau`; it does not rely on the omissions. The cone has neither a clopen invariant partition nor a maximally irreducible one, for the reasons proved in the earlier `MATHEMATICS.md`. Thus the cited WHS global theorems with those hypotheses do not automatically cover the cone. Their nonapplicability does not certify originality.

## 7. Coverage and route A verdict

| P6/R01–R03 assertion | What the complete sources establish | Verdict |
|---|---|---|
| Positive WHS entropy of initial area, zero entropy of apex probabilities | Existing WHS definitions concern arbitrary initial-state probabilities and cylinder mass | A self-contained application; not a new major principle |
| Positive pressure-derived entropy with zero conditional KS entropy of every lift measure | NWH constructs a different entropy from feasible catalogue pressure on control-value probabilities | Existing method after explicit normalization; no identification with KS entropy |
| Fixed-alphabet abstract lift/trajectory diagram with varying exact/outer/tracking rates | Neither source removes the initial-state or ambient data from its controlled equivalence | R01 proof remains consistent; these two papers do not state that exact diagram theorem; independent first-discovery status remains uncertified |
| Equality under time-variant conjugacy and mere forward set inclusion | The NWH equality is contradicted by section 3; Kawan's corresponding result is one-way | A source correction, not a restored pure-lift formula or a four-journal upgrade route |
| An effective new structure formula after restoring initial-state projection | Exact counts are recovered by the feasible initial-state covering problem; pressure duality is already available | No independently important, precisely uncovered target has been identified |

**Target importance:** no route-A main theorem currently has independent evidence of Annals/Inventiones/JAMS/Acta-level consequences. Correcting the finite-dimensional conjugacy statement or its units does not supply that evidence.

**Current mathematical content:** the new complete results in this addendum are the explicit normalization test, the positive-area time-variant counterexample (including its pressures and measure version), and the extended-value diagnostic. The corrected duality verification safeguards earlier applications. Their proofs and scope are supplied above; their first-discovery status is not certified.

**Feasibility:** these interface checks are complete. No long new proof was launched, because no important uncovered route-A target passed the selection gate. The core obstacle is the absence of such a target and a proof interface going beyond restored covering data and known duality, rather than the now-closed 2022 full-text acquisition gap.

Route A's proof expansion and whole-paper rewrite remain paused. The four-journal objective is unchanged. This conclusion neither rejects the original paper nor imposes a journal ceiling on a future, different main theorem. No third route or chaos restart has been introduced.
