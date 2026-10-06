# R31: first-jet mismatch in general feedback systems

2026-10-06 UTC. Repository baseline:
`134b7f949173a3182795db449ffa0247e1954c89`.
This completes the single low-precision proposition authorized for R31.
The unique manuscript is unchanged. All logarithms are natural.

## 1. Actual object and complete statement

Fix
\[
a_0,a_1\in(0,1),\quad a_0+a_1=1,\quad a_0\ne a_1,
\qquad \beta_0,\beta_1>1,\quad \beta_0\ne\beta_1.
\]
Put \(\rho_i=a_i^{\beta_i}\), \(t_i=\rho_i/a_i<1\), and
\[
 A_0=\begin{pmatrix}\rho_0&0\\t_0a_1&t_0\end{pmatrix},\qquad
 A_1=\begin{pmatrix}\rho_1&0\\-t_1a_0&t_1\end{pmatrix}.
 \tag{31.1}
\]
Assume that \(F_0,F_1:\mathbb R^2\to\mathbb R^2\) are global
\(C^2\) diffeomorphisms, fix the origin, and have derivatives (31.1).
Keep
\[
 Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad |Q|=1.
\]
Assume controlled feasibility
\(Q\subset F_0^{-1}Q\cup F_1^{-1}Q\), and that for some
\(\Lambda\ge1\), \(0<\theta<1\),
\[
 V(s,z)=\max\{\Lambda|s|,|z|\},\qquad
 V(F_i x)\le\theta V(x)\quad(x\in\mathbb R^2, i=0,1).
 \tag{31.2}
\]
This is contraction toward the origin, not contraction of distances
between arbitrary pairs. Every infinite binary input is allowed. Set
\(F_u^0=\mathrm{id}\), \(F_u^k=F_{u_k}\circ\cdots\circ F_{u_1}\), and
\[
 A_u(n,\delta;K)=\{x\in K:
     \operatorname{dist}_2(F_u^kx,Q)<\delta\ (0\le k\le n)\}.
 \tag{31.3}
\]
The number \(r_F(n,\delta;K)\) is the least number of infinite inputs
whose sets (31.3) cover every actual state of \(K\). Inputs may leave
and reenter \(Q\). Only the first \(n\) letters affect this count;
controlled feasibility gives a finite catalogue of at most \(2^n\)
inputs. No selected strategy is presumed optimal.

Define
\[
 \lambda_w=\prod_{j=1}^{|w|}a_{w_j},\qquad
 P_w=\prod_{j=1}^{|w|}\rho_{w_j},
 \tag{31.4}
\]
with empty products one, and
\[
 h=-\sum_i a_i\log a_i,\quad
 \chi=-\sum_i a_i\log\rho_i,\quad
 \gamma_0=-\log\max_i\rho_i>0,
 \qquad \rho_0^D+\rho_1^D=1.
 \tag{31.5}
\]
The root is unique and belongs to \((0,1)\): the left side decreases
continuously from two to zero, and at one it is less than
\(a_0+a_1=1\). Also \(\chi>h>0\) and \(\chi\ge\gamma_0\).

**Theorem 31.1.** For every fixed system above and every
\(\zeta\in(0,1)\), there is one compact \(K_\zeta\subset Q\), of area
greater than \(1-\zeta\), such that for every \(0<\gamma<\gamma_0\)
and every positive sequence \(\delta_n\to0\) with
\(-\log\delta_n/n\to\gamma\),
\[
 \lim_n\frac{\log r_F(n,\delta_n;Q)}n=\gamma D,
 \qquad
 \lim_n\frac{\log r_F(n,\delta_n;K_\zeta)}n
          =\gamma\frac h\chi<\gamma D.
 \tag{31.6}
\]
The same compact set precedes all these exponents, sequences, and
horizons; it may depend on the fixed system and \(\zeta\).
No monotonicity of \(\delta_n\) is required. Every other fixed
positive-area compact \(K\subset Q\) has lower rate at least
\(\gamma h/\chi\) in this range. Its accurate rate is not classified.

The decisive extension is a two-product first-true-exit area estimate,
proved below for arbitrary approximate inputs and angle-dependent
radial trajectories. A tree will be used only for an upper bound;
its necessity or a polynomial comparison with the exact tree is
not asserted.

## 2. Nonempty class, including actual angular feedback

The linear pair \(A_i\) is a member. Its angular maps are
\[
 L_0(y)=(y+a_1)/a_0,\qquad L_1(y)=(y-a_0)/a_1,
 \tag{31.7}
\]
with complete feasible domains \([-1,a_0-a_1]\) and
\([a_0-a_1,1]\). Its radius decreases by \(\rho_i\).
Put \(t^*=\max_i t_i<1\),
\(\Lambda=1+4t^*/(1-t^*)\), and
\(\theta=\max\{\max_i\rho_i,t^*(1+1/\Lambda)\}<1\).
The bound on the second coordinate follows from
\(|z'|\le t^*|z|+t^*|s|\), and proves (31.2) globally.
Invertibility is immediate from \(\det A_i=\rho_i^2/a_i>0\).

For completeness, the class also allows radius to depend on angle
in the original coordinates. This is a check of nonemptiness of that
possibility, not a second research problem or a claim of nonconjugacy.
Use a fixed nonnegative smooth cutoff \(\kappa\), equal to one on
\(\overline B(0,3/2)\) and supported inside \(B(0,7/4)\), as in
paper §7.1. Put \(\phi(s,z)=z^2\kappa(s,z)\),
\(M_\phi=\max\{1,\|x\cdot\nabla\phi\|_\infty\}\), and fix
\(0<c<1/(2M_\phi)\). Define
\[
 H(x)=e^{-c\phi(x)}x,\qquad F_i(x)=A_iH(x).
 \tag{31.8}
\]
On each ray \(x=te\), \(t\ge0\), the output radius
\(t e^{-c\phi(te)}\) has strictly positive derivative
\(e^{-c\phi(te)}[1-c\,te\cdot\nabla\phi(te)]\).
It tends to infinity and preserves the ray. Thus \(H\) is bijective.
Its derivative has determinant
\(e^{-2c\phi(x)}[1-cx\cdot\nabla\phi(x)]>0\), and it is the identity
off a compact set. The inverse function theorem gives a global smooth
inverse, including at zero. Since \(DH(0)=I\), the required jets are
unchanged. The factor is positive and at most one, so the same global
norm bound holds. Angles (31.7) are unchanged and the radius still
decreases; hence controlled feasibility holds with all endpoints.
On \(Q\), \(\kappa=1\), and the first coordinate is
\(\rho_i s e^{-cz^2}\). At fixed positive \(s\) it genuinely depends
on the initial angle. We make no claim that (31.8), or every member,
has been excluded from all simultaneous coordinate reductions.

## 3. Two derived products and complete local feasible intervals

All constants in this section depend on the fixed maps. Write
\(z=sy\), for \(s>0\), and set
\[
 R_i(s,y)=F_i^s(s,sy)/s,\quad N_i(s,y)=F_i^z(s,sy)/s,
 \qquad T_i=N_i/R_i.
\]
Taylor's integral formula extends \(R_i,N_i\) as \(C^1\) functions
to \(s=0\), with \(R_i(0,y)=\rho_i\) and \(T_i(0,y)=L_i(y)\).
Let \(L\) bound the bilinear operator norms of the two second
derivatives on \(\overline B(0,2)\). Put
\(\rho_* =\min_i\rho_i\), \(\rho^*=\max_i\rho_i\),
\(a_* =\min_i a_i\), \(a^*=\max_i a_i\), and
\(B=10^4(1+L)/\rho_*^3\). Choose a local radius \(b>0\) satisfying
\[
 b\le\min\left\{\frac14,\frac{\rho_*}{8(1+L)},
  \frac{1-\rho^*}{8B},\frac{1/a^*-1}{16B},
  \frac1{16B},\frac{a_*}{16B}\right\}.
 \tag{31.9}
\]
On \(0\le s\le b, |y|\le1\), the integral formula gives
\(|R_i-\rho_i|\le2Ls\),
\(|\partial_sR_i|,|\partial_sN_i|\le2L\),
\(|\partial_yR_i|\le2Ls\), and
\(|\partial_yN_i-t_i|\le2Ls\). In particular \(R_i\ge\rho_*/2\).
Dividing by \(R_i\) and differentiating the quotient gives
\[
\begin{split}
 &|R_i-\rho_i|\le Bs,\quad |\log(R_i/\rho_i)|\le Bs,\quad
 |\partial_s\log R_i|\le B,\quad |\partial_y\log R_i|\le Bs,\\
 &|T_i-L_i|\le Bs,\quad |\partial_sT_i|\le B,\quad
 |\partial_yT_i-1/a_i|\le Bs.
\end{split} \tag{31.10}
\]
For these quotient bounds, \(|N_i|\le3\) after (31.9),
\(R_i^{-2}\le4/\rho_*^2\), and \(t_i<1\). Thus the specified generous
\(B\) dominates the needed constants; no distortion is being assumed.
Set \(\bar r=\rho^*+Bb<1\), \(\widehat r=\rho^*+2Bb<1\).
Local feasible radii satisfy \(s_k\le\bar r^k s_0\).

The wrong edge maps obey \(T_1(s,-1)<-1\) and \(T_0(s,1)>1\).
Controlled feasibility, positive radius and radius below one therefore
force \(T_0(s,-1)\ge-1\) and \(T_1(s,1)\le1\).
Both \(T_i\) are increasing. Their complete one-step domains are
\([-1,\vartheta_0(s)]\), \([\vartheta_1(s),1]\), where
\(T_0(s,\vartheta_0)=1\), \(T_1(s,\vartheta_1)=-1\).
The cuts lie at \(a_0-a_1+O(s)\) and satisfy
\(\vartheta_1\le\vartheta_0\). Any overlap is angular \(O(s)\),
not an assumed fixed separation or fixed positive Euclidean margin.

For a radial graph \(s=S(y)\), with \(|S'/S|\le1\), let \(k=S'/S\).
Its next angular derivative and logarithmic radial slope are
\[
 J_i=\partial_yT_i+\partial_sT_i S'=1/a_i+O(BS)>0,
\qquad
 k_{\rm new}=\frac{k+(\partial_s\log R_i)S'
                       +\partial_y\log R_i}{J_i}.
 \tag{31.11}
\]
The numerator has modulus at most \(1+2Bb\) and the denominator
is at least \(1/a^*-2Bb\). Condition (31.9) makes their ratio at
most one. This includes piecewise \(C^1\) graphs almost everywhere.

Starting from the horizontal graph \(S\equiv s_0\), let \(I_w(s_0)\)
be the initial angles feasible at **every** time of \(w\).
Inductively its angular image is an interval on a graph in (31.11).
Extend that graph constantly beyond its domain. The angular maps
remain increasing; control zero cannot violate the lower edge and
control one cannot violate the upper edge. The other constraint gives
one cut. Pulling back leaves a closed interval, which may be empty or
a singleton. The feasible children cover their parent. Their images
need not fill \([-1,1]\).

Summing (31.10) along any complete feasible local prefix gives
\[
 C_R^{-1}s_0P_w\le s_{|w|}\le C_Rs_0P_w,
 \qquad
 C_A^{-1}\lambda_w^{-1}\le \frac{dY_w}{dy_0}
                      \le C_A\lambda_w^{-1},
 \tag{31.12}
\]
where one may use
\(C_R=\exp(Bb/(1-\bar r))\),
\(C_A=\exp(4Bb/(1-\bar r))\).
Indeed \(|\log(R_i/\rho_i)|\le Bs_j\), while
\(|a_iJ_i-1|\le2Bs_j\le1/8\), so
\(|\log(a_iJ_i)|\le4Bs_j\). These sums converge geometrically.
The first product is \(P_w\), not \(\lambda_w^\beta\).
They have no common-power identity in the present class.
Integration over the actual angular image gives
\[
 |I_w(s_0)|\le2C_A\lambda_w,\qquad
 |\mathcal I_w|\le C_Ab^2\lambda_w,
 \quad \mathcal I_w=\{(s,sy):0<s\le b,\ y\in I_w(s)\}.
 \tag{31.13}
\]
The physical Jacobian is \(s\). Empty, singleton, and truncated fibres
are retained where relevant to covering, but give no positive-area
lower estimate. No full-image or nonempty-word assumption has entered.

## 4. The decisive weighted true-exit estimate

Suppose a local prefix \(w\) is exactly feasible, and the next
prescribed input \(i\) is the first to leave \(Q\). Its output radius
is positive, at most \(b\), and at least \(c s_0P_w\), for fixed
\(c>0\). Thus the violated boundary is angular. At that time,
\[
 \operatorname{dist}_2((s,z),Q)<\delta
       \ \Longrightarrow\ (|z|-s)_+<2\delta,
 \tag{31.14}
\]
because \(z-s\) and \(-z-s\) are \(\sqrt2\)-Lipschitz and
nonpositive on \(Q\). Along the current radial graph, the next
angular derivative is at least \(1/(2a_i)\).
The covered part of the wrong side therefore has diameter at most
\(C\delta/(s_0P_w)\) in the current angle. Pulling back through
(31.12) bounds its initial-angle length by
\(C\delta\lambda_w/(s_0P_w)\). After integrating against
\(s_0\,ds_0\), its actual physical area is at most
\[
                         C\delta\frac{\lambda_w}{P_w}.
 \tag{31.15}
\]
This argument uses diameters and monotonicity, so it still applies
if the crossing cut is outside a truncated actual image or a fibre
is a singleton. A switch to another feasible branch is not called
an exit. Reentry after the first true exit cannot remove (31.14).
Angle-dependent radii do not disappear: their uniform lower bound
in (31.12) is used before taking this band diameter.

Choose a fixed integer \(J\ge1\) with
\(\theta^J\sup_Q V\le b\). All exact feasible \(J\)-prefixes end
in \(Q_b\). If an approximate input first exits during these \(J\)
times, its exit image lies in \(Q_\delta\setminus Q\).
The polygon has tube area \(O(\delta)\), for \(0<\delta\le1\).
The inverse determinants of the finitely many actual prefix maps
are bounded on the compact \(\overline{Q_1}\). Pulling back and
summing over first-exit times gives a uniform bound \(C_J\delta\)
on these initial states. This is a finite-transient consequence of
invertibility, not an assumption of global bounded distortion.

## 5. One typical physical compact set and arbitrary-input area

For a length-\(m\) word with zero frequency outside a distance \(d\)
of \(a_0\), the reference weights have total at most
\(2e^{-2d^2m}\). For a self-contained proof, a Bernoulli variable
of mean \(a_0\) has centered log moment generating function with
second derivative at most \(1/4\); its value and derivative at zero
vanish, so it is at most \(t^2/8\). Exponential Markov at \(t=4d\)
and \(t=-4d\) proves this bound.
By (31.13), the union of the **complete feasible** regions of these
words has summable physical area. Borel–Cantelli for countably many
positive rational \(d\) shows that, outside a null set in \(Q_b\),
all feasible length-\(m\) words at a point have zero frequency tending
uniformly to \(a_0\). This union bound permits overlapping regions.
Controlled feasibility supplies at least one word at each length.
It is not typicality for a single selected code.

Pull this exceptional null set back through all feasible \(J\)-prefixes.
There are finitely many diffeomorphisms, so its pullback is null.
On almost every point of \(Q\), the maximum frequency deviation over
all feasible transient choices and subsequent words tends to zero.
These maxima are measurable, being finite maxima over closed
finite-word feasibility sets. Egorov and compact inner approximation
give one compact \(T\subset Q\setminus\{0\}\), of area greater than
\(1-\zeta\), on which the convergence is uniform.
For any other fixed positive-area compact \(K\), the same procedure
gives a positive-area compact \(T\subset K\setminus\{0\}\).

The set is chosen now, before any precision exponent, sequence,
horizon, or error parameter. Since the two logarithmic costs are
affine functions of word frequency, for each \(0<e<h\) there is
\(D_e\ge1\) such that every local feasible tail \(w\) after every
feasible transient from \(T\) satisfies
\[
\begin{split}
 D_e^{-1}e^{-(h+e)|w|}&\le\lambda_w\le D_ee^{-(h-e)|w|},\\
 D_e^{-1}e^{-(\chi+e)|w|}&\le P_w\le D_ee^{-(\chi-e)|w|}.
\end{split} \tag{31.16}
\]
Finite early lengths are absorbed in \(D_e\); the same \(T\) works
for every \(e\). No independence of actual control digits is assumed.

**Lemma 31.2 (weighted actual-area comparison).** For the fixed
\(J,T\) above and every \(0<e<h\), there is \(C_e<\infty\) such that
\[
 |T\cap A_u(n,\delta;K)|\le C_J\delta+
 C_e\left[e^{-(h-e)m}+\delta e^{(\chi-h+2e)m}\right]
 \tag{31.17}
\]
for every input \(u\), \(n\ge J\), \(0\le m\le n-J\), and
\(0<\delta\le1\).

**Proof.** The first term covers early true exits. On the remaining
states, the prescribed transient \(\sigma=u|_J\) is exactly feasible.
Its inverse area distortion is a fixed constant on the compact
target set. If its next \(m\) inputs are still exactly feasible,
(31.13) bounds the local area by \(C\lambda_{u_{J+1}\cdots u_{J+m}}\).
When this class meets the transported \(T\), (31.16) bounds it by
\(C_e e^{-(h-e)m}\). Otherwise it contributes zero.

At a first local true exit at time \(j\le m\), the prescribed
length-\(j-1\) prefix is feasible for a point of the transported set.
Combining (31.15) with both inequalities in (31.16) bounds the area
of its class by
\(C_e\delta e^{(\chi-h+2e)(j-1)}\). Since \(\chi>h\), this geometric
sum is at most another constant times
\(\delta e^{(\chi-h+2e)m}\). Reentry has not been excluded or used to
enlarge the cover. These classes and exact agreement through \(m\)
exhaust the remaining covered states. This proves (31.17). ∎

Take
\[
 m_n=\min\left\{n-J,
        \left\lfloor\frac{-\log\delta_n}{\chi+e}\right\rfloor\right\}.
 \tag{31.18}
\]
Eventually \(m_n\ge0\) and \(\delta_n\le e^{-(\chi+e)m_n}\).
Every term in (31.17) is then at most a constant times
\(e^{-(h-e)m_n}\). A catalogue covering \(K\) covers \(T\), of
positive actual area, so
\[
 \liminf_n n^{-1}\log r_F(n,\delta_n;K)
        \ge\gamma\frac{h-e}{\chi+e}
 \quad(0<\gamma<\gamma_0\le\chi).
 \tag{31.19}
\]
Let \(e\downarrow0\). This proves the claimed universal positive-area
lower bound, without any assumption about its exact coding catalogue.

## 6. Complete upper catalogues and the same near-full set

Put \(M=\max\{1,4\sqrt2\Lambda C_Rb\}\),
\(c_{\min}=-\log\rho^*=\gamma_0\),
\(c_{\max}=-\log\rho_*\). Use a full reference binary tree, stopped
at the first \(P_w\le\delta/M\), or at depth \(n-J\).
For every actual state choose an exact feasible infinite input.
Its feasible transient and subsequent word reach a reference leaf.
Keep every transient/leaf pair with a nonempty actual initial region;
empty pairs can be discarded, while singleton and boundary states
are not discarded by definition.

Before stopping these assigned states are exactly feasible.
At an early threshold leaf, (31.12) gives
\(s_{|w|}\le C_Rb\delta/M\le\delta/(4\sqrt2\Lambda)\).
Thus \(V\le\delta/(4\sqrt2)\). Appending the same infinite zero
tail, (31.2) and \(\|x\|_2\le\sqrt2 V(x)\) give Euclidean norm at
most \(\delta/4\) at **every** remaining time. Since zero lies in
\(Q\), all constraints are satisfied strictly. A horizon leaf is
already exactly feasible through time \(n\); its later extension
is irrelevant. The origin is covered as well.

For any exponent \(\gamma<\gamma_0\), every branch has crossed
before depth \(n-J\) for all sufficiently large \(n\), because
\[
 P_w\le e^{-\gamma_0(n-J)}<\delta_n/M
       \quad\text{at depth }n-J.
 \tag{31.20}
\]
The strict inequality follows from
\(n^{-1}\log[e^{-\gamma_0(n-J)}M/\delta_n]\to\gamma-\gamma_0<0\).
This explicitly includes all \(o(n)\) precision fluctuations.

Write \(N(t)\) for the uncapped reference stopping count. Replacing
a parent by its children preserves \(\sum P_w^D\), so that sum
is one on its finite leaves. Each leaf has
\(\rho_*t<P_w\le t\). Consequently
\[
 t^{-D}\le N(t)\le(\rho_*t)^{-D},\qquad
 r_F(n,\delta_n;Q)\le2^J N(\delta_n/M).
 \tag{31.21}
\]
The tree identity is classical and concerns reference weights,
not a partition of actual states or a proof of catalogue optimality.
The construction above establishes its validity as an upper bound.
It gives \(\limsup n^{-1}\log r_F(n,\delta_n;Q)\le\gamma D\).

Set \(K_\zeta=T\cup\{0\}\), using the single near-full \(T\) of §5.
Retain only pairs actually realised on \(T\), append the same tails,
and add one input for the origin if necessary. Put
\(q_\delta=-\log(\delta/M)\). A realised stopped tail of length
\(\ell\) satisfies
\[
 q_\delta\le-\log P_w<q_\delta+c_{\max},\qquad
 \ell\le\frac{q_\delta+c_{\max}+\log D_e}{\chi-e}.
 \tag{31.22}
\]
At each length, (31.16) gives
\(\lambda_w\ge D_e^{-1}e^{-(h+e)\ell}\). All reference length-\(\ell\)
weights sum to one, so at most \(D_e e^{(h+e)\ell}\) such distinct
words exist. Multiply by the at most \(2^J\) transients and sum over
the lengths allowed in (31.22). For fixed \(e\), this gives
\[
 \log r_F(n,\delta_n;K_\zeta)
 \le\frac{h+e}{\chi-e}
       [q_{\delta_n}+c_{\max}+\log D_e]
       +O_e(\log(1+q_{\delta_n}))+O_e(1).
 \tag{31.23}
\]
Here \(q_{\delta_n}=\gamma n+o(n)\). Let \(e\downarrow0\) and combine
with (31.19). The second limit in (31.6) follows, on the same set
for every allowed exponent and every sequence. No choice of a
precision-dependent compact set has been made.

## 7. Actual bounded-run witnesses and the full-set lower bound

The bounded-run realisation of R27 can be verified with the separate
radial product. Here are all ingredients needed for that extension.
For fixed \(L\ge2\), the inverse reference maps are
\(f_0(y)=a_0y-a_1\), \(f_1(y)=a_1y+a_0\). Each infinite input \(v\)
has a unique reference bounded orbit \(y_k^0\).
If all runs have length at most \(L\), it satisfies
\[
 |y_k^0|\le1-d_L,\qquad d_L=2a_*^{L+1}>0.
 \tag{31.24}
\]
Indeed \(f_0(y)+1=a_0(y+1)\), \(1-f_1(y)=a_1(1-y)\); seeing the
opposite digit within \(L+1\) symbols inserts endpoint distance at
least \(2a_*\), multiplied by at most \(L\) factors each at least
\(a_*\).

On the closed sequence ball \(\|y-y^0\|_\infty\le d_L/4\), choose
a small fixed initial radius \(s_*\le b\) and recursively set
\(s_{k+1}=s_kR_{v_{k+1}}(s_k,y_k)\).
These radii obey \(s_k\le\bar r^k s_*\) even before angular
consistency is imposed. By (31.10), the derivative in \(s\) of
\(sR_i\) is bounded by \(\widehat r<1\), and its derivative in
\(y\) is bounded by \(Bs^2\). Hence for two candidate sequences,
\[
 \sup_k|s_k(y)-s_k(\widetilde y)|
       \le C_s s_*^2\|y-\widetilde y\|_\infty,
       \qquad C_s=B/(1-\widehat r).
 \tag{31.25}
\]
This estimate explicitly retains the angular dependence of radius.
Write \(e_i=T_i-L_i\). Its modulus, radial derivative and angular
derivative are bounded by \(Bs,B,Bs\), respectively. Define
\[
 (\mathcal B y)_k=f_{v_{k+1}}(y_{k+1})
       -a_{v_{k+1}}e_{v_{k+1}}(s_k(y),y_k).
 \tag{31.26}
\]
Choose \(s_*\) so that
\[
 a^*Bs_*\le(1-a^*)d_L/8,\qquad
 a^*B(s_*+C_s s_*^2)<(1-a^*)/2.
 \tag{31.27}
\]
It maps the ball into itself and contracts with constant at most
\(a^*+a^*B(s_*+C_s s_*^2)<1\). Its fixed sequence satisfies the
**actual** angular recursion, and \(|y_k|\le1-3d_L/4\).
The coupled physical orbit stays in \(Q\) at all times.

If the chosen digit is zero, inserting
\(T_0(s_k,y_k)=y_{k+1}\le1-3d_L/4\) into (31.7),(31.10) gives
\[
 T_1(s_k,y_k)\le-1-3a_0d_L/(4a_1)
                     +B(1+a_0/a_1)s_k.
\]
For chosen digit one the symmetric computation gives
\[
 T_0(s_k,y_k)\ge1+3a_1d_L/(4a_0)
                     -B(1+a_1/a_0)s_k.
\]
Shrink \(s_*\), uniformly over sequences, so each error is at most
\(a_*d_L/(4a^*)\). The wrong angular excess is at least
\(d_L'=a_*d_L/(2a^*)>0\). Put \(s_L=s_*\).
This produces a real positive-radius witness and a genuine wrong-input
margin for every bounded-run sequence. It uses no common exponent.

Only one frequency is needed for the present low-precision lower bound.
Let \(p_* =\rho_0^D\in(0,1)\), so \(1-p_* =\rho_1^D\), and define
\(\chi_R(p)=-p\log\rho_0-(1-p)\log\rho_1\).
Then the classical entropy identity is
\[
 H_b(p_*)=D\chi_R(p_*).
 \tag{31.28}
\]
Choose integers \(j_L\) with \(j_L/L\to p_*\), and use all length-\(L\)
blocks starting in zero, ending in one and containing exactly \(j_L\)
zeros. There are \(M_L=\binom{L-2}{j_L-1}\) such blocks. Put
\(B_L=L^{-1}\log M_L\), \(c_L=\chi_R(j_L/L)\).
The bounds
\[
 \frac{e^{LH_b(j/L)}}{L+1}\le\binom Lj\le e^{LH_b(j/L)},\qquad
 \binom{L-2}{j-1}=\frac{j(L-j)}{L(L-1)}\binom Lj
\]
give \(B_L\to H_b(p_*)\), \(c_L\to\chi_R(p_*)\).
The first two binomial bounds follow by using the corresponding term
of the binomial law of parameter \(j/L\); that term is a largest one,
hence at least \(1/(L+1)\). Endpoint types are not needed because
\(p_*\) is interior.

Fix \(L\) first. Fix \(0<t<\gamma/c_L<1\), let
\(k_n=\lfloor tn/L\rfloor\), \(m_n=Lk_n\), and choose all
\(M_L^{k_n}\) initial block concatenations, followed by one allowable
block forever. Their runs have length at most \(L\). The construction
above realises them at the same radius \(s_L>0\).
Every prefix of length at most \(m_n\) has
\(P_{v|k}\ge P_{v|m_n}=e^{-c_Lm_n}\).
If a catalogue input first differs at \(j\le m_n\), its preceding
states are exactly the witness states. By (31.12) their radius is at
least \(C_R^{-1}s_L e^{-c_Lm_n}\). The wrong radial factor is at
least \(\rho_*/2\), and the wrong angular excess at least \(d_L'\).
Thus at that actual time
\[
 |z_j|-s_j\ge E_L e^{-c_Lm_n},\qquad
 E_L=s_L\rho_*d_L'/(2C_R)>0.
 \tag{31.29}
\]
But
\[
 n^{-1}\log\frac{E_Le^{-c_Lm_n}}{2\delta_n}
               \longrightarrow\gamma-c_Lt>0.
\]
For large \(n\), this violates (31.14), irrespective of later reentry.
Distinct chosen prefixes give distinct actual states: at their first
different digit one control is feasible and the other has this margin.
Any approximate catalogue input can cover at most one such witness.
Therefore
\[
 r_F(n,\delta_n;Q)\ge M_L^{k_n},\qquad
 \liminf_n n^{-1}\log r_F(n,\delta_n;Q)\ge tB_L.
 \tag{31.30}
\]
For fixed \(L\), take the supremum over the strict \(t\), then let
\(L\to\infty\). Equation (31.28) gives the lower bound \(\gamma D\).
The order matters: \(L,s_L,E_L\) are fixed during each horizon limit.
Integer rounding and all precision fluctuations are covered by the
strict inequality \(t<\gamma/c_L\). No uniform positive radius as
\(L\to\infty\) is required. Combining with (31.21) proves the first
limit in (31.6).

## 8. Strict difference and a scoped matching criterion

Put \(b_i=\rho_i^D\), so \(b_0+b_1=1\). Then
\[
 D\chi-h=\sum_i a_i\log(a_i/b_i)\ge0.
 \tag{31.31}
\]
Concavity of logarithm gives
\(\sum_i a_i\log(b_i/a_i)\le\log\sum_i b_i=0\), with equality
only when \(b_i/a_i\) is constant, hence \(b_i=a_i\) for both labels.
Equality would require \(\beta_i D=1\) for both \(i\), contrary to
\(\beta_0\ne\beta_1\). Thus \(D>h/\chi\), finishing Theorem 31.1.
This relative-entropy identity is classical, not a new pressure tool.

**Corollary 31.3 (necessity within the specified first-jet family).**
Allow also \(\beta_0=\beta_1\), retaining the global hypotheses and
the first-jet form (31.1). For every fixed such system, the following
property holds if and only if \(\beta_0=\beta_1\): there exists a
nonempty interval of positive precision exponents adjacent to zero
on which all fixed positive-area compact subsets of \(Q\) have the
same accurate rate, for every sequence of each exponent.

**Proof.** Sections 3–6 also apply when the exponents are equal:
none of their estimates uses their inequality. In this case
\(D=1/\beta\) and \(\chi=\beta h\). The universal positive-area
lower bound (31.19) and the full-set upper bound (31.21) therefore
give the common accurate rate \(\gamma/\beta\) for every such
compact set on \(0<\gamma<\gamma_0\). This already supplies the
required interval, and agrees with the adopted matched theorem in
paper Theorem 2.1, which supplies the larger low-side range.
Under mismatch, Theorem 31.1 separates \(Q\) and one fixed nearly
full-area compact set for every \(0<\gamma<\gamma_0\).
Every interval adjacent to zero contains such an exponent. ∎

This is a criterion in the explicitly stipulated binary first-jet
family with controlled triangle and global contraction/invertibility.
It is not a necessity theorem for arbitrary feedback systems.
No full high-precision mismatch spectrum or arbitrary-compact
classification has been proved or attacked here.

## 9. Attribution and the actual increment

The local estimates, graph cone, truncated intervals, finite transient,
typicality of all feasible prefixes and bounded-run construction are
the mechanisms already proved in R27. Inspection of their derivations
shows that they use the angular jets (31.7), positive contracting
radial constants and summable Taylor errors, not a common \(\beta\).
Sections 3–7 supply the required two-product verification rather than
assuming this transfer. In particular the true-exit factor changes
from \(\lambda_w^{1-\beta}\) to \(\lambda_w/P_w\), and typicality
must control both products. Stopped typical lengths supply the tighter
near-full upper rate; the matched global bound alone would not do so.

R21 already proved the two slopes and relative-prefix packing for its
specified radius-autonomous family. Its fixed-radius common radial
trajectory and exact full-image partition are not used here. With
truncated or empty fibres, the R21 midpoint-tree lower comparison is
not available as written. The full-set lower bound instead uses the
R27 physical bounded-run construction and R29 shorter prefixes. We
do not claim the R21 factor \(1+Bn\) for this whole class.

The new conclusion is the general-feedback low-precision mismatch
theorem and the enlarged **scoped** matching criterion. It is a
checked extension and synthesis of existing project geometry, not a
new independent geometric mechanism. Classical stopping identities,
types, Egorov, graph transforms and relative entropy retain their
standard attribution. The class no longer requires radius autonomy,
but still specifies its two jets and a common contracting origin.
No field-wide priority, quartile or TOP status is certified.

The proof found no concrete error in the adopted matched chain that
requires a manuscript correction. The manuscript and all history are
unchanged. The R09–R14 constant-overlap comparison remains paused.
