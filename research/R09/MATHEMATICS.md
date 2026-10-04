# R09: first-exit repair, a genuine limit, and a narrower interval

4 October 2026. All logarithms are natural. Only the fixed R08 system and the full initial cone are considered. The limit now exists. Its exact stopping-cover characterization is proved, but its constant is not evaluated; two distinct algebraic bounds must not be described as a matching formula.

## 1. Fixed data and the main result

Set

$$
\epsilon=2^{-20},\quad q=2-\epsilon,\quad
\rho_0=1/4,\quad\rho_1=1/256,\quad
F_i(s,z)=(\rho_i s,\rho_i(qz-q\sigma_i s/2)),
\quad \sigma_0=-1,\ \sigma_1=1.
$$

Let \(Q=\{0\le s\le1,\ |z|\le s\}\), \(Q^\delta=\{x:\operatorname{dist}_2(x,Q)<\delta\}\), and \(r_n=r(n,2^{-n};Q)\) with the R08 definition: one of finitely many binary controls is assigned to each actual initial state, and its states at every time \(0,\ldots,n\) lie in \(Q^{2^{-n}}\). All binary inputs are allowed, including inputs whose trajectories leave and reenter \(Q\).

For a finite word \(w=w_1\cdots w_l\), define

$$
c(w)=\#_0(w)+4\#_1(w),\qquad A(w)=4^{-c(w)},\qquad
T_i(y)=qy-q\sigma_i/2,
$$

and its exact feasible ratio interval

$$
I_w=\{y\in[-1,1]:T_{w_k}\cdots T_{w_1}(y)\in[-1,1]
\text{ for every }1\le k\le l\}.
$$

The empty word has cost zero, product one and interval \([-1,1]\). For integers \(m\ge1\), put

$$
N_m=\min\{|\mathcal W|:\mathcal W\text{ finite},\
c(w)\ge m\ (w\in\mathcal W),\
[-1,1]\subset\bigcup_{w\in\mathcal W} I_w\},\qquad N_0=1. \tag{1.1}
$$

The intervals can overlap. There is no prescribed partition or reference itinerary in this minimization. Radius products and feasibility remain part of the object.

**Theorem 9.1.** For this fixed system:

1. There are constants \(B,C>0\), independent of \(n\), such that for every sufficiently large \(n\),

$$
N_{m_-(n)}\le B(n+1)r_n,\qquad
r_n\le N_{m_+(n)}, \tag{1.2}
$$

where

$$
C=\frac{4\sqrt2}{\epsilon\rho_{\min}},\quad
m_-(n)=\left\lceil n/2-\log_4 C\right\rceil,\quad
m_+(n)=\left\lceil n/2+\log_4(2\sqrt2)\right\rceil .
$$

2. The limit exists and satisfies the exact characterization

$$
H:=\lim_{n\to\infty}\frac{\ln r_n}{n}
=\frac12\kappa,\qquad
\kappa=\lim_{m\to\infty}\frac{\ln N_m}{m}
=\inf_{m\ge1}\frac{\ln N_m}{m}. \tag{1.3}
$$

3. For \(R\ge2\), let \(x_R\in(0,1)\) be the unique root

$$
\left(\sum_{a=1}^R x_R^a\right)
\left(\sum_{b=1}^R x_R^{4b}\right)=1,
\qquad d_R=-\frac{\ln x_R}{\ln4}.
$$

Then

$$
\frac{17\ln2}{82}
<d_{19}\ln2
\le H\le d_{21}\ln2
<D\ln2,\qquad 4^{-D}+256^{-D}=1. \tag{1.4}
$$

Both R08 bounds are strictly improved. No equality to \(d_{19}\), \(d_{21}\), \(D\), or a fixed-policy pressure is asserted. Equation (1.3) is a useful exact representation and existence theorem, not an evaluation of the remaining optimization in \(N_m\).

The decisive new interface is (1.2): approximate controls are converted to exact feasible stopping covers with only a linear multiplicity loss. This is a comparison with the *minimal actual interval cover*, not with the full binary stopping tree. Classical concatenation, the subadditivity lemma and finite-state weighted counting are used after this geometric comparison.

## 2. Actual cone states and full-time intervals

### 2.1 Keeping the actual projection

Let \(L=\{(1,y):-1\le y\le1\}\). Linearity gives
\(\varphi(k,(s,sy),u)=s\varphi(k,(1,y),u)\).
Since \(0\in Q\) and \(aQ\subset Q\) for \(0\le a\le1\),

$$
\operatorname{dist}_2(ax,Q)\le a\operatorname{dist}_2(x,Q).
$$

A catalogue covering the actual states on \(L\) therefore covers every actual state of \(Q\) under the same assigned controls, and restriction gives the reverse inequality. Thus

$$
r(n,\delta;Q)=r(n,\delta;L). \tag{2.1}
$$

This is a proved physical scaling reduction. It does not replace initial states by input sequences or discard their controlled feasibility.

### 2.2 Exact Euclidean formula

For a word \(w\) of length \(n\), write

$$
A_k=\prod_{j=1}^k\rho_{w_j},\qquad
b_k=\frac12\sum_{j=1}^k\sigma_{w_j}q^{-(j-1)},\qquad
y_k=q^k(y-b_k).
$$

Starting at \((1,y)\), the state is \((A_k,A_ky_k)\). If \(0<\delta\le1/4\) and \(k\ge1\), \(A_k\le1/4\), and

$$
\operatorname{dist}_2((A_k,A_ky_k),Q)<\delta
\quad\Longleftrightarrow\quad
A_k(|y_k|-1)<\sqrt2\delta. \tag{2.2}
$$

Necessity follows from the linear side functionals \(z-s\) and \(-z-s\), each of norm \(\sqrt2\). For sufficiency, if \(|A_ky_k|\le A_k\), the state is in \(Q\). Otherwise its projection onto the relevant slanted edge of the infinite cone has first coordinate
\((A_k+|A_ky_k|)/2<A_k+\delta/\sqrt2<1\).
It lies on the corresponding edge of the finite triangle \(Q\), and the distance is \((|A_ky_k|-A_k)/\sqrt2\).

Consequently the entire set covered by this arbitrary approximate word is the relative interval

$$
J_w(\delta)=[-1,1]\cap
\bigcap_{k=1}^n
\left(b_k-q^{-k}(1+\sqrt2\delta/A_k),\
b_k+q^{-k}(1+\sqrt2\delta/A_k)\right). \tag{2.3}
$$

Every intermediate constraint is present. Formula (2.3) allows exits and returns; imposing only the final interval would be incorrect.

### 2.3 A fixed safe policy and contraction

Use control 0 for \(y\le0\), and control 1 for \(y>0\). It maps \([-1,1]\) into \([-q/2,q/2]\). Its normalized angular margin is

$$
a_q=1-q/2=\epsilon/2>0.
$$

In the max norm, both physical maps have operator norm at most

$$
\rho_{\max}(q+q/2)=3q/8<3/4<1. \tag{2.4}
$$

The origin is fixed and all inputs contract. The angular margin is not a uniform positive Euclidean distance from the boundary at the vertex.

## 3. A uniformly bounded local stopping cover

**Lemma 9.2.** Fix \(K_0>0\). There is an integer \(M_{K_0}\), depending on \(K_0,q\) but not on \(A,\delta\), with this property. If \(0<A\le1\) and \(J\subset[-1,1]\) is an interval of length at most \(K_0\delta/A\), then \(J\) is covered by at most \(M_{K_0}\) words which are exactly feasible from their assigned actual states \((A,Ay)\), through their whole prefixes, and end with radius at most \(\delta\).

**Proof.** Put \(\eta=\delta/A\). If \(\eta\ge1\), the empty word suffices. Otherwise let

$$
t=\left\lceil\frac{\ln(1/\eta)}{\ln4}\right\rceil,\qquad
e_t=(a_q/2)q^{-t}.
$$

Choose centers in the closure of \(J\) whose \(e_t\)-neighborhoods cover it. At most

$$
2+\frac{K_0\eta}{e_t}
=2+\frac{2K_0\eta q^t}{a_q}
\le2+\frac{2K_0q}{a_q} \tag{3.1}
$$

are needed: \(q^t\le q\eta^{-\ln q/\ln4}\) and \(\ln q/\ln4<1\).

At each center follow the safe policy until its product first becomes at most \(\eta\). This takes at most \(t\) inputs, since all products are at most \(4^{-t}\). For any actual ratio within \(e_t\) of the center, following the same word gives ratio error exactly \(q^j\) times the initial error, at most \(a_q/2\) at every positive time \(j\le t\). The reference ratio is at most \(q/2\) in magnitude, so the actual ratio is at most \(q/2+a_q/2<1\). The whole prefix is exactly feasible and its ending radius is at most \(A\eta=\delta\). Take \(M_{K_0}\) to be an integer above the right-hand side of (3.1). ∎

Centers choose controls; they do not replace actual initial states. The inequality \(\ln q<\ln4\) is essential to the uniform bound. A generic interval-cover assertion without contraction costs would not prove this lemma.

## 4. First-exit repair for every approximate control

We prove the left-hand side of (1.2). Let \(\delta=2^{-n}\), choose \(n\) large enough that
\(\delta\le1/4\) and \(C\delta<1\), and put

$$
C_s=4\sqrt2/\epsilon,\qquad C=C_s/\rho_{\min}.
$$

Consider any length-\(n\) control word \(w\). Let \(l\) be its first index with \(A_l\le C_s\delta\). Such an index exists because \(A_n\le4^{-n}=\delta^2<C_s\delta\), and \(l\le n\). Moreover

$$
A_{l-1}=A_l/\rho_{w_l}\le C\delta. \tag{4.1}
$$

Take any \(y\in J_w(\delta)\). If its original word is exactly feasible through time \(l-1\), that prefix already provides an exact stopping word with radius at most \(C\delta\).

Otherwise let \(k<l\) be its first exact exit. All earlier states are in \(Q\), and \(A_k>C_s\delta\). If \(y_k>1\), exact feasibility of \(y_{k-1}\) forces the chosen control to be 0, because \(T_1([-1,1])\) has upper endpoint \(q/2<1\). By (2.2),

$$
1<y_k<1+\sqrt2\delta/A_k<1+\epsilon/4.
$$

Replace this single input by 1. The new ratio is

$$
y'_k=y_k-q\in(1-q,\ 1-q+\epsilon/4)\subset(-1,1). \tag{4.2}
$$

If \(y_k<-1\), the chosen input was 1. Replacing it by 0 gives

$$
y'_k=y_k+q\in(q-1-\epsilon/4,\ q-1)\subset(-1,1). \tag{4.3}
$$

For each \(k\) and exit side, the relevant initial states form an interval: intersect \(J_w(\delta)\) with the exact feasible prefix interval at time \(k-1\) and with the corresponding first-violation half-line. There are at most two such pieces per \(k\). On each piece, after replacement the radius is the common number

$$
A'_k=A_{k-1}\rho_{1-w_k}.
$$

Its ratio interval has length at most

$$
\sqrt2\delta/A_k
=\sqrt2\frac{\rho_{1-w_k}}{\rho_{w_k}}\frac{\delta}{A'_k}
\le64\sqrt2\,\delta/A'_k. \tag{4.4}
$$

Its closure remains in \([-1,1]\) by (4.2) or (4.3). Apply Lemma 9.2 with \(K_0=64\sqrt2\). At most \(M=M_{64\sqrt2}\) exactly feasible suffixes cover that entire actual ratio interval and end at radius at most \(\delta\). Concatenate the unchanged exact prefix, the replaced input, and these suffixes.

Thus \(J_w(\delta)\) can be covered by at most

$$
1+2(l-1)M\le B(n+1),\qquad B=1+2M, \tag{4.5}
$$

exactly feasible words ending at radius at most \(C\delta\). The one extra word covers the states whose original prefix through \(l-1\) was feasible. The new controls need not follow the old word later; all their newly used prefixes have just been proved feasible.

Apply this procedure to each word in a minimal approximate catalogue. By (2.1) its intervals cover \([-1,1]\). The resulting exact words cover every actual initial ratio and all have cost at least \(\lceil\log_4(1/(C\delta))\rceil\). This gives

$$
N_{\lceil\log_4(1/(C\delta))\rceil}
\le B(n+1)r(n,\delta;Q). \tag{4.6}
$$

Multiple later exits or overlap switches cause no missing case: on each piece the first exit has been repaired, and its replacement suffix is safe at every time. The proof uses all input words, including those not generated by the safe policy.

## 5. Exact stopping covers: pruning, concatenation and the limit

### 5.1 Finite minima and pruning

For every \(m\), \(N_m<\infty\). Cover \([-1,1]\) by a finite mesh with radius \((a_q/2)q^{-m}\) and use each center's first \(m\) safe-policy inputs. The same error estimate as in Lemma 9.2 proves feasibility on neighboring actual ratios, and every word has cost at least \(m\).

Replace any word with the prefix at which its cost first reaches \(m\). The new exact feasible interval contains the old one. Such prefixes have length at most \(m\) and costs in \([m,m+3]\). Removing duplicates cannot increase the count. There are finitely many possible normalized words, so the minimum in (1.1) is attained in this normalized family. This justifies using minima without relying on a closed-cover compactness argument.

### 5.2 The upper comparison

Take a normalized minimal catalogue for \(N_{m_+(n)}\). Its words have length at most \(m_+(n)\le n\) for large \(n\), and products at most

$$
4^{-m_+(n)}\le\delta/(2\sqrt2).
$$

Every actual state is exactly feasible through its assigned prefix. At its endpoint the max norm is at most \(\delta/(2\sqrt2)\). Append any fixed binary tail. By (2.4), its Euclidean norm at every later time is at most \(\delta/2\). Since the origin belongs to \(Q\), every later state lies in \(Q^\delta\). This proves the right-hand side of (1.2) for the complete horizon.

### 5.3 Submultiplicativity is proved, not assumed

For \(m,j\ge1\), take minimal catalogues for \(N_m,N_j\). For each actual ratio, select a first word keeping it in \([-1,1]\) through cost at least \(m\), then select a second catalogue word for its actual endpoint ratio in \([-1,1]\). Their concatenation is exactly feasible, with cost at least \(m+j\). All pairs provide at most \(N_mN_j\) words. Hence

$$
N_{m+j}\le N_mN_j. \tag{5.1}
$$

The words' intervals may overlap; assignment to a state does not require a fixed global partition. Set \(f(m)=\ln N_m\). It is finite, nonnegative, monotone and subadditive. For any fixed positive \(j\), write \(m=aj+b\), \(0\le b<j\). Then

$$
f(m)\le af(j)+f(b)\le(a+1)f(j).
$$

Together with \(f(m)/m\ge\inf_{j\ge1}f(j)/j\), this proves the last two expressions in (1.3), by the classical subadditivity argument.

Finally \(m_\pm(n)/n\to1/2\) and \(\ln(B(n+1))/n\to0\). Taking logarithms in (1.2) proves \(\ln r_n/n\to\kappa/2\). The original horizon catalogue \(r_n\) is not assumed submultiplicative at the changing ambient tolerance; that gap is precisely why (4.6) was necessary.

## 6. The geometric run bounds 19 and 21

These bounds use the fixed \(q\), rather than modifying the parameter or inferring feasibility from a pressure equation.

### 6.1 Uniformly forced codes with runs at most 19

For a binary sequence \(\omega\), write

$$
Y_q(\omega)=\frac12\sum_{j=0}^\infty\sigma_{\omega_{j+1}}q^{-j},
\qquad
T_{\omega_1}(Y_q(\omega))=Y_q(\operatorname{shift}\omega).
$$

If all equal-symbol runs have length at most \(R\), every shift satisfies

$$
|Y_q|\le M_R:=P-\frac{q}{q^{R+1}-1},
\qquad P=\frac{q}{2(q-1)}. \tag{6.1}
$$

To prove the upper bound, enumerate positions \(j_1,j_2,\ldots\) of the negative symbols, starting positions at zero. No positive run exceeds \(R\), so \(j_l\le l(R+1)-1\). Their subtraction from the all-positive series \(P\) is at least
\(\sum_{l\ge1}q^{-[l(R+1)-1]}=q/(q^{R+1}-1)\).
Changing all signs gives the absolute bound. This is an infinite geometric estimate, not enumeration of trajectories.

For \(R=19\),

$$
\begin{aligned}
\kappa_{19}:=q-1-M_{19}
&=\frac{q}{q^{20}-1}
-\frac{\epsilon(2q-1)}{2(q-1)}\\
&>\frac{q\epsilon}{1-\epsilon}
-\frac{\epsilon(2q-1)}{2(1-\epsilon)}
=\frac{\epsilon}{2(1-\epsilon)}>0. \tag{6.2}
\end{aligned}
$$

Here \(q^{20}<2^{20}=1/\epsilon\). Thus \(M_{19}<q-1<1\). The recurrence and the tail bound imply that the sign of \(Y_q\) is its first sign, with

$$
|Y_q|\ge1/2-M_{19}/q>1/q-1/2.
$$

The intended input is exactly feasible at every shift. The opposite input has absolute next ratio at least \(q-M_{19}>1+\kappa_{19}\). Therefore every such actual ratio has a unique exactly feasible control at every future time.

This is a sharper direct coding estimate than R08's sufficient continuity bound. Unique coding itself is classical.

### 6.2 A safe policy covering every initial state has tail runs at most 21

After the first input of the safe policy, the ratio lies in \([-q/2,q/2]\). For a zero run starting in this interval,

$$
T_0^j(y)=q^j(y+P)-P\ge P(q^j\epsilon-1),
$$

since \(P-q/2=P\epsilon\). A twenty-second consecutive zero would require the pre-input ratio at \(j=21\) to be nonpositive. But

$$
q^{21}\epsilon
=2(1-\epsilon/2)^{21}
\ge2-21\epsilon>1, \tag{6.3}
$$

by Bernoulli's inequality. It is therefore impossible. Changing signs excludes twenty-two consecutive ones as well. The initial input is treated separately, so no claim is made that the entire word has run cap 21.

This policy supplies a feasible code for every actual initial ratio, despite repeated passage through the overlap.

## 7. Finite-state weighted counting and strict improvement

Let \(S_R(m)\) count the first-cost-\(m\) prefixes of all infinite sequences with runs at most \(R\). The prefix tree is complete within this language. Its leaves have costs between \(m\) and \(m+3\).

Put \(\alpha_R=-\ln x_R=d_R\ln4\), \(a=x_R\), \(b=x_R^4\). The run-state graph has states \((i,r)\), \(1\le r\le R\), recording the last digit and its current run. Its edge weight is \(a\) for a new 0 and \(b\) for a new 1. The condition

$$
\left(\sum_{j=1}^R a^j\right)
\left(\sum_{j=1}^R b^j\right)=1 \tag{7.1}
$$

provides a positive vector \(v\) satisfying

$$
v_{0,r}=b v_{1,1}\sum_{j=0}^{R-r}a^j,\qquad
v_{1,r}=a v_{0,1}\sum_{j=0}^{R-r}b^j.
$$

Indeed take \(v_{0,1}=1\), \(v_{1,1}=a\sum_{j=0}^{R-1}b^j\); (7.1) verifies the remaining \(r=1\) identity and all transition identities. Define transition probabilities by edge weight times \(v_{\text{next}}/v_{\text{current}}\); these sum to one. At the initial state use probabilities \(a v_{0,1}/V,b v_{1,1}/V\), where \(V=a v_{0,1}+b v_{1,1}\).

For every allowed nonempty word \(w\), telescoping gives

$$
\mu[w]=e^{-\alpha_R c(w)}v_{\text{last state}}/V.
$$

Its ratio to \(e^{-\alpha_Rc(w)}\) is bounded above and below by positive constants depending only on \(R\). The finite first-cost-\(m\) leaves have total probability one. Their costs lie in \([m,m+3]\). Hence there are constants \(u_R,v_R>0\) such that

$$
u_R e^{\alpha_R m}\le S_R(m)\le v_R e^{\alpha_R m}
\quad(m\ge1). \tag{7.2}
$$

This is the elementary finite-state pressure calculation; the controlled geometric comparisons must come separately.

For each run-19 leaf append an allowed infinite tail. Its actual ratio has the unique feasible code of §6.1. Every normalized exact cost-\(m\) covering word assigned to this ratio must coincide with that leaf: it must follow the unique code and stop at its first cost crossing. Distinct leaves give distinct actual ratios and require distinct covering words. Thus

$$
N_m\ge S_{19}(m).
$$

For the upper bound use §6.2. After its first input, every safe-policy code has run cap 21. For \(m>4\), collect each possible first input and all run-21 stopping suffixes at remaining cost \(m-1\) or \(m-4\). This catalogue covers every actual ratio through a feasible prefix of total cost at least \(m\), so

$$
N_m\le S_{21}(m-1)+S_{21}(m-4).
$$

Together with (7.2), this proves
\(\alpha_{19}\le\kappa\le\alpha_{21}\), and hence the middle inequalities of (1.4).

For strict comparison to R08, first observe \(3^{41}<2^{65}\), so at \(d_0=17/82\),
\(4^{-d_0}=2^{-17/41}>3/4\). At \(x=3/4\),

$$
\left(\sum_{a=1}^5 x^a\right)
\left(\sum_{b=1}^3 x^{4b}\right)
=\frac{17618125239}{17179869184}>1.
$$

The defining run-19 polynomial at \(4^{-d_0}\) is therefore greater than one. It decreases with \(d\), proving \(d_{19}>17/82\).

At the unrestricted root \(D\), let \(a=4^{-D},b=256^{-D}\), so \(a+b=1\). For every finite \(R\),

$$
\left(\sum_{j=1}^R a^j\right)
\left(\sum_{j=1}^R b^j\right)
=(1-a^R)(1-b^R)<1.
$$

Thus \(d_R<D\). The polynomials increase strictly with \(R\), giving \(d_{19}<d_{21}\); these two bounds do not match. This completes Theorem 9.1. ∎

For orientation only, the certified root intervals

$$
\begin{aligned}
724666391905/10^{12}&<x_{19}<724666391906/10^{12},\\
724583297715/10^{12}&<x_{21}<724583297716/10^{12}
\end{aligned}
$$

follow by exact rational sign substitution into the increasing defining polynomials. They give bounds approximately \(0.16102194\le H\le0.16107928\), compared with R08's approximately \(0.14370124\le\liminf\le\limsup\le0.16114231\). The analytic proof is §§2–7; these polynomial evaluations neither enumerate control catalogues nor establish an exact value of \(H\).

## 8. What remains unresolved

The remaining problem is to evaluate \(\kappa=\inf_m\ln N_m/m\). This is optimization over overlapping actual feasible intervals with controlled contraction costs. The full binary language overcounts, the safe policy is only one upper catalogue, and the run-19 uniquely coded set is only one necessary subset. Their pressure roots cannot be equated without another proof.

The new mechanism is that a first early approximate exit puts its initial-state piece in a ratio interval of width \(O(\delta/A_k)\); the opposite branch repairs that interval. Because \(q\rho_{\max}<1\), a uniformly bounded number of exactly feasible suffixes handles the whole piece. Late exits occur only after the radius is already \(O(\delta)\). This is why repeated outside excursions cannot create an additional exponential saving beyond the optimal exact stopping cover, although exact overlap choices themselves still affect \(\kappa\).

No classification for other parameters, dimensions, initial sets or nonlinear systems is claimed. No communication scheme, new pressure duality, all-library priority or journal tier follows. SOURCES.md records the direct originals, existing methods, actual reading and formal-version limitations.
