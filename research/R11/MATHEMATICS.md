# R11: subexponential geometric recoding, with the cost deficit retained

4 October 2026. Natural logarithms. This is one bounded attack on the R10 comparison for the same fixed system. The comparison is **unresolved**: neither rate optimality of the specified selector nor a positive exponential gap has been proved. The completed interface below separates geometric fragmentation from a genuinely unestimated stopping-cost deficit.

## 1. Fixed objects and the one proved interface

Retain

$$
q=2-2^{-20},\quad \rho_0=1/4,\quad\rho_1=1/256,\qquad
T_0(y)=qy+q/2,\quad T_1(y)=qy-q/2,
$$

$$
F_i(s,z)=(\rho_i s,\rho_i T_i(z/s)s),\qquad
Q=K=\{0\le s\le1,\ |z|\le s\}.
$$

The displayed expression for positive \(s\) denotes the original linear maps, which fix the vertex. All binary controls are allowed. The genuine catalogue assigns controls to actual initial states, uses the Euclidean environment distance, and requires all times \(0,\ldots,n\) to lie in the open \(2^{-n}\)-neighborhood of \(Q\). Exits and returns remain allowed. These objects have not been replaced by a policy partition.

For a finite word \(w\), let

$$
c(w)=\#_0(w)+4\#_1(w),\qquad
I_w=\{y\in[-1,1]:T_{w_k}\cdots T_{w_1}(y)\in[-1,1]
\text{ for every }1\le k\le |w|\}.
$$

Let \(N_m\) be the smallest cardinality of a family of cost-at-least-\(m\) words whose \(I_w\) cover all \([-1,1]\). Every intermediate constraint belongs to \(I_w\). Empty feasible intervals are discarded from every cover used below, without losing coverage or increasing its size. R09's normalization at first cost crossing permits a minimizing family consisting of words with

$$
m\le c(w)\le m+3,\qquad \lceil m/4\rceil\le |w|\le m. \tag{1}
$$

Put \(b=1/q-1/2\), and use exactly the authorized selector

$$
\pi_0(y)=\begin{cases}0,&y\le b,\\1,&y>b,\end{cases}
\qquad f(y)=T_{\pi_0(y)}(y).
$$

Write \(p_l(y)\) for its first \(l\) inputs. Let \(G_m\) count the distinct first-cost-\(m\) prefixes generated from all actual \(y\in[-1,1]\); set \(G_0=1\). Counts include every actual boundary itinerary. A policy cylinder

$$
C_v=\{y\in[-1,1]:p_{|v|}(y)=v\}
$$

is an interval, possibly half-open or a singleton, and \(C_v\subset I_v\); equality is not assumed.

For each nonempty \(I_w\) in a normalized threshold family, define the integer deficit

$$
D_m(w)=\max_{y\in I_w}\big(m-c(p_{|w|}(y))\big)_+. \tag{2}
$$

This maximum exists because only finitely many policy prefixes of length \(|w|\) occur. It measures a difference in contraction cost at the same elapsed time, not a distance or a covering rate. In particular

$$
0\le D_m(w)\le m-|w|\le\lfloor3m/4\rfloor. \tag{3}
$$

**Theorem 11.1 (geometric recoding with an explicit residual budget).** For the fixed data above:

(a) For every \(\eta>0\) there is \(A_\eta<\infty\), independent of \(l,J,w,m\), such that, for every integer \(l\ge1\) and every interval \(J\subset[-1,1]\) with diameter at most \(2q^{-l}\),

$$
\#\{p_l(y):y\in J\}\le A_\eta e^{\eta l}. \tag{4}
$$

All actual endpoints and singleton pieces are included.

(b) For every \(m\ge1\) and every normalized exact threshold cover \(\mathcal W\) of all \([-1,1]\),

$$
N_m\le G_m\le A_\eta e^{\eta m}
\sum_{w\in\mathcal W}G_{D_m(w)}. \tag{5}
$$

The right-hand side retains the different remaining budgets; it does not assert that they vanish. If

$$
\Delta_m=\min_{\substack{\mathcal W\text{ normalized exact cover}\\
|\mathcal W|=N_m}}\ \max_{w\in\mathcal W}D_m(w),
$$

then

$$
G_m\le A_\eta e^{\eta m}N_mG_{\Delta_m}. \tag{6}
$$

Consequently \(\Delta_m=o(m)\) would imply the requested comparison. This condition is proved to be sufficient, **not** necessary, and is itself unproved.

(c) The selector count has a finite rate

$$
g=\lim_m\frac{\ln G_m}{m}=\inf_{m\ge1}\frac{\ln G_m}{m}.
$$

With the already proved R09 rate \(\kappa=\lim_m\ln N_m/m\),

$$
0\le g-\kappa\le g\limsup_m\frac{\Delta_m}{m}. \tag{7}
$$

No new numerical bound for \(\kappa\) follows, since no suitable estimate of \(\Delta_m\) has been obtained. Existence of \(g\) uses the classical concatenation argument, not a new pressure formula.

## 2. Feasibility, actual cylinders and their scale

One-step feasibility gives \(D_0=[-1,b]\), \(D_1=[-b,1]\). The chosen policy satisfies

$$
T_0([-1,b])=[-q/2,1],\qquad
T_1((b,1])=(1-q,q/2]\subset[-1,1].
$$

It is therefore defined and exactly feasible for every actual initial ratio for all future times, including \(y=b\). At positive radius, \(s_k=4^{-c(p_k)}s\le1\), so the corresponding actual cone states stay in \(Q\) at every prefix time; the vertex remains fixed.

On a fixed policy prefix \(v\), each intermediate ratio is an increasing affine function of the initial ratio, with slope \(q^k\). Each decision is a half-line condition on this function: \(\le b\) for 0, \(>b\) for 1. Their intersection with \([-1,1]\) is an interval. This establishes the cylinder assertion without closing the strict inequalities or discarding their endpoints.

Independently, \(I_w\) is a closed interval, as an intersection of all its closed intermediate preimages. Its final affine map has slope \(q^{|w|}\) and sends it into \([-1,1]\). Hence

$$
\operatorname{diam}I_w\le2q^{-|w|}. \tag{8}
$$

The final constraint proves this upper estimate; none of the preceding constraints has been removed from the definition of \(I_w\).

## 3. Uniform subexponential fragmentation: proof of (4)

Fix a positive integer block length \(L\). Form a finite set \(B_L\) consisting of \(-1,1\) and all points in \([-1,1]\) of the form

$$
T_{v_k}\cdots T_{v_1}(y)=b,
\qquad 0\le k<L,\quad v\in\{0,1\}^k. \tag{9}
$$

For \(k=0\) this means \(y=b\). Each affine equation has one solution. Extraneous solutions whose preceding controls are not feasible are harmless: they only enlarge the finite set.

On every component of \([-1,1]\setminus B_L\), the first \(L\) policy decisions are constant. Indeed, if two decisions first differ, continuity of the common preceding affine branch places a preimage of \(b\) between the corresponding initial ratios; this is one of (9). Let \(d_L>0\) be the minimum distance between distinct points of \(B_L\).

An interval of diameter less than \(d_L\) meets at most one point of \(B_L\). It therefore produces at most three distinct length-\(L\) policy prefixes: one from each side and, if needed, a separate actual itinerary at that point. The bound three deliberately includes every tie and singleton. It is not a claim that boundary itineraries may be ignored.

Choose an integer \(h_L\ge0\) with

$$
2q^{-h_L}<d_L. \tag{10}
$$

Start with an interval \(J\) as in (4). After restricting to any one actual prefix of length \(j\), its current image is an interval of diameter at most

$$
q^j\operatorname{diam}J\le2q^{j-l}.
$$

For \(j\le l-h_L\), this diameter is less than \(d_L\), by (10). Refining such a current interval by the next block of \(L\) decisions creates at most three nonempty prefix pieces. Each piece is again an interval, and its current affine slope continues to be the appropriate power of \(q\). No sum of their lengths or separation of their images is assumed.

Use

$$
t=\left\lfloor\frac{(l-h_L)_+}{L}\right\rfloor
$$

full blocks. The number of pieces is at most \(3^t\). The remaining number of inputs is less than \(h_L+L\) if \(l\ge h_L\), and less than \(h_L\) otherwise; at most \(2^{h_L+L}\) continuations suffice in either case. Thus, for all \(l,J\),

$$
\#\{p_l(y):y\in J\}\le2^{h_L+L}3^{l/L}. \tag{11}
$$

Given \(\eta>0\), choose \(L\) with \(\ln3/L\le\eta\), and set \(A_\eta=2^{h_L+L}\). This proves (4).

The finite set \(B_L\) is used for each separately chosen block length, followed by an arbitrary number of blocks. It is **not** a finite-state model of the whole language. Its spacing can be very small, and no bound uniform in \(L\), no finite orbit of the discontinuity, and no pressure-root representation are needed. Formula (11) is an analytic all-length proof, not a finite enumeration.

This is a fixed-block multiplicity argument of an existing kind; its method is not asserted to be original. SOURCES.md identifies the directly read precedent. Here it is applied to the actual controlled intervals (8), with the stopping budget treated separately below.

## 4. Recoding the entire initial-state cover: proof of (5)–(6)

First \(G_d\) is nondecreasing for integer \(d\ge0\). For \(d\le D\), every first-cost-\(d\) prefix has a realizing initial state and extends along its infinite feasible policy orbit to a first-cost-\(D\) prefix. Taking the first-cost-\(d\) ancestor of a first-cost-\(D\) prefix gives a surjection. Therefore \(G_d\le G_D\), including \(d=0\).

Fix a nonempty normalized feasible interval \(I_w\), and put \(l=|w|\). By (8) and (4), it realizes at most \(A_\eta e^{\eta l}\) distinct length-\(l\) policy prefixes. Restrict to one such prefix \(v\).

If \(c(v)\ge m\), its first-cost-\(m\) ancestor is uniquely determined. If \(c(v)<m\), the current ratios of the actual points in \(I_w\cap C_v\) belong to \([-1,1]\). Their further policy stopping words are among those generated on the full interval at remaining cost \(m-c(v)\), and so number at most

$$
G_{m-c(v)}\le G_{D_m(w)}.
$$

The completed prefix is feasible through all its newly used times because it follows \(f\), not a reused suffix of \(w\). Every actual boundary point of \(I_w\cap C_v\) is included. As \(G_0=1\), the same bound also covers prefixes already stopped. Thus

$$
\#\{\text{first-cost-}m\text{ policy prefixes realized on }I_w\}
\le A_\eta e^{\eta l}G_{D_m(w)}. \tag{12}
$$

Every first-cost-\(m\) policy prefix has an actual realizing initial ratio. Since \(\mathcal W\) covers all \([-1,1]\), that ratio lies in at least one \(I_w\) in the family. Sum (12), use \(l\le m\) from (1), and obtain the upper bound (5). Double counting on overlaps only enlarges the right-hand side. Conversely the actual policy prefixes themselves are exactly feasible threshold words covering all actual ratios, which proves \(N_m\le G_m\).

The set of normalized threshold words is finite. Consequently the set of normalized minimizing families is finite and nonempty, and \(\Delta_m\) is attained. Choose such a family realizing \(\Delta_m\) in (5), use monotonicity of \(G_d\), and obtain (6).

No alternative coding was declared optimal. No policy cell was identified with a full feasible interval. The cardinality of an arbitrary genuine exact cover is retained, and every extra continuation carries its own residual contraction budget.

## 5. The rate consequence, without an optimality conclusion

For \(m,j\ge1\), split any actual first-cost-\((m+j)\) policy word at its first crossing of \(m\). There are at most \(G_m\) initial pieces. If one has cost \(m+a\), \(0\le a\le3\), its remaining suffix is a policy first crossing of \(j-a\) if \(j>a\), and empty otherwise. From its actual endpoint the number is at most \(G_j\), by monotonicity. Hence

$$
G_{m+j}\le G_mG_j. \tag{13}
$$

The counts are finite, nondecreasing and positive: words stop by time \(m\), and \(G_m\le\sum_{l=1}^m2^l<2^{m+1}\). The classical subadditivity proof applied to \(\ln G_m\) establishes \(g\) in (c); this does not evaluate \(g\).

For each \(\theta>0\), the existence of \(g\) gives a finite \(C_\theta\) such that

$$
\ln G_d\le(g+\theta)d+C_\theta\qquad(d\ge0). \tag{14}
$$

Taking logarithms in (6) and using (14),

$$
0\le\ln G_m-\ln N_m
\le\ln A_\eta+\eta m+(g+\theta)\Delta_m+C_\theta.
$$

Divide by \(m\), use R09's already established limit for \(N_m\), and then let \(\eta,\theta\downarrow0\). This proves (7). In particular, if \(\Delta_m=o(m)\), the requested inequality \(G_m\le e^{\eta m}N_m\) holds eventually for every \(\eta>0\).

The stronger uniform deficit condition is not needed in the proof of (5). A more flexible sufficient condition would be a choice of normalized minimizing covers \(\mathcal W_m\) with

$$
\ln\left(\frac1{N_m}\sum_{w\in\mathcal W_m}G_{D_m(w)}\right)=o(m). \tag{15}
$$

Neither (15) nor \(\Delta_m=o(m)\) has been proved. Failure of either sufficient condition would **not** disprove the original comparison: (12) uses the entire interval for the remaining continuation and can overcount. Equation (15) is a remaining proof interface, not a proved equivalence or an assumption of Theorem 11.1. This completes that theorem. ∎

## 6. What the remaining deficit means dynamically

For \(y\in I_w\), \(l=|w|\), let \(y_k^w\) be its controlled ratios under \(w\), \(y_k^\pi=f^k(y)\), and \(d_k=y_k^\pi-y_k^w\). Both trajectories are actually feasible through all \(l\) times, so \(d_0=0\) and \(|d_k|\le2\). Directly from the maps,

$$
d_{k+1}=qd_k-q(\pi_{k+1}-w_{k+1}),
$$

where inputs are read as 0 or 1. Since a length-\(l\) word has cost \(l+3\#_1\), telescoping gives the exact identity

$$
c(p_l(y))-c(w)
=\frac{3(q-1)}q\sum_{k=1}^{l-1}d_k-\frac3q d_l. \tag{16}
$$

In particular, (2) is the maximum over the actual interval of

$$
\left(m-c(w)-\frac{3(q-1)}q\sum_{k=1}^{l-1}d_k+\frac3q d_l\right)_+.
$$

Thus the obstruction is an accumulated controlled-state discrepancy, not merely the final small displacement. Boundedness of each \(d_k\) gives only a linear estimate, which is insufficient for (15). No sign or sublinear lower bound for that accumulated sum on minimizing covers was established in this attack.

The R10 blocks have different costs 81 and 24, and endpoint ratios \(\Lambda y\pm p\). Their fixed nonzero shift is fully compatible with (4): the bound counts new continuations at the same elapsed time, and never substitutes the same suffix. A finite initial cost advantage alone does not bound the future sum in (16). Nor does R10's common-tail counterexample give a positive global gap \(g-\kappa\).

The one remaining authorized objective is still

$$
\ln G_m-\ln N_m=o(m).
$$

This round has proved (5), with no missing boundary states or intermediate feasibility conditions, but has not controlled its residual-budget factor. There is no matching optimal-rate proof or strict exponential counterexample. The accurate value of \(\kappa\) remains unknown; R09's two different bounds and \(H=\kappa/2\) remain unchanged.

## 7. Dependency check and contribution boundary

R09 MATHEMATICS §§2–5 were restored in full for the actual interval, first-exit repair, full-horizon tail, threshold normalization and genuine catalogue comparison. The first-exit pieces and their replacement intervals, the uniform local suffix bound, the prefix lengths and the later Euclidean tolerance were checked at their used steps; no affecting error was found. Their proofs are not reproduced as new R11 results. R10 Theorem 10.1 and its mixed translated-cover identities were read in full; the current argument retains its unequal budgets and does not reverse its counterexample.

The subexponential fixed-block argument and concatenation are existing methods. The project increment is a full-time, all-state recoding inequality comparing an arbitrary genuine exact catalogue with the specified selector, with its unestimated costs displayed rather than silently set to zero. It narrows the proof obstruction but does not establish rate optimality, a sharper bound, an accurate constant or an independent new main theorem for the stage paper. No journal-tier increase or full-literature priority is claimed.
