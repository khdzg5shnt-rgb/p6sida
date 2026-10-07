# R38 — A noncollapsing transient can change reliability costs

Pinned starting main: `81d0f39c5787e0794b2e5f897a8747b605ba5238`.
This note concerns exactly the matched structure class and physical
probability requirement authorised for R38. It gives a counterexample to
the proposed universal transfer, not another system class or a new
definition of catalogue. Logs are natural.

## 1. Object, dependency check, and conclusion

Let
\[
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad \mu=\operatorname{area}|_Q,
\qquad \operatorname{area}(Q)=1.
\]
For an infinite binary input \(u\), retain the actual covered set
\[
A_u^F(n,\delta;Q)=\{x\in Q:
 \operatorname{dist}_2(F_u^jx,Q)<\delta\text{ for every }0\le j\le n\}.
\]
Let \(r_e^F(n,\delta;Q)\) be the minimum finite catalogue size whose
union of these sets has \(\mu\)-measure at least \(1-e\). All binary
inputs are allowed; assignments depend on actual states, and departure
and re-entry are permitted subject to every constraint. The probability
space remains the same uniform physical triangle. Only the success set
may change with the horizon.

The R37 linear stopping comparison was checked directly: the stopping
leaf weight is at least \(a_*\delta^{1/\beta}\); the constraint at that
leaf time places every successfully covered positive-radius angle in
a constant-size neighbouring-leaf cover; the slab has mass \(3/4\),
giving the error factor \(4/3\). The upper construction uses an exactly
feasible prefix and a common norm-small tail at every remaining time.
The strict-frequency lower bounds, critical exponents and \(o(n)\)
sequence errors in its type argument are valid. No repair is needed.

R33 instead deletes a *fixed* small area, then uses finitely many regular
inverse charts and all-prefix typicality on a fixed compact window.
Its null-pullback proof correctly uses the domain feasible before the
last step; that output may be outside \(Q\). Its constants are not
uniform as the deleted area tends exponentially to zero. Nothing in
that proof supplies such uniformity, and the following construction
shows that it cannot hold in the whole class.

**Theorem 38.1 (failure of the universal reliability transfer).**
There is a single pair of global \(C^2\) maps in the R38 matched class
with
\[
a_0=2^{-10},\quad a_1=1-2^{-10},\quad \beta=4096,
\quad \lambda=a_0a_1,\quad
\gamma=-\beta\log\lambda,\quad \alpha=1/8,
\tag{38.1}
\]
such that, for *every* pair of sequences
\[
\delta_n\to0,\quad -\log\delta_n/n\to\gamma,
\qquad e_n\to0,\quad -\log e_n/n\to\alpha,
\]
with positive tolerances and \(0<e_n<1\),
\[
\liminf_n\frac{\log r_{e_n}^F(n,\delta_n;Q)}n
 \ge\frac{\log2}{2}
 >\min\{S(\gamma),L_a(\alpha)\}.
\tag{38.2}
\]
Both maps are even globally injective homeomorphisms, although their
inverses are not differentiable everywhere. Each critical set in \(Q\)
has area zero, and no positive-area set is collapsed onto a null set.
The specified first derivatives, controlled feasibility and a common
global toward-origin norm contraction all hold.

In fact, for every \(n\ge1\) and \(\delta>0\), the *full-state*
catalogue equals that of the matched linear pair:
\[
r_F(n,\delta;Q)=r_{\mathsf A}(n,\delta;Q).
\tag{38.3}
\]
Thus the obstruction is not a change in the full-state spectrum or
the earlier fixed-area theorem. It is an exponential-scale change in
physical probabilities during one nonlinear transient.

Here \(H_b,\chi,I_a,S,L_a\) have the definitions in the R38 instruction;
in particular \(I_a(p)=\chi(p)-H_b(p)\). The theorem only needs a
strict lower-rate gap. It does not assert an exact new chance-cover
rate or its limit for this example.

## 2. Two Cantor sets and a fixed C² increasing map

Use the reference inverse angle maps
\[
f_0(y)=a_0y-a_1,\qquad f_1(y)=a_1y+a_0.
\]
The block maps for the two actual words \(01,10\) are
\[
B_0=f_0\circ f_1=\lambda y+a_0^2-a_1,
\qquad B_1=f_1\circ f_0=\lambda y+a_0-a_1^2.
\tag{38.4}
\]
Let
\[
A=\frac{a_0^2-a_1}{1-\lambda},\qquad
B=\frac{a_0-a_1^2}{1-\lambda},\qquad
\ell=B-A=\frac{2\lambda}{1-\lambda}>0.
\]
Both endpoints are strictly inside \((-1,1)\): they are the reference
angles of \((01)^\infty\) and \((10)^\infty\), and directly
\(A+1=2a_0^2/(1-\lambda)>0\), \(1-B=2a_1^2/(1-\lambda)>0\).
The two images of
\([A,B]\) under (38.4) are its left and right subintervals of relative
length \(\lambda<1/2\). Their gap has length \((1-2\lambda)\ell\).
The associated ordered Cantor set \(\mathcal C\) consists of angles
whose reference control is an infinite concatenation of \(01,10\).

For the source interval \(J=[-1/2,1/2]\), fix \(b=2/5\) and the maps
\[
h_0(y)=by-(1-b)/2,\qquad h_1(y)=by+(1-b)/2.
\tag{38.5}
\]
Their Cantor set \(\mathcal D\) has zero length, because the total
length of its level-\(k\) intervals is \((2b)^k\to0\).
For a block address \(\sigma\in\{0,1\}^k\), put
\[
J_\sigma=h_{\sigma_1}\circ\cdots\circ h_{\sigma_k}(J),
\qquad Z_\sigma=B_{\sigma_1}\circ\cdots\circ B_{\sigma_k}([A,B]).
\tag{38.6}
\]
They have lengths \(b^k\) and \(\ell\lambda^k\). Within each family
the closed intervals are separated by positive gaps. Both infinite
address maps are unique, including their endpoints, and preserve
lexicographic order. The target Cantor set has zero length since
\((2\lambda)^k\to0\).

We construct an increasing \(C^2\) homeomorphism \(g:\mathbb R\to
\mathbb R\) such that
\[
g(y)=y\ (|y|\ge1),\quad g([-1,1])=[-1,1],\quad
g(J_\sigma)=Z_\sigma,\quad
g'(y)=0\iff y\in\mathcal D.
\tag{38.7}
\]
In particular \(|g(y)-y|\le2\) globally. This construction is a
classical flat Cantor interpolation; its regularity is proved here.

Let \(E(t)=e^{-1/t}\) for \(t>0\), and zero otherwise, and define
\[
\phi(t)=E(t)E(1-t),\qquad
\sigma(t)=\frac{\int_0^t\phi(v)\,dv}{\int_0^1\phi(v)\,dv}
\quad(0\le t\le1),
\]
extended by zero to the left and one to the right. It is smooth,
strictly increasing on \((0,1)\), and flat at its two endpoints.
First map each point of \(\mathcal D\) to the point of
\(\mathcal C\) with the same block address. On a source gap \((u,v)\)
with corresponding target gap \((U,V)\), put
\[
g(y)=U+(V-U)\sigma((y-u)/(v-u)).
\tag{38.8}
\]
The endpoints of each \(J_\sigma\) belong to \(\mathcal D\) and
are sent to the endpoints of \(Z_\sigma\). Strict increase on the
gaps and the ordered Cantor correspondence therefore give the full
interval identity in (38.7), not just an identity on Cantor points.
The correspondence of gaps is determined by their finite address.
A level-\(k\) gap has source and target lengths
\[
(1-2b)b^k,\qquad (1-2\lambda)\ell\lambda^k.
\]
For \(j=1,2\), its interior derivative satisfies
\[
|g^{(j)}(y)|\le C_j(\lambda/b^j)^k.
\tag{38.9}
\]
Here the constants only involve the fixed lengths and derivatives of
\(\sigma\). Since \(\lambda<2^{-10}<b^2\), these bounds tend to
zero with the level. Define candidate derivatives \(q_1,q_2\) as the
derivatives in the gaps and zero on \(\mathcal D\). They are
continuous: for high-level gaps use (38.9); at endpoints of any
fixed finite collection of gaps use the flatness of \(\sigma\).

For completeness the candidate derivatives are the actual derivatives,
not merely continuous assignments. The integral of \(q_1\) over each
gap is its target gap length. Since the target Cantor set is null,
order preservation shows
\[
g(x)=A+\int_{-1/2}^x q_1(y)\,dy\qquad(x\in J).
\]
Indeed the target interval up to a Cantor point is exhausted in length
by its complete gaps; for a point inside a gap add the partial integral
in (38.8). Also
\[
\sum_{\text{gaps}}\int|q_2|
 \le C\sum_{k\ge0}(2\lambda/b)^k<\infty.
\]
Each complete-gap integral of \(q_2\) is zero, since \(q_1\) is zero
at its two endpoints; a partial-gap integral is \(q_1(x)\).
The source Cantor set is null. It follows that
\(q_1(x)=\int_{-1/2}^xq_2(y)\,dy\). The fundamental theorem of
calculus now gives \(g'=q_1\), \(g''=q_2\) on \(J\).
Thus \(g\) is \(C^2\) there, with both derivatives zero on
\(\mathcal D\) and positive first derivative on every gap.

Extend to \([-1,-1/2]\) and \([1/2,1]\) as follows. On an interval
\([L,R]\) with a prescribed positive total increment \(T\), take
\(d=\min\{(R-L)/4,T/4\}\) and the positive interior bump
\(v(x)=E(x-L)E(R-x)\). For the left extension choose
\(c(x)=1-\sigma((x-L)/d)\); for the right choose
\(c(x)=\sigma((x-R+d)/d)\). In either case \(\int_L^R c\le d<T\).
Use the density
\[
q(x)=c(x)+\frac{T-\int_L^R c}{\int_L^R v}\,v(x).
\tag{38.10}
\]
For the left interval set \((L,R,T)=(-1,-1/2,A+1)\), and integrate
starting at \(g(-1)=-1\). It joins the identity with first derivative
one and second derivative zero at \(-1\), and joins (38.8) with both
derivatives zero at \(-1/2\). For the right interval set
\((L,R,T)=(1/2,1,1-B)\), integrating from \(g(1/2)=B\); the
endpoint roles are reversed. Density (38.10) is positive in each
interior. Extend by the identity outside \([-1,1]\). This proves
all of (38.7), including strict increase on the whole line. The map
itself is fixed once and for all; it does not depend on \(n\) or on
the precision or failure sequences.

## 3. The actual maps and every standing assumption

With the same \(E\), set
\[
\psi(s)=\frac{E(s-1/4)}{E(s-1/4)+E(1/2-s)}.
\]
The denominator is positive everywhere. This smooth function is zero
for \(s\le1/4\), one for \(s\ge1/2\), and strictly between them
in between. Define on the whole plane
\[
H(s,z)=
\begin{cases}
(s,z),&s\le1/4,\\
(s,z+s\psi(s)[g(z/s)-z/s]),&s>1/4,
\end{cases}
\qquad F_i=\mathsf A_i\circ H,
\tag{38.11}
\]
where
\[
\mathsf A_0=\begin{pmatrix}a_0^\beta&0\\
a_0^{\beta-1}a_1&a_0^{\beta-1}\end{pmatrix},\qquad
\mathsf A_1=\begin{pmatrix}a_1^\beta&0\\
-a_1^{\beta-1}a_0&a_1^{\beta-1}\end{pmatrix}.
\]

**Regularity and first derivatives.** The quotient in (38.11) is used
only for \(s>1/4\). Flatness of \(\psi\) at \(1/4\) joins the
formula in \(C^2\). Near each such point all the derivatives of
\(g(z/s)\) needed here are bounded locally. Thus the maps are global
\(C^2\); no higher regularity of \(g\) at its Cantor set is claimed.
Near the origin \(H\) is the identity, so \(F_i(0)=0\) and
\(DF_i(0)=\mathsf A_i\), exactly the prescribed matching.

**Controlled viability.** At each fixed \(s>0\), the angle action of
\(H\) is the increasing homeomorphism
\[
g_s(y)=(1-\psi(s))y+\psi(s)g(y).
\]
It maps \([-1,1]\) onto itself. The linear feasible domains
\([-1,a_0-a_1]\), \([a_0-a_1,1]\) cover that interval. For any
\(x\in Q\), choose the corresponding linear feasible control at
\(H(x)\); its radius is \(a_i^\beta s\le1\). This proves
\(Q\subset F_0^{-1}Q\cup F_1^{-1}Q\), including all edge and apex
states. It also gives finite exact catalogues, so \(r_e^F\) is a
well-defined minimum integer and at most \(2^n\).

**Global common norm.** Put
\[
m=\max_i\{a_i^\beta,a_i^{\beta-1}\}<1,\qquad
\Lambda=1+\frac{10m}{1-m},\qquad V(s,z)=\max\{\Lambda|s|,|z|\}.
\]
From (38.7), \(|H^z-z|\le2|s|\) everywhere. Therefore
\[
V(Hx)\le(1+2/\Lambda)V(x),\qquad
V(\mathsf A_i x)\le m(1+1/\Lambda)V(x).
\]
Consequently
\[
V(F_i x)\le\theta V(x),\qquad
\theta=m(1+1/\Lambda)(1+2/\Lambda)
 \le m(1+5/\Lambda)<(1+m)/2<1.
\tag{38.12}
\]
This is a whole-plane estimate for both inputs, including trajectories
which leave \(Q\). It proves uniform convergence of every input on
bounded initial sets. It is only toward-origin contraction.

**Null critical sets and no positive-area collapse.** For \(s>1/4\),
\[
\det DH(s,z)=1-\psi(s)+\psi(s)g'(z/s),\qquad
\det DF_i=a_i^{2\beta-1}\det DH.
\tag{38.13}
\]
For \(s\le1/4\), \(\det DH=1\). Because \(g'>0\) outside
\(\mathcal D\), the critical set in \(Q\) is exactly
\[
\{(s,sy):1/2\le s\le1,\ y\in\mathcal D\}.
\]
It has area zero by Fubini and the physical Jacobian \(s\).
There is no positive-area saturated region. A countable cover by
regular local inverse charts off this null set shows that the
pullback of any null target set has area zero, just as in R33.
Thus \(H_*\mu\) is absolutely continuous, and no positive-area
initial set can be sent into a null set by either control.

In fact \(H\) is globally one-to-one and onto: it leaves \(s\)
fixed, and its angle map on each \(s>1/4\) fibre is strictly
increasing and equals the identity outside \([-1,1]\). Continuity
and properness give a continuous inverse; properness follows, for
example, from \(|H^z-z|\le2|s|\) and the unchanged first coordinate.
Each \(F_i\) is therefore a global homeomorphism too. It is not a
global diffeomorphism, and this particular \(H\) is not bi-Lipschitz:
its angular derivative vanishes on \(\mathcal D\).

**One transient step and unchanged full catalogues.** Write
\(\rho_i=a_i^\beta\). Our fixed choice gives
\[
\rho_1=(1-2^{-10})^{4096}<e^{-4}<1/4,
\qquad \rho_0<1/4.
\]
From any \(x\in Q\) the first output radius is \(\rho_i s<1/4\),
whether or not its angle is feasible. Since the first coordinate is
always \(\rho_i s\), all subsequent maps use the identity part of
\(H\), even on an approximate trajectory outside \(Q\). Hence,
for every input and all \(j\ge1\),
\[
F_u^j x=\mathsf A_u^j Hx\qquad(x\in Q).
\tag{38.14}
\]
At time zero both \(x\) and \(Hx\) lie in \(Q\). Thus
\(A_u^F(n,\delta;Q)=H^{-1}(A_u^{\mathsf A}(n,\delta;Q))\) on
\(Q\). Since \(H(Q)=Q\), full covers correspond bijectively,
proving (38.3). Probability covers correspond only after transporting
\(\mu\) to \(H_*\mu\), which is not uniform area. We do not assert
that all nonlinear members are irreducible to old coordinates, or
claim exclusion of some other possible conjugacy. The specific
non-bi-Lipschitz probability transport is the issue here.

## 4. Positive-area families with physically forced prefixes

Every reference sequence made of the blocks \(01,10\) has run length
at most two. At every shifted position its reference angle satisfies
\[
|y_j|\le1-d,\qquad d=2a_*^3>0,\qquad a_* =a_0.
\tag{38.15}
\]
Indeed \(f_0(y)+1=a_0(y+1)\) and
\(1-f_1(y)=a_1(1-y)\); within the next three digits the opposite
digit inserts an endpoint distance at least \(2a_*\).
Multiplying by at most two preceding factors gives (38.15).

For \(\sigma\in\{0,1\}^k\), let \(w(\sigma)\) be the length-\(2k\)
word replacing zero by \(01\) and one by \(10\). Each point of
\(Z_\sigma=f_{w(\sigma)}([A,B])\) has all its first \(2k\) angular
outputs within \([-1+d,1-d]\) when using that word. To prove this
for the *whole interval*, not only the Cantor subset, observe that
its two endpoints come from two infinite block sequences. Their
outputs satisfy (38.15). Each angular map is affine and increasing,
so every intervening point has outputs between the endpoint outputs
at every one of those times. No full terminal-image assumption or
chosen-strategy optimality is involved.

If a chosen zero gives output angle at most \(1-d\), its current
angle is at most \(a_0-a_1-a_0d\), so the other control gives an
angle at most \(-1-(a_0/a_1)d\). If a chosen one gives output at
least \(-1+d\), the symmetric bound for the other control is
\(1+(a_1/a_0)d\). Both wrong-control excesses are therefore at least
\[
d_*=(a_*/a^*)d>0,\qquad a^*=a_1.
\tag{38.16}
\]

Consider the actual sets of initial states
\[
E_{\sigma,k}=\{(s,sy):1/2\le s\le1,\ y\in J_\sigma\},
\qquad E_k=\bigcup_{|\sigma|=k}E_{\sigma,k}.
\tag{38.17}
\]
Here \(\psi=1\), and (38.7) sends every such angle into
\(Z_\sigma\) at the preprocessing step. Along the assigned word
the first radius and every later radius are the exact products
\(s\lambda_{w|j}^\beta\). The prefix stays in \(Q\) at every
step; at its end any exactly feasible continuation is available.
These are positive-area physical sets, not symbolic points replacing
the initial triangle. Their areas are
\[
\mu(E_{\sigma,k})=\int_{1/2}^1 s\,ds\,|J_\sigma|
 =\frac38 b^k,
\qquad \mu(E_k)=\frac38(2b)^k.
\tag{38.18}
\]

Fix one of these states and an *arbitrary* input which first differs
from \(w(\sigma)\) at time \(j\le2k\). Up to that time it has
the same physical states as the feasible prefix. At \(j=1\) the
common angle preprocessing is \(g\), so (38.16) applies there too;
for later steps (38.14) is linear. The preceding product is at least
the full word product \(\lambda^k\). The wrong output therefore has
\[
|z_j|-s_j\ge c_0\lambda^{\beta k},\qquad
c_0=\frac12 a_*^\beta d_*>0.
\tag{38.19}
\]
The function \(|z|-s\) is Euclidean \(\sqrt2\)-Lipschitz and is
nonpositive on \(Q\). Thus (38.19) gives a distance at least its
right side divided by \(\sqrt2\). It is a violation at an actual
time within the horizon; later re-entry cannot remedy it.

Set \(k=k_n=\lfloor n/2\rfloor\). For every precision sequence
in Theorem 38.1,
\[
\lim_n\frac1n\log\frac{c_0\lambda^{\beta k_n}}{2\delta_n}
 =\gamma+\frac\beta2\log\lambda
 =-\frac\beta2\log\lambda>0.
\tag{38.20}
\]
For sufficiently large \(n\), an input successful at any point
of \(E_{\sigma,k_n}\) must consequently agree with the entire
length-\(2k_n\) word \(w(\sigma)\). A single arbitrary catalogue
member can succeed on at most one of the \(2^{k_n}\) sets in
(38.17). This is a physical forcing statement for arbitrary
approximate inputs, not merely uniqueness of a prescribed code.
Every estimate is uniform on the whole radial band and closed
angle intervals, including their endpoints. Odd horizons just leave
one additional constrained time; it cannot increase the mass one
input already covers in these sets.

## 5. Strict gap for the true optimal catalogue

For a catalogue of size \(R\), (38.18) and the forcing statement give
\[
\mu\left(E_{k_n}\cap\bigcup_{u\in W}A_u^F(n,\delta_n;Q)\right)
 \le R\frac38 b^{k_n}.
\]
At most \(e_n\) of the entire \(Q\), and hence at most \(e_n\)
of \(E_{k_n}\), can fail. Therefore every successful catalogue obeys
\[
R\ge 2^{k_n}-\frac{8e_n}{3b^{k_n}}
 =2^{k_n}\left(1-\frac{8e_n}{3(2b)^{k_n}}\right).
\tag{38.21}
\]
Our fixed error exponent is larger than the exponent of the physical
rare layer, since
\[
-\tfrac12\log(2b)=\tfrac12\log(5/4)<1/8=\alpha.
\]
The strict inequality follows from \(\log(1+x)<x\) with \(x=1/4\).
Thus the parenthesis in (38.21) tends to one for every allowed error
sequence. This proves the lower rate \((\log2)/2\), with the full
sequence quantifiers and integer rounding included.

It remains to compare that rate to the actual candidate in the question.
At \(p=1/2\), \(\chi(p)=-\tfrac12\log\lambda\), and (38.1) gives
\(\gamma/[\beta\chi(p)]=2\). Hence \(S(\gamma)=\log2\).
For \(q=1/16\),
\[
H_b(q)=\tfrac14\log2+\tfrac{15}{16}\log(16/15)
 <\tfrac14\log2+1/16<\tfrac12\log2,
\tag{38.22}
\]
where \(\log2>1/2\), for example by integrating \(1/t>1/2\)
on \([1,2)\). Moreover
\[
I_a(q)=\chi(q)-H_b(q)
 >\tfrac{10}{16}\log2-H_b(q)
 >\tfrac38\log2-1/16>1/8.
\tag{38.23}
\]
The function \(I_a\) strictly increases above \(a_0\), since its
derivative is \(\log[p a_1/((1-p)a_0)]\). Its nonempty compact
sublevel set \(\{I_a\le1/8\}\) therefore has a largest point
\(q'<1/16\), and lies in \([0,q']\). Entropy is increasing on
\([0,1/16]\), so
\[
L_a(1/8)<H_b(1/16)<\tfrac12\log2.
\tag{38.24}
\]
Together (38.20)–(38.24) prove (38.2) and disprove the proposed
universal transfer. In particular the gap exceeds
\(\tfrac14\log2-1/16>0\), without numerical fitting or enumeration.
An upper rate \(\log2\) is supplied by complete exact catalogues.
The present proof does not determine where between these bounds the
example's exact chance-cover rate lies, or assert its limit.

## 6. The fixed-window constants really acquire an exponential cost

The same example quantifies the finite-transient obstruction; it is
not just a restatement of an unknown factor. Let \(E_k^0\) be the
union in (38.17) restricted to block addresses starting with zero.
It has \(2^{k-1}\) intervals for \(k\ge1\). Put
\(B_k^0=H(E_k^0)\). Their exact areas are
\[
\mu(E_k^0)=\tfrac3{16}(2b)^k,\qquad
\operatorname{area}(B_k^0)=\tfrac3{16}\ell(2\lambda)^k.
\]
Every state in \(E_k^0\) has a feasible first zero control, so
\(F_0(E_k^0)=\mathsf A_0 B_k^0\subset Q\). Let \(T_n\subset Q\)
be *any* measurable sets with \(\mu(T_n)\ge1-e_n\). For large \(n\),
at \(k=k_n\), at least half of \(E_k^0\) remains in \(T_n\).
If a finite inverse-area constant \(L_n\) satisfies even just
\[
\mu(T_n\cap F_0^{-1}B)\le L_n\operatorname{area}(B)
\quad\text{for all measurable }B\subset\mathbb R^2,
\]
then, taking \(B=\mathsf A_0B_k^0\) and using
\(\det\mathsf A_0=a_0^{2\beta-1}>0\), it must obey
\[
L_n\ge\frac{1}{2\ell\det\mathsf A_0}(b/\lambda)^{k_n},
\qquad \liminf_n\frac{\log L_n}n
 \ge\tfrac12\log(b/\lambda)>0.
\tag{38.25}
\]
If no such finite constant exists, it certainly cannot be replaced by
a subexponential one. This covers all possible regular-window
selections with the specified error loss, not one failed choice.
It uses an actual feasible transient branch, and no derivative
condition at an outside last output.

For fixed positive area loss, R33 can remove a sufficiently fine
level neighbourhood and still obtain a finite constant. For the
exponential failure loss, (38.25) forbids a subexponential constant.
Null pullbacks and absolute continuity are intact, but they do not
preserve the large-deviation weights. This is precisely the difference
between the two tasks, with the underlying uniform \(Q\) unchanged.

## 7. Scope and attribution

The target universal formula is **false**, resolved here by a single
fixed admissible counterexample and a lower bound for *all* actual
catalogues. R37 remains valid on its matched linear subclass. The
unique paper's fixed-loss noncollapse theorem is unaffected: (38.3)
even preserves all full-state finite-horizon counts, and the rare
layers (38.18) tend to zero area. No positive-area collapse, ignored
boundary state, changed tolerance, or restricted set of inputs was used.

Cantor interpolation, null-set pullback arguments, linear angle coding
and elementary entropy inequalities are classical tools. The new project
answer is their connection to the physical finite-transient failure
budget: an explicit exponential lower bound for the true optimal
catalogue, and the unavoidable inverse-area cost (38.25). It is not a
new source-coding formula or general pressure method. It identifies a
limit to exporting the R37 reliability law from first-order and
qualitative noncollapse data alone.

The two directly reviewed sources and formal-version limits are recorded
in SOURCES.md. This note does not certify field-wide novelty. The
counterexample is complete; a sufficient quantitative probability-
transport criterion or the exact new reliability spectrum is not proved
here and is not automatically pursued as a second task. The unique
manuscript remains unchanged, and the bounded R38 task stops here.
