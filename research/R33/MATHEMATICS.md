# R33: noninjectivity, null critical sets, and actual precision costs

2026-10-06 UTC. Pinned mathematical and manuscript baseline:
a8712bcbcffd3d1983e37cb9eb195a8906a858c2.
The unique manuscript remains the R32 manuscript. This note proves the
authorized weakening of its finite-transient hypothesis; it does not
introduce a different entropy or an additional research route.
Area means two-dimensional Lebesgue measure, and logarithms are natural.

## 1. Class, actual object, and complete conclusion

Fix
\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,\qquad
\beta_0,\beta_1>1,\quad \rho_i=a_i^{\beta_i},\quad t_i=\rho_i/a_i<1.
\]
Here the powers are allowed either to agree or to differ. Define
\[
A_0=\begin{pmatrix}\rho_0&0\\t_0a_1&t_0\end{pmatrix},\qquad
A_1=\begin{pmatrix}\rho_1&0\\-t_1a_0&t_1\end{pmatrix},\qquad
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\quad |Q|=1.
\tag{33.1}
\]
The actual maps \(F_i:\mathbb R^2\to\mathbb R^2\) satisfy:

1. \(F_i\) is \(C^2\), \(F_i(0)=0\), and \(DF_i(0)=A_i\).
2. \(Q\subset F_0^{-1}Q\cup F_1^{-1}Q\).
3. For some \(\Lambda\ge1\) and \(0<\theta<1\),
   \[
   V(s,z)=\max\{\Lambda|s|,|z|\},\qquad
   V(F_i x)\le\theta V(x)\quad(x\in\mathbb R^2,\ i=0,1).
   \tag{33.2}
   \]
4. Each closed critical set
   \[
   C_i=\{x\in Q:\det DF_i(x)=0\}
   \tag{33.3}
   \]
   has area zero.

There is no global injectivity, inverse-map, bounded inverse-Jacobian,
finite-global-multiplicity, or two-point contraction assumption.
In particular (33.2) is only a norm inequality toward the origin.
No condition on the critical sets outside \(Q\) is imposed.

All infinite binary inputs are allowed. Put
\[
F_u^0=\operatorname{id},\quad F_u^k=F_{u_k}\circ\cdots\circ F_{u_1},
\qquad
A_u(n,\delta;K)=\{x\in K:\operatorname{dist}_2(F_u^kx,Q)<\delta
                       \ (0\le k\le n)\}.
\tag{33.4}
\]
For a nonempty compact \(K\subset Q\), \(r_F(n,\delta;K)\) is the
minimum number of these infinite inputs whose sets cover every actual
point of \(K\). The input assignment may depend on the state. Exit and
reentry are allowed, subject to each intermediate constraint in (33.4).
Controlled feasibility gives \(1\le r_F\le2^n\).

Use
\[
\lambda_w=\prod_{j=1}^{|w|}a_{w_j},\quad
P_w=\prod_{j=1}^{|w|}\rho_{w_j},\quad
h=-\sum_i a_i\log a_i,\quad
\chi_R=-\sum_i a_i\log\rho_i>h,\quad
\gamma_0=-\log\max_i\rho_i.
\tag{33.5}
\]
Products for the empty word equal one. Let \(D\in(0,1)\) be the unique
root of \(\rho_0^D+\rho_1^D=1\).

**Theorem 33.1 (noncollapsing finite-transient extension).**
For every fixed pair satisfying assumptions 1–4 above, all the following hold.
Every precision sequence in the statements is positive, tends to zero,
and satisfies \(-\log\delta_n/n\to\gamma\); monotonicity is not required.

**Matched case.** If \(\beta_0=\beta_1=\beta\), set
\[
H_b(p)=-p\log p-(1-p)\log(1-p),\quad
\chi_A(p)=-p\log a_0-(1-p)\log a_1,\quad
S(\gamma)=\max_{p\in[0,1]}H_b(p)
                   \min\{1,\gamma/[\beta\chi_A(p)]\},
\tag{33.6}
\]
with \(0\log0=0\). For every finite \(\gamma\ge0\) and every sequence
of that exponent,
\[
\lim_n n^{-1}\log r_F(n,\delta_n;Q)=S(\gamma).
\tag{33.7}
\]
Every fixed positive-area compact \(K\subset Q\) has
\[
\min\{h,\gamma/\beta\}\le
\liminf_n n^{-1}\log r_F(n,\delta_n;K)\le
\limsup_n n^{-1}\log r_F(n,\delta_n;K)\le S(\gamma).
\tag{33.8}
\]
Consequently its limit is \(\gamma/\beta\) for
\(0\le\gamma\le\beta h\). For every \(\zeta\in(0,1)\) there is
one fixed compact \(K_\zeta\subset Q\), of area greater than
\(1-\zeta\), such that, simultaneously for every finite
\(\gamma\ge0\) and every sequence of that exponent,
\[
\lim_n n^{-1}\log r_F(n,\delta_n;K_\zeta)=\min\{h,\gamma/\beta\}.
\tag{33.9}
\]
The common-cost and saturation thresholds remain \(\beta h\) and
\(-(\beta/2)\log(a_0a_1)\), respectively; the R32 three-piece formula
and exact gap follow from (33.6) by the same elementary optimisation.

**Mismatched case.** If \(\beta_0\ne\beta_1\), for every
\(\zeta\in(0,1)\) there is one fixed compact \(K_\zeta\subset Q\)
of area greater than \(1-\zeta\) such that, simultaneously for
all \(0<\gamma<\gamma_0\) and all their precision sequences,
\[
\lim_n n^{-1}\log r_F(n,\delta_n;Q)=\gamma D,\qquad
\lim_n n^{-1}\log r_F(n,\delta_n;K_\zeta)
                  =\gamma h/\chi_R<\gamma D.
\tag{33.10}
\]
Every other fixed positive-area compact \(K\subset Q\) has lower
rate at least \(\gamma h/\chi_R\) in this range.

In both cases the near-full compact set is selected before the
exponent, precision sequence, and horizon; it may depend on the
fixed maps and \(\zeta\). Within this specified first-jet family,
all fixed positive-area compact initial sets share an accurate rate
on an interval of positive exponents adjacent to zero if and only
if the two powers agree. This is not a classification of arbitrary
control systems, high-precision mismatch rates, or arbitrary compact
high-side spectra.

The new proof concerns only the finite transient. The local controlled
geometry, physical witnesses, stopping scales, and type optimisation
are the already derived R27/R31/R29 steps. Sections 2–5 replace the
two uses of global inverse maps; Section 6 verifies the deductions,
including the uniform compact-set quantifier.

## 2. Exact feasible domains and null-set pullbacks

For a finite word \(w\), write
\[
D_w=\{x\in Q:F_{w|k}x\in Q\ (1\le k\le |w|)\},
\qquad D_\varnothing=Q.
\tag{33.11}
\]
These are compact sets. Write \(w^-\) for the word with its last
letter removed. To include a first true exit at the last step, the
relevant domain for the map \(F_w\) is \(D_{w^-}\), not just \(D_w\).
This distinction ensures that every derivative factor is evaluated
at a state in \(Q\), even when the last output is outside \(Q\).

**Lemma 33.2 (null pullbacks along feasible prefixes).**
If \(B\subset\mathbb R^2\) is a Lebesgue null set, then
\[
|Q\cap F_i^{-1}B|=0,\qquad
|D_w\cap F_w^{-1}B|=0
\tag{33.12}
\]
for every \(i\) and every finite word \(w\).

**Proof.** At every point of \(Q\setminus C_i\), the inverse
function theorem gives an open inverse chart for \(F_i\). The
regular portion is covered by countably many such charts, using
the countable base of the plane. On any chart the inverse is
\(C^1\), hence locally Lipschitz. Exhaust its open image by
countably many relatively compact subcharts. A Lipschitz map
preserves Lebesgue null sets: cover a bounded null set by squares
with arbitrarily small total area; their images have diameter
bounded by the Lipschitz constant times the square diameter and
are covered by discs with a constant multiple of that total area.
Thus the pullback of \(B\) in each inverse chart is null.
The omitted \(C_i\) is null by (33.3), proving the first assertion.
For a non-Borel null set, apply the argument to a Borel null
superset and use completeness of Lebesgue measure.

Induct on the word length. If \(w=vi\), then
\[
D_w\cap F_w^{-1}B
\subset D_v\cap F_v^{-1}(Q\cap F_i^{-1}B).
\]
The inner set is null by the first assertion, and induction gives
the second. The empty word case is immediate. Every intermediate
state required in this induction belongs to \(Q\). No inverse
branch outside \(Q\), nor any bound on its Jacobian, was used. ∎

**Lemma 33.3 (finite composition critical sets are null).**
For every nonempty word \(w\), the compact set
\[
Z_w=D_{w^-}\cap\{x:\det DF_w(x)=0\}
\tag{33.13}
\]
has area zero.

**Proof.** The chain rule writes the determinant as the product
of \(\det DF_{w_j}(F_{w|j-1}x)\). On \(D_{w^-}\), all these input
states belong to \(Q\). If a factor is zero, then
\[
x\in D_{w|j-1}\cap F_{w|j-1}^{-1}C_{w_j}.
\]
Each set on the right is null by Lemma 33.2 (also for \(j=1\)).
Their finite union contains \(Z_w\). Compactness follows from
continuity of the determinant and closedness of \(D_{w^-}\). ∎

The lemmas also show that an exactly feasible finite prefix cannot
send a positive-area collection of initial states into any given
area-zero set. They do not assert a Jacobian lower bound on all \(Q\),
a global finite multiplicity, or a uniform inverse density.

## 3. A regular compact window for every transient choice

Let \(b>0\) be the fixed local radius obtained from the first jets
and the \(C^2\) Taylor estimates in paper Section 3
(equivalently R31 (31.9)–(31.15)). Put \(Q_b=Q\cap\{s\le b\}\).
Choose one integer \(J\ge1\) satisfying
\[
\theta^J\sup_Q V\le b.
\tag{33.14}
\]
Every exactly feasible \(J\)-prefix then ends in \(Q_b\).
The integer depends only on the fixed system.

**Lemma 33.4 (finite local inverse bound on a fixed window).**
For any positive-area compact \(K\subset Q\) and any
\(0<\varepsilon<|K|\), one can choose a compact \(T\subset
K\setminus\{0\}\) with \(|T|>|K|-\varepsilon\) and a finite
constant \(L_T\) such that for every \(1\le|w|\le J\) and every
Lebesgue measurable \(B\subset\mathbb R^2\),
\[
|T\cap D_{w^-}\cap F_w^{-1}B|\le L_T |B|.
\tag{33.15}
\]
The same \(T\) can additionally be chosen so that, for every
\(e\in(0,h)\), some \(D_e\ge1\) satisfies
\[
\begin{split}
D_e^{-1}e^{-(h+e)|v|}&\le\lambda_v\le D_e e^{-(h-e)|v|},\\
D_e^{-1}e^{-(\chi_R+e)|v|}&\le P_v\le D_e e^{-(\chi_R-e)|v|}
\end{split}
\tag{33.16}
\]
for every exactly feasible \(J\)-prefix from \(T\) and every
subsequent exactly feasible local tail \(v\).
The window precedes \(e\), every input, tolerance, and horizon.
The constant \(L_T\) may depend on this window, the maps, and \(J\).

**Proof.** First verify the local exceptional set without any
global inverse. The derived complete feasible local regions
\(\mathcal I_v\subset Q_b\) have area at most \(C_b\lambda_v\).
Under the reference weights \(\lambda_v\), the length-\(m\)
words whose zero frequency differs from \(a_0\) by more than \(d\)
have total weight at most \(2e^{-2d^2m}\), by the elementary
Bernoulli exponential-moment bound used in R31 Section 5.
Union over their actual complete feasible regions, and
Borel–Cantelli for rational \(d>0\), give a null Borel exceptional
set \(B_{\rm loc}\subset Q_b\), including the origin, outside
which all feasible prefixes have frequencies tending uniformly
to \(a_0\). Overlaps are allowed in this union bound.

By Lemma 33.2, the finite union
\[
B_J=\bigcup_{|\sigma|=J}(D_\sigma\cap F_\sigma^{-1}B_{\rm loc})
\]
is null. Also \(Z_J=\bigcup_{1\le|w|\le J}Z_w\) is a compact
null set by Lemma 33.3. On \(Q\setminus B_J\), controlled
feasibility guarantees a feasible transient and local prefixes,
and the maximum frequency deviation over all feasible transient
choices and all their length-\(m\) tails tends to zero.
This is a measurable function of the actual initial state:
there are finitely many words for each \(J+m\), with closed
complete feasibility domains. Taking all these words, rather
than a selected strategy, is essential.

Apply Egorov on \(K\), losing less than \(\varepsilon/2\) of
area, for this single convergence. Remove \(B_J\cup Z_J\cup\{0\}\).
Compact inner approximation supplies \(T\) with the claimed
area, with uniform convergence and disjoint from these sets.
The selection has made no precision choice. Both logarithmic
products in (33.16) are affine functions of frequency.
Uniform convergence therefore gives (33.16) for each \(e>0\);
finitely many early lengths are absorbed in \(D_e\), on the same
window for every \(e\).

For each \(w\) with \(1\le|w|\le J\), the set
\(M_w=T\cap D_{w^-}\) is compact and disjoint from \(Z_w\).
Thus \(DF_w\) is nonsingular at every point of \(M_w\).
Cover \(M_w\) by finitely many open inverse charts \(U_{w,k}\)
for the composition \(F_w\), chosen with compact closures inside
regular inverse charts. On each such chart the ordinary
change-of-variables theorem gives
\[
|M_w\cap U_{w,k}\cap F_w^{-1}B|
\le
\left(\sup_{\overline U_{w,k}}|\det DF_w|^{-1}\right)|B|.
\tag{33.17}
\]
The supremum is finite by compactness and regularity. Summing
over the finite charts and taking the maximum over the finite
word family proves (33.15). Empty \(M_w\)'s are simply omitted.
Chart overlaps only enlarge this upper bound. All multiple local
inverse branches that meet \(M_w\) are covered; a global inverse,
or a bound on the number of branches for all \(Q\), is unnecessary.
For completed transients \(T\cap D_\sigma\subset M_\sigma\),
the same bound applies. ∎

This is where null critical sets are used quantitatively. They
permit deletion with arbitrarily small area loss, followed by a
regular compact selection. They do not themselves give a lower
bound for the Jacobian before that selection. The lemma is also
valid for a positive-area compact \(K\) with no interior.

## 4. Actual area for every approximate input

**Lemma 33.5 (arbitrary-input area after a noninjective transient).**
With \(J,T\) selected as in Lemma 33.4, there is \(C_T<\infty\)
such that for every \(e\in(0,h)\) some \(C_{T,e}<\infty\) obeys
\[
|T\cap A_u(n,\delta;K)|
\le C_T\delta+
C_{T,e}\left[e^{-(h-e)m}+
                    \delta e^{(\chi_R-h+2e)m}\right]
\tag{33.18}
\]
for every infinite input \(u\), \(n\ge J\), integer
\(0\le m\le n-J\), and \(0<\delta\le1\).

**Proof.** Let \(Q_\delta=\{x:\operatorname{dist}_2(x,Q)<\delta\}\).
The outer tube \(Q_\delta\setminus Q\) has area at most
\(C_Q\delta\), where one can take
\(C_Q=2(2+2\sqrt2)+3\pi\) for \(0<\delta\le1\):
the tubes around the three closed edges cover it, each having
area at most twice the edge length times \(\delta\) plus
\(\pi\delta^2\).

If an initial state in \(T\cap A_u\) first truly exits \(Q\) at
\(j\le J\), let \(w=u|j\). All earlier states are exactly in
\(Q\), so it belongs to
\[
T\cap D_{w^-}\cap F_w^{-1}(Q_\delta\setminus Q).
\]
Lemma 33.4 bounds its area by \(L_TC_Q\delta\). Summing over
the at most \(J\) possible first-exit times gives
\(JL_TC_Q\delta\). This argument does not use a critical-set
hypothesis in \(Q_\delta\setminus Q\): the derivative inputs,
including the last one, are all in \(Q\). Nothing about any
subsequent reentry can remove the constraint at this first exit.

For the remaining states \(\sigma=u|J\) is exactly feasible.
Its endpoints belong to \(Q_b\), and (33.15) pulls any endpoint
area estimate back with factor at most \(L_T\).
The local estimates, independent of global injectivity, are:
\[
|\mathcal I_v|\le C_b\lambda_v,\qquad
|\{\text{first true local exit after feasible }v
                          \text{ with distance}<\delta\}|
                    \le C_b'\delta\,\lambda_v/P_v .
\tag{33.19}
\]
For clarity, these are the R31 two-product estimates, not
estimates for a strategy cylinder. Taylor's formula gives
\(R_i=\rho_i+O(s)\), \(\partial_y\log R_i=O(s)\),
\(T_i=L_i+O(s)\), and \(\partial_yT_i=1/a_i+O(s)\),
where \(L_0=(y+a_1)/a_0\), \(L_1=(y-a_0)/a_1\).
The logarithmic radial graph cone yields positive angular
derivatives. Summing errors along feasible contracting radii
gives
\[
s_{|v|}\asymp s_0P_v,\qquad
dY_v/dy_0\asymp\lambda_v^{-1}.
\]
The complete feasible slice is a closed interval which can be
empty, a point, or truncated in its terminal image. Integrating
its angular length against the physical Jacobian \(s_0\,ds_0\)
proves the first inequality in (33.19). At a first true exit,
the necessary inequality \((|z|-s)_+<2\delta\), the lower
radius \(c s_0P_v\), and the positive angular derivative give
initial-angle diameter at most
\(C\delta\lambda_v/(s_0P_v)\). Integrating gives the second.
It holds also for truncated intervals. These derivations use
only local \(C^2\) estimates, the jets, and controlled
feasibility, not a global inverse or full terminal image.

If the next \(m\) prescribed digits remain exactly feasible for
some transported state, (33.16) bounds their area by
\(C_{T,e}e^{-(h-e)m}\), after the finite pullback. If they
are feasible for none, this class is empty. For a first true
exit at local time \(j\le m\), its \(j-1\) prescribed digits
are exactly feasible from a transported state whenever that
class is nonempty. Hence (33.16) and (33.19) bound its
pulled-back area by
\[
C_{T,e}\delta e^{(\chi_R-h+2e)(j-1)}.
\]
Since \(\chi_R>h\), the geometric sum is at most a fixed
multiple of \(\delta e^{(\chi_R-h+2e)m}\). These classes and
exact survival through local time \(m\) exhaust the covered
states. This proves (33.18) for every approximate input.
A change between feasible codes was never mistaken for a
true exit; all earlier constraints and possible later
reentries have been retained. ∎

## 5. What changed in the adopted proof

| Adopted step | Need for global inverse | Verified R33 replacement |
|---|---|---|
| Local graph cone, complete intervals and separate products | None; Taylor, jets and feasibility suffice | Paper Section 3 / R31 Sections 3–4 remain valid |
| Pullback of local exceptional null sets through feasible \(J\)-prefixes | A global inverse was a sufficient device | Lemma 33.2 on exact feasible domains |
| Early first true exit by time \(J\) | Bounded inverse determinants on the whole target tube | Lemma 33.4 on \(T\cap D_{w^-}\), then \(C_T\delta\) |
| Pullback of a local actual-area estimate | A global inverse was used for area distortion | Finite inverse charts for all active transients on the same \(T\) |
| All-prefix typicality and fixed compact set | Egorov and compact approximation | Same argument, with the critical pullbacks removed before selection |
| Physical bounded-run states and wrong-control margin | Only local reference inverse maps and a sequence contraction | Unchanged local proof; no inverse of a global actual map |
| Full stopping upper catalogue and common tail | Feasibility and the global norm inequality | Unchanged; every actual point, including critical and boundary states, is assigned |
| Pressure-root identity and type optimisation | No invertibility | Classical counting after physical bounds |

The finite chart constants can become large near a fold and may
depend on \(\zeta\). They are fixed before the horizon and tolerance
and consequently have zero exponential rate. No claim of a global
\(O(\delta)\) early-exit area estimate on all \(Q\) is made for this
weaker class. The needed lower bounds use the fixed window; upper
catalogues still cover all \(Q\), including points deleted from it.

## 6. Proof of Theorem 33.1

### 6.1 Every positive-area compact set: lower rate

Take the positive-area window \(T\subset K\) of Lemma 33.4.
For fixed \(e\in(0,h)\) and all sufficiently large \(n\), put
\[
m_n=\min\left\{n-J,\left\lfloor
                     \frac{-\log\delta_n}{\chi_R+e}\right\rfloor\right\}.
\tag{33.20}
\]
It is nonnegative and \(\delta_n\le e^{-(\chi_R+e)m_n}\).
Each term in (33.18) is at most a fixed multiple of
\(e^{-(h-e)m_n}\): for the second exponential term the exponent
is \(-(\chi_R+e)m_n+(\chi_R-h+2e)m_n=-(h-e)m_n\);
the early \(\delta_n\) term is smaller since \(\chi_R+e>h-e\).
Any catalogue covering \(K\) covers \(T\), so its cardinality
is at least the area of \(T\) divided by the uniform per-input
area bound. Taking lower rates and then \(e\downarrow0\) gives
\[
\liminf_n n^{-1}\log r_F(n,\delta_n;K)
                  \ge h\min\{1,\gamma/\chi_R\}.
\tag{33.21}
\]
The floor and fixed transient have zero rate. If \(\gamma=0\),
\(r_F\ge1\) supplies the same lower bound. Thus the conclusion
includes every \(o(n)\) fluctuation of the precision sequence.

### 6.2 Full \(Q\): catalogue upper bound without any inverse

Use the fixed local radial constant \(C_R\), and put
\(M=\max\{1,4\sqrt2\Lambda C_Rb\}\).
The reference binary tree stops at first \(P_w\le\delta/M\)
or at local depth \(n-J\). Each actual state has an exactly
feasible infinite input by assumption 2 in Section 1,
independently of (33.3).
Its exact transient and local tail reach one tree leaf.
Keep all realised transient/leaf pairs, including those realised
only by boundary or critical states; delete empty actual pairs.
The assignment supplies at most
\[
r_F(n,\delta;Q)\le2^J\,\#\mathcal L_P(n-J,\delta/M).
\tag{33.22}
\]
Before stopping the assigned trajectory is exactly feasible.
At a threshold leaf its actual radius is at most
\(C_RbP_w\le\delta/(4\sqrt2\Lambda)\). Its \(V\)-norm,
and then (33.2) for any appended common zero tail, keep its
Euclidean norm at most \(\delta/4\) at every remaining time.
Since the origin belongs to \(Q\), the entire tail is permitted,
even if it exits and reenters \(Q\). A horizon leaf is already
feasible through time \(n\). This proves (33.22) and covers all
actual initial points. The tree is an upper construction, not
an assumed physical partition or a necessary optimum.

If the powers match, \(P_w=\lambda_w^\beta\). A leaf of length
\(\ell\), zero frequency \(p\), has
\(\ell\chi_A(p)<[-\log\delta+\log M]/\beta+c_{\max}\),
where \(c_{\max}=-\log\min a_i\). There are at most
\(e^{\ell H_b(p)}\) words of that type and at most \((n+1)^2\)
length/type pairs. With
\(\Gamma_n=(-\log\delta_n+\log M+\beta c_{\max})/n\),
(33.22) is at most
\[
2^J(n+1)^2e^{nS(\Gamma_n)}.
\]
Continuity of \(S\), following from a uniform Lipschitz bound
in its maximum, and \(\Gamma_n\to\gamma\), give upper rate
\(S(\gamma)\). Also the leaf \(\lambda\)-weights sum to one
and each is at least \((\min a_i)(\delta/M)^{1/\beta}\).
Consequently \(r_F(n,\delta;Q)\le C\delta^{-1/\beta}\).

If the powers differ and \(0<\gamma<\gamma_0\), every reference
branch hits the threshold before the horizon for large \(n\):
\(P_w\le e^{-\gamma_0(n-J)}<\delta_n/M\) at that depth.
For the uncapped stopping tree the weights \(P_w^D\) sum to
one and \((\min\rho_i)\delta_n/M<P_w\le\delta_n/M\).
Its leaf count is between \((\delta_n/M)^{-D}\) and a fixed
multiple thereof. The actual upper catalogue (33.22) therefore
has upper rate \(\gamma D\).

### 6.3 Full \(Q\): local physical lower witnesses

The proof of paper Lemmas 5.1–5.2 (R27 Lemma 27.2 and
R31 Section 7) uses the local Taylor estimates only. Its
inverse maps are the affine reference maps
\(f_0(y)=a_0y-a_1\), \(f_1(y)=a_1y+a_0\), not inverses of the
global actual maps. To check that the mechanism survives,
for each fixed run bound \(L\) their reference orbit has
\(|y_k^0|\le1-d_L\), \(d_L=2(\min a_i)^{L+1}>0\).
On a small sequence ball around that orbit, the radial recursion
\(s_{k+1}=s_kR_{v_{k+1}}(s_k,y_k)\) depends on the candidate
angles with Lipschitz constant \(O(s_L^2)\).
The angular operator
\[
(\mathcal B y)_k=f_{v_{k+1}}(y_{k+1})
 -a_{v_{k+1}}[T_{v_{k+1}}(s_k(y),y_k)-L_{v_{k+1}}(y_k)]
\]
is a contraction for one sufficiently small fixed \(s_L>0\).
Its fixed sequence is an actual all-time feasible orbit.
Substitution in the alternative angular map gives a uniform
positive wrong-control excess \(d'_L\).
This local proof does not see a fold in the transient region.

Take length-\(L\) blocks starting in zero and ending in one
with \(j\) zeros; their number is
\(M_L=\binom{L-2}{j-1}\), and their radial cost is
\(c_L=-(j/L)\log\rho_0-(1-j/L)\log\rho_1\).
For fixed \(0<t<\min\{1,\gamma/c_L\}\), concatenate
\(\lfloor tn/L\rfloor\) such blocks and then a fixed block
forever. Every selected infinite sequence has run bound \(L\)
and a physical state at the same fixed radius \(s_L\).
If an arbitrary approximate catalogue input first differs by
time \(m_n=L\lfloor tn/L\rfloor\), the preceding states agree,
and the wrong-control physical excess is at least
\(E_L e^{-c_Lm_n}\), \(E_L>0\). Its ratio to \(2\delta_n\)
has logarithmic rate \(\gamma-c_Lt>0\). Hence the input must
agree with the whole prefix. Later reentry cannot cure the
constraint already violated. Distinct prefixes give distinct
actual states by this same wrong-control margin. Thus
\[
\liminf_n n^{-1}\log r_F(n,\delta_n;Q)
                 \ge t L^{-1}\log M_L.
\tag{33.23}
\]
First take the supremum over strict \(t\), with \(L\) and its
radius fixed in each horizon limit; then let \(j/L\to p\) and
\(L\to\infty\). The binomial type bounds give
\(L^{-1}\log M_L\to H_b(p)\).
In the matched case \(c_L\to\beta\chi_A(p)\), yielding every
term in (33.6). The endpoint entropies are zero; continuity
handles endpoints and critical precision exponents.
For \(\gamma=0\), the upper bound and \(r_F\ge1\) give zero.
This proves (33.7).

For mismatch take \(p_*=\rho_0^D\), so
\(H_b(p_*)=D[-p_*\log\rho_0-(1-p_*)\log\rho_1]\).
Since the bracket is at least \(\gamma_0>\gamma\), (33.23)
gives lower rate \(\gamma D\), matching (33.22). There is
no new pressure identity here.

### 6.4 The same compact set for every declared precision choice

Apply Lemma 33.4 to \(K=Q\), with area loss less than \(\zeta\),
and set \(K_\zeta=T\cup\{0\}\). This compact set has area
greater than \(1-\zeta\).
All exactly feasible local words meeting \(T\), after any
feasible transient, obey (33.16). Consequently their length-\(n\)
number is at most \(e^{(h+o(1))n}\), by summing types with
frequency uniformly tending to \(a_0\), and multiplying by the
finite \(2^J\) transient count. Keep all realised words and
extend each arbitrarily after the horizon. They cover \(T\)
exactly; one input covers zero.
This supplies upper rate \(h\) for all precision sequences.
In the matched case the full stopping upper bound
\(C\delta_n^{-1/\beta}\) supplies the other upper rate
\(\gamma/\beta\). Formula (33.21), with
\(\chi_R=\beta h\), proves (33.9) and the lower side of
(33.8); the upper side follows by inclusion in \(Q\).

For mismatch and \(0<\gamma<\gamma_0\), retain the actual
stopped pairs meeting \(T\) in (33.22). Let
\(q_n=-\log(\delta_n/M)\), \(c_R^{\max}=-\log\min\rho_i\).
Every retained tail of length \(\ell\) obeys
\[
q_n\le-\log P_w<q_n+c_R^{\max},\qquad
\ell\le[q_n+c_R^{\max}+\log D_e]/(\chi_R-e).
\]
At each length it has
\(\lambda_w\ge D_e^{-1}e^{-(h+e)\ell}\).
All reference length-\(\ell\) weights sum to one, so there
are at most \(D_e e^{(h+e)\ell}\) retained distinct words.
Sum over the \(O(q_n+1)\) lengths and the finite transients.
The resulting upper rate is at most
\(\gamma(h+e)/(\chi_R-e)\); let \(e\downarrow0\).
Formula (33.21) gives the matching lower rate
\(\gamma h/\chi_R\).
All selections of \(T\) preceded \(e,\gamma,\delta_n,n\);
only estimates and constants vary with these later choices.
This proves the required simultaneous quantifiers.

Finally \(b_i=\rho_i^D\) satisfy \(\sum b_i=1\), and
\[
D\chi_R-h=\sum_i a_i\log(a_i/b_i)\ge0.
\]
Equality requires \(b_i=a_i\), hence \(\beta_iD=1\) for both
labels. It is impossible under mismatch. Thus \(D>h/\chi_R\).
Matching gives the common low-side rate on \((0,\beta h)\);
mismatch separates \(Q\) and \(K_\zeta\) on every
\((0,\gamma_0)\). This proves the scoped if-and-only-if
criterion, and finishes Theorem 33.1. ∎

## 7. A smooth fold inside the actual constraint

The extension has members whose actual feasible geometry cannot
come from an injective map by a coordinate conjugacy.
The following single construction works for every fixed allowed
parameter choice, matched or mismatched.

Let \(c=1/5\). Define \(E(v)=e^{-1/v}\) for \(v>0\) and zero
otherwise, and
\[
\psi(s)=\frac{E(s-1/4)}{E(s-1/4)+E(1/2-s)}.
\]
The denominator is positive everywhere; \(0\le\psi\le1\),
\(\psi=0\) on \(s\le1/4\), and \(\psi=1\) on \(s\ge1/2\).
Put
\[
H(s,z)=
\begin{cases}
(s,z),&s\le1/4,\\
(s,z+c\,s\psi(s)\sin(2\pi z/s)),&s>1/4,
\end{cases}
\qquad F_i=A_iH.
\tag{33.24}
\]
The quotient is used only away from \(s=0\). Flatness of
\(\psi\) at \(1/4\) proves global \(C^\infty\) smoothness.
Near the origin \(H\) is the identity, so \(F_i(0)=0\) and
\(DF_i(0)=A_i\).

For \(s>0\), its angular map on \(Q\) is
\(g_\tau(y)=y+c\tau\sin(2\pi y)\), where \(\tau=\psi(s)\).
For \(0\le y\le1/2\), \(0\le g_\tau(y)\le1/2+c<1\).
For \(1/2\le y\le1\), \(1/2-c\le g_\tau(y)\le1\).
Oddness handles the negative half. Its endpoints are
\(g_\tau(\pm1)=\pm1\). Thus \(H(Q)\subset Q\).
The feasible angular domains of the linear \(A_i\) cover
\([-1,1]\); their radius factor is \(\rho_i<1\).
For each \(x\in Q\), choose a feasible \(A_i\) at \(H(x)\).
This proves controlled feasibility of \(F_i\), including
all boundary points.

Let \(m_*=\max\{\rho_0,\rho_1,t_0,t_1\}<1\) and choose
\[
\Lambda=1+\frac{2m_*(1+2c)}{1-m_*}.
\]
For all states, \(|H^z-z|\le c|s|\), so
\[
V(Hx)\le(1+c/\Lambda)V(x),\qquad
V(A_i x)\le m_*(1+1/\Lambda)V(x).
\]
Hence (33.2) holds with
\[
\theta=m_*(1+1/\Lambda)(1+c/\Lambda)
\le m_*[1+(1+2c)/\Lambda]<(1+m_*)/2<1.
\tag{33.25}
\]
This is checked on the whole plane, including every approximate
tail, not only on feasible states. All inputs therefore converge
uniformly to zero on bounded initial sets.

Since the first coordinate of \(H\) is \(s\),
\[
\det DH(s,z)=1+2\pi c\psi(s)\cos(2\pi z/s)\quad(s>1/4),
\qquad
\det DF_i=(\rho_i^2/a_i)\det DH.
\tag{33.26}
\]
For each fixed \(s\), the determinant either equals one or
has only finitely many zeros for \(|z|\le s\).
The zero fibres consequently have one-dimensional measure
zero; Fubini proves that the critical set in \(Q\) has area
zero. At \(s=3/4\), the determinant of \(H\) is positive at
\(y=0\) and negative at \(y=1/2\), since \(2\pi/5>1\).
Continuity gives a zero between them. Thus no positive
lower bound for the absolute determinant on all \(Q\) exists.

There is nonetheless genuine noninjectivity inside \(Q\).
At \(s_0=3/4\), \(\psi=1\). With \(g(y)=y+c\sin(2\pi y)\),
\[
g(1/4)=9/20<1/2,\qquad
g(2/5)=2/5+(1/5)\sin(\pi/5)>1/2,\qquad
g(1/2)=1/2,
\]
where \(\sin(\pi/5)>\sin(\pi/6)=1/2\).
The intermediate value theorem gives some
\(y_1\in(1/4,2/5)\) with \(g(y_1)=1/2\).
Thus the distinct interior states
\((s_0,s_0y_1)\) and \((s_0,s_0/2)\) have the same image
under both \(F_i\). At least one of these two controls is
feasible at their common intermediate state \(H(x)=(s_0,s_0/2)\),
by the linear feasible-domain cover. The fold therefore occurs
even on a genuinely feasible branch of the actual constraint.
It is not an artefact confined to \(Q\)'s exterior.

Injectivity is preserved by a simultaneous coordinate
homeomorphism. These two distinct inputs with the same feasible
output preclude a \(Q\)-preserving simultaneous conjugacy to
injective controls. No exclusion of unrelated semiconjugacies
or altered catalogue objects is claimed.
Theorem 33.1 applies to this example in both parameter regimes.
The example illustrates the single extension; its extra formula
or multiplicity is not counted as a separate main contribution.

## 8. Attribution, necessity, and completed scope

Global invertibility is a sufficient finite-transient
noncollapse device, but is not necessary for the adopted rates.
Nonsingularity at area-almost every state of \(Q\) suffices
here. The decisive verified replacement is (33.15) on a fixed
regular compact window, leading to (33.18) for every approximate
input and to the unchanged precision-cost conclusions.

A fold can identify different states while its critical set
has area zero; it still pulls every null target set back to
a null set along an exactly feasible finite transient.
The R18 saturated example instead sends a positive-area
region onto a ray. Its determinant vanishes on that region,
and the pullback of that area-zero ray contains positive area.
It violates (33.3) and defeats typicality transfer.
This distinguishes the two mechanisms without declaring
zero-area critical sets necessary for every possible
cost theorem. Some maps outside this sufficient class may
still have the same rates.

Local inverse charts, change of variables, null-set
preservation by locally Lipschitz maps, finite coverings,
Egorov and compact inner approximation are classical.
The finite-transient lemma and Theorem 33.1 are a checked
structural extension of the project proof, not a new
area formula, pressure theorem, or inverse-function method.
No new local entropy mechanism or new spectrum is asserted.
No mathematical gap remains in the R33 transfer as stated.
The whole class still has two planar controls, the specified
jets, a controlled triangle and a common globally contracting
origin. High-side mismatch and arbitrary compact high-side
classification remain outside the statement.
The unique manuscript is deliberately unchanged; the R33
result is not yet a claim of that manuscript.
