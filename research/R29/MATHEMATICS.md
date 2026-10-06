# R29: the exact full-Q precision spectrum

2026-10-06 UTC. Baseline: `503801f1b028316159cf78aa63fae3ed35120e1c`.
This is a uniform consequence of the actual controlled geometry proved in
R27, with a sharper stopping-tree count and a shorter forced-prefix count.
It does not add a system class or assert that the reference tree is an
optimal physical catalogue. The existing paper remains unchanged.

## 1. Objects, hypotheses, and statement

Fix

\[
 a_0,a_1\in(0,1),\qquad a_0+a_1=1,\qquad a_0\ne a_1,
 \qquad \beta>1.
\]

Let \(F_0,F_1:\mathbb R^2\to\mathbb R^2\) be global \(C^2\)
diffeomorphisms fixing the origin, with

\[
 DF_0(0)=
 \begin{pmatrix}a_0^\beta&0\\a_0^{\beta-1}a_1&a_0^{\beta-1}\end{pmatrix},
 \qquad
 DF_1(0)=
 \begin{pmatrix}a_1^\beta&0\\-a_1^{\beta-1}a_0&a_1^{\beta-1}\end{pmatrix}.
\]

Put \(Q=\{(s,z):0\le s\le1,\ |z|\le s\}\), of area one.
Assume one-step controlled feasibility: for every \(x\in Q\), at least
one \(i\in\{0,1\}\) has \(F_i x\in Q\). Assume also that for some
\(\Lambda\ge1\), \(\theta\in(0,1)\),

\[
 V(s,z)=\max\{\Lambda|s|,|z|\},\qquad
 V(F_i x)\le\theta V(x)
 \quad(x\in\mathbb R^2,\ i=0,1).
\]

This is contraction toward the origin, not a claim about distances
between arbitrary pairs of states. All infinite binary inputs are
allowed. For \(u=(u_1,u_2,\ldots)\), set
\(F_u^0=\operatorname{id}\),
\(F_u^k=F_{u_k}\circ\cdots\circ F_{u_1}\), and

\[
 A_u(n,\delta;Q)=
 \{x\in Q:\operatorname{dist}(F_u^kx,Q)<\delta
                         \text{ for every }0\le k\le n\}.
\]

Distance is Euclidean. The real catalogue number \(r_F(n,\delta;Q)\)
is the least number of infinite inputs whose actual sets \(A_u\)
cover \(Q\). Controls may be assigned separately to each initial state;
approximate trajectories may exit and reenter \(Q\). Finite catalogues
exist: choose feasible length-\(n\) prefixes and append any infinite tail.

Define, with \(0\log0=0\),

\[
 H_b(p)=-p\log p-(1-p)\log(1-p),\qquad
 \chi(p)=-p\log a_0-(1-p)\log a_1,
\]

\[
 S(\gamma)=\max_{0\le p\le1}
       H_b(p)\min\left\{1,\frac{\gamma}{\beta\chi(p)}\right\}.
 \tag{29.1}
\]

**Theorem 29.1 (exact spectrum in the R27 class).** For every fixed
system satisfying the above hypotheses, every finite \(\gamma\ge0\),
and every positive sequence \(\delta_n\to0\) such that
\(-\log\delta_n/n\to\gamma\),

\[
 \lim_{n\to\infty}\frac{\log r_F(n,\delta_n;Q)}n=S(\gamma).
 \tag{29.2}
\]

No monotonicity of \(\delta_n\) is assumed. This concerns the full
physical triangle; it is not a classification of the high-precision
rates of arbitrary positive-area compact subsets.

## 2. Previously proved geometric dependencies and their actual scope

The following facts were independently checked in the adopted proof
chain: R27/MATHEMATICS.md §§2–3, 6–8 and the corresponding complete
proofs in the R28 paper, §§3, 5–6. They are used as proved lemmas,
not new hypotheses about covering rates or catalogue losses.

**G1: local radial comparison.** Write \(z=sy\), for \(s>0\), and

\[
 R_i(s,y)=F_i^s(s,sy)/s,\qquad
 T_i(s,y)=F_i^z(s,sy)/F_i^s(s,sy).
\]

There are \(0<\rho<1\), \(C_R\ge1\), and
\(r_*=\min_i a_i^\beta>0\), depending only on the fixed system, such
that \(R_i\ge r_*/2\) on \(0<s\le\rho,\ |y|\le1\). For every
exactly feasible local word \(w\), starting at radius \(s_0\le\rho\),
with \(\lambda_w=\prod_j a_{w_j}\),

\[
 C_R^{-1}s_0\lambda_w^\beta\le s_{|w|}
                      \le C_Rs_0\lambda_w^\beta.
 \tag{29.3}
\]

The comparison includes every prefix. It follows from
\(\log R_i=\beta\log a_i+O(s)\) and uniformly geometrically
decreasing local radii. C² Taylor estimates yield these errors from
the specified jets; summability is proved, not assumed. There is no
claim that a fixed-radius complete feasible word interval is nonempty
for every word, or that its final angular image fills the whole fibre.

**G2: a finite exact transient and a full common tail.** Choose a
fixed integer \(J\ge1\) with \(\theta^J\sup_QV\le\rho\). Every
exactly feasible length-\(J\) prefix from \(Q\) ends in
\(Q_\rho=Q\cap\{s\le\rho\}\). One-step controlled feasibility
gives an exact infinite continuation from every state of \(Q\).
If an exactly feasible prefix ends at a state with
\(V\le\delta/(4\sqrt2)\), the global norm inequality and
\(\|x\|_2\le\sqrt2 V(x)\) keep its whole subsequent common zero
tail within \(\delta/4\) of the origin, hence within \(\delta\) of \(Q\).

**G3: bounded-run physical realisation with a wrong-control margin.**
For each fixed integer \(L\ge2\), Lemma 27.2 gives \(s_L\in(0,\rho]\)
and \(d'_L>0\), uniform over all infinite binary sequences whose
successive runs have length at most \(L\). Each such sequence is
realised by an actual exactly feasible orbit starting at
\((s_L,s_Ly_0)\); at every step, the alternative control gives
\(|T_i(s_k,y_k)|\ge1+d'_L\). The lemma constructs the orbit through
a contraction on bounded angular sequences coupled to the actual
radial recursion. It does not replace an actual state by a symbolic
sequence, nor assert that all words occur at one fixed positive radius.

**G4: a necessary constraint at a true exit.** The two linear
boundary functionals \(z-s\) and \(-z-s\) are \(\sqrt2\)-Lipschitz
and nonpositive on \(Q\). Consequently

\[
 \operatorname{dist}((s,z),Q)<\delta
             \quad\Longrightarrow\quad (|z|-s)_+<2\delta.
 \tag{29.4}
\]

A later reentry cannot remove a violation of (29.4) at an earlier
time. This elementary condition is applied to the first *wrong*
control on the special physical orbits of G3, where it is proved
genuinely infeasible. No such assertion is made for arbitrary early
differences between feasible codes in an overlap region.

## 3. Upper bound: type counting of an auxiliary stopping tree

Put

\[
 c_i=-\log a_i>0,\qquad c_{\max}=\max_i c_i,\quad
 c_{\min}=\min_i c_i>0,
\]

and \(M_0=4\sqrt2\Lambda C_R\rho\). For small positive \(\delta\),
set

\[
 t_\delta=\min\{1,(\delta/M_0)^{1/\beta}\},\qquad
 b_\delta=-\log t_\delta.
\]

For \(n\ge J\), build the full *reference* binary tree, capped at
depth \(N=n-J\), stopping a word at the first
\(\lambda_w\le t_\delta\), or at depth \(N\), whichever is earlier.
This is only an upper-catalogue construction.

For each actual initial state choose an exact feasible infinite input.
Its first \(J\) digits give an exact transient, and its subsequent
digits lead to a leaf of the reference tree. Keep all transient/leaf
pairs that are actually feasible; empty feasible leaves can be
discarded. If a leaf stops by the weight threshold, G1 gives

\[
 s_{|w|}\le C_R\rho\,t_\delta^\beta
                       \le\delta/(4\sqrt2\Lambda).
\]

On an exact state of \(Q\), \(V=\Lambda s\), and globally
\(\|x\|_2\le\sqrt2 V(x)\). Thus appending one common infinite
zero tail keeps every later Euclidean norm at most \(\delta/4\).
Before that stopping time, every assigned state is exactly feasible.
A leaf reaching the horizon already specifies the complete constraint
through time \(n\); an infinite zero extension does not impose
additional constraints. The origin is included in this construction.
There are at most \(2^J\) transient choices. All-time feasibility,
including the tail, has therefore been justified for actual states.

For \(\delta\) sufficiently small, \(b_\delta>0\). Let
\(C(w)=-\log\lambda_w\). A leaf stopped by the threshold satisfies
\(b_\delta\le C(w)<b_\delta+c_{\max}\), since its proper prefix
has cost below \(b_\delta\). A horizon leaf that has not crossed
the threshold has cost below \(b_\delta\). Hence every nonempty
leaf, of length \(\ell\le n\) and containing \(j\) zeros, satisfies

\[
 C(w)=\ell\chi(j/\ell)<b_\delta+c_{\max}.
 \tag{29.5}
\]

There are at most \(\binom\ell j\le e^{\ell H_b(j/\ell)}\)
words of this type. Define

\[
 \Gamma_{n,\delta}=\frac{\beta(b_\delta+c_{\max})}{n}.
\]

With \(p=j/\ell\), (29.5) and \(\ell/n\le1\) imply

\[
 \frac\ell n\le
   \min\{1,\Gamma_{n,\delta}/[\beta\chi(p)]\},\qquad
 \ell H_b(p)\le nS(\Gamma_{n,\delta}).
\]

The empty leaf, if present, has count one and can be included separately.
There are at most \((n+1)^2\) length/type pairs, including this case.
Thus, for sufficiently large \(n\) and small \(\delta\),

\[
 r_F(n,\delta;Q)\le
           2^J(n+1)^2e^{nS(\Gamma_{n,\delta})}.
 \tag{29.6}
\]

The binomial upper bound is elementary: the corresponding term of
the binomial law with parameter \(j/\ell\) is at most one.
Endpoint types have one word. No pressure theorem or optimal-tree
assumption is used in (29.6).

The function \(S\) is continuous. In fact each function under the
maximum in (29.1) is Lipschitz in \(\gamma\), with common constant
at most \(\log2/(\beta c_{\min})\); so is their maximum. For the
given precision sequence, eventually
\(\beta b_{\delta_n}=-\log\delta_n+\log M_0\), whence
\(\Gamma_{n,\delta_n}\to\gamma\). The fixed transient factor and
the polynomial in (29.6) have zero exponential rate. Therefore

\[
 \limsup_n n^{-1}\log r_F(n,\delta_n;Q)\le S(\gamma).
 \tag{29.7}
\]

This also proves the zero upper rate when \(\gamma=0\), even if
\(-\log\delta_n\) grows very slowly or is not monotone.

## 4. Lower bound: forcing a shorter actual prefix

Let \(\gamma>0\), and fix an arbitrary \(p\in(0,1)\). Choose
integers \(j_L\in\{1,\ldots,L-1\}\) with \(j_L/L\to p\).
Use all length-\(L\) blocks that start with zero, end with one,
and contain exactly \(j_L\) zeros. Set

\[
 M_L=\binom{L-2}{j_L-1},\qquad B_L=L^{-1}\log M_L,\qquad
 \chi_L=\chi(j_L/L).
\]

All concatenations of these blocks have runs of length at most
\(L\). Their common cost per complete block is \(L\chi_L\).
Moreover

\[
 B_L\longrightarrow H_b(p),\qquad \chi_L\longrightarrow\chi(p).
 \tag{29.8}
\]

For completeness, the exact identity

\[
 \binom{L-2}{j-1}=\frac{j(L-j)}{L(L-1)}\binom Lj
\]

and the two type inequalities

\[
 \frac{e^{LH_b(j/L)}}{L+1}\le\binom Lj\le e^{LH_b(j/L)}
\]

prove (29.8). For the lower type inequality, the \(j\)-th term is
a largest term of the binomial law with parameter \(j/L\), hence
at least \(1/(L+1)\). Since \(p\) is interior, the extra fraction
in the identity has logarithm \(o(L)\).

Now **fix \(L\) before sending the horizon to infinity**. Fix

\[
 0<t<\min\{1,\gamma/(\beta\chi_L)\},\qquad
 k_n=\lfloor tn/L\rfloor,\qquad m_n=Lk_n\le n.
 \tag{29.9}
\]

For each of the \(M_L^{k_n}\) choices of these first \(k_n\)
blocks, append one fixed allowable block forever. G3 gives an
exactly feasible physical orbit at the same radius \(s_L>0\),
independent of the block choices and of \(n\). Its first \(m_n\)
digits are the selected prefix.

For every \(k\le m_n\), monotonicity of reference products gives

\[
 \lambda_{v|k}\ge\lambda_{v|m_n}=e^{-\chi_Lm_n}.
\]

Suppose an arbitrary catalogue input first differs from such a witness
at time \(j\le m_n\). The preceding actual states agree exactly
with the witness. By G1, their radius at time \(j-1\) is at least
\(C_R^{-1}s_Le^{-\beta\chi_Lm_n}\). The wrong radial multiplier
is at least \(r_*/2\), and G3 supplies the angular excess \(d'_L\).
At that time its actual physical excess is therefore at least

\[
 |z_j|-s_j\ge E_Le^{-\beta\chi_Lm_n},\qquad
 E_L=\frac{s_Lr_*d'_L}{2C_R}>0.
 \tag{29.10}
\]

The margin is quantitative for the *physical* state, not just for
an angular coordinate. No exact agreement after this time is assumed.
By (29.9) and the stated precision exponent,

\[
 \frac1n\log\frac{E_Le^{-\beta\chi_Lm_n}}{2\delta_n}
        \longrightarrow\gamma-\beta\chi_Lt>0.
\]

For sufficiently large \(n\), (29.10) violates the necessary
constraint (29.4). Thus an input approximately feasible for a witness
must agree with its whole first \(m_n\) digits, regardless of any
later exit or reentry. Witnesses with different selected prefixes
are distinct actual states: otherwise at their first different
digit one would be exactly feasible and simultaneously violate the
wrong-control margin. A single catalogue input can cover at most
one of these distinct prefix witnesses. Consequently

\[
 r_F(n,\delta_n;Q)\ge M_L^{k_n},\qquad
 \liminf_n n^{-1}\log r_F(n,\delta_n;Q)\ge tB_L.
 \tag{29.11}
\]

For this fixed \(L\), take the supremum over the strict choices of
\(t\) in (29.9), obtaining the lower bound
\(B_L\min\{1,\gamma/(\beta\chi_L)\}\). Next send \(L\to\infty\)
using (29.8), and then take the supremum over \(p\in(0,1)\).
The endpoint frequencies have entropy zero, so continuity extends
the supremum to \([0,1]\). This proves

\[
 \liminf_n n^{-1}\log r_F(n,\delta_n;Q)\ge S(\gamma).
 \tag{29.12}
\]

The order of limits is essential. No uniform positive witness radius
or margin as \(L\to\infty\) is asserted; \(L\), \(s_L\), and
\(E_L\) are fixed during every horizon limit. The strict choice of
\(t\) handles equality at a stopping exponent, integer rounding,
and every \(o(n)\) fluctuation in \(-\log\delta_n\). For
\(\gamma=0\), the elementary lower bound \(r_F\ge1\), together
with (29.7), gives the zero limit. Equations (29.7) and (29.12)
complete the proof of Theorem 29.1.

## 5. Exact evaluation and the two thresholds

The maximum in (29.1) can also be evaluated, rather than left as
an unresolved optimisation. Write

\[
 \alpha=\min\{a_0,a_1\}\in(0,1/2),\qquad
 c=-\log(1-\alpha),\qquad d=\log\frac{1-\alpha}{\alpha}>0,
\]

\[
 h=H_b(\alpha)=h_a,\qquad
 \gamma_* =\beta h,\qquad
 \gamma_{\rm sat}=-\frac\beta2\log(a_0a_1)
                    =\beta(c+d/2)>\gamma_*.
\]

**Corollary 29.2 (closed spectrum).** In the same class,

\[
 S(\gamma)=
 \begin{cases}
 \gamma/\beta,&0\le\gamma\le\gamma_*,\\[2pt]
 H_b\!\left(\dfrac{\gamma/\beta-c}{d}\right),
       &\gamma_*<\gamma<\gamma_{\rm sat},\\[6pt]
 \log2,&\gamma\ge\gamma_{\rm sat}.
 \end{cases}
 \tag{29.13}
\]

**Proof.** Reparameterise the maximum by the frequency \(q\) of
the smaller branch. This merely relabels the optimisation variable,
not the dynamics or the control assignments. Then \(\chi=c+dq\),
and with \(x=\gamma/\beta\) the objective is
\(H_b(q)\min\{1,x/(c+dq)\}\).
The entropy inequality

\[
 c+dq-H_b(q)
 =q\log\frac q\alpha+(1-q)\log\frac{1-q}{1-\alpha}\ge0
\]

follows from \(-\log t\ge1-t\), with equality at \(q=\alpha\).
If \(x\le h\), the objective is at most \(x\) everywhere and
equals \(x\) at \(q=\alpha\).

If \(h<x<c+d/2\), put \(q_x=(x-c)/d\in(\alpha,1/2)\).
For \(q\le q_x\), the objective is \(H_b(q)\), at most
\(H_b(q_x)\). For \(q\ge q_x\), it is \(xH_b(q)/(c+dq)\).
This ratio decreases for \(q>\alpha\): the numerator of its
derivative is

\[
 D(q)=(c+dq)H_b'(q)-dH_b(q),\quad
 D(\alpha)=0,\quad D'(q)=(c+dq)H_b''(q)<0.
\]

Thus the maximum is \(H_b(q_x)\). Endpoint values follow by
continuity. Finally, if \(x\ge c+d/2\), the objective at \(q=1/2\)
is \(\log2\), the universal entropy maximum. The three expressions
agree at both thresholds. This proves (29.13).

In particular the binary saturation rate \(\log2\) is reached
**exactly** when \(\gamma\ge\gamma_{\rm sat}\). For smaller
\(\gamma\), the attained maximum is strictly below \(\log2\).

## 6. Consequences for the fixed near-full set and the inward example

Reusing the single compact set \(K_\zeta\) of Theorem 27.1, for
each fixed system and each \(\zeta\in(0,1)\),

\[
 |K_\zeta|>1-\zeta,\qquad
 \lim_n n^{-1}\log r_F(n,\delta_n;K_\zeta)
                         =\min\{h_a,\gamma/\beta\}
 \tag{29.14}
\]

for every finite \(\gamma\ge0\) and every stated precision sequence.
The set is selected before all these exponents, sequences, and horizons.
Equation (29.14) is entirely inherited from R27, not a new construction.
The exact gap between this set and full \(Q\) is zero on the low
side, \(H_b((\gamma/\beta-c)/d)-h_a\) on the intermediate side,
and \(\log2-h_a\) at and above saturation. It is strictly positive
for each \(\gamma>\gamma_*\). This quantifies the earlier strict
gap without classifying other compact initial sets.

As a direct specialisation, the previously proposed inward example
has \(a_0=1/3, a_1=2/3, \beta=2\), and
\(g(s)=1-(1/100)s/(1+s^2)\), with the maps already given in R27 §9
and paper §7.2. It belongs to the same class: with \(\Lambda=9\),
the checked global norm factor is at most \(67/90<1\). At exponent
\(\gamma=\log4\),

\[
 2\left(\log3-\tfrac23\log2\right)<\log4<\log(9/2),
 \qquad
 \lim_n n^{-1}\log r_F(n,\delta_n;Q)
                  =H_b\!\left(\frac{\log(4/3)}{\log2}\right).
 \tag{29.15}
\]

This follows from (29.13) for every exponent-\(\log4\) sequence,
not only \(\delta_n=4^{-n}\). It is not a second proof task or a
new example. The inequalities follow respectively from
\(\log(4/3)-\log2/3>0\) and \(4<9/2\).

## 7. Attribution and limits of the result

The controlled content needed here is already R27: exact radial
comparison, the actual feasible prefix plus full common tail, and
bounded-run physical realisation with a genuine wrong-control margin.
Classical binomial type bounds and stopping scales supply the counting.
R29 sharpens the *use* of these facts by counting types for all leaf
lengths and forcing shorter prefixes before the tolerance becomes
too coarse. No new distortion lemma, strategy-optimality theorem,
or inverse-entropy argument is required.

The full-Q high-side limit and its exact value were not previously
established. They are now a proved uniform consequence for the entire
existing structural class, including its inward-boundary examples.
This finishes the previously unresolved spectrum, provides both exact
thresholds, and quantifies the initial-set gap. Its incremental value
is completion and a usable evaluation, not a new general mechanism.

The result remains specific to the matched binary planar class and
its global hypotheses. It does not settle constant limiting overlap,
arbitrary compact-set spectra, necessity in general feedback classes,
or systems lacking injectivity/common origin contraction. It does not
certify priority beyond the recorded source scopes, or a journal tier.
The R28 paper and all its historical scope statements are unchanged;
R29 is recorded separately for a possible later authorised integration.
