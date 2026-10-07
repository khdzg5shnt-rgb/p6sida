# R37 — Precision and exponentially vanishing failure probability

This is one bounded application of the existing route A. It does not enlarge
the system class of the current paper. The theorem below concerns its matched
linear subclass and the same actual finite-time covered sets. Source-coding
reliability and binary type estimates are classical. The additional control
step is the finite-time comparison in Lemma 37.2; its proof uses arbitrary
approximate inputs, rather than declaring an exact coding optimal.

## 1. The two candidates and the chosen scope

Write

\[
A_u(n,\delta;Q)=\{x\in Q:\operatorname{dist}(F_u^k x,Q)<\delta
\text{ for every }0\le k\le n\}.
\]

Here \(Q=\{0\le s\le1,\ |z|\le s\}\). Let \(\mu\) be planar Lebesgue
measure restricted to \(Q\), whose area is one.
For \(0<e<1\), define the chance-cover catalogue number

\[
r_e(n,\delta;Q)=\min\{|W|:
 \mu(\bigcup_{u\in W}A_u(n,\delta;Q))\ge1-e\}.
\tag{37.1}
\]

Here \(W\) is a finite set of infinite binary inputs. The input assigned to a
state may depend on the state and the horizon. There is no strategy or exact
coding restriction. All times, the Euclidean environment distance, and
possible departure and re-entry are retained. This is a separately defined
distributional requirement on the fixed actual set \(Q\); it does not replace
the original requirement to cover every state of a fixed compact initial set.

**Candidate 1: fixed failure fraction.** Fix
\(a_0,a_1\in(0,1)\), \(a_0+a_1=1\), \(a_0\ne a_1\), \(\beta>1\).
Let \(F_0,F_1:\mathbb R^2\to\mathbb R^2\) be global C² maps fixing
the origin, with

\[
DF_0(0)=\begin{pmatrix}a_0^\beta&0\\
a_0^{\beta-1}a_1&a_0^{\beta-1}\end{pmatrix},\qquad
DF_1(0)=\begin{pmatrix}a_1^\beta&0\\
-a_1^{\beta-1}a_0&a_1^{\beta-1}\end{pmatrix}.
\]

Assume that for every \(x\in Q\) some \(F_i x\) belongs to \(Q\),
that \(\{x\in Q:\det DF_i(x)=0\}\) has area zero for each control,
and that there exist \(\Lambda\ge1\), \(\theta\in(0,1)\) such that
\(V(F_i x)\le\theta V(x)\) for all \(x\in\mathbb R^2\) and both
controls, where \(V(s,z)=\max\{\Lambda|s|,|z|\}\).
No global injectivity is required. For every such fixed system, every
fixed \(e\in(0,1)\), every finite \(\gamma\ge0\), and every
\(\delta_n\to0\) with \(-\log\delta_n/n\to\gamma\), the candidate is

\[
\lim_{n\to\infty}\frac{\log r_e(n,\delta_n;Q)}n
 =\min\{h_a,\gamma/\beta\}.
\tag{37.2}
\]

This is a direct application of the existing regular-window area estimate
and the fixed near-full compact set; it is not selected as a new main result.
For completeness, take a regular compact window \(T\) with \(\mu(T)>e\).
Any successful catalogue covers at least \(\mu(T)-e>0\) of this window.
The current paper's Theorem 2.5 (the theorem labelled thm:area) bounds the
area covered there by each arbitrary input by
\(\exp[-n(\min\{h_a,\gamma/\beta\}-o(1))]\).
More precisely, in its displayed area estimate use
\(m/n\to\min\{1,\gamma/(\beta h_a)\}\), with the fixed transient
removed from the allowed horizon. For \(\gamma>0\), the two principal
exponents tend to \(h_a m/n\) and
\(\gamma-(\beta-1)h_a m/n\); let the theorem's small error parameter
tend to zero after the horizon limit. Both are at least
\(\min\{h_a,\gamma/\beta\}\). The \(O(\delta_n)\) term is faster.
Summing this bound proves the lower rate in (37.2). The existing single
near-full compact set of area greater than \(1-e\) proves the upper rate.
For \(\gamma=0\), the lower bound is just \(r_e\ge1\).
The window and the compact set are fixed before the precision sequence.
This argument adds no new controlled-geometric interface.

**Candidate 2, selected: exponentially vanishing failure fraction.** Fixed
near-full compact sets and qualitative typicality do not specify how the
omitted physical area can decay exponentially with the horizon. We solve
that finite-horizon question on the existing matched linear systems:

\[
\begin{split}
F_0(s,z)&=(a_0^\beta s,\ a_0^{\beta-1}(z+a_1s)),\\
F_1(s,z)&=(a_1^\beta s,\ a_1^{\beta-1}(z-a_0s)),\\
Q&=\{0\le s\le1,\ |z|\le s\},
\end{split}
\tag{37.3}
\]

where \(a_0,a_1\in(0,1)\), \(a_0+a_1=1\), \(a_0\ne a_1\), and
\(\beta>1\). This subclass is already in the paper. No new model, feedback
restriction, distribution of disturbances, or noisy channel is introduced.

## 2. Complete result

Use natural logarithms, \(0\log0=0\), and put

\[
\begin{split}
H_b(p)&=-p\log p-(1-p)\log(1-p),\\
\chi(p)&=-p\log a_0-(1-p)\log a_1,\\
I_a(p)&=p\log(p/a_0)+(1-p)\log((1-p)/a_1)
        =\chi(p)-H_b(p),\\
h_a&=\chi(a_0)=H_b(a_0),\\
L_a(\alpha)&=\max_{I_a(p)\le\alpha}H_b(p),\\
S(\gamma)&=\max_{0\le p\le1}H_b(p)
                 \min\{1,\gamma/[\beta\chi(p)]\}.
\end{split}
\tag{37.4}
\]

**Theorem 37.1.** For each fixed system (37.3), each finite
\(\gamma\ge0\), each finite \(\alpha>0\), and every pair of sequences

\[
\delta_n>0,\quad\delta_n\to0,\quad
-\log\delta_n/n\to\gamma,
\qquad
0<e_n<1,\quad e_n\to0,\quad-\log e_n/n\to\alpha,
\]

the actual chance-cover catalogue has the limit

\[
\boxed{\displaystyle
\lim_{n\to\infty}\frac1n\log r_{e_n}(n,\delta_n;Q)
 =\min\{S(\gamma),L_a(\alpha)\}.}
\tag{37.5}
\]

The success subset is allowed to depend on \(n\), as specified by (37.1).
The physical initial probability space is always the same \(Q\). No
exponential error conclusion is asserted for a fixed compact subset of
this probability space, or for the whole nonlinear family of the paper.

## 3. Exact reference cells, without an optimality assumption

First verify the dynamical assumptions in the selected subclass. Both
maps are global linear diffeomorphisms, with determinant
\(a_i^{2\beta-1}>0\), and have the required first-order matrices. Let
\(t_* =\max_i a_i^{\beta-1}<1\), take

\[
\Lambda=1+\frac{4t_*}{1-t_*},\quad
V(s,z)=\max\{\Lambda|s|,|z|\},\quad
\theta=\max\{\max_i a_i^\beta,\ t_*(1+1/\Lambda)\}<1.
\]

Directly from (37.3), \(V(F_i x)\le\theta V(x)\) on the whole plane.
Thus every binary input converges uniformly to the common origin on
bounded sets; this is not a pairwise distance-contraction assertion.

For \(s>0\), set \(y=z/s\). The angle maps and their inverse branches are

\[
T_0(y)=(y+a_1)/a_0,\quad T_1(y)=(y-a_0)/a_1,
\qquad f_0(y)=a_0y-a_1,\quad f_1(y)=a_1y+a_0.
\]

The one-step feasible angle domains are the closed intervals
\([-1,a_0-a_1]\) and \([a_0-a_1,1]\), so \(Q\) is controlled viable.
For a word \(w=i_1\cdots i_\ell\), write

\[
\lambda_w=\prod_{j=1}^{\ell}a_{i_j},\qquad
I_w=f_{i_1}\circ\cdots\circ f_{i_\ell}([-1,1])
   =[d_w-\lambda_w,d_w+\lambda_w].
\tag{37.6}
\]

This is the complete exact feasible angle interval for that word. Indeed,
each inverse branch maps \([-1,1]\) into \([-1,1]\), so membership in
the terminal inverse image entails every intermediate angle constraint.
The intermediate radii are \(s\lambda_{w|j}^{\beta}\le1\).
Conversely feasibility at the last time entails membership in (37.6).
For every real initial angle, feasible or not, the exact algebra is

\[
s_\ell=s\lambda_w^\beta,\qquad
y_\ell=(y-d_w)/\lambda_w.
\tag{37.7}
\]

Shared closed endpoints and the cone apex are never deleted. Their area
is zero and will have no effect on probability computations.

For \(n\ge1\), \(0<t<1\), let \(\mathcal L(n,t)\) be the finite
prefix-free tree stopped at the first time \(\lambda_w\le t\), or at
length \(n\), whichever comes first. These are reference cells, not a
claim about a necessary or optimal control catalogue. Their closed
intervals partition \([-1,1]\) with disjoint interiors. If
\(a_* =\min\{a_0,a_1\}\), then every leaf satisfies

\[
\lambda_w\ge a_*t,
\quad |I_w|=2\lambda_w,\quad
\sum_{w\in\mathcal L(n,t)}\lambda_w=1.
\tag{37.8}
\]

Threshold leaves also satisfy \(\lambda_w\le t\); unfinished
length-\(n\) leaves satisfy \(\lambda_w>t\). The coordinates
\((s,y)\mapsto(s,sy)\) give

\[
d\mu=s\,ds\,dy=(2s\,ds)(dy/2).
\tag{37.9}
\]

In particular, the entire actual region over a leaf has probability
\(\lambda_w\). Define

\[
C(n,t;e)=\min\{|J|:J\subset\mathcal L(n,t),
                          \ \sum_{w\in J}\lambda_w\ge1-e\}.
\tag{37.10}
\]

## 4. The actual approximate-input comparison

**Lemma 37.2.** There are system constants \(M>1\) and an integer
\(B\ge1\) such that for every \(n\ge1\), \(0<\delta<1\), and
\(0<e<3/4\),

\[
\frac1B C(n,\delta^{1/\beta};4e/3)
 \le r_e(n,\delta;Q)
 \le C(n,(\delta/M)^{1/\beta};e).
\tag{37.11}
\]

**Proof, lower comparison.** Fix \(s_0=1/2\) and the actual slab
\(s\in[s_0,1]\). Its probability is \(1-s_0^2=3/4\).
Given any infinite input \(u\), let \(v\) be its stopped prefix in
\(\mathcal L(n,t)\), where \(t=\delta^{1/\beta}\). This choice does not
assert that the input is feasible.

The functions \(z-s\) and \(-z-s\) have Euclidean Lipschitz constant
\(\sqrt2\) and are nonpositive on \(Q\). Thus any actual state within
distance \(\delta\) of \(Q\) satisfies
\((|z|-s)_+<\sqrt2\delta\). Applying the full-time condition at time
\(|v|\le n\), and using (37.7), gives, for every successfully covered
initial state in this slab,

\[
\operatorname{dist}(y,I_v)
 <\frac{\sqrt2\delta}{s_0}\lambda_v^{1-\beta}
 \le C_0t,\qquad C_0=\frac{\sqrt2}{s_0}a_*^{1-\beta}.
\tag{37.12}
\]

The last inequality uses (37.8) and \(\beta>1\). This argument applies
also to an input that previously left and subsequently re-entered \(Q\).
No earlier coding difference is being counted as a true exit. We only
use a necessary consequence of the actual constraint at a time inside
the stated horizon.

Expand the reference leaf interval \(I_v\) by \(C_0t\) on each side.
Outside its own interior it intersects at most

\[
B=5+2\left\lceil C_0/(2a_*)\right\rceil
\]

reference leaves, counting its own leaf in this bound. To see this,
each distinct other interior has length at least \(2a_*t\) by (37.8),
and each side extension has length \(C_0t\); at most two extra
intervals per side account for partial intersections and endpoint
contacts. This elementary count also covers adjacent singleton
endpoint contacts.

For a catalogue with \(R\) inputs, let \(U\subset[-1,1]\) be the union
of all reference leaf intervals so encountered. It uses at most
\(BR\) leaves, and by (37.12) contains the angular projection of every
success in the slab. For each angle outside \(U\), the whole slab
fails. Therefore (37.9) gives

\[
\frac34\,\mu_y(U^c)\le e,
\qquad\mu_y(dy)=dy/2.
\]

These leaves have total weight at least \(1-4e/3\). Taking the minimum
catalogue proves the left inequality of (37.11). This is the link
from arbitrary actual inputs to a weighted exact reference tree; the
tree was not assumed optimal.

**Proof, upper comparison.** Take \(M=4\sqrt2\Lambda\) and
\(t'=(\delta/M)^{1/\beta}\). Choose a subset realizing (37.10) for
\(n,t',e\). Every actual state above a chosen angular leaf can use
its exact feasible prefix. This satisfies all intermediate constraints.
If the leaf reaches the threshold at length \(\ell\le n\), then

\[
V(F_w(s,sy))=\Lambda s\lambda_w^\beta
 \le\Lambda\delta/M=\delta/(4\sqrt2).
\]

Append the same input \(000\ldots\) to every such leaf. The global
toward-origin contraction gives Euclidean norm at most \(\delta/4\)
at every remaining time, hence distance strictly less than \(\delta\)
from \(Q\), which contains the origin. A leaf stopped only at length
\(n\) remains exactly feasible through the complete horizon, and may
have any tail. The cone apex and shared endpoints can use any of
their feasible prefixes. Equation (37.9) shows that the covered
probability is at least \(1-e\). This proves the upper inequality and
also the existence of finite catalogues. The minimum in (37.1) is
then an attained integer. QED.

## 5. Weighted stopping-cover asymptotics

**Lemma 37.3.** Let \(t_n\in(0,1)\) tend to zero with
\(-\log t_n/n\to c\ge0\), and let \(e_n\to0\) satisfy
\(-\log e_n/n\to\alpha\in(0,\infty)\). Then

\[
\lim_{n\to\infty}\frac1n\log C(n,t_n;e_n)
 =\min\{S_{\rm ang}(c),L_a(\alpha)\},
\quad
S_{\rm ang}(c)=\max_p H_b(p)\min\{1,c/\chi(p)\}.
\tag{37.13}
\]

The proof is classical type counting once the actual comparison in
Lemma 37.2 has been established. We include it, so no formula missing
from an electronic rendering of a source is a premise.

### 5.1 Elementary type estimates and optimization

If \(p=j/N\) is a binary type, then

\[
\frac{e^{NH_b(p)}}{N+1}\le {N\choose j}\le e^{NH_b(p)},
\qquad
\frac{e^{-NI_a(p)}}{N+1}
 \le {N\choose j}e^{-N\chi(p)}\le e^{-NI_a(p)}.
\tag{37.14}
\]

For the first upper bound, the probability of that type under the
Bernoulli distribution of parameter \(p\) is at most one. For the
lower bound, its count \(j\) is a mode of that binomial distribution
(also for \(j=0,N\)), and a largest one of \(N+1\) probabilities
is at least \(1/(N+1)\). The second pair follows by multiplying by
\(e^{-N\chi(p)}\). There are at most \(N+1\) types.

For the optimization, relabel the frequency variable as the frequency
\(q\) of the smaller branch \(a=a_*<1/2\). Put

\[
c_b=-\log(1-a),\quad d=\log((1-a)/a)>0,
\quad \chi(q)=c_b+dq,\quad h=H_b(a),\quad c_s=\chi(1/2).
\]

Since \(I_a=\chi-H_b\ge0\), equality only at \(q=a\),
\(S_{\rm ang}(c)=c\) for \(0\le c\le h\).
For \(h<c<c_s\), let \(q_c=(c-c_b)/d\in(a,1/2)\).
The ratio \(H_b(q)/\chi(q)\) decreases for \(q>a\): its derivative
has numerator

\[
(c_b+d)\log(1-q)-c_b\log q,
\]

which vanishes at \(a\) and has strictly negative derivative.
On \(q\le q_c\), entropy is at most \(H_b(q_c)\); on
\(q>q_c\), the decreasing ratio gives the same upper bound for
\(cH_b(q)/\chi(q)\). Consequently

\[
S_{\rm ang}(c)=
\begin{cases}
c,&0\le c\le h,\\
H_b((c-c_b)/d),&h<c<c_s,\\
\log2,&c\ge c_s.
\end{cases}
\tag{37.15}
\]

Define \(J_a=I_a(1/2)=-\tfrac12\log(4a_0a_1)>0\).
The function \(I_a(q)\) is strictly increasing for \(q>a\).
No maximizer for \(L_a\) needs \(q<a\), where entropy is at most
\(h\). If \(q>1/2\), replacing it by \(1-q\) preserves entropy
and decreases \(\chi\), and therefore decreases \(I_a\). Thus

\[
L_a(\alpha)=H_b(q_\alpha),\qquad
q_\alpha=
\begin{cases}
\text{the unique }q\in(a,1/2)\text{ with }I_a(q)=\alpha,
   &0<\alpha<J_a,\\
1/2,&\alpha\ge J_a.
\end{cases}
\tag{37.16}
\]

In particular \(L_a(\alpha)\ge h\), and it is continuous for
\(\alpha>0\). Continuity at the cap in (37.16) is included.
Also \(S_{\rm ang}\) is continuous, or directly is Lipschitz with
constant at most \(\max H_b/\min\chi\) from its maximum definition.

### 5.2 Upper bounds

Let \(b_n=-\log t_n\) and \(c_{\max}=-\log a_*\). Every leaf of
length \(\ell\le n\) and type \(p\) has
\(\ell\chi(p)\le b_n+c_{\max}\), since the last threshold step
overshoots by at most one letter cost; unfinished leaves have smaller
total cost. Hence

\[
\frac\ell n H_b(p)\le
H_b(p)\min\{1,(b_n+c_{\max})/[n\chi(p)]\}.
\]

Summing the first upper estimate in (37.14) over all lengths and
types bounds the number of all leaves by

\[
(n+1)^2\exp\{nS_{\rm ang}((b_n+c_{\max})/n)\}.
\]

This proves an upper rate \(S_{\rm ang}(c)\) for \(C\).

For a separate reliability upper bound, fix \(\eta>0\) and keep the
length-\(n\) words with type \(I_a(p)\le\alpha+\eta\). By
(37.14), the omitted Bernoulli probability is at most
\((n+1)e^{-(\alpha+\eta)n}<e_n\) for all sufficiently large \(n\).
Replace each retained word by its stopped ancestor. This only merges
words and covers at least their original probability. The number of
ancestors is no more than

\[
(n+1)\exp\{nL_a(\alpha+\eta)\}.
\]

Letting \(\eta\downarrow0\) proves the other upper rate
\(L_a(\alpha)\). These two catalogue constructions may be different;
their smaller asymptotic rate gives the stated minimum.

### 5.3 Lower bounds, including critical cases

When \(0<c<h\), under the Bernoulli branch probabilities the
length-\(n\) accumulated letter cost divided by \(n\) tends to
\(h\). This follows, for example, from the finite variance of its
independent letters and Chebyshev's inequality. Therefore the total
weight \(P_n\) of threshold-stopped leaves tends to one. A selected
leaf set of weight at least \(1-e_n\) must carry at least
\(P_n-e_n\) of that threshold class. Each such leaf has weight at
most \(t_n\), so

\[
C(n,t_n;e_n)\ge(P_n-e_n)/t_n.
\]

Its lower rate is \(c\), equal to the minimum in (37.13) by
(37.15) and \(L_a\ge h\). When \(c=0\), \(C\ge1\) and the
full-tree upper rate tends to zero, which suffices.

For \(c\ge h\), fix any frequency \(q\) for which
\(\chi(q)<c\) and \(I_a(q)<\alpha\). Approximate it by types
\(q_n=j_n/n\). For large \(n\), every word of that type is an
unfinished length-\(n\) leaf: its total cost is below \(b_n\), and
all letter costs are positive, so every earlier prefix is also below
\(b_n\). Its full type class has weight at least

\[
(n+1)^{-1}\exp[-nI_a(q_n)].
\]

This weight is exponentially larger than \(e_n\), because the two
strict inequalities leave a fixed margin and the sequence exponents
have only \(o(n)\) errors. All words in this class have equal weight
\(e^{-n\chi(q_n)}\). A selected leaf set must consequently retain
at least half the class for all sufficiently large \(n\); distinct
leaf interiors cannot cover its omitted cells. By (37.14), this
forces lower rate at least \(H_b(q)\).

At \(c=h\), take \(q<a\) tending upward to \(a\). Then
\(\chi(q)<h\), \(I_a(q)<\alpha\) eventually, and
\(H_b(q)\to h\). This proves the critical lower rate \(h\).

At \(c>h\), define
\(q_c=\min\{1/2,(c-c_b)/d\}>a\).
Choose \(a<q<\min\{q_c,q_\alpha\}\) and let \(q\) tend
upward to this minimum, after taking the horizon limit. Both strict
inequalities hold before the final limit, also if \(c=c_s\) or
\(\alpha=J_a\). Equations (37.15)–(37.16) yield exactly
\(\min\{S_{\rm ang}(c),L_a(\alpha)\}\).
Integer type rounding is included in \(q_n\to q\). No limit is
interchanged across a vanishing strict margin. This completes all
cases of (37.13). QED.

## 6. Completion and its operational meaning

Apply Lemma 37.3 to both sides of (37.11). Multiplying \(e_n\)
by \(4/3\), multiplying \(\delta_n\) by \(1/M\), and dividing
the number of leaves by \(B\) leave the respective exponents
\(\alpha\), \(\gamma/\beta\), and the catalogue rate unchanged.
For large \(n\), \(e_n<3/4\). Since
\(S_{\rm ang}(\gamma/\beta)=S(\gamma)\), the matching limits
prove Theorem 37.1 for every allowed precision and error sequence.

There is an exact finite-horizon information interpretation. Suppose
a noiseless encoder observes the actual initial state once at time
zero and sends one fixed-length binary index to an actuator; the
actuator then applies the indexed infinite input, with no further
messages. A catalogue realizing (37.1) admits a Borel assignment:
choose the first successful member in a fixed ordering and choose
an arbitrary default on the failure set. Its sets are Borel because
the maps and the finite-time distance functions are continuous.
A catalogue of size \(R\) uses \(\lceil\log_2 R\rceil\) bits.
Conversely a \(b\)-bit index can specify no more than \(2^b\)
inputs, so its success requirement implies \(2^b\ge r_e\).
The minimum index length is exactly
\(\lceil\log_2 r_e\rceil\), with zero bits permitted when \(r_e=1\).
Thus Theorem 37.1 gives its per-horizon asymptotic bit cost as
\(\min\{S(\gamma),L_a(\alpha)\}/\log2\).
The conversion from catalogue size to index length is an elementary
equivalence, not an additional new theorem. The substantive application
is the joint precision–failure exponent in (37.5).
This is not a causal feedback data-rate theorem, channel capacity,
or stochastic stabilization claim.

For \(\gamma\le\beta h_a\), reliability does not change the rate
\(\gamma/\beta\). For \(\gamma>\beta h_a\), the vanishing-failure
rate is strictly greater than \(h_a\) whenever \(\alpha>0\), until
it reaches the full-state rate. In the intermediate precision
range it reaches that rate precisely when
\(\alpha\ge I_a(q_c)\), with
\(q_c=(\gamma/\beta-c_b)/d\).
At or above \(\gamma_s=-(\beta/2)\log(a_0a_1)\), it reaches
\(\log2\) precisely when \(\alpha\ge J_a\).
These consequences follow from (37.15)–(37.16), not from numerics.

## 7. Attribution and boundaries of the result

The exact branch intervals and common tail use the already studied
linear dynamics. The full-state spectrum \(S\) was already obtained
in R29 and is rederived only as a counting ingredient. \(L_a\),
binary types, relative entropy, and source error exponents are
classical tools, not new formulas or new methods.

The additional answer is the coupling of precision and an exponential
physical failure budget, proved by (37.11) for arbitrary approximate
inputs and all intermediate times. The current nonlinear regular
window only controls fixed area loss; it does not itself give this
exponential failure profile. No extension of (37.11) or (37.5) to
the whole nonlinear/noninjective family has been proved here.

The two directly checked sources and exact reading limitations are
in SOURCES.md. Their inspected statements do not supply (37.11).
This is not a claim to have excluded all literature on probabilistic
control coding. In particular, the electronic rendering of the
types paper loses displayed formulas; our proof is self-contained,
and a complete formal-version novelty exclusion is not claimed.
Theorem 37.1 is a quantitative application with an independent
operational question, not a new general controlled-geometric method.
