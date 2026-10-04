# R19 — Precision-boundary transfer with reversible state-dependent branches

4 October 2026 UTC / 5 October 2026 Asia/Shanghai. Baseline: `5af5226468fe41a69ca0313cd382cdb058c86a94`. Natural logarithms. One fixed system class and one boundary-transfer problem are treated.

## 1. Complete statement and the actual catalogue

Fix
\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,\quad\beta>1,
\quad 0<\epsilon<\frac{a_{\min}}{4(\beta+1)},
\quad a_{\min}=\min_i a_i,\ a_{\max}=\max_i a_i.
\]
On the whole Euclidean plane set
\[
f(s)=s/(1+s^2),\qquad p_0(s)=a_0+\epsilon f(s),\quad p_1(s)=a_1-\epsilon f(s),
\]
\[
G_0(s,z)=\big(s p_0(s)^\beta,p_0(s)^{\beta-1}[z+p_1(s)s]\big),
\quad
G_1(s,z)=\big(s p_1(s)^\beta,p_1(s)^{\beta-1}[z-p_0(s)s]\big).
\tag{1}
\]
All infinite binary inputs are admissible. Keep the actual constraint
\(Q=\{0\le s\le1,\ |z|\le s\}\), of area one. For nonempty compact K⊂Q,
\[
r_G(n,\delta;K)=\min\{|\mathcal C|:\mathcal C\subset\{0,1\}^{\mathbb N}\text{ finite},\quad
\forall x\in K\ \exists u\in\mathcal C\ \forall k=0,\ldots,n:
\operatorname{dist}_2(\varphi_G(k,x,u),Q)<\delta\}.
\tag{2}
\]
The input is assigned to the actual planar state. It may leave and reenter Q. There is one tolerance throughout each horizon. No boundary states are removed.

Write
\[
h=-a_0\ln a_0-a_1\ln a_1,\quad
H(t)=-t\ln t-(1-t)\ln(1-t),\quad
\chi(t)=-t\ln a_0-(1-t)\ln a_1.
\]

**Theorem 19.1.** The maps (1) are global C∞ diffeomorphisms with the R17 derivative matrices at the origin. All inputs converge exponentially to the common origin, uniformly on bounded sets, and Q is controlled invariant. Moreover:

(a) For every fixed positive-area compact K⊂Q, every finite γ≥0 and every positive sequence δ_n→0 with −lnδ_n/n→γ,
\[
\min\{h,\gamma/\beta\}\le\liminf_n\frac{\ln r_G(n,\delta_n;K)}n
\le\limsup_n\frac{\ln r_G(n,\delta_n;K)}n
\le\min\{\ln2,\gamma/\beta\}.
\tag{3}
\]
In particular, for 0≤γ≤βh the limit exists and equals γ/β.

(b) For every ζ∈(0,1), there is a single compact K_ζ⊂Q with area(K_ζ)>1−ζ, such that for every finite γ>βh and every sequence with that exponent,
\[
\lim_n n^{-1}\ln r_G(n,\delta_n;K_\zeta)=h
<\liminf_n n^{-1}\ln r_G(n,\delta_n;Q).
\tag{4}
\]
The set depends only on the fixed system and ζ, not on γ, the precision sequence or the horizon. No exact high-side full-Q spectrum is asserted.

(c) There is no simultaneous homeomorphic conjugacy to the R17 linear maps that preserves Q, even allowing a permutation of the two labels. In particular, the transfer below is not a Q-preserving C¹ or bi-Lipschitz coordinate corollary. A conjugacy sending Q to a different constraint is not excluded by (c) and would not directly give the R17 theorem for this Q.

The controlled geometric estimates in §§3–5 are the decisive interface. The entropy, typical-set and stopping arguments in §§6–7 extend the verified R15–R17 methods; they are not new pressure theory.

## 2. Smooth invertibility, convergence, and complete one-step feasibility

Put
\[
\underline p=a_{\min}-\epsilon/2>0,\qquad
\overline p=a_{\max}+\epsilon/2<1,\qquad r=\overline p^\beta<1.
\]
Globally |f|≤1/2, |f′|≤1, and |s f′(s)|≤1/2. The latter follows from |1−s²|≤1+s². Therefore \(g_i(s)=s p_i(s)^\beta\) has derivative
\[
g_i'(s)=p_i(s)^{\beta-1}[p_i(s)+\beta s p_i'(s)],
\]
bounded below by \(\underline p^{\beta-1}[a_{\min}-(\beta+1)\epsilon/2]>0\), and above by
\[
q=\overline p^{\beta-1}[a_{\max}+(\beta+1)\epsilon/2]<1.
\tag{5}
\]
Both bounds use the stipulated ε range; in particular the last bracket is less than a_max+a_min/8<1. Each g_i is onto ℝ since p_i(s)→a_i as |s|→∞. Its inverse is smooth. Recover s from the first output coordinate and then z from the second, whose z coefficient is p_i(s)^(β−1)>0. Thus (1) are global smooth diffeomorphisms, with
\[
\det DG_i(s,z)=p_i(s)^{2\beta-2}[p_i(s)+\beta s p_i'(s)]>0.
\tag{6}
\]
At zero the derivative is exactly the corresponding R17 matrix; terms involving p_i′ acquire an s or z factor and do not change the first jet.

Take M≥1 with \(M>\overline p^\beta/(1-\overline p^{\beta-1})\), for example one plus that ratio. In the norm \(\|(s,z)\|_M=\max(M|s|,|z|)\),
\[
\|G_i(s,z)\|_M\le L\|(s,z)\|_M,
\quad L=\max\{\overline p^\beta,\overline p^{\beta-1}+\overline p^\beta/M\}<1.
\tag{7}
\]
This uses |p_{1−i}s|≤overline p |s| and works off Q and for negative s too. It is a bound toward zero, not a claim of a global pairwise Lipschitz constant for G_i. It proves the requested all-input convergence and supplies a full-time tail estimate.

For s>0 and y=z/s, the angle maps at radius s are
\[
T_{0,s}(y)=[y+p_1(s)]/p_0(s),\qquad
T_{1,s}(y)=[y-p_0(s)]/p_1(s).
\]
With ξ(s)=p_0(s)−p_1(s), the complete feasible domains are [-1,ξ(s)] and [ξ(s),1], each mapped onto [-1,1]. The inverse branches are
\[
B_{0,s}(y)=p_0(s)y-p_1(s),\quad B_{1,s}(y)=p_1(s)y+p_0(s).
\tag{8}
\]
They retain the lower ray for control 0 and the upper ray for control 1. Radial outputs remain in [0,1]. Assign a tie to 0 and otherwise choose the unique feasible branch at the current state. This yields an infinite exactly feasible input for every state of Q. The vertex is fixed. The branching threshold actually varies with radius when ε>0.

## 3. Derived cumulative comparison and genuine curved cylinders

For a word w of length l and initial radius s∈[0,1], let s_0=s, s_{k+1}=g_{w_{k+1}}(s_k), and define
\[
P_w(s)=\prod_{k=0}^{l-1}p_{w_{k+1}}(s_k),\qquad
\lambda_w=\prod_{j=1}^{l}a_{w_j},\qquad P_\varnothing=\lambda_\varnothing=1.
\]
The radii depend on the word but not on the initial angle, and
\[
s_l=s P_w(s)^\beta,\qquad 0\le s_k\le r^k s.
\tag{9}
\]
Since |p_i(s_k)−a_i|≤εs_k and the logarithm has derivative at most 1/underline p on the relevant range,
\[
|\ln(P_w(s)/\lambda_w)|\le
\frac{\epsilon}{\underline p}\sum_{k<l}s_k
\le B:=\frac{\epsilon}{\underline p(1-r)}.
\]
Consequently, with D=e^B,
\[
D^{-1}\lambda_w\le P_w(s)\le D\lambda_w
\quad\text{uniformly over all }s\in[0,1],w,l.
\tag{10}
\]
This is proved from the maps, not assumed as bounded distortion. For reference (5) also gives |∂_s lnP_w(s)|≤ε/[underline p(1−q)], by differentiating the product and using s_k′≤q^k. No covering estimate follows merely from this derivative bound.

Let I_w(s) be the complete exact feasible initial-angle interval for w at initial radius s. Induction retaining every intermediate constraint gives
\[
I_{iv}(s)=B_{i,s}(I_v(g_i(s))),\qquad |I_w(s)|=2P_w(s).
\tag{11}
\]
Indeed the inverse image of a subset of [-1,1] under T_{i,s} is in its feasible domain, and the remaining radius is g_i(s). These intervals cover [-1,1] with disjoint interiors at each depth. The same is true for every complete prefix-free leaf family. All closed endpoints are retained. The final angle map T_{w,s} is affine of slope P_w(s)^−1.

Thus actual cylinders are curved strips
\(\mathcal Q_w=\{(s,sy):0<s\le1,y\in I_w(s)\}\), together with the vertex if desired. Their endpoints are smooth functions of s for each finite word. The physical Jacobian s yields
\[
\operatorname{area}(\mathcal Q_w)=\int_0^1 2sP_w(s)\,ds
\in[D^{-1}\lambda_w,D\lambda_w].
\tag{12}
\]
There is no assumption that a word has one angle interval independent of s. Boundary curves have area zero but remain in all covering catalogues.

## 4. Arbitrary approximate inputs and the full-horizon area estimate

For an arbitrary word u of length n, let V(n,δ,u) be the actual states in Q for which u satisfies the constraints at all times 0,…,n. No exact feasibility of u is imposed.

Compare u with the assigned exact control of an actual state (s,sy), s>0. If the first difference is at j, let a=u_1…u_{j−1}, i=u_j, and
\[
b_a(s)=T_{a,s}^{-1}(\xi(s_{j-1})).
\]
At that time the wrong branch takes the angle outside [-1,1], with the exact identity
\[
|y_j|-1=\frac{|y-b_a(s)|}{P_{ai}(s)},\qquad
s_j=sP_{ai}(s)^\beta.
\tag{13}
\]
For a tie this excess is zero and the ensuing band includes the boundary. A necessary condition for a state (s_j,z_j) in Q^δ is |z_j|−s_j<2δ. Therefore every covered first-difference point is in a one-sided radius-dependent band
\[
|y-b_a(s)|<\frac{2\delta}{sP_{ai}(s)^{\beta-1}}
\le\frac{C_b\delta\lambda_a^{1-\beta}}s,
\quad C_b=2D^{\beta-1}a_{\min}^{1-\beta}.
\tag{14}
\]
Integrating its width against s ds gives covered area at most C_bδλ_a^(1−β). The centre may move with s; the bound is on each physical fibre and hence remains valid. No positive lower bound on initial radius is used. Later reentry cannot remove the constraint at the first difference.

For example stop a given u at its first reference product λ≤δ^(1/β), or at n. The agreement area is at most D(δ^(1/β)+a_max^n). Earlier differences satisfy λ_a>δ^(1/β), and summing their inverse products backwards bounds the bands by
\[
\operatorname{area}V(n,\delta,u)\le D a_{\max}^n+
\left[D+\frac{C_b}{1-a_{\max}^{\beta-1}}\right]\delta^{1/\beta}.
\tag{15}
\]
This is an actual-input estimate. It does not declare a prescribed code optimal.

For the sharper typical estimate used below, suppose a fixed positive-area compact T consists of states with uniform reference-product behaviour: for each 0<η<h some D_η≥1 satisfies
\[
D_\eta^{-1}e^{-(h+\eta)k}\le\lambda_{c_k(x)}
\le D_\eta e^{-(h-\eta)k}\quad(x\in T,k\ge0),
\tag{16}
\]
where c_k(x) is its assigned exact prefix. Section 6 constructs T from actual Lebesgue measure; (16) is not a hypothesis of the theorem.

Agreement with u through m≤n occupies at most the curved cylinder Q_{u|m}. If it meets T, (12) and (16) bound its area by DD_ηe^−(h−η)m. A first-difference class j≤m, if nonempty on T, has the actual common prefix of a point in T; hence (16) bounds λ_a from below. Sum (14) to obtain, uniformly in u,n,m,δ,
\[
\operatorname{area}(T\cap V(n,\delta,u))\le
C_\eta[e^{-(h-\eta)m}+\delta e^{(\beta-1)(h+\eta)m}].
\tag{17}
\]
Empty classes contribute zero. All these arguments retain the preceding exact constraints, the required first-deviation time and the permitted later behaviour.

## 5. True catalogue versus reference stopping: full tail and midpoint witnesses

Let L(n,t) be all words stopped at the first reference λ_w≤t, or at depth n if no earlier crossing occurs; let N(n,t)=#L(n,t). This reference product tree is a counting tool only. Every leaf satisfies λ_{w^-}>t and λ_w>a_min t. Its λ weights sum to one because a_0+a_1=1 and the family is complete and prefix-free. Hence N(n,t)≤(a_min t)^−1.

Set
\[
C_0=2\sqrt2 M D^\beta,\qquad
B_0=\lceil1+D^\beta a_{\min}^{-\beta}\rceil.
\]
**Lemma 19.2 (real-catalogue comparison).** For every n≥1 and 0<δ<1,
\[
\frac{N(n,\delta^{1/\beta})}{1+B_0n}\le r_G(n,\delta;Q)
\le N(n,(\delta/C_0)^{1/\beta})
\le C_U\delta^{-1/\beta}.
\tag{18}
\]

For the upper bound use each leaf at t=(δ/C_0)^(1/β) as one exact prefix followed by an arbitrary fixed infinite tail. At every actual initial radius, (11) makes the leaf intervals a complete exact cover. A depth-n leaf satisfies all required constraints exactly. At an earlier stopping time, (9)–(10) give s_l≤D^βt^β and |z_l|≤s_l. Its norm is at most MD^βδ/C_0=δ/(2√2). Every later input obeys (7), so the entire remaining trajectory is within δ/2 of the origin in Q. This includes every endpoint, the vertex and all initial radii; it is not an almost-everywhere catalogue. The leaf count gives C_U=a_min^−1 C_0^(1/β). Exact length-n prefixes also give r_G≤2^n.

For the lower bound set t=δ^(1/β). Choose the actual witness (1,y_w) at the midpoint of I_w(1) for each reference leaf. By (10)–(11), every such interval has length greater than 2D^−1 a_min t. Ordered midpoints of these disjoint-interior intervals have the same lower spacing bound.

For any arbitrary length-n control u, at most one leaf is its prefix. Every other covered witness has a first difference at j≤|w|, with common a=u|j−1 and λ_a>t. At s=1 the centre b_a(1) and the side in (14) are fixed by u,j. Its band length is at most C_b t. The midpoint spacing limits its count to 1+D^βa_min^−β, hence to B_0. Summing over j≤n gives at most 1+B_0n witnesses per arbitrary control. Every catalogue for all Q must cover these actual states, proving (18). Later reentry has not been forbidden; the necessary constraint at j still applies.

The loss in (18) is polynomial, not an assumed quasi-multiplicativity or an assertion that exact natural words are an optimal catalogue. It is the missing controlled step beyond mere product comparison.

## 6. Physical typical sets and the universal low side

For normalized physical area on Q, (12) bounds the probability of any assigned length-k word by Dλ_w. The countably many finite-word boundary curves and the vertex have zero area. With zero frequency t=j/k, the elementary binomial bound gives
\[
\mu\{|j/k-a_0|\ge\eta\}\le
D(k+1)e^{-2\eta^2 k}.
\tag{19}
\]
Indeed a type has weight at most D binom(k,j)a_0^j a_1^(k−j)≤Dexp[−k D_KL(t∥a_0)], and D_KL(t∥a_0)≥2(t−a_0)². Summation, Borel–Cantelli and a countable sequence of η prove frequency tending to a_0 for physical-almost-every state. Independence of these state-dependent digits is neither true by definition nor needed. This distinction from R15 is essential.

For any given positive-area compact K, Egorov and inner regularity select one compact T⊂K of positive area, avoiding the null boundary set, with uniform frequency convergence. It is fixed before choosing γ or δ_n. This implies (16), absorbing finitely many early times into D_η.

For small δ take
\[
m=\min\{n,\lfloor-\ln\delta/[\beta(h+\eta)]\rfloor\}.
\]
Then δexp[β(h+η)m]≤1. Equation (17) bounds the area covered by one arbitrary input by 2C_ηexp[−(h−η)m]. Every catalogue spanning K must span T, so
\[
r_G(n,\delta;K)\ge\frac{\operatorname{area}(T)}{2C_\eta}e^{(h-\eta)m}.
\tag{20}
\]
For a sequence with exponent γ, taking rates and then η↓0 yields min(h,γ/β) as lower bound. Equation (18) and r_G≤2^n give the upper bound in (3). They match at γ/β when γ≤βh, including equality at the boundary and γ=0. No monotonicity of the precision sequence is used.

## 7. One fixed near-full-area set and strict high-side separation

Apply Egorov and inner regularity once on Q to obtain compact T_ζ of area>1−ζ, outside the null boundary set, with uniform frequency convergence. Set K_ζ=T_ζ∪{0}. It is compact and chosen before γ and all precision sequences. The added vertex does not have to satisfy the frequency property: it is covered separately by one input.

For every η>0 and sufficiently large n, every length-n natural prefix realized on T_ζ has frequency within η of a_0. The number of such words is at most
\[
(n+1)\exp\{n\max_{|t-a_0|\le\eta}H(t)\}.
\tag{21}
\]
Use them as exact length-n prefixes, each with an infinite extension, and include the vertex input. This covers all of K_ζ at every required time, for every δ>0. Continuity of H gives upper rate h for every precision sequence. For finite γ>βh, (3) supplies lower rate h on this same positive-area set. Thus its limit is h for every high-side exponent.

For full Q fix γ>βh. Let
\[
\Delta=\chi(1/2)-h=(a_0-1/2)\ln(a_0/a_1)>0,
\quad \theta=\min\{1/2,(\gamma/\beta-h)/(2\Delta)\},
\quad t_\gamma=(1-\theta)a_0+\theta/2.
\]
Then χ(t_γ)<γ/β and H(t_γ)>h. Choose integers j_n/n→t_γ. Every length-n word of that type has total reference cost nχ(j_n/n)<−ln(δ_n)/β eventually; each proper prefix has lower cost, so all these words are terminal leaves of L(n,δ_n^(1/β)). Using the standard type bound binom(n,j)≥exp[nH(j/n)]/(n+1) in (18),
\[
r_G(n,\delta_n;Q)\ge
\frac{\exp[nH(j_n/n)]}{(n+1)(1+B_0n)}.
\tag{22}
\]
Hence the full-Q lower rate is at least H(t_γ)>h. This proves (4) with the simultaneous quantifiers stated in §1. The gap may depend on γ and vanish as γ decreases to βh; no uniform positive gap is claimed. The type bound follows, for example, because j is a mode of the binomial law with parameter j/n and its mass is at least 1/(n+1); endpoint cases are immediate.

## 8. No Q-preserving coordinate reduction, even topological

This check addresses the actual constrained system, rather than an arbitrary change of ambient constraint. Let A_0,A_1 be the R17 linear maps, and suppose an injective continuous coordinate change H maps Q onto Q and simultaneously conjugates G_i to A_i, possibly permuting labels, on a domain containing the needed images.

For G_0, the states remaining in Q under the constant input 0 forever are exactly its lower ray S_0={(s,−s):0≤s≤1}. Indeed y+1 is multiplied at every step by p_0(s_k)^−1≥overline p^−1>1; any y>−1 eventually exceeds the upper feasible boundary. Similarly S_1 is the upper ray. The same characterization holds for A_i. Thus H sends these rays to the corresponding constant-input rays, according to the label permutation, and fixes their common vertex. Let f_−,f_+:[0,1]→[0,1] be the first-coordinate homeomorphisms along the two actual rays, and let τ_0,τ_1 be the positive target radial factors. They satisfy
\[
f_-(g_0(s))=\tau_0 f_-(s),\qquad
f_+(g_1(s))=\tau_1 f_+(s).
\tag{23}
\]

The state x_s=(s,sξ(s)) admits both controls: G_0x_s=(g_0(s),g_0(s)) and G_1x_s=(g_1(s),−g_1(s)). H must send the intersection of the two feasible domains to the corresponding R17 dividing ray. If its image has radial coordinate R(s), then, with either label permutation,
\[
f_+(g_0(s))=\tau_0 R(s),\qquad
f_-(g_1(s))=\tau_1 R(s).
\tag{24}
\]
Consequently for small positive s, with \(L_*=g_1\circ g_0^{-1}\),
\(f_+=(\tau_0/\tau_1) f_-\circ L_*\).
Combining with the second equation of (23) shows
\[
f_-\circ h_1=\tau_1 f_-,\qquad h_1=L_*\circ g_1\circ L_*^{-1}.
\tag{25}
\]
Thus the injective f_− would simultaneously conjugate g_0 and h_1 to two commuting scalar contractions. It follows that g_0∘h_1=h_1∘g_0 near zero. No derivative of H is assumed in this implication.

We now disprove that equality directly from the given maps. Write
\[
\rho_i=a_i^\beta,\qquad
g_i(s)=\rho_i s+b_i s^2+O(s^3),
\quad b_0=\beta\epsilon a_0^{\beta-1}>0,\quad
b_1=-\beta\epsilon a_1^{\beta-1}<0.
\]
Taylor expansion of the local inverses and compositions gives
\[
h_1(s)=\rho_1s+\widetilde b_1s^2+O(s^3),\qquad
\widetilde b_1=b_1(\rho_0+\rho_1-1)/\rho_1+b_0(1-\rho_1)/\rho_0.
\]
For clarity the intermediate expansion is
\(L_*(s)=(\rho_1/\rho_0)s+[(b_1\rho_0-\rho_1b_0)/\rho_0^3]s^2+O(s^3)\); substituting it and its inverse yields the displayed coefficient. Therefore
\[
(g_0\circ h_1-h_1\circ g_0)(s)=C s^2+O(s^3),
\]
\[
C=(\rho_0+\rho_1-1)
\left[\frac{\rho_0(1-\rho_0)b_1}{\rho_1}-b_0(1-\rho_1)\right]>0.
\tag{26}
\]
Here ρ_0+ρ_1<1 follows from β>1 and a_0+a_1=1; the bracket is strictly negative. Hence the two radial maps do not commute on sufficiently small positive s, contradicting (25). This proves (c). The boundary argument excludes Q-preserving homeomorphisms, and thus both regular coordinate classes requested; it does not assert nonexistence of all conceivable unconstrained ambient conjugacies.

## 9. What has and has not transferred

The proof establishes the exact common-cost boundary for the prescribed reversible nonlinear class. Unlike R18, no positive-area set is collapsed in finite time; (6) is everywhere positive. Unlike R17, initial-angle cylinders move with radius and digits are not assumed independent. Derived uniform cylinder comparison, fibrewise first-deviation integration, and actual midpoint spacing close the real-catalogue interface. The transfer therefore exceeds an unverified replacement of parameters, and §8 prevents a Q-preserving coordinate dismissal.

It remains a specialized triangular class with exact instantaneous matching between branch proportions and radial factors. The bounded-error argument, typical sets, type counts, stopping scales and entropy optimization are classical. This is a checked nonlinear extension of the project's sufficient regime, not a general theorem that invertibility or first-order matching suffices. It does not solve overlap systems, arbitrary nonlinear perturbations, the high-side full-Q spectrum, or the paused κ problem. Its priority and independent publication weight remain subject to the actual literature scope in SOURCES.md. The existing unique paper is unchanged. ∎
