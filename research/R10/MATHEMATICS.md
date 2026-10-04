# R10: forced overlap blocks and failure of common-tail dominance

4 October 2026. Natural logarithms. The fixed system, full initial cone, Euclidean environment metric and tolerance sequence remain those of R09. This round proves one local optimal-cover interface and an all-large-cost counterexample to a deletion rule. It does not evaluate the global rate, sharpen its bounds or prove an optimal policy.

## 1. Objects and the single theorem

Put

$$
\epsilon=2^{-20},\ q=2-\epsilon,\ \rho_0=1/4,\ \rho_1=1/256,\quad
T_0(y)=qy+q/2,\quad T_1(y)=qy-q/2.
$$

The physical maps are \(F_i(s,z)=(\rho_i s,\rho_i(qz-q\sigma_i s/2))\), with \(\sigma_0=-1,\sigma_1=1\), and \(Q=\{0\le s\le1,\ |z|\le s\}\). For a word \(w\), retain

$$
c(w)=\#_0(w)+4\#_1(w),\quad A(w)=4^{-c(w)},\quad
I_w=\{y\in[-1,1]:T_{w_k}\cdots T_{w_1}(y)\in[-1,1]
\text{ for every }1\le k\le |w|\}.
$$

All binary inputs are allowed. For \(r(n,2^{-n};Q)\), each actual initial state is assigned a catalogue control, and its states at every time \(0,\ldots,n\) must lie in the open Euclidean \(2^{-n}\)-neighborhood of \(Q\); trajectories may leave and reenter \(Q\). The tolerance sequence and full initial set stay fixed.

The empty word has cost zero and interval \([-1,1]\). The global \(N_m\) minimizes the number of cost-at-least-\(m\) words whose actual feasible intervals cover **all** \([-1,1]\). R09 proves
\(H=\lim_n n^{-1}\ln r(n,2^{-n};Q)=\kappa/2\), where \(\kappa=\lim_m m^{-1}\ln N_m\). That constant remains unknown.

One input is feasible on

$$
D_0=[-1,b],\quad D_1=[-b,1],\qquad
b=1/q-1/2=\epsilon/(2q).
$$

The actual overlap is \(O=[-b,b]\). A local cover of \(O\) is only an auxiliary part of the global problem; the initial set has not been replaced.

Set

$$
P=\frac{q}{2(q-1)},\quad \theta=\epsilon q^{20}=(1-\epsilon/2)^{20},
\quad\Lambda=q^{21},\quad p=P(1-\theta),\quad
X=\Lambda O=[-\theta/2,\theta/2],
$$

and \(u=0\,1^{20},\ v=1\,0^{20}\).

**Theorem 10.1 (the overlap-cover interface).**

(a) Every \(y\in O\) can follow either block feasibly through all 21 times. After choosing the first input, the next 20 inputs are forced by exact feasibility. Their endpoint maps and costs are

$$
T_u(y)=\Lambda y+p,\quad c(u)=81,\quad A(u)=4^{-81};
\qquad T_v(y)=\Lambda y-p,\quad c(v)=24,\quad A(v)=4^{-24}. \tag{1}
$$

They are not asserted to be first returns to \(O\): their endpoints generally lie in a larger interval.

(b) For every finite suffix \(a\), including the empty suffix,

$$
I_{ua}\cap O=O\cap\Lambda^{-1}(I_a-p),\qquad
I_{va}\cap O=O\cap\Lambda^{-1}(I_a+p). \tag{2}
$$

Let \(L_m\) be the auxiliary minimum number of exact cost-at-least-\(m\) words covering \(O\). For every integer \(m>81\),

$$
\begin{split}
L_m=\min\{|\mathcal A|+|\mathcal B|:\;&
\mathcal A,\mathcal B\text{ finite suffix families},\\
&c(a)\ge m-81\ (a\in\mathcal A),\
c(a)\ge m-24\ (a\in\mathcal B),\\
&X\subset(U_{\mathcal A}-p)\cup(U_{\mathcal B}+p)\},
\end{split} \tag{3}
$$

where \(U_{\mathcal A}=\bigcup_{a\in\mathcal A}I_a\). Empty families are allowed. This is a mixed optimization, with two different remaining budgets and a nonzero translation.

(c) For every integer \(m\ge161\), there exist normalized first-cost-\(m\) words \(u_m,v_m\), beginning with \(u,v\), whose actual feasible intervals have positive length and are disjoint:

$$
I_{u_m}\cap I_{v_m}=\varnothing. \tag{4}
$$

They are obtained using the same infinite continuation. Thus even after legitimate pruning at the same threshold, the initially faster contracting block need not cover its slower counterpart's states.

This excludes a common-tail exchange. It neither excludes exchanges using other continuations nor proves that a fixed policy is suboptimal.

## 2. All intermediate states in the forced blocks

Bernoulli's inequality and Taylor's theorem give

$$
1-10\epsilon\le\theta<1,\qquad
\theta\le1-10\epsilon+\frac{95}{2}\epsilon^2.
$$

For the specified \(\epsilon\), therefore,

$$
9\epsilon<1-\theta\le10\epsilon,\quad 1<P<2,\quad
9\epsilon<p<20\epsilon,\quad q^{-20}=\epsilon/\theta<2\epsilon. \tag{5}
$$

These are analytic inequalities, not catalogue enumeration.

After the initial 0 and then \(j\) inputs equal to 1,

$$
Y_j(y)=T_1^jT_0(y)=q^{j+1}y+P(1-\epsilon q^j),\qquad0\le j\le20. \tag{6}
$$

Indeed \(T_1(x)=q(x-P)+P\) and \(q/2-P=-P\epsilon\). For all these \(j\), the maximum on \(O\) is

$$
P-\epsilon q^j(P-1/2)\le P-\epsilon(P-1/2)
=q/2+\epsilon/2=1. \tag{7}
$$

For \(0\le j\le19\), \(\epsilon q^j<1/2\); the minimum is consequently

$$
P-\epsilon q^j(P+1/2)>P/2-1/4>1/4>b. \tag{8}
$$

At each of these times the ratio is in \((b,1]\), where 0 is infeasible, so 1 is the only feasible next input. At \(j=20\), the image is

$$
Y_{20}(O)=[p-\theta/2,p+\theta/2]\subset(-1,1), \tag{9}
$$

by (5). Thus all 20 forced inputs are feasible, and all preceding constraints have been checked. Reflection, using \(T_0(-y)=-T_1(y)\), proves the corresponding statements for \(v\), with image \([-p-\theta/2,-p+\theta/2]\).

Counting inputs gives (1). On actual cone states the full block maps are

$$
F_u(s,z)=4^{-81}(s,\Lambda z+ps),\qquad
F_v(s,z)=4^{-24}(s,\Lambda z-ps). \tag{10}
$$

Every state \((s,sy)\), \(0<s\le1,y\in O\), remains in \(Q\) throughout its block. The vertex remains fixed. The factor \(4^{-57}\) compares the two radial products; it supplies no continuation-feasibility inclusion.

## 3. The exact cover and deletion identities

The prefix blocks are feasible for all of \(O\). A continuation after \(u\) is feasible at all its times exactly when \(\Lambda y+p\in I_a\); after \(v\), exactly when \(\Lambda y-p\in I_a\). This proves (2), with every intermediate suffix constraint retained.

For finite suffix families \(\mathcal C,\mathcal D\), local coverage of \(v\mathcal C\) is contained in local coverage of \(u\mathcal D\) if and only if

$$
\big(U_{\mathcal C}\cap(X-p)\big)+2p\subset U_{\mathcal D}. \tag{11}
$$

Put \(x=\Lambda y-p\). Coverage by the old family means \(x\in U_{\mathcal C}\cap(X-p)\); the same actual initial state is covered by the new family precisely when \(x+2p\in U_{\mathcal D}\). This proves both directions. At threshold \(m\), suffix costs must also be at least \(m-24\) for the old family and \(m-81\) for the new one. Reusing a suffix adds 57 cost units, but it does not establish (11). This criterion concerns the portion in \(O\); deleting a whole global word also requires preserving its coverage outside \(O\).

For (3), normalize any catalogue covering \(O\) at first cost crossing and discard words covering no point of \(O\). When \(m>81\), such a word cannot stop within either forced block. Part (a) forces its prefix to be \(u\) or \(v\). Grouping by first input gives suffix costs at least \(m-81\) or \(m-24\); rescaling (2) gives the displayed mixed cover of \(X\). The two prefix types are distinct words, so the counts add.

Conversely any pair of suffix families in (3) yields \(u\mathcal A\cup v\mathcal B\), covering every actual ratio in \(O\), feasible through all prefix and suffix times, and meeting the threshold. Pruning does not lose coverage. The minimum exists: first-crossing words have length at most \(m\), so only finitely many words are available. Finiteness follows by restricting a finite full cover for \(N_m\), whose mesh construction was checked in R09.

The return images \(X+p\) and \(X-p\) overlap. Optimizing them separately and adding their sizes does not prove (3). Nor is \(L_m\) automatically the global \(N_m\).

## 4. Counterexample after normalization, at every large cost

Set \(a_*=q/[2(q+1)]<1/3\) and \(\alpha=(10)^\infty\). Then \(T_1(a_*)=-a_*\) and \(T_0(-a_*)=a_*\); this continuation is feasible forever. Define actual starting ratios

$$
y_u=(a_*-p)/\Lambda,\qquad y_v=(a_*+p)/\Lambda. \tag{12}
$$

They are interior points of \(O\), since

$$
a_*+p<1/3+20\epsilon<1/2-5\epsilon\le\theta/2=\Lambda b. \tag{13}
$$

Their distance is \(2p/\Lambda>0\). The controls \(u\alpha\) and \(v\alpha\), from their respective initial states, reach the same \(a_*\) after the block and then stay on its two-cycle. Every ratio is strictly inside \([-1,1]\).

For each \(m>81\), let \(u_m,v_m\) be their prefixes stopped at first cost crossing of \(m\). They have costs in \([m,m+3]\) and are the normalized words allowed by the original optimization. For any length-\(\ell\) feasible word,

$$
\operatorname{diam} I_w\le2q^{-\ell}; \tag{14}
$$

the final ratio map has slope \(q^\ell\), its feasible image lies in \([-1,1]\), and the earlier constraints can only shrink its interval. Every input costs at most 4. Each tail therefore has length at least \((m-81)/4\), and for \(m\ge161\),

$$
\operatorname{diam}I_{u_m},\operatorname{diam}I_{v_m}
\le2q^{-41}=2\Lambda^{-1}q^{-20}. \tag{15}
$$

The intervals contain \(y_u,y_v\) respectively. For all \(x\in I_{u_m}\), \(y\in I_{v_m}\), the triangle inequality and (5) give

$$
|x-y|\ge\frac{2p-4q^{-20}}{\Lambda}
>\frac{10\epsilon}{\Lambda}>0. \tag{16}
$$

Thus they are disjoint for every \(m\ge161\). Each has positive length, since its witness satisfies every one of its finitely many constraints strictly. This proves (4) and completes Theorem 10.1. ∎

This is not a numerical test at cost 161. It specifies actual starting states, infinite feasible controls, legitimate cost normalization and a uniform argument for all larger integers. Common-tail intervals have a fixed nonzero displacement \(2p/\Lambda\), about \(9.0950\cdot10^{-12}\), while their diameters tend to zero. The displacement cannot be set to zero in the limiting optimization.

## 5. Dependencies and the remaining unproved comparison

The actual interval definition, physical cost product and threshold pruning have been rederived or checked above. R09's first-exit repair, all-horizon tail comparison and submultiplicativity were also read through and independently checked at their dependency steps: the first-exit pieces are intervals, the opposite branch repairs each early exit, its ratio width permits a uniform suffix cover, and the late-stop/short-prefix tail meets the whole original horizon. No error affecting the current argument was found. These are not new R10 results.

The global bounds remain

$$
-\tfrac12\ln x_{19}\le H\le-\tfrac12\ln x_{21},\quad
\left(\sum_{j=1}^R x_R^j\right)\left(\sum_{j=1}^R x_R^{4j}\right)=1.
$$

Equation (3) leaves a mixed minimum and only describes the overlap component. It does not sharpen these bounds.

For a precise unresolved comparison, define the feasible selector
\(\pi_0(y)=0\) when \(y\le b\), and \(1\) when \(y>b\). It selects the faster forced block \(u\) on \(O\); no assertion about the fastest entire trajectory is made. Let \(G_m\) count its distinct first-cost-\(m\) prefixes from **all** \(y\in[-1,1]\). These are a finite exact catalogue, so \(N_m\le G_m\).

**Unresolved, not a theorem:**

$$
\forall\eta>0\ \exists m_0\ \forall m\ge m_0:
\quad G_m\le e^{\eta m}N_m. \tag{17}
$$

If true, this would certify that selector's rate optimality; its rate would still require accurate evaluation. Theorem 10.1 neither proves nor disproves (17). It excludes the common-tail replacement used to try to justify it. A valid argument must use other continuations and retain their shifted coverage and residual budgets. No such subexponential comparison was assumed or obtained.

This is the single unclosed comparison recorded for another authorized attack. No other policy, parameter, initial-set classification or pressure computation was pursued.

Affine composition, block substitutions, interval inclusion and prefix pruning are existing tools. The increment is the actual forced-block mixed cover, its unequal budgets and the all-large-cost failure of common-tail dominance. This is narrower than R09's global existence theorem and insufficient to raise a journal-tier assessment. Formal literature and reading boundaries are in SOURCES.md.
