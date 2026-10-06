# R27: a local geometric criterion for actual approximate coverage

2026-10-05 UTC. Repository baseline:
`69f5ff3fd81f26d6677bf7804c972120e6249b29`.
The actual R26 parent is
`2edacc4769d2dc4ad418fd7f3d1f1179dd47f138`;
the extra `d` in the supplied recovery identifier was a transcription error.

This is a self-contained proof, not an appeal to the historical verdicts.
The unique paper is still the R25 paper and is not modified here.

## 1. Object, two candidates, and the selected statement

Write
\[
 Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad |Q|=1.
\]
For an infinite binary input \(u=(u_1,u_2,\ldots)\), set
\(F_u^k=F_{u_k}\circ\cdots\circ F_{u_1}\), with \(F_u^0\) the identity.
The object throughout is
\[
 A_u(n,\delta;K)=\{x\in K:
   \operatorname{dist}(F_u^kx,Q)<\delta\quad(0\le k\le n)\}.       \tag{1}
\]
Distance is Euclidean. Let \(r_F(n,\delta;K)\) be the least number of
infinite inputs whose sets (1) cover every point of \(K\).
An input may leave and reenter \(Q\). No strategy, symbolic subset, or
attractor replaces the actual initial set.

Fix \(a_0,a_1\in(0,1)\), \(a_0+a_1=1\), \(a_0\ne a_1\), and \(\beta>1\).
Put \(r_i=a_i^\beta\), \(t_i=a_i^{\beta-1}\), and
\[
 A_0=\begin{pmatrix}r_0&0\\t_0a_1&t_0\end{pmatrix},\qquad
 A_1=\begin{pmatrix}r_1&0\\-t_1a_0&t_1\end{pmatrix},\qquad
 h=-a_0\log a_0-a_1\log a_1.                                  \tag{2}
\]

Two precise candidates were considered.

**Candidate B (finite transient only).** Suppose two global \(C^2\)
diffeomorphisms fix zero, satisfy controlled invariance of \(Q\) and the
pointwise contraction (3) below, and agree *in a neighbourhood of zero*
with an already verified R26 system. Then the R26 cost boundary transfers
to \(Q\) and to every positive-area compact initial set. This needs a
finite-prefix inverse-Jacobian estimate and a boundary tube estimate;
it is mainly a finite-transient consequence of the old local result.
It does not handle a different local geometry. It is not selected as
the principal result.

**Selected candidate A (local jets, with truncated feasible images).**
The maps need not agree with any old formula, preserve either boundary
ray, or make every word feasible at each fixed initial radius. Assume only:

1. \(F_0,F_1:\mathbb R^2\to\mathbb R^2\) are \(C^2\) diffeomorphisms,
   \(F_i(0)=0\), and \(DF_i(0)=A_i\).
2. \(Q\subset F_0^{-1}Q\cup F_1^{-1}Q\).
   This is one-step controlled invariance, checked on the actual maps.
3. There exist \(\Lambda\ge1\) and \(0<\theta<1\) such that, for
   \(V(s,z)=\max\{\Lambda|s|,|z|\}\),
   \[
                 V(F_i(x))\le\theta V(x)
                 \quad(x\in\mathbb R^2, i=0,1).              \tag{3}
   \]

Condition (3) is a pointwise Lyapunov inequality, not a statement that
the distance between two trajectories contracts. These hypotheses are
about maps, their first derivatives, feasibility, and a common norm.
They assume no word-area estimate, bounded accumulated distortion,
catalogue loss, or cost formula. Global invertibility supplies
noncollapse during the finite transient. All inputs converge uniformly
to the common origin on each bounded initial set, directly by (3).

### Theorem 27.1 (actual-area comparison and cost boundary)

Under 1–3, choose a fixed positive-area compact \(K\subset Q\).
There exist an integer \(J\ge1\), a compact
\(T\subset K\setminus\{0\}\) of positive area, and \(C_J<\infty\)
such that the following holds. For every \(e\in(0,h)\) there is
\(C_e<\infty\) with
\[
 |T\cap A_u(n,\delta;K)|
 \le C_J\delta+C_e\left[e^{-(h-e)m}
             +\delta e^{(\beta-1)(h+e)m}\right]               \tag{4}
\]
for every input \(u\), every \(n\ge J\), every integer
\(0\le m\le n-J\), and \(0<\delta\le1\).
The integer and the set are chosen before \(e,n,\delta,u\).
For \(K=Q\), \(T\) can instead be chosen with \(|T|>1-\zeta\)
for any prescribed \(\zeta\in(0,1)\).

Consequently, for every \(\delta_n\to0\) with
\(-\log\delta_n/n\to\gamma\in[0,\infty)\),
\[
 \min\{h,\gamma/\beta\}
 \le\liminf_n\frac{\log r_F(n,\delta_n;K)}n
 \le\limsup_n\frac{\log r_F(n,\delta_n;K)}n
 \le\min\{\log2,\gamma/\beta\}.                              \tag{5}
\]
In particular every fixed positive-area compact \(K\) has rate
\(\gamma/\beta\) when \(0\le\gamma\le\beta h\).

For each \(\zeta\in(0,1)\) there is one fixed compact
\(K_\zeta\subset Q\), \(|K_\zeta|>1-\zeta\), such that for **every**
finite \(\gamma>\beta h\) and **every** corresponding precision sequence,
\[
 \lim_n\frac{\log r_F(n,\delta_n;K_\zeta)}n=h
       <\liminf_n\frac{\log r_F(n,\delta_n;Q)}n.               \tag{6}
\]
The same set works for all these exponents, sequences, and horizons.
No exact high-precision spectrum or high-side limit for \(Q\) is claimed.

The independent geometric content is (4), valid for actual arbitrary
approximate inputs even when a fixed-radius complete feasible word interval is empty
or its terminal angular image is only a subinterval. Sections 2–6
prove it; Section 7 supplies physical difficult-state witnesses, without
assuming all words are feasible. Section 9 gives an explicit application
outside the boundary-ray geometry used in R26.

## 2. Estimates obtained from the first jets

Use \((s,y)\) with \(z=sy\), only for \(s>0\). Define
\[
 R_i(s,y)=F_i^s(s,sy)/s,\quad
 N_i(s,y)=F_i^z(s,sy)/s,\quad T_i=N_i/R_i.
\]
The integral formula
\(F_i(s,sy)/s=\int_0^1DF_i(ts,tsy)(1,y)\,dt\)
extends \(R_i,N_i\) as \(C^1\) functions to \(s=0\).
At zero
\[
 R_i(0,y)=r_i,\quad
 L_0(y):=T_0(0,y)=(y+a_1)/a_0,\quad
 L_1(y):=T_1(0,y)=(y-a_0)/a_1.                                \tag{7}
\]

Here is a way to choose all local constants from the maps. Let
\(L\) bound the Euclidean bilinear operator norm of both second
derivatives on \(\overline B(0,2)\), and let
\(r_*=\min r_i\), \(r^*=\max r_i\), \(a^*=\max a_i\),
\(a_*=\min a_i\). Take
\(B=10^4(1+L)/r_*^3\), and shrink \(\rho>0\) so that
\[
 \rho\le\min\left\{\tfrac14,\frac{r_*}{8(1+L)},
  \frac{1-r^*}{8B},\frac{1/a^*-1}{16B},
  \frac1{16B},\frac{a_*}{16B}\right\}.                        \tag{8}
\]
Taylor's integral formula gives \(|R_i-r_i|\le2Ls\),
\(|\partial_sR_i|,|\partial_sN_i|\le2L\), and
\(|\partial_yR_i|\le2Ls\),
\(|\partial_yN_i-t_i|\le2Ls\).
The same bounds apply with the appropriate constant linear term in
\(N_i\). In particular \(R_i\ge r_*/2\).
Dividing these formulas by \(R_i\), and differentiating the quotient,
gives, with the generous common constant \(B\),
\[
\begin{split}
 &|R_i-r_i|\le Bs,\qquad |\log(R_i/r_i)|\le Bs,\\
 &|\partial_s\log R_i|\le B,
          \quad |\partial_y\log R_i|\le Bs,\\
 &|T_i-L_i|\le Bs,\qquad |\partial_sT_i|\le B,
          \quad |\partial_yT_i-1/a_i|\le Bs .                 \tag{9}
\end{split}
\]
For example \(|N_i|\le3\) on this rectangle; quotient derivatives
use \(R_i^{-2}\le 4/r_*^2\).
Thus the displayed choice of \(B\) dominates all the constants in (9).
These are derived local inequalities, not extra hypotheses.

Set \(\bar r=r^*+B\rho<1\) and
\(\widehat r=r^*+2B\rho<1\). On an exactly feasible local orbit,
\(s_k\le\bar r^ks_0\). The bounds in (8) also give
\(T_1(s,-1)<-1\) and \(T_0(s,1)>1\). Controlled invariance therefore
forces
\[
                   T_0(s,-1)\ge-1,\qquad T_1(s,1)\le1.       \tag{10}
\]
In contrast to the old formula, equality is not required in (10).
The increasing functions \(T_i(s,\cdot)\) have unique cut points
\(\vartheta_0(s)\) with \(T_0=1\) and \(\vartheta_1(s)\) with
\(T_1=-1\). They equal \(a_0-a_1+O(s)\).
Their feasible intervals are respectively
\([-1,\vartheta_0(s)]\) and \([\vartheta_1(s),1]\).
Controlled invariance gives \(\vartheta_1\le\vartheta_0\).
Thus any local overlap has angular width \(O(s)\) and physical
width \(O(s^2)\). Positivity of the overlap is not assumed.

## 3. Truncated feasible intervals and derived distortion

Consider a radial graph \(s=S(y)\), on any closed subinterval of
\([-1,1]\), with \(|S'/S|\le1\). Put \(k=S'/S\).
For either input its terminal angular derivative along the graph is
\[
 J_i=\partial_yT_i+\partial_sT_i S'
           =1/a_i+O(BS)>0.
\]
The new radial graph has logarithmic slope
\[
 k_{\rm new}
 =\frac{k+(\partial_s\log R_i)S'+\partial_y\log R_i}{J_i}.
                                                                  \tag{11}
\]
Its numerator is at most \(1+2B\rho\) in absolute value and its
denominator at least \(1/a^*-2B\rho\). By (8), \(|k_{\rm new}|\le1\).
Piecewise \(C^1\) graphs obey the same assertion almost everywhere.

For a fixed initial radius \(0<s_0\le\rho\), start with the horizontal
graph \(S\equiv s_0\). Let \(I_w(s_0)\) be the set of initial angles
whose trajectory under a finite word \(w\) stays in \(Q\) at every
intermediate time. It is a closed interval, possibly empty or a point.
Here is the induction that checks all constraints. The current angular
image is an interval, with a graph obeying (11). Extend that graph
constantly to the two sides of its domain. The extension is positive,
bounded by \(\rho\), and obeys the logarithmic-slope bound almost
everywhere. Both \(T_i(S(y),y)\) are increasing. By (10), control 0
cannot violate the lower angular boundary, and control 1 cannot
violate the upper one. The other boundary imposes one cut. Pulling
that cut back through the increasing preceding angular map leaves
an interval. No terminal map is asserted to be onto \([-1,1]\).
The two allowed children cover the parent, by controlled invariance,
but either child can be empty.

Write \(\lambda_w=\prod_{j=1}^{|w|}a_{w_j}\).
Along any such feasible graph, (9) and the geometric decay of \(s_j\)
give constants independent of \(w,s_0\) and its initial angle:
\[
 C_R^{-1}s_0\lambda_w^\beta\le s_{|w|}
                  \le C_Rs_0\lambda_w^\beta,\qquad
 C_A^{-1}\lambda_w^{-1}\le \frac{dY_w}{dy_0}
                  \le C_A\lambda_w^{-1}.                    \tag{12}
\]
For instance one may take
\(C_R=\exp(B\rho/(1-\bar r))\),
\(C_A=\exp(4B\rho/(1-\bar r))\):
\(|a_iJ_i-1|\le2Bs_j\le1/8\), so its logarithm has modulus at
most \(4Bs_j\). Integration over the *actual* angular image implies
\[
 |I_w(s_0)|\le2C_A\lambda_w,
 \quad |\mathcal I_w|\le C_A\rho^2\lambda_w,
 \quad \mathcal I_w=\{(s,sy):0<s\le\rho,\ y\in I_w(s)\}.      \tag{13}
\]
The Jacobian of \((s,y)\mapsto(s,sy)\) is \(s\).
There is no positive lower bound on \(|I_w|\); some fixed-radius
slices in Section 9 are empty. This does not mean the same finite word
has an empty physical feasible region throughout \(Q\).

## 4. First true infeasibility, for arbitrary inputs

Suppose the prefix \(w\) of length \(j-1\) is exactly feasible and
the next prescribed input \(i\) is the first one to leave \(Q\).
On the current graph the map \(T_i\) is increasing with derivative
at least \(1/(2a_i)\). The radial output is at least
\(c s_0\lambda_w^\beta\), by (9),(12), with \(c>0\) fixed.
If this wrong step nonetheless has distance less than \(\delta\)
from \(Q\), then
\[
                  (|z_j|-s_j)_+<2\delta.                    \tag{14}
\]
This follows from the Euclidean Lipschitz linear functionals
\(z-s\) and \(-z-s\). The output radius is positive and at most
\(\rho\), so the violated constraint is angular, not the upper radius.
Consequently the wrong part of the terminal angular interval has
diameter at most \(C\delta/(s_0\lambda_w^\beta)\).
By (12), its initial-angle preimage has length at most
\[
                         C\delta\lambda_w^{1-\beta}/s_0.
\]
After integration against \(s_0\,ds_0\), its physical area is at most
\[
                            C\delta\lambda_w^{1-\beta}.     \tag{15}
\]
This argument also covers a point interval or a terminal interval
lying wholly beyond the cut: monotonicity bounds the diameter of
the part satisfying (14), without requiring a cut point inside the
actual image. It does not require the wrong trajectory to remain
outside afterwards. Any later reentry cannot erase constraint (14)
at its first exit. A different exact feasible coding is not counted
as an exit and has no role in (15).

## 5. One physical typical set for all feasible prefixes

For any \(d>0\), the total weight \(\sum\lambda_w\) of length-\(m\)
words with \(|\#0/m-a_0|>d\) is at most \(2e^{-2d^2m}\).
To see this without importing a new result, regard the weights as
Bernoulli probabilities. For a Bernoulli variable \(X\),
\(\log\mathbb E e^{t(X-a_0)}\le t^2/8\), since the second
derivative of this logarithm is a tilted Bernoulli variance, at most
\(1/4\); apply the exponential Markov inequality with \(t=4d\)
and with \(-4d\). By (13), the area of the union of the corresponding
complete feasible regions is summable in \(m\). Overlaps do not
invalidate the union bound. Borel–Cantelli for rational \(d>0\)
shows that for area-almost every \(x\in Q_\rho\), **all** feasible
length-\(m\) prefixes at \(x\) have zero frequency tending to \(a_0\),
uniformly over those prefixes. Here \(Q_\rho=Q\cap\{s\le\rho\}\).
Controlled invariance guarantees at least one such prefix for every
\(m\); the origin can be discarded as an area-zero point.

Choose \(J\ge1\) so large that
\(\theta^J\sup_QV\le\rho\). Every exactly feasible length-\(J\)
prefix then ends in \(Q_\rho\). For each of the finitely many such
words \(\sigma\), let \(D_\sigma\subset Q\) be its complete feasible
initial region. Each \(F_\sigma\) is a diffeomorphism, so the pullback
of the local exceptional null set is null. Hence on almost every
initial state of \(Q\), all exact feasible transient prefixes and all
their feasible length-\(m\) tails have frequencies tending uniformly
to \(a_0\). The maximum over the finitely many transient choices
has this same property. These maxima are measurable: they are
maxima over finitely many closed finite-word feasibility regions.

Egorov followed by compact inner approximation gives a compact
\(T\subset K\setminus\{0\}\) of positive area on which this convergence
is uniform. For \(K=Q\) it gives \(|T|>1-\zeta\). This single set is
chosen using frequency convergence, without choosing a precision
exponent or sequence. For every \(e>0\) there is \(D_e\ge1\) such
that every feasible tail \(w\), after every feasible \(\sigma\) from
every state of \(T\), obeys
\[
 D_e^{-1}e^{-(h+e)|w|}\le\lambda_w
                      \le D_e e^{-(h-e)|w|}.                 \tag{16}
\]
Finitely many short lengths are absorbed in \(D_e\).

The finite transient does not silently assume exact feasibility for
an approximate input. The polygon \(Q\) has
\(|Q_\delta\setminus Q|\le C\delta\) for \(0<\delta\le1\).
For all prefixes of length at most \(J\), the inverse Jacobian
determinants are bounded on the compact \(\overline{Q_1}\).
If an approximately feasible input first exits during these \(J\)
steps, its initial state belongs to a pullback of this boundary tube.
Summing over its at most \(J\) possible first-exit times, with the
maximum over the finite prefix family, gives
\[
 |\{x\in Q:\text{this input first exits by time }J
                 \text{ and satisfies (1)}\}|\le C_J\delta. \tag{17}
\]
No bounded-distortion assumption is hidden here: the determinant
bound exists because these are finitely many actual diffeomorphisms.
It is uniform in the continuation, horizon, and input.

Fix an arbitrary input and split its covered states into (17) and
the states exact through time \(J\). On the latter, let \(\sigma\)
be its actual length-\(J\) prefix and use \(F_\sigma\) to transport
the states to \(Q_\rho\). Its inverse area distortion is a fixed
constant. Exact feasibility through the next \(m\) steps has area
at most \(C\lambda_{u_{J+1}\cdots u_{J+m}}\), bounded using (16).
For a first true exit at tail time \(j\le m\), its length-\(j-1\)
prefix intersects the transported set, so (16) applies to that
prefix and (15) bounds its area. The geometric sum of these bounds
is at most \(C_e\delta e^{(\beta-1)(h+e)m}\). This proves (4),
including all times, all inputs, and all later reentries.

## 6. Real catalogue lower and upper bounds

If a finite catalogue covers \(K\), it covers \(T\); thus its
cardinality is at least \(|T|/\sup_u|T\cap A_u|\).
Take
\[
 m_n=\min\left\{n-J,
          \left\lfloor\frac{-\log\delta_n}{\beta(h+e)}\right\rfloor
          \right\}.
\]
For large \(n\) this is nonnegative. Since
\(\delta_n\le e^{-\beta(h+e)m_n}\), both the last term in (4)
and \(C_J\delta_n\) are at most a constant times
\(e^{-(h-e)m_n}\). Therefore
\[
 \liminf_n n^{-1}\log r_F(n,\delta_n;K)
      \ge (h-e)\min\{1,\gamma/[\beta(h+e)]\}.
\]
Let \(e\downarrow0\). For \(\gamma=0\), the elementary bound
\(r_F\ge1\) supplies the zero lower rate.

For the upper bound, keep all exactly feasible transient words;
there are at most \(2^J\). Use the reference weight \(\lambda_w\)
only to build an *upper* catalogue. Stop at the first \(\lambda_w\le t\),
or at tail horizon \(n-J\), whichever is earlier, with
\[
                    t=\min\left\{1,\left[\frac{\delta}
                         {4\sqrt2\Lambda C_R\rho}\right]^{1/\beta}\right\}.
\]
When a state has an exact feasible infinite continuation (provided
by controlled invariance), its chosen prefix follows a leaf of this
finite tree. Empty feasible leaves can be discarded. If a leaf stops
early, (12) puts its actual terminal norm below \(\delta/(4\sqrt2)\).
Append the same infinite zero tail; (3) keeps every later Euclidean
distance below \(\delta/4\). Before stopping all states assigned to
this word are exactly feasible. An unfinished leaf simply specifies
the complete horizon; its later continuation is irrelevant.

Each tree leaf has weight at least \(a_*t\), and the weights sum to
one, by the elementary two-child identity \(a_0+a_1=1\).
This identity is about an auxiliary reference tree, not a partition
of the actual plane. Thus
\[
 r_F(n,\delta;Q)\le C\delta^{-1/\beta},\qquad
 r_F(n,\delta;Q)\le2^n.                                     \tag{18}
\]
For \(n<J\) the second bound suffices; enlarge \(C\) if needed.
All these catalogues specify actual controls and satisfy the complete
time constraint. Equations (4),(18) prove (5).

For the near-full set, choose \(T\) as in Section 5 and put
\(K_\zeta=T\cup\{0\}\). All exact feasible length-\(n\) words that
meet \(T\) have tail frequency uniformly close to \(a_0\).
The number of binary words of frequency \(p\) is at most
\(e^{mH_b(p)}\), where \(H_b(p)=-p\log p-(1-p)\log(1-p)\).
Summing over at most \(m+1\) types, and over the \(2^J\) transient
choices, shows their number is at most \(e^{(h+o(1))n}\).
They cover \(T\) exactly through time \(n\); one additional input
covers the origin. Hence the upper rate for \(K_\zeta\) is at most
\(h\), for every precision sequence. The lower bound in (5) gives
the matching rate whenever \(\gamma>\beta h\).
It remains to prove the strict full-\(Q\) lower bound without the
old assumption that every word has a nonempty feasible region.

## 7. Bounded-run physical shadowing, rather than full cylinders

### Lemma 27.2

For each integer \(L\ge2\), there is a positive radius \(s_L\)
and \(d_L'>0\) such that every infinite binary sequence whose
successive runs have length at most \(L\) is realised by an actual
exactly feasible orbit starting at \((s_L,s_Ly_0)\).
At every step of that orbit the alternative control is genuinely
infeasible, with an angular excess at least \(d_L'\).
The radius and margin are uniform over the sequences. No such
assertion is made for unbounded runs or all constant words.

**Proof.** The inverse reference maps are
\(f_0(y)=a_0y-a_1\), \(f_1(y)=a_1y+a_0\).
For any fixed infinite input \(v\), successive inverse compositions
give a unique reference bounded orbit \(y_k^0\in[-1,1]\).
If runs have length at most \(L\), the next opposite digit is seen
within \(L+1\) digits. Since
\(f_0(y)+1=a_0(y+1)\), \(1-f_1(y)=a_1(1-y)\), and each opposite
digit inserts an endpoint distance at least \(2a_*\),
\[
                    |y_k^0|\le1-d_L,
              \qquad d_L=2a_*^{L+1}>0.                     \tag{19}
\]

Let \(b=d_L/4\) and consider the complete closed ball of sequences
\(\|y-y^0\|_\infty\le b\) in \(\ell^\infty\).
For each such sequence and a positive fixed initial radius \(s_*\),
recursively define \(s_{k+1}=s_kR_{v_{k+1}}(s_k,y_k)\).
These radii stay below \(\bar r^ks_*\), independently of whether
the angular recursion has yet been imposed.
The scalar map \(s\mapsto sR_i(s,y)\) has derivative bounded in
absolute value by \(\widehat r<1\), and its \(y\) derivative is
bounded by \(B s^2\), since \(R_i\le\bar r<1\) and (9) bounds
its logarithmic angular derivative. Thus two candidate sequences give
\[
 \sup_k|s_k(y)-s_k(\widetilde y)|
       \le C_s s_*^2\|y-\widetilde y\|_\infty,
       \qquad C_s=B/(1-\widehat r).                         \tag{20}
\]
Write \(e_i(s,y)=T_i(s,y)-L_i(y)\). By (9),
\(|e_i|\le Bs\), \(|\partial_s e_i|\le B\), and
\(|\partial_y e_i|\le Bs\). Define
\[
 (\mathcal By)_k=f_{v_{k+1}}(y_{k+1})
         -a_{v_{k+1}}e_{v_{k+1}}(s_k(y),y_k).               \tag{21}
\]
Choose \(s_*\le\rho\) so small that
\[
 a^*Bs_*\le(1-a^*)b/2,
 \qquad a^*B(s_*+C_s s_*^2)<(1-a^*)/2.                     \tag{22}
\]
Then (21) maps the ball into itself and has Lipschitz constant at
most \(a^*+a^*B(s_*+C_s s_*^2)<1\).
The contraction mapping theorem gives a fixed sequence. Its equation
is exactly \(y_{k+1}=T_{v_{k+1}}(s_k,y_k)\), not a formal symbolic
substitution. It has \(|y_k|\le1-3d_L/4\), so the constructed
physical trajectory is exactly feasible for all times.

To check the alternative control, suppose the chosen digit is zero.
Then \(T_0(s_k,y_k)=y_{k+1}\le1-3d_L/4\), and (9) gives
\[
 y_k\le a_0-a_1-3a_0d_L/4+a_0Bs_k.
\]
Substitution into \(T_1=L_1+e_1\) yields
\[
 T_1(s_k,y_k)\le-1-\frac{3a_0d_L}{4a_1}
                           +B(1+a_0/a_1)s_k.
\]
For chosen digit one, the symmetric computation gives
\[
 T_0(s_k,y_k)\ge1+\frac{3a_1d_L}{4a_0}
                           -B(1+a_1/a_0)s_k.
\]
Shrink \(s_*\) once more, before considering any particular sequence,
so that these last error terms are at most
\(a_*d_L/(4a^*)\). Both wrong angular excesses are then at least
\(d_L'=a_*d_L/(2a^*)\). Set \(s_L=s_*\).
All choices depend only on \(L\) and the fixed system.
This proves the lemma, including the physical realisation and the
genuine-infeasibility assertion. \(\square\)

## 8. Rare physical states force the strict high-side difference

Fix \(\gamma>\beta h\). Choose \(p\) strictly between \(a_0\) and
\(1/2\), sufficiently close to \(a_0\), so that
\[
 H_b(p)>h,
 \qquad \beta\chi(p)<\gamma,
 \qquad \chi(p)=-p\log a_0-(1-p)\log a_1.                   \tag{23}
\]
Choose large \(L\) and an integer \(j\) with \(j/L\) close to \(p\).
Use all length-\(L\) blocks starting with zero, ending with one, and
containing \(j\) zeros. Their number is
\[
 B_L={L-2\choose j-1},\qquad
 \chi_L=-\frac jL\log a_0-\left(1-\frac jL\right)\log a_1.
\]
We can arrange
\(\log B_L/L>h\) and \(\beta\chi_L<\gamma\).
Indeed the usual type bound
\({L\choose j}\ge e^{LH_b(j/L)}/(L+1)\) and the exact identity
\({L-2\choose j-1}=j(L-j){L\choose j}/[L(L-1)]\)
give \(L^{-1}\log B_L\to H_b(p)\).
The type bound follows by evaluating the largest term of the
binomial law with parameter \(j/L\), whose \(L+1\) terms sum to one.

Concatenations of these blocks have runs of length at most \(L\).
For every choice of the first \(\lfloor n/L\rfloor\) blocks,
continue with one fixed allowable block forever and apply Lemma 27.2.
These are actual states of \(Q\), at one fixed positive radius.
For every prefix length \(k\le n\), their reference weights obey
\(\lambda_{v|k}\ge e^{-\chi_L n-C_L}\), since every complete block
has the same logarithmic weight and the unfinished block has bounded
length. By (12), the physical radius before any such step is at least
\(c_L e^{-\beta\chi_L n}\).

If an arbitrary input first differs from a witness input by time
\(n\), its previous states coincide exactly with that witness.
Its wrong radial multiplier is at least \(r_*/2\); Lemma 27.2
therefore gives a physical excess
\[
                   |z_k|-s_k\ge E_L e^{-\beta\chi_L n},
                   \qquad E_L>0.                           \tag{24}
\]
Since \(-\log\delta_n/n\to\gamma>\beta\chi_L\), (14) rules this
out for large \(n\). Later reentry is immaterial. One input in a
real catalogue can therefore cover at most one of the distinct block
prefix witnesses. Distinctness also follows from the wrong-branch
margin: two different witness prefixes cannot describe the same
initial state. Hence
\[
 r_F(n,\delta_n;Q)\ge B_L^{\lfloor n/L\rfloor},\qquad
 \liminf_n n^{-1}\log r_F(n,\delta_n;Q)\ge\log B_L/L>h.       \tag{25}
\]
The auxiliary witness radius may depend on \(\gamma\). The initial
set \(K_\zeta\) from Section 6 does not. Equations (5),(25) complete
Theorem 27.1 for every stated precision sequence. \(\square\)

## 9. An application with missing word slices and inward boundary images

This verifies that the selected criterion handles a local geometry
not covered by merely applying the old full-image argument.
Let \(t=\max a_i^{\beta-1}<1\),
\(\Lambda=1+4t/(1-t)\), \(v=t(1+1/\Lambda)<1\), and fix
\[
       0<c<\min\{1-a^*,\ (1-v)/v,\ 1\},\qquad
       g(s)=1-\frac{cs}{1+s^2}.
\]
Consider the single explicit family
\[
\begin{split}
 F_0(s,z)&=(r_0s,\ g(s)t_0(z+a_1s)),\\
 F_1(s,z)&=(r_1s,\ g(s)t_1(z-a_0s)).                         \tag{26}
\end{split}
\]
Both are global smooth diffeomorphisms: \(g\in[1-c/2,1+c/2]\)
is positive, the first coordinate has the explicit inverse
\(s=s'/r_i\), and the second is an affine invertible function of
\(z\) at that radius. Their first jets are (2).
For the stated \(V\),
\[
 V(F_i x)\le\max\{r^*,(1+c/2)v\}\,V(x),
 \qquad \max\{r^*,(1+c/2)v\}<1.                            \tag{27}
\]
Thus the norm inequality is checked globally, not inferred from
feasible trajectories.

For \(0<s\le1\), \(a^*<g(s)<1\). The complete one-step angular
domains are
\[
 D_0(s)=[-1,a_0/g(s)-a_1],\qquad
 D_1(s)=[a_0-a_1/g(s),1].                                   \tag{28}
\]
Their endpoints lie strictly inside \((-1,1)\), and their overlap
has angular width \(1/g(s)-1>0\), physical width
\(s(1/g(s)-1)=O(cs^2)\) near zero. This proves controlled
invariance and the actual overlap geometry. Theorem 27.1 applies.

Yet for every fixed \(0<s_0\le1\), a sufficiently long all-zero word
is infeasible for every initial angle. To verify this, write
\(s_k=r_0^ks_0\) and \(q_k=y_k+1\). Under zero input,
\[
 q_{k+1}=\frac{g(s_k)}{a_0}q_k+1-g(s_k).                    \tag{29}
\]
The multiplier is uniformly greater than one, since
\(g(s)>a^*\), and \(q_1\ge1-g(s_0)>0\) for \(y_0\ge-1\).
The sequence eventually exceeds two, violating \(y\le1\).
Monotonicity means that this also holds for the smallest initial
angle, hence for all of them. The old nonempty/full-image assertion
is false for this example. This is a counterexample to that proof
property, not to the cost boundary proved above.

This statement concerns \(I_{0^m}(s_0)\) at a fixed radius, not the
whole physical region \(\mathcal I_{0^m}\). Choosing the radius smaller
can make a given finite word feasible. Indeed any finite word admits
a bounded-run infinite extension, and Lemma 27.2 realises that
extension at a sufficiently small positive radius. Missing fixed-radius
slices must not be confused with removing a word everywhere in \(Q\).

There is also a precise obstruction to a fixed coordinate reduction.
For (26), \(F_0\) sends the positive lower edge of \(Q\) strictly
inside \(Q\), and its upper edge outside; \(F_1\) does the symmetric
thing. The image of the top edge has constant radius \(r_i<1\)
and crosses the opposite angular boundary exactly once. Thus
\[
                  F_i(\partial Q)\cap\partial Q
                  \text{ consists of exactly two points}.  \tag{30}
\]
For the old R24/R26 formula classes, control zero preserves the
whole lower edge as a boundary continuum and control one preserves
the whole upper edge. A homeomorphism \(H\) of the plane with
\(H(Q)=Q\), simultaneously conjugating the two labelled controls
(even allowing a label permutation), would map each intersection
in (30) onto the corresponding old intersection. Finite versus
continuum is impossible. Thus this example is not reducible to
those specified classes by a fixed \(Q\)-preserving simultaneous
control homeomorphism, and in particular not by such a \(C^1\)
or bi-Lipschitz map. No assertion about unconstrained coordinate
changes or every member of the new class is made.

## 10. What has and has not advanced

- New: a criterion based on matched first jets, directly checked
  controlled invariance, and a common toward-origin norm inequality;
  the actual-area bound (4) tolerates missing fixed-radius word intervals and truncated
  angular images, with explicit \(O(\delta)\) transient leakage.
- New geometric step relative to the R26 proof: local interval
  comparison without onto images, and the physical shadowing lemma
  with a uniform wrong-control margin. Example (26) needs both.
- Reused methods: graph cones, summable Taylor errors, boundary
  tubes, inverse Jacobians, Borel–Cantelli/Egorov, type counting,
  reference stopping scales, and the contraction mapping theorem.
  The cost deductions from the new actual comparison use the same
  logic as R26; entropy optimisation itself is not new.
- The class retains a common contracting fixed point, matched
  first jets, controlled \(Q\), global invertibility and (3).
  It does not cover fixed positive overlap at the limiting angular
  scale, noninvertible collapse, or arbitrary control systems.
- No unresolved lemma remains for Theorem 27.1. The exact full-\(Q\)
  high-side cost spectrum and its limit remain unproved, and are not
  automatically the next task. R09–R14 remain paused.

The four-journal reading guided the separation between actual mass
and rare all-state witnesses, and the insistence on a geometric
bridge before entropy counting. No convolution identity, inverse
entropy theorem, \(L^q\) theorem, or stationary fractal measure has
been invoked to prove (4) or (25).
