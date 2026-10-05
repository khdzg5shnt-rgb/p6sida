# R22: real catalogues under angular feedback

5 October 2026. Baseline main: 68df1453eafe7483d73e361372bb50122eb8ad0e.

## 1. Object and complete conclusion

Fix $a_0,a_1\in(0,1)$, $a_0+a_1=1$, $a_0\ne a_1$, $\beta>1$, and
$$
0<\epsilon<\frac{\min(a_0,a_1)}{16(\beta+1)}.
$$
On the whole plane put
$$
p_0(s,z)=a_0+\frac{\epsilon z}{1+s^2+z^2},\qquad
p_1(s,z)=a_1-\frac{\epsilon z}{1+s^2+z^2},
$$
$$
H_0(s,z)=(p_0^\beta s,\ p_0^{\beta-1}(z+p_1s)),\qquad
H_1(s,z)=(p_1^\beta s,\ p_1^{\beta-1}(z-p_0s)).
\tag{1}
$$
All factors in (1) are evaluated at the input state. Let
$Q=\{0\le s\le1,\ |z|\le s\}$; its physical planar area is 1.
For an infinite input $u$ and an actual initial state $x$, let $x_j^u$
be the state after $j$ applications. Define
$$
V(n,\delta,u)=\{x\in Q:\operatorname{dist}_2(x_j^u,Q)<\delta
                       \text{ for every }j=0,\ldots,n\}.
$$
For compact $K\subset Q$, $r_H(n,\delta;K)$ is the minimum cardinality
of a finite family of infinite inputs whose sets $V$ cover $K$.
Inputs may depend on the actual initial state through assignment to this
family. No exact itinerary, prescribed partition, or common input is
required; exits and reentries are allowed. The constructions below prove
finiteness. Using a closed instead of open neighbourhood changes none
of the conclusions.

Write $h=-a_0\ln a_0-a_1\ln a_1$. All logarithms are natural.

**Theorem 22.1 (the entire stipulated family).** The maps (1) are global
$C^\infty$ diffeomorphisms with common fixed origin, the prescribed
linear first jets, uniform convergence to the origin for all inputs on
each bounded initial set, and controlled invariance of $Q$. For every
fixed positive-area compact $K\subset Q$, every finite $\gamma\ge0$, and
every sequence $\delta_n\to0$ with $-\ln\delta_n/n\to\gamma$,
$$
\min\{h,\gamma/\beta\}\le
\liminf_n\frac{\ln r_H(n,\delta_n;K)}n
\le\limsup_n\frac{\ln r_H(n,\delta_n;K)}n
\le\min\{\ln2,\gamma/\beta\}.
\tag{2}
$$
In particular, for $0\le\gamma\le\beta h$ the limit is $\gamma/\beta$.
For every $\zeta\in(0,1)$ there is ONE fixed positive-area compact
$K_\zeta\subset Q$ with $\operatorname{area}(K_\zeta)>1-\zeta$ such that,
simultaneously for every finite $\gamma>\beta h$ and every corresponding
precision sequence,
$$
\lim_n\frac{\ln r_H(n,\delta_n;K_\zeta)}n=h
<\liminf_n\frac{\ln r_H(n,\delta_n;Q)}n.
\tag{3}
$$
This set is chosen before $\gamma$, the precision sequence, and the
horizon. No exact high-precision spectrum or high-side limit for $Q$
is asserted.

The new interface is the graph and first-deviation estimate in §§3–5.
The threshold deductions in §6 use the established R19/R20 argument
after that interface has been proved here; they are not a new entropy
or pressure method. Section 7 gives a scoped, rigorous exclusion of
coordinate reduction, rather than assuming that a nonlinear formula is
a new mechanism.

## 2. Global candidate checks

Set $a_*=\min(a_0,a_1)$,
$$
p_-=a_*-\epsilon/2,\qquad p_+=1-p_-,\qquad r=p_+^\beta<1.
$$
Both $p_i$ lie in $[p_-,p_+]$ on the whole plane. For
$f=z/(1+s^2+z^2)$ direct differentiation gives
$$
|f|\le\tfrac12,\quad |s f_s|\le1,\quad
|z f_z|\le\tfrac12,\quad |s f_z|\le\tfrac12.
\tag{4}
$$
These inequalities follow by inserting
$f_s=-2sz/(1+s^2+z^2)^2$ and
$f_z=(1+s^2-z^2)/(1+s^2+z^2)^2$ and using
$2|sz|\le s^2+z^2$.

Let $\sigma_0=-1$, $\sigma_1=1$. In shear coordinates
$v=z-\sigma_i s$, the input/output form of $H_i$ is
$$
(s,v)\longmapsto (S,V)=(s p_i^\beta,\ v p_i^{\beta-1}),
$$
where the output shear is $V=Z-\sigma_i S$.
In the original coordinates its Jacobian determinant is
$$
\det DH_i
=p_i^{2\beta-2}
 \{p_i+\beta s(p_i)_s+((\beta-1)z+\sigma_i s)(p_i)_z\}>0.
\tag{5}
$$
Indeed, the absolute value of the added derivative terms is at most
$3\beta\epsilon/2$, and $p_--3\beta\epsilon/2>0$.

Global bijectivity is not inferred just from (5). Given $(S,V)$ and
$t\in[p_-,p_+]$, define
$$
s(t)=S t^{-\beta},\quad v(t)=Vt^{1-\beta},\quad
z(t)=v(t)+\sigma_i s(t),\quad F(t)=t-p_i(s(t),z(t)).
$$
Then $F(p_-)\le0\le F(p_+)$ and, by (4),
$$
F'(t)=1+
\frac{\beta s(p_i)_s+((\beta-1)z+\sigma_i s)(p_i)_z}{t}
\ge1-\frac{3\beta\epsilon}{2p_-}>0.
$$
There is exactly one root. It supplies the unique preimage, and the
implicit function theorem gives a smooth inverse everywhere, including
at $(S,V)=(0,0)$. Positivity of $p_i$ also makes every real power smooth.
The first jets are
$$
DH_0(0)=
\begin{pmatrix}a_0^\beta&0\\a_0^{\beta-1}a_1&a_0^{\beta-1}\end{pmatrix},
\qquad
DH_1(0)=
\begin{pmatrix}a_1^\beta&0\\-a_1^{\beta-1}a_0&a_1^{\beta-1}\end{pmatrix}.
$$

Choose $M\ge1$ with $M>r/(1-p_+^{\beta-1})$, and set
$$
\|(s,z)\|_*=\max(M|s|,|z|),\qquad
L=\max\{r,p_+^{\beta-1}+r/M\}<1.
$$
For every state in the whole plane and either input,
$$
\|H_i(s,z)\|_*\le L\|(s,z)\|_*.
\tag{6}
$$
This follows from $|s'|\le r|s|$ and
$|z'|\le p_+^{\beta-1}|z|+r|s|$.
It proves all-input convergence and will control complete tails even
after leaving $Q$. It is a bound relative to the origin, not a claimed
pairwise contraction estimate.

For $s>0$ use $y=z/s$ only as a calculation coordinate, and write
$P_i(s,y)=p_i(s,sy)$. The actual map becomes
$$
S=sP_i^\beta,\qquad Y=\sigma_i+\frac{y-\sigma_i}{P_i}.
\tag{7}
$$
This does not replace the physical initial set or its Euclidean metric.
On $0<s\le1$, $|y|\le1$,
$$
|(P_i)_s|\le\epsilon,\qquad |(P_i)_y|\le\epsilon s.
\tag{8}
$$
There is a unique $\theta(s)\in(-1,1)$ satisfying
$$
\theta(s)=2P_0(s,\theta(s))-1
=a_0-a_1+\frac{2\epsilon s\theta(s)}
                    {1+s^2+s^2\theta(s)^2}.
\tag{9}
$$
The defining function has derivative at least $1-2\epsilon$ in $y$,
and opposite signs at $-1,1$. The COMPLETE one-step feasible branches
are $[-1,\theta(s)]$ for 0 and $[\theta(s),1]$ for 1; (7) maps their
angular endpoints onto $-1,1$. Since $S<s\le1$, these are exactly
$Q\cap H_i^{-1}Q$, with the apex included. Choosing 0 at the shared
endpoint defines a Borel natural exact code for all actual states in
$Q$. This proves controlled invariance.

## 3. Moving radial graphs: the decisive geometry

Fix an actual initial radius $0<s_0\le1$. Along a complete feasible word
the image of the initial horizontal fibre will be a graph $s=S(y)$
over the entire interval $[-1,1]$, not a fibre of constant radius.
The radius is allowed to depend on the initial angle.

**Lemma 22.2 (invariant graph cone and full feasible intervals).**
For every finite word $w$, its complete feasible initial angular set
$I_w(s_0)$ is a nondegenerate closed interval. Its terminal angular map
$Y_{w,s_0}$ is increasing and maps that interval diffeomorphically onto
$[-1,1]$. Its terminal radial graph satisfies
$$
\left|\frac{S'(y)}{S(y)}\right|\le1.
\tag{10}
$$
The intervals for a complete prefix-free tree cover $[-1,1]$, with
disjoint interiors and all shared endpoints retained.

**Proof.** Suppose (10) holds for a feasible-prefix graph, and put
$k=S'/S$. Along that graph, for branch $i$,
$$
A=(P_i)_s S'+(P_i)_y,\qquad |A|\le2\epsilon S.
$$
By (7),
$$
q_i=1-\frac{(y-\sigma_i)A}{P_i},\quad
\frac{dY}{dy}=\frac{q_i}{P_i}>0,\quad
k_{\rm new}=\frac{P_i k+\beta A}{q_i}.
\tag{11}
$$
In particular, $q_i\ge1-4\epsilon S/P_i$. The stated parameter bound
implies
$$
p_-\!>\frac{63}{64}a_*,\qquad
(2\beta+4)\epsilon<\frac{3}{16}a_*<p_-/2,
$$
and
$P_i(1-P_i)\ge p_-(1-p_-)\ge p_-/2$.
Consequently
$$
|k_{\rm new}|
\le\frac{P_i+2\beta\epsilon S}{1-4\epsilon S/P_i}<1.
\tag{12}
$$
No derivative bound was assumed along the word; (12) establishes it
inductively from the initial constant graph, for which $k=0$.

On this graph the actual separating function
$$
\Psi(y)=y-\{2P_0(S(y),y)-1\}
$$
has derivative at least $1-4\epsilon S\ge1-4\epsilon>0$, and its signs
at $-1,1$ are opposite. It has exactly one zero. Restricting to the two
sides of that zero is exactly the next-time feasibility condition.
On each restricted graph (7) is increasing onto the ENTIRE $[-1,1]$,
and (12) still applies after this restriction. Starting with the
horizontal fibre proves the interval and graph statements by induction.
Splitting every parent interval proves the prefix-free partition
statement. This proof imposes every intermediate constraint; it does
not test only the terminal state. Endpoints are included at each split.
Smooth dependence on $s_0>0$ follows from the implicit function theorem.
The apex is fixed and belongs to every physical feasible strip. QED.

For a word $w$ of length $\ell$, put
$$
\lambda_w=\prod_{j=1}^{\ell}a_{w_j},\qquad
\mathcal P_w(x)=\prod_{j=1}^{\ell}p_{w_j}(x_{j-1}).
$$
The second product genuinely depends on the initial angle; it is NOT
a common radial trajectory for all states having that word.
Nevertheless exact feasibility, (6), and (8) give uniform comparisons.
Define
$$
B_P=\frac{\epsilon}{p_-(1-r)},\quad C_P=e^{B_P},\quad
d_0=\frac{4\epsilon}{p_-}<1,\quad
B_q=\frac{4\epsilon}{p_-(1-d_0)(1-r)},\quad C=e^{B_P+B_q}.
$$
At step $j$, $s_j\le r^j s_0$, and hence
$$
|\ln(\mathcal P_w(x)/\lambda_w)|\le B_P.
$$
By (11), $|q_i-1|\le4\epsilon s_j/p_-$, so
$\sum|\ln q_i|\le B_q$. Applying the chain rule along the moving
graphs, not at a falsely fixed terminal radius, yields
$$
C^{-1}\lambda_w^{-1}\le
\partial_{y_0}Y_{w,s_0}\le C\lambda_w^{-1},\qquad
C_P^{-\beta}s_0\lambda_w^\beta
\le s_\ell\le C_P^\beta s_0\lambda_w^\beta.
\tag{13}
$$
The full-range assertion of Lemma 22.2 now gives
$$
2C^{-1}\lambda_w\le |I_w(s_0)|\le2C\lambda_w.
\tag{14}
$$
In physical coordinates the complete feasible strip
$A_w=\{(s_0,s_0y):0<s_0\le1,\ y\in I_w(s_0)\}\cup\{0\}$
therefore satisfies
$$
C^{-1}\lambda_w\le \operatorname{area}(A_w)\le C\lambda_w.
\tag{15}
$$
Here the Jacobian is $s_0$ and $\int_0^1s_0\,ds_0=1/2$.
All boundary curves have area zero, by fibrewise singleton sections
and Fubini; the countable union of finite-word boundaries is null.
Formula (14) and the graph induction are the missing geometry that a
comparison of exact products alone would not supply.

## 4. Arbitrary-input first deviation

**Lemma 22.3 (physical first-deviation band).** Let any input $u$ cover
a state $x=(s_0,s_0y_0)$ through time $n$ at tolerance $\delta$. Suppose
its first difference from the natural exact code occurs at time $j$.
The common prefix $a$ has length $j-1$. There is a separating point
$b_a(s_0)\in I_a(s_0)$, independent of $y_0$, such that
$$
|y_0-b_a(s_0)|
\le C_b\frac{\delta\,\lambda_a^{1-\beta}}{s_0},
\qquad
C_b=\frac{2C_P^\beta p_-^{1-\beta}C}{1-4\epsilon}.
\tag{16}
$$
For a fixed $u,j$ the eligible states lie on ONE side of that point.
Their physical area is at most $C_b\delta\lambda_a^{1-\beta}$.

**Proof.** The common prefix is exact, so its entire image fibre is
the graph of Lemma 22.2. Let $Y_*$ be the unique zero of $\Psi$ on it,
and $b_a(s_0)=Y_{a,s_0}^{-1}(Y_*)$. If the wrong branch is $i$, direct
substitution in (7) gives
$$
|Y_j|-1=\frac{|\Psi(Y)|}{p_i},\qquad
|z_j|-s_j=S p_i^{\beta-1}|\Psi(Y)|.
\tag{17}
$$
The shared endpoint has both sides zero, including when the alternate
branch differs from the chosen tie convention.
Membership in $Q^\delta$ necessarily implies $|z_j|-s_j<2\delta$.
Using (13) and $p_i\ge p_-$ in (17) gives
$$
|\Psi(Y)|\le
2C_P^\beta p_-^{1-\beta}\delta/(s_0\lambda_a^\beta).
$$
The derivative of $\Psi(Y_{a,s_0}(y_0))$ is at least
$(1-4\epsilon)C^{-1}\lambda_a^{-1}$. The mean value theorem proves
(16). The wrong-branch side is fixed by $u_j$, so integration of the
one-sided width times the physical Jacobian $s_0$ proves the area
bound, even without a lower bound on $s_0$.
The estimate used only the necessary constraint at the first
difference. Leaving and then reentering $Q$ cannot remove that
constraint. No cone bound on the later approximate trajectory has
been assumed. QED.

## 5. True stopped-catalogue comparison and full tails

For $0<t<1$, let $\mathcal L(n,t)$ consist of words stopping for the
first time that $\lambda_w\le t$, or at depth $n$ if that has not
happened. Let $N(n,t)$ be its cardinality. This is a complete
prefix-free binary tree determined by reference products, not an
assumed optimal catalogue. With $a_*=\min(a_0,a_1)$,
$$
\sum_{w\in\mathcal L(n,t)}\lambda_w=1,\qquad
\lambda_w>a_*t,\qquad N(n,t)\le(a_*t)^{-1}.
\tag{18}
$$
The sum follows by replacing each parent weight by its two children,
whose weights add to it. The strict lower bound also holds for leaves
capped at depth $n$, because their parent has weight greater than $t$.

**Proposition 22.4 (real catalogue loss is linear).** There are fixed
constants $B,C_0,C_U$, depending only on the stipulated system, such
that for every $n\ge1$ and all sufficiently small $\delta>0$,
$$
\frac{N(n,\delta^{1/\beta})}{1+Bn}
\le r_H(n,\delta;Q)
\le N\!\left(n,(\delta/C_0)^{1/\beta}\right)
\le C_U\delta^{-1/\beta}.
\tag{19}
$$
Also $r_H(n,\delta;Q)\le2^n$.

**Proof of the lower bound.** Set $t=\delta^{1/\beta}$. For each leaf
choose the actual witness $(1,y_w)$ where $y_w$ is the midpoint of
$I_w(1)$. By Lemma 22.2 and (14), these points are ordered with
successive angular gaps greater than $2C^{-1}a_*t$.
For an arbitrary covering input $u$, at most one witness can have its
entire natural stopping leaf as a prefix of $u$; this uses prefix
freeness, not an itinerary restriction on $u$.
Every other covered witness has a first difference at some $j\le n$.
Its common prefix is precisely $u|_{j-1}$ and has $\lambda_a>t$.
For this ONE prefix and fixed radius 1, (16) confines all such
witnesses to a one-sided interval of width at most
$$
C_b\delta\lambda_a^{1-\beta}\le C_b\delta t^{1-\beta}=C_b t.
$$
It contains at most
$B=\lceil 1+C C_b/(2a_*)\rceil$ witnesses, by the proved spacing.
Thus an arbitrary input covers at most $1+Bn$ witnesses, proving the
lower bound. Approximate inputs, later reentry, and alternate boundary
choices were included in Lemma 22.3. Midpoints are interior to every
ancestor, so each witness has the claimed natural prefix.

**Proof of the upper bounds.** Use every leaf at threshold
$t=(\delta/C_0)^{1/\beta}$ and append the SAME infinite tail, for
example $000\ldots$. Lemma 22.2 makes these exact feasible prefixes
cover every physical initial fibre; all their intermediate times are
in $Q$. A leaf reaching depth $n$ needs no further constrained time.
For an earlier stopped leaf, (13) gives terminal radius at most
$C_P^\beta t^\beta$. Since that terminal state is in $Q$, its adapted
norm is at most $M C_P^\beta t^\beta$. Choose
$C_0=2\sqrt2 M C_P^\beta$. Formula (6), which holds on the whole
plane, makes its entire tail have Euclidean norm at most $\delta/2$,
hence distance to $Q$ less than $\delta$ at EVERY remaining time.
The apex is fixed. The catalogue has at most $N(n,t)$ entries; (18)
gives $C_U=C_0^{1/\beta}/a_*$. Alternatively all length-$n$ exact
prefixes cover $Q$ and prove the $2^n$ bound. QED.

The new estimate is (19) for the actual angle-dependent radial
system, derived through (10)–(17). The relative-prefix witness
architecture is already present in R06 and R19/R21. The number of
witnesses is not inferred from exact coding or a pressure identity.

## 6. Fixed physical typical sets and the boundary

Choose the natural code with the tie convention in §2, and let
$f_k(x)$ be its proportion of zeros through time $k$. Outside the
null boundary set it lies in the interior of its assigned complete
feasible strip. By (15), the physical area of states assigned a
length-$k$ word $w$ is at most $C\lambda_w$. Consequently for each
$\eta>0$,
$$
\operatorname{area}\{|f_k-a_0|\ge\eta\}
\le C(k+1)e^{-2\eta^2 k}.
\tag{20}
$$
For completeness, a type with $j$ zeros has probability at most
$\exp[-k D(j/k\,\|\,a_0)]$: use
$\binom{k}{j}\le e^{kH(j/k)}$ and multiply by
$a_0^j a_1^{k-j}$. The binary relative entropy has second derivative
$1/[t(1-t)]\ge4$, value and first derivative zero at $a_0$, so
$D(t\,\|\,a_0)\ge2(t-a_0)^2$, including the endpoint values by
continuity. Summing at most $k+1$ types proves (20).
It follows by summability, and then countably many $\eta$, that
$f_k\to a_0$ for physical area-almost every state. Independence of
these actual state itineraries has NOT been assumed.

For any positive-area compact $K$, Egorov's theorem and inner
regularity give a positive-area compact $T\subset K$ on which this
convergence is uniform; null coding boundaries and the apex can be
discarded at this selection step. For every $\eta>0$ there is then
$D_\eta\ge1$ with
$$
D_\eta^{-1}e^{-(h+\eta)k}\le\lambda_{v_k(x)}
\le D_\eta e^{-(h-\eta)k},\quad x\in T,\ k\ge0.
\tag{21}
$$
Here $v_k(x)$ denotes the actual assigned code prefix. The same $T$
works for ALL $\eta$, since the single frequency convergence is
uniform; finitely many early times are absorbed in $D_\eta$.

For any input $u$, horizon $n$, and integer $0\le m\le n$, partition
its covered portion of $T$ by agreement through $m$ or first
difference at $j=1,\ldots,m$. Agreement has area at most
$C D_\eta e^{-(h-\eta)m}$, by (15) and (21), when it is nonempty.
For a nonempty first-difference part, its common word is a prefix
of the code of some point of $T$, so (21) bounds that word from
below. Lemma 22.3 gives area at most
$$
C_b\delta D_\eta^{\beta-1}
       e^{(\beta-1)(h+\eta)(j-1)}.
$$
Summing the geometric series proves, for $0<\eta<h$,
$$
\operatorname{area}(T\cap V(n,\delta,u))
\le A_\eta\{e^{-(h-\eta)m}
                  +\delta e^{(\beta-1)(h+\eta)m}\}.
\tag{22}
$$
This controls all arbitrary inputs, not just the natural language.
Take
$m=\min\{n,\lfloor(-\ln\delta)/[\beta(h+\eta)]\rfloor\}$ when
$\delta<1$. The second summand in (22) is at most
$e^{-(h+\eta)m}$. Covering the positive area of $T$ therefore gives
$$
r_H(n,\delta;K)\ge
\frac{\operatorname{area}(T)}{2A_\eta}e^{(h-\eta)m}.
\tag{23}
$$
For a precision sequence of finite exponent $\gamma>0$, (23),
followed by $\eta\downarrow0$, proves the lower bound in (2).
The upper bound is (19) and $2^n$, applied also to $K\subset Q$.
For $\gamma=0$ the lower bound is simply $r\ge1$, and (19) gives
the matching zero upper rate. This proves the low side including
the critical exponent and sequences with arbitrary subexponential
factors; no monotonicity of $\delta_n$ is needed.

To prove (3), apply Egorov and inner regularity ONCE to the
full-area typical set to obtain compact $T_\zeta$ of area
greater than $1-\zeta$, with uniform frequency convergence.
Set $K_\zeta=T_\zeta\cup\{0\}$. This fixed compact set has the
required area. For any $\eta>0$, every sufficiently long natural
prefix on $T_\zeta$ has zero frequency within $\eta$ of $a_0$.
The number of such length-$n$ words is at most
$$
(n+1)\exp\{n\max_{t\in[0,1],\ |t-a_0|\le\eta}H(t)\},
$$
where $H(t)=-t\ln t-(1-t)\ln(1-t)$.
Their exact feasible prefixes and arbitrary appended tails form a
catalogue through time $n$ at EVERY tolerance. One input covers the
added apex. Thus the upper rate on $K_\zeta$ is $h$, independently
of the precision sequence. For $\gamma>\beta h$, (2) gives the
matching lower rate $h$.

It remains to prove STRICTLY larger lower rate on $Q$, rather than
merely the non-strict bound in (2). Put
$$
\chi(t)=-t\ln a_0-(1-t)\ln a_1,\quad
\Delta=\chi(1/2)-h>0.
$$
For a given finite $\gamma>\beta h$ choose
$$
\alpha_\gamma=\min\{1/2,\ (\gamma/\beta-h)/(2\Delta)\},\quad
t_\gamma=(1-\alpha_\gamma)a_0+\alpha_\gamma/2.
$$
Then $\chi(t_\gamma)<\gamma/\beta$ and $H(t_\gamma)>h$.
All length-$n$ words with zero count $j_n$, $j_n/n\to t_\gamma$,
have product $e^{-n\chi(j_n/n)}>\delta_n^{1/\beta}$ eventually.
Every proper prefix has even larger product. These words are
therefore capped leaves of $\mathcal L(n,\delta_n^{1/\beta})$.
For their type,
$$
\binom{n}{j_n}\ge\frac{e^{nH(j_n/n)}}{n+1}.
$$
For example this follows by using a binomial law with parameter
$j_n/n$: that type is a mode and has probability at least
$1/(n+1)$. The lower comparison (19) now proves
$$
\liminf_n\frac{\ln r_H(n,\delta_n;Q)}n
\ge H(t_\gamma)>h.
\tag{24}
$$
Only this lower bound depends on $\gamma$; $K_\zeta$ was selected
before it. This completes Theorem 22.1 with all its simultaneous
quantifiers. No uniform positive gap as $\gamma\downarrow\beta h$
is claimed.

## 7. Coordinate reduction: an actual exclusion and its scope

It is not legitimate to infer nonconjugacy just because (1) depends
on $z$. We give a topological obstruction on the nonempty parameter
subrange
$$
0<|a_0-a_1|<\epsilon/4.
\tag{25}
$$
The boundary theorem itself holds on the ENTIRE original range;
(25) restricts only this exclusion of a coordinate explanation.

Put $D_i=Q\cap H_i^{-1}Q$, $J_i=H_i(D_i)$, and $\xi=a_0-a_1$.
For every old radius-autonomous matched or mismatched system in
R17/R19/R21, the radial function $g_i(s)$ is increasing and
independent of $y$, and the feasible angular map is onto $[-1,1]$.
Thus its corresponding feasible image is
$\{0\le s\le g_i(1),\ |z|\le s\}$. The two such images are always
nested, regardless of the order of the radial endpoints.

For (1), let $\theta_1=\theta(1)$. By (9),
$|\theta_1|\le|\xi|/(1-\epsilon)$. The maximum radial coordinates
on the two boundary rays in its feasible images are

| Image | Lower output ray $z=-s$ | Upper output ray $z=s$ |
|---|---|---|
| $J_0$ | $(a_0-\epsilon/3)^\beta$ | $((1+\theta_1)/2)^\beta$ |
| $J_1$ | $((1-\theta_1)/2)^\beta$ | $(a_1-\epsilon/3)^\beta$ |

Here is a check that these are the maxima, not just four sample
points. Formula (7) shows that preimages of the lower/upper output
ray are, respectively, the outer source ray or the dividing curve
$y=\theta(s)$, as appropriate to the branch. On each outer ray
$s\mapsto sP_i(s,\pm1)^\beta$ has positive derivative, because
$(P_i)_s$ has absolute value at most $\epsilon$ and
$p_--\beta\epsilon>0$. On the dividing curve,
$|\theta'|\le2\epsilon/(1-2\epsilon)$, and
$$
\left|\frac{d}{ds}P_i(s,\theta(s))\right|
\le\frac{\epsilon}{1-2\epsilon},\qquad
p_--\frac{\beta\epsilon}{1-2\epsilon}>0.
$$
So both dividing-curve radial images also increase up to $s=1$.
At the divider $P_0=(1+\theta)/2$, $P_1=(1-\theta)/2$.
On the outer rays at $s=1$, the feedback term is $\pm\epsilon/3$.
These facts prove the table, with entire ray segments included.

Let $d=(\xi+\theta_1)/2$. Under (25),
$$
|d|\le|\xi|/(1-\epsilon)<\epsilon/3,
$$
since the stipulated bound has $\epsilon<1/64$. The difference of
the two lower-ray bases is $d-\epsilon/3<0$, and the difference
of the upper-ray bases is $d+\epsilon/3>0$. Hence $J_1$ extends
further on the lower ray while $J_0$ extends further on the upper:
neither $J_0$ nor $J_1$ contains the other.

A simultaneous homeomorphism of a neighbourhood of $Q$ onto the
old model, mapping $Q$ to itself and conjugating both controls
(even after permuting their labels), maps $D_i$ to the respective
old feasible domain and $J_i$ to the respective old feasible image.
Here the conjugacy identities are required on all of $Q$, and its
domain contains $Q\cup H_0(Q)\cup H_1(Q)$, as needed to change
coordinates in the actual constrained system.
Inclusion is preserved by a bijection. Nonnested images cannot
become nested images. Thus on (25) there is no such
$Q$-preserving homeomorphism, in particular no fixed $C^1$ or
bi-Lipschitz simultaneous coordinate change to those old models.
The subrange is nonempty: choose any allowed sufficiently small
$\epsilon$ with $a_0,a_1$ sufficiently close to $1/2$ and unequal.
The two strict bounds persist on an open set.

Outside (25), the above image argument does NOT decide reduction
to an old radius-autonomous model. No general nonconjugacy claim
is made there. No exclusion is claimed for changes that do not
preserve $Q$, the control labels up to permutation, and the actual
state covering problem.

## 8. Mathematical status and attribution

The unique transfer target is proved. There is no missing R22
catalogue lemma: (10)–(17) establish complete feasible intervals,
angle-dependent radial comparability, physical first-deviation
bands, and (19) for arbitrary approximate controls; §6 finishes
the stated boundary. Reentry and the complete tail are handled
by different, explicitly proved bounds.

Graph transforms, cone invariance, summable distortion, prefix
stopping, type counts, Borel–Cantelli, Egorov, and pressure roots
are existing tools. See SOURCES.md for actual versions and reading
scope, including the graph-transform volume proof of Kawan–Da
Silva (2018). Here the additional application requires (11),
the complete feasible-graph split, the physical band (16), and
the actual stopped-catalogue comparison; it is not obtained by
declaring a fixed symbolic language optimal.

Relative to R19/R21, the restriction that a word on a fixed
initial-radius fibre has one shared radial trajectory has been
removed. Genuine instances cannot be coordinate corollaries of
those models by §7. Nevertheless both branches retain the SAME
matching power $\beta$, full nonoverlapping angular feasibility,
and feedback whose cumulative effect is summable under uniform
origin contraction. No theorem is proved for arbitrary smooth
perturbations, persistent nonsummable feedback, or overlapping
feasible branches. No full-field priority, general necessary and
sufficient classification, or journal quartile is certified.
