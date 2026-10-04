# R08: overlap and an inward margin do not force one precision cost

4 October 2026. Natural logarithms. One structural sufficiency question is answered negatively in the authorized family. The proof is self-contained. It separates actual catalogue exponents despite overlap and a strict inward margin. Existence or an exact formula for the intermediate joint limits is **not** asserted. Classical coding, type counting and stopping methods are tools, not novelty claims.

## 1. System, quantifiers, and one main theorem

For \(1<q<2\), \(0<\rho_0,\rho_1<1/q\), define

$$
F_0(s,z)=(\rho_0s,\rho_0(qz+qs/2)),\qquad
F_1(s,z)=(\rho_1s,\rho_1(qz-qs/2)),\qquad
Q=\{0\le s\le1,\ |z|\le s\}. \tag{1.1}
$$

The ambient space is \(\mathbb R^2\), with Euclidean distance; all binary input sequences are allowed. Let \(Q^\delta=\{x:\operatorname{dist}_2(x,Q)<\delta\}\), and for compact nonempty \(K\subset Q\) put

$$
r(n,\delta;K)=\min\{|C|:C\subset\{0,1\}^{\mathbb N}\text{ finite},\
\forall x\in K\ \exists u\in C\ \forall k=0,\ldots,n:\
\varphi(k,x,u)\in Q^\delta\}. \tag{1.2}
$$

The actual initial state is not approximated. There are \(n\) inputs and \(n+1\) constrained states. Trajectories may leave and reenter \(Q\). Each horizon uses one tolerance. Write \(r_E(n;K)\) for the exact count, and

$$
\underline h_\delta(K)=\liminf_n n^{-1}\ln r(n,\delta_n;K),\quad
\overline h_\delta(K)=\limsup_n n^{-1}\ln r(n,\delta_n;K),\quad
\delta_n\to0,\quad -n^{-1}\ln\delta_n\to\gamma\in[0,\infty]. \tag{1.3}
$$

The tolerances need not be monotone.

**Theorem 8.1 (strict separation with overlap and an inward margin).** Fix any distinct \(0<\rho_0,\rho_1<1/2\). There are \(q_0\in(1,2)\) and constants \(h,c_b,c_->0\), chosen from the contractions and the finite blocks in §6, with

$$
h/c_b>\ln2/c_-,\qquad \gamma_*=\min(c_b,c_-)>0, \tag{1.4}
$$

such that, for every \(q\in(q_0,2)\):

1. The feasible ratio branches overlap on an interval of positive length; every ratio has a control with a strict uniform inward margin. All trajectories from bounded sets converge to the origin uniformly over all inputs.
2. For every positive-area compact \(K\subset Q\), the exact rate is \(\ln q\), and the ordinary outer rate is zero.
3. For every \(\varepsilon\in(0,1)\), there is one compact \(K_\varepsilon\subset Q\), of area \(>1-\varepsilon\) and with empty interior, such that **for every** sequence in (1.3),

$$
\underline h_\delta(Q)\ge h\min(1,\gamma/c_b),\qquad
\overline h_\delta(K_\varepsilon)
\le\min\{\ln q,\ \ln2\min(1,\gamma/c_-)\}. \tag{1.5}
$$

Here \(q_0,h,c_b,c_-\) precede the choices of \(q,\varepsilon,\gamma,\delta_n\). The set can depend on \(q,\rho_0,\rho_1,\varepsilon\), but not on \(\gamma\) or the tolerance sequence. At infinity the minima with \(\gamma/c\) equal one. In particular, for \(0<\gamma\le\gamma_*\),

$$
\underline h_\delta(Q)>\overline h_\delta(K_\varepsilon). \tag{1.6}
$$

This refutes the sufficiency of overlap and margin for a common positive-area precision law. It compares \(Q\), which has interior, with a nearly full-area compact set. It does **not** classify every set with interior or prove either intermediate limit exists.

## 2. Feasibility, contraction and coordinate obstruction

For \(s>0\), use \(y=z/s\) only for calculation. The ratio maps are

$$
T_0(y)=qy+q/2,\qquad T_1(y)=qy-q/2. \tag{2.1}
$$

Their feasible domains in \([-1,1]\) are \([-1,b]\) and \([-b,1]\), with \(b=1/q-1/2>0\). Choosing 0 for \(y\le0\) and 1 for \(y>0\) sends every ratio into \([-q/2,q/2]\). The inward margin is \(1-q/2>0\). Radii decrease and the origin is fixed, proving controlled invariance.

This is a uniform normalized angular margin for \(s>0\), not a uniform positive Euclidean distance from \(\partial Q\). Absolute inward distances tend to zero at the fixed cone vertex.

Choose \(M\ge1\) sufficiently large that

$$
L=\rho_{\max}(q+q/(2M))<1,\qquad
\|(s,z)\|_M=\max(M|s|,|z|). \tag{2.2}
$$

Each map has operator norm at most \(L\); \(\|x\|_2\le\sqrt2\|x\|_M\). This proves uniform convergence for **all** inputs, including off-constraint trajectories. These properties hold throughout the authorized parameter family.

A fixed \(C^1\) state conjugacy taking origin to origin and respecting labels, up to permutation, cannot reduce the unequal-contraction family to R05: its two spectral radii \(q\rho_0,q\rho_1\) differ, whereas R05 has one common spectral radius. Derivatives of corresponding controls must be similar. Nor can \(q<2\) be transformed into the R06 linear family: the ratio of the two positive eigenvalues is \(q\), rather than 2. No claim about singular topological changes, which need not preserve area or exponential precision, is required.

## 3. A forced coding subset inside an overlapping system

Let \(\sigma_0=-1,\sigma_1=1\), and define

$$
Y_q(\omega)=\frac12\sum_{j=0}^{\infty}\sigma_{\omega_{j+1}}q^{-j}.
\qquad
T_{\omega_1}(Y_q(\omega))=Y_q(\operatorname{shift}\omega). \tag{3.1}
$$

The series converges uniformly. General sequences need not give ratios in \(Q\).

**Lemma 8.2.** Suppose all runs of equal symbols in \(\omega\) have length at most \(R\ge1\). Put \(d=2^{-R-1}\). If

$$
E(q):=(2-q)/(2(q-1))<d/4, \tag{3.2}
$$

then every shifted ratio is exactly feasible, has the sign of its first \(\sigma\), and satisfies

$$
3d/4\le|Y_q|\le1-7d/4. \tag{3.3}
$$

The opposite control sends this ratio to absolute value \(>1+\kappa\), where \(\kappa=d/2\).

**Proof.** Both signs occur among the first \(R+1\) symbols. At \(q=2\), comparison with the constant-sign series yields \(|Y_2|\le1-2^{-R}=1-2d\). Apply this bound to the tail in \(Y_2=\sigma_{\omega_1}/2+Y_2(\operatorname{shift}\omega)/2\): its sign is the first \(\sigma\), and its magnitude is at least \(d\). Uniformly,

$$
|Y_q-Y_2|\le\frac12\sum_{j=1}^{\infty}(q^{-j}-2^{-j})=E(q)<d/4.
$$

This proves (3.3) at every shift and hence exact feasibility by (3.1). The wrong control gives absolute next ratio \(q(|Y_q|+1/2)\), whose excess over one is

$$
q|Y_q|-(1-q/2)>3qd/4-d/4>d/2.
$$

Here \(1-q/2<E(q)<d/4\) and \(q>1\). ∎

The coding subset has a unique viable control, although branches overlap elsewhere. Survivor/univoque coding is a classical idea. Its transfer to actual approximate trajectories is the next, separate step.

## 4. The lower bound for arbitrary controls, including reentry

Let \(\mathcal B\) be a finite collection of blocks of common length \(\ell\), common zero and one counts \(a_0,a_1\), and cardinality \(N\ge2\). Suppose every infinite concatenation has runs of length at most \(R\). Put

$$
c_i=-\ln\rho_i,\quad C_b=a_0c_0+a_1c_1,\quad
c_b=C_b/\ell,\quad h=\ln N/\ell. \tag{4.1}
$$

Assume Lemma 8.2. Fix \(s_*=1/2\). For each of the \(N^k\) strings of \(k\) blocks, append a fixed infinite block tail and choose the actual witness

$$
x_w=(s_*,s_*Y_q(\omega_w)).
$$

These lie in the interior of \(Q\). They are distinct: at the first disagreement, their ratios after the common prefix have opposite signs by (3.3). Their intended trajectories are exactly feasible.

A necessary condition for \((s',z')\in Q^\delta\), \(s'\ge0\), is

$$
|z'|-s'<2\delta. \tag{4.2}
$$

Choose a point of \(Q\) within distance \(\delta\) and bound its two coordinate differences to obtain this inequality.

Take any length-\(n\) input \(u\), without coding or exact-feasibility restrictions. If it first disagrees with a witness at \(j\le\ell k\le n\), its actual radius there is

$$
s_*A_{j-1}(\omega_w)\rho_{u_j}
\ge s_*\rho_{\min}e^{-kC_b}.
$$

All factors are less than one and the product after \(k\) full blocks is \(e^{-kC_b}\). Lemma 8.2 therefore gives vertical excess at least

$$
\kappa s_*\rho_{\min}e^{-kC_b}. \tag{4.3}
$$

If \(e^{-kC_b}>C_*\delta\), with \(C_*=2/(\kappa s_*\rho_{\min})\), condition (4.2) fails at this intermediate time. Later reentry cannot repair a past violation. A covering input must agree through all \(\ell k\) symbols, so it covers at most one witness. Thus

$$
r(n,\delta;Q)\ge N^k\quad
\text{if }\ell k\le n,\ e^{-kC_b}>C_*\delta. \tag{4.4}
$$

For \(T_n=-\ln\delta_n\), choose

$$
k_n=\max\left(0,\min\left(\lfloor n/\ell\rfloor,\
\left\lfloor(T_n-\ln C_*)/C_b\right\rfloor-1\right)\right).
$$

For \(k_n>0\) the strict threshold holds, and \(k_n=0\) gives the trivial bound \(r\ge1\). Floors and fixed constants yield

$$
\underline h_\delta(Q)\ge h\min(1,\gamma/c_b). \tag{4.5}
$$

This lower bound tests every approximate control and the complete time interval. It does not claim forced coding on all of \(Q\).

## 5. One near-full-area compact set with a cheaper catalogue

Use the measurable sign selection of §2. Let \(p_m(y)\) be its zero frequency in the first \(m\) symbols. The initial domain of any fixed selected length-\(m\) word is Borel and has length at most \(2q^{-m}\): its ratio map has slope \(q^m\) and its final ratio belongs to \([-1,1]\). The domains partition \([-1,1]\) with assigned endpoints. No independent or equidistributed digits are assumed.

Write \(H(p)=-p\ln p-(1-p)\ln(1-p)\). For \(0<\eta<1/2\), the elementary binomial bound and the symmetry and concavity of \(H\) give

$$
\operatorname{Leb}\{|p_m-1/2|>\eta\}
\le2(m+1)\exp[-m(\ln q-H(1/2-\eta))]. \tag{5.1}
$$

Indeed each of at most \(m+1\) bad types has at most \(e^{mH(1/2-\eta)}\) words, each covering length at most \(2q^{-m}\). The binomial upper bound follows by bounding a binomial probability by one.

If \(\ln q>H(1/2-\eta)\), (5.1) is summable. Borel–Cantelli shows that almost every ratio eventually stays in the frequency band at every subsequent \(m\). This is a band, **not** convergence to exactly \(1/2\).

Put

$$
\bar c=(c_0+c_1)/2,\qquad c_-=\bar c-\eta|c_0-c_1|>0. \tag{5.2}
$$

At every good time the selected prefix cost is \(S_m=m[p_mc_0+(1-p_m)c_1]\ge c_-m\). Let \(S_N\) be the set obeying the band for every \(m\ge N\). These sets increase and their union has full measure. By inner regularity, choose \(N\) and a compact

$$
E\subset S_N\cap((-1,1)\setminus\mathbb Q),\qquad
|E|>2(1-\varepsilon/2).
$$

Removing the rationals has no measure cost and ensures no interval is contained in \(E\). With \(C=Nc_-\), early times and positive costs give

$$
S_m(y)\ge c_-m-C\quad(y\in E,\ m\ge0). \tag{5.3}
$$

Choose \(s_0>0\), \(s_0^2<\varepsilon/2\), and set

$$
K_\varepsilon=\{(s,sy):s_0\le s\le1,\ y\in E\}. \tag{5.4}
$$

It is compact with empty interior. The Jacobian is \(s\), so its area is \((1-s_0^2)|E|/2>(1-\varepsilon/2)^2>1-\varepsilon\). Its selection precedes every tolerance and decay exponent.

An exactly followed selected prefix of length \(m\) has endpoint norm at most \(Me^Ce^{-c_-m}\). For small \(\delta\), take

$$
m=\min\left(n,\left\lceil
\frac{-\ln\delta+\ln(2\sqrt2Me^C)}{c_-}
\right\rceil\right). \tag{5.5}
$$

Use all selected prefixes meeting \(E\), at most \(2^m\) words. If \(m=n\) they cover the whole horizon exactly. Otherwise append a fixed tail, e.g. \(0^\infty\). Its entire trajectory has Euclidean norm at most \(\delta/2\) by (2.2), starting with norm at most \(\delta/(2\sqrt2)\). Since the origin is in \(Q\), all times qualify. Hence

$$
\overline h_\delta(K_\varepsilon)\le\ln2\min(1,\gamma/c_-). \tag{5.6}
$$

This includes \(\gamma=0,\infty\), all radii, every intermediate time and nonmonotone sequences. The exact upper rate in §8 supplies the additional \(\ln q\) cap.

## 6. Choosing blocks for every unequal contraction pair

Let \(D>0\) solve the classical equation

$$
\rho_0^D+\rho_1^D=1. \tag{6.1}
$$

At \(p_D=\rho_0^D\), direct substitution gives \(H(p_D)=D\chi(p_D)\), where \(\chi(p)=pc_0+(1-p)c_1\). At \(D_0=\ln2/\bar c\), strict AM–GM gives \(e^{-D_0c_0}+e^{-D_0c_1}>1\), since \(c_0\ne c_1\). The sum decreases strictly with the exponent, so \(D>\ln2/\bar c\). This established entropy/contraction calculation only chooses the blocks.

For integers \(L\ge2\), \(1\le j\le L-1\), take all blocks \(w01\), where \(w\) has length \(L\) and \(j\) zeros. Then

$$
\ell=L+2,\quad N=\binom Lj,\quad
C_b=(j+1)c_0+(L-j+1)c_1.
$$

Concatenations have run length at most \(R=L+1\). With \(j/L\to p_D\), the bounds

$$
e^{LH(j/L)}/(L+1)\le\binom Lj\le e^{LH(j/L)}
$$

show that \(\ln N/C_b\to H(p_D)/\chi(p_D)=D\). For the lower binomial bound, its probability at \(j\), with success parameter \(j/L\), is a mode among \(L+1\) probabilities. Fix a finite choice with \(h/c_b>\ln2/\bar c\). Choose small \(\eta>0\) so this remains strict with \(c_-=\bar c-\eta|c_0-c_1|\). Finally choose \(q_0<2\) sufficiently close to 2 that

$$
E(q_0)<2^{-R-1}/4,\quad
\ln q_0>H(1/2-\eta),\quad \ln q_0>h.
$$

These are possible since \(E(q)\to0\), \(H(1/2-\eta)<\ln2\), and \(h<\ln2\); they hold for all \(q>q_0\). Sections 4–5 prove (1.5), and their strict slope comparison proves (1.6). Sections 2 and 8 give the remaining assertions. This proves Theorem 8.1. ∎

All assumptions above concern the dynamics or explicitly chosen words. None assumes the desired covering rate. There is one system family and one counterexample mechanism.

## 7. An explicit certificate

Take

$$
\rho_0=1/4,\quad\rho_1=1/256,\quad 2-2^{-19}<q<2. \tag{7.1}
$$

Let \(\mathcal W\) be the length-64 words with 46 zeros and 18 ones, containing neither \(0^{16}\) nor \(1^{16}\). A prescribed run position gives \(\binom{48}{30}\) or \(\binom{48}{46}\) words. There are 49 positions. A union bound gives

$$
\begin{aligned}
N=|\mathcal W|
&\ge\binom{64}{46}-49\left(\binom{48}{30}+\binom{48}{46}\right)\\
&=3\,243\,506\,777\,908\,712
>2^{51}=2\,251\,799\,813\,685\,248. \tag{7.2}
\end{aligned}
$$

This exact binomial inequality uses no enumeration or fitting. The total is \(3\,601\,688\,791\,018\,080\); the subtracted union bound is \(358\,182\,013\,109\,368\).

Use blocks \(w01\), \(w\in\mathcal W\). Each has length 66, 47 zeros and 19 ones. Runs inside \(w\) have length at most 15; a separator extends a run by at most one at either boundary, so all concatenations have run length at most 16. Thus

$$
C_b=246\ln2,\quad c_b=(41/11)\ln2,\quad
d=2^{-17},\quad\kappa=2^{-18}.
$$

For (7.1), \(E(q)<2^{-19}=d/4\). Choose \(\eta=1/100\). Since \(H''(p)=-1/[p(1-p)]\le-4\),

$$
H(49/100)\le\ln2-1/5000<\ln q.
$$

The last inequality uses \(\ln(2/q)\le(2-q)/q<2^{-19}<1/5000\). Here \(c_-=(247/50)\ln2>c_b\). For every \(\varepsilon\), the same construction gives one \(K_\varepsilon\) for all sequences, with

$$
\underline h_\delta(Q)\ge\frac{17}{82}\gamma,\qquad
\overline h_\delta(K_\varepsilon)\le\frac{50}{247}\gamma,\qquad
0<\gamma\le(41/11)\ln2. \tag{7.3}
$$

Indeed \(\ln N>51\ln2\), and

$$
\frac{17}{82}-\frac{50}{247}=\frac{99}{20254}>0. \tag{7.4}
$$

For example fix one system with \(q=2-2^{-20}\), and \(\delta_n=2^{-n}\). Then

$$
\liminf_n n^{-1}\ln r(n,2^{-n};Q)
\ge\frac{17\ln2}{82}
>\frac{50\ln2}{247}
\ge\limsup_n n^{-1}\ln r(n,2^{-n};K_\varepsilon). \tag{7.5}
$$

Overlap and margin are strictly positive but small. This certificate does not address substantial overlap or bases far from 2. Neither intermediate limit is claimed to exist.

## 8. Endpoints and further bounds: established-method applications

### 8.1 Exact and ordinary outer rates

A fixed exact word has ratio slope \(q^n\), so its feasible initial ratio section has length at most \(2q^{-n}\). Integration against the Jacobian \(s\) bounds its covered area by \(q^{-n}\), giving \(r_E(n;K)\ge\operatorname{area}(K)q^n\).

Let \(m_q=1-q/2\). Cover \([-1,1]\) by at most \(C_q q^n\) centers with radius \((m_q/2)q^{-n}\). Use the sign-policy word of each center. At every positive time its reference ratio has magnitude at most \(q/2\). A nearby ratio differs by exactly \(q^k\) times its initial discrepancy, at most \(m_q/2\) for every \(k\le n\). Thus the same word is exactly feasible for every radius, and \(r_E(n;Q)\le C_q q^n\). The exact rate is \(\ln q\) for every positive-area compact set. This is the R05 mesh/section method applied to radius-independent exact ratio feasibility, not a new counting principle.

At fixed \(\delta>0\), a fixed exact prefix length \(m\) makes \(M\rho_{\max}^m<\delta/(2\sqrt2)\). Append a fixed tail and apply (2.2) for all future times. Outer counts are uniformly bounded in the horizon, hence the outer rate is zero. This boundedness framework is already studied by Chen–Zhong 2024.

### 8.2 A universal positive-area lower bound

Let \(c_{\max}=\max_i c_i\). Truncate positive-area \(K\) to \(s\ge s_0>0\), retaining positive area. Under an arbitrary actual control, radius at time \(k\) is \(sA_k\), with \(A_k\ge e^{-c_{\max}k}\). The ratio map has slope \(q^k\). Condition (4.2) bounds initial ratios covered through the whole horizon by a set of length at most

$$
2q^{-k}\left(1+2\delta e^{c_{\max}k}/s_0\right)
\quad\text{for each }k\le n.
$$

Fubini gives \(r(n,\delta;K)\ge B_Kq^k/(1+C_K\delta e^{c_{\max}k})\). Choosing \(k=\min(n,\lfloor-\ln\delta/c_{\max}\rfloor)\) yields

$$
\underline h_\delta(K)\ge\ln q\min(1,\gamma/c_{\max}). \tag{8.1}
$$

The exact upper bound matches \(\ln q\) when \(\gamma\ge c_{\max}\), including equality and infinity.

### 8.3 The full binary stopping tree is only an upper catalogue

Stop each binary path when its product first drops below \(t=\delta/(2\sqrt2M)\), or at depth \(n\). Each actual state has a feasible sign-policy code. Follow it to its stopping leaf and append a fixed tail; (2.2) proves validity at every time. Some other leaves may have no feasible states, which does not invalidate the upper catalogue.

For \(D\) in (6.1), probabilities \(p_i=\rho_i^D\) sum to one. The finite complete prefix-free tree has leaf probabilities \(A_w^D\) summing to one, each greater than \((\rho_{\min}t)^D\). The count is at most \((\rho_{\min}t)^{-D}\), so

$$
\overline h_\delta(Q)\le\min\{\ln q,D\gamma\}. \tag{8.2}
$$

At \(\gamma=0\) this gives zero for all \(K\). When \(\gamma>c_{\max}\), eventually no path stops before \(n\), so this raw tree has \(2^n\) leaves while the actual catalogue has rate \(\ln q<\ln2\). Overlap can therefore save exponentially many raw words. The R06 polynomial comparison to the full binary tree cannot be imported. This ordinary overlap/covering consequence is not the novelty claim of Theorem 8.1.

## 9. Remaining obstacle and contribution boundary

Theorem 8.1 answers the sufficiency question: inward margin does not remove contraction costs attached to forced viable prefixes. Overlap somewhere does not supply every initial state with useful alternative controls before errors become visible.

The new controlled interfaces are (4.3)–(4.5) and (5.1)–(5.6), with one set preceding all precision sequences. Bounded-run coding, binomial counting, Borel–Cantelli, inner regularity, mesh covers and the root (6.1) are established tools. SOURCES.md gives direct comparisons, without claiming all-library priority.

For the fixed system \(q=2-2^{-20},\rho_0=1/4,\rho_1=1/256,\delta_n=2^{-n}\), the minimum unresolved problem is existence and evaluation of the full-\(Q\) rate. The proved bounds are

$$
\frac{17\ln2}{82}\le\underline h_\delta(Q)
\le\overline h_\delta(Q)\le D\ln2,\qquad
4^{-D}+256^{-D}=1, \tag{9.1}
$$

and for the constructed \(K_\varepsilon\),

$$
\frac{\ln q}{8}\le\underline h_\delta(K_\varepsilon)
\le\overline h_\delta(K_\varepsilon)\le\frac{50\ln2}{247}. \tag{9.2}
$$

A sharp lower bound must accommodate repeated alternative controls in the overlap instead of charging every binary prefix as necessary. No interval-cover comparison with subexponential loss is proved. No classification at appreciable overlap, nonlinear control-dependent theorem, communication implementation, new pressure duality, or four-major-journal significance follows.
