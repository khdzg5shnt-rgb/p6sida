# R07 — Critical precision with a transversely expanding branch

2026-10-04. Baseline: `148bdcc17ffac67e83312bcb5131dff6f599c584`. This note resolves only the system, initial set and precision sequence authorized for R07. All logarithms are natural.

## 1. Exact statement

On the ambient Euclidean plane let

$$
F_0(s,z)=\left(\frac34s,\frac34(2z+s)\right),\qquad
F_1(s,z)=\left(\frac14s,\frac14(2z-s)\right),\qquad
Q=\{(s,z):0\le s\le1,\ |z|\le s\}.
$$

The actual initial set is the whole of $Q$, of area one. Every infinite binary input is allowed. Write $x_0=x$ and $x_j=F_{u_j}(x_{j-1})$. For $n\ge1$ and $\delta>0$, let $r(n,\delta;Q)$ be the least cardinality of a finite catalogue $\mathcal U\subset\{0,1\}^{\mathbb N}$ such that

$$
\forall x\in Q\quad\exists u\in\mathcal U\quad
\forall j\in\{0,\ldots,n\}:\quad
\operatorname{dist}_2(x_j,Q)<\delta. \tag{1.1}
$$

Thus leaving $Q$ is permitted; leaving its open $\delta$-neighbourhood is not. Only the first $n$ symbols affect (1.1), so finite words and their arbitrary infinite extensions give the same minimum. We do not approximate or replace the actual initial point.

Put

$$
\alpha=\ln2,\quad p_* =\frac{\ln2}{\ln3},\quad
H(p)=-p\ln p-(1-p)\ln(1-p),\quad
\lambda=\frac{\ln(p_* /(1-p_*))}{\ln3}>0.
$$

We use the convention $0\ln0=0$ at the endpoints of $H$.

**Theorem 7.1.** With $\delta_n=2^{-n}$ and $j_n=\lceil p_*n\rceil$, for every integer $n\ge1$,

$$
\frac{\binom n{j_n}}{n(3n+1)}
\ \le\ r(n,2^{-n};Q)
\ \le\ N\left(n,\frac{2^{-n}}{2\sqrt2}\right)
\ \le\ (8\sqrt2)^\lambda e^{nH(p_*)}. \tag{1.2}
$$

Here $N(n,t)$ counts the complete binary tree stopped at radial product at most $t$, or at depth $n$, as defined in §4. Consequently the requested limit exists and is

$$
\boxed{\displaystyle
\lim_{n\to\infty}\frac1n\ln r(n,2^{-n};Q)
=H\left(\frac{\ln2}{\ln3}\right).} \tag{1.3}
$$

In fact, for a constant $C$ independent of $n$,

$$
r(n,2^{-n};Q)\le N\left(n,\frac{2^{-n}}{2\sqrt2}\right)
\le C n^3 r(n,2^{-n};Q). \tag{1.4}
$$

Equation (1.4) concerns this fixed system, $K=Q$, and this precision sequence only. It is not R06's uniform statement about all stopped-leaf witnesses.

## 2. The precise R06 dependencies

The following conclusions result from checking the actual steps in R06 §§2–4, rather than importing its main theorem outside its hypotheses.

| R06 step | Status here |
|---|---|
| Binary feasible cylinders and their exact lengths | Valid: the ratio maps remain $2y+1$ and $2y-1$. Reproved in §3. |
| Exact prefix followed by a small tail | Valid with the specified tail $1^\infty$. Arbitrary tails no longer contract. See §4. |
| Geometry at the first wrong feasible branch | Valid for an arbitrary approximate control. Reproved in §6. |
| R06 (3.5), using $2^{-\ell}\ge\prod\rho_i$ | Invalid here: already $1/2<\rho_0=3/4$. Its stopped-cylinder separation conclusion cannot be imported. |
| Positive-cost stopped-tree type count in R06 §4 | Its proof uses $c_i>0$, not $\rho_i<1/2$, so that counting argument survives. We give a shorter independent upper estimate at the specified precision in §4. |

There is no error to correct in R06 under its stated $\rho_i<1/2$ assumptions. The new lower bound below uses a large selected family of depth-$n$ cylinders. It makes no assertion that the failed length comparison holds for all stopped cylinders.

## 3. Feasible coding in the actual cone

Set $\rho_0=3/4$, $\rho_1=1/4$, $v_0=1$, $v_1=-1$. For a word $w=w_1\cdots w_k$, write

$$
A_w=\prod_{i=1}^k\rho_{w_i},\qquad S(w)=-\ln A_w,
\qquad A_\varnothing=1.
$$

For $s>0$, the ratio $y=z/s$ satisfies $y\mapsto 2y+v_i$. Its inverse branches on $[-1,1]$ are

$$
b_0(y)=(y-1)/2,\qquad b_1(y)=(y+1)/2.
$$

Define $b_w=b_{w_1}\circ\cdots\circ b_{w_k}$ and $I_w=b_w([-1,1])$. Every inverse branch sends $[-1,1]$ into itself. Hence if $y\in I_w$, all ratio states through time $k$ are in $[-1,1]$. Conversely, the final ratio being in $[-1,1]$ implies $y\in I_w$ by inversion, and therefore implies the intermediate conditions as well. The radii are $sA_{w_1\cdots w_j}\in[0,1]$. Thus $w$ is exactly feasible through time $k$ at $(s,sy)\in Q$ precisely when $y\in I_w$.

The intervals $I_w$ of depth $k$ partition $[-1,1]$ with disjoint interiors and length $2^{1-k}$. Their midpoints form a grid of spacing $2^{1-k}$. Endpoints can have two codings, which does not affect the covering argument; every chosen midpoint is interior to its own depth-$k$ interval. The apex is fixed by both maps.

The ratio is used only for computation. The estimates below are estimates for actual states $(s,z)$ with Euclidean distance, not a replacement metric on the ratio space.

## 4. An all-time upper bound with the fast tail

For $0<t<1$, stop each binary path at the first word $w$ with $A_w\le t$, or at length $n$ if that happens earlier. Denote the leaves by $\mathcal L(n,t)$ and their number by $N(n,t)$. This is a finite complete prefix-free family. Its intervals $I_w$ cover $[-1,1]$.

For each leaf use the infinite control $w1^\infty$. Until $|w|$, every initial point coded by $I_w$ remains in $Q$. If $|w|=n$, this already proves (1.1). Otherwise $A_w\le t$. In the maximum norm,

$$
\|F_1(s,z)\|_\infty
\le\max\{\tfrac14|s|,\tfrac12|z|+\tfrac14|s|\}
\le\tfrac34\|(s,z)\|_\infty.
$$

At the end of the exact prefix, $\|x_{|w|}\|_\infty\le sA_w\le A_w$. Consequently, for every tail length $m\ge0$,

$$
\operatorname{dist}_2(x_{|w|+m},Q)
\le\|x_{|w|+m}\|_2
\le\sqrt2(3/4)^m A_w.
$$

With $t=\delta/(2\sqrt2)$, this is at most $\delta/2<\delta$. This proves the middle inequality of (1.2), including all intermediate times and the strict neighbourhood convention. The construction does not require $F_0$ to contract transversely.

We now count this tree at $\delta=2^{-n}$. Write

$$
c_0=\ln(4/3),\quad c_1=\ln4,\quad
T_n=n\ln2+\ln(2\sqrt2).
$$

The parent of every leaf has cost less than $T_n$, so every leaf of length $k\le n$ has

$$
S(w)<T_n+c_1. \tag{4.1}
$$

Let $\nu$ be the Bernoulli probability on binary sequences with symbol-zero probability $p_*$. Define

$$
\beta=-\ln(1-p_*)-\lambda c_1.
$$

We need $\beta>0$. Indeed $1/2<p_*<3/4$ (equivalently $4>3$ and $16<27$), and

$$
\beta=\frac{g(p_*)}{\ln3},\qquad
g(p)=c_0\ln(1-p)-c_1\ln p,
\quad g'(p)=-\frac{c_0}{1-p}-\frac{c_1}{p}<0,
\quad g(3/4)=0.
$$

For any word of length $k$, its cylinder probability is exactly

$$
\nu([w])=\exp\{-\beta k-\lambda S(w)\}. \tag{4.2}
$$

This follows by checking $\beta+\lambda c_0=-\ln p_*$ and $\beta+\lambda c_1=-\ln(1-p_*)$. Since the leaf cylinders partition the entire input space, their probabilities sum to one. By $\beta,\lambda>0$, $k\le n$ and (4.1),

$$
N(n,e^{-T_n})
\le\exp\{\beta n+\lambda(T_n+c_1)\}
=(8\sqrt2)^\lambda\exp\{n(\beta+\lambda\ln2)\}.
$$

Finally, $p_*\ln3=\ln2$ gives $\beta+\lambda\ln2=H(p_*)$. This proves the last inequality in (1.2). The Bernoulli weight is an elementary counting device, not a new invariance-pressure or measure-entropy theorem.

## 5. Exponentially many words with controlled prefixes

For a word $w$, set

$$
D_k(w)=\ln(2^k A_{w_1\cdots w_k})
=N_0(w_1\cdots w_k)\ln3-k\ln2,\qquad D_0=0.
$$

These are the cumulative logarithms of transverse multipliers: symbol zero contributes $\ln(3/2)>0$, and symbol one contributes $-\ln2<0$.

Among all words of length $n$ with exactly $j_n=\lceil p_* n\rceil$ zeros, let $\mathcal G_n$ be those satisfying

$$
D_k(w)\ge0\qquad(0\le k\le n). \tag{5.1}
$$

Every word of this type has total sum

$$
0\le D_n(w)=j_n\ln3-n\ln2<\ln3. \tag{5.2}
$$

**Cyclic-minimum argument.** Given any such word, choose an index $l\in\{0,\ldots,n-1\}$ where $D_l$ is minimal over these indices, and rotate the word to begin at $l+1$. A non-wrapping prefix of the rotated word has sum $D_{l+k}-D_l\ge0$: for the possible endpoint $l+k=n$, use $D_n\ge0\ge D_l$. A wrapping prefix has sum $D_n-D_l+D_h\ge D_n\ge0$ for some $h\le l$. Thus every cyclic orbit of words of this type contains a member of $\mathcal G_n$. Each orbit has at most $n$ distinct words, even when the word is periodic. Therefore

$$
|\mathcal G_n|\ge\frac1n\binom n{j_n}. \tag{5.3}
$$

This is the classical cyclic-minimum/ballot device, proved here for the real increments needed in this system. It is not a new combinatorial lemma; see SOURCES for the original-method attribution and actual reading scope. In particular we do not import an integer-step formula for the exact number of good rotations.

For every $w\in\mathcal G_n$, choose the actual witness $x_w=(1,y_w)\in Q$, where $y_w$ is the midpoint of $I_w$. The witness ordinates are a subset of a grid with spacing $2^{1-n}=2\delta_n$. Condition (5.1), not a bound on all stopped-cylinder lengths, will prevent an approximate control from covering too many of them.

## 6. Every approximate control covers at most $3n+1$ witnesses

First note the Euclidean necessary condition

$$
(r,z)\in Q^\delta\quad\Longrightarrow\quad |z|<r+2\delta. \tag{6.1}
$$

Indeed choose $(r',z')\in Q$ within Euclidean distance $\delta$; then $|z|\le|z'|+|z-z'|\le r'+|z-z'|<r+2\delta$. We use only this necessary condition, not a claimed equality between distance and vertical excess.

Fix any length-$n$ input $u$. No exact feasibility assumption is imposed on $u$. There is at most one $w\in\mathcal G_n$ equal to $u$. For any other covered witness, let $j$ be the first position with $w_j\ne u_j$, and put $a=u_1\cdots u_{j-1}=w_1\cdots w_{j-1}$. Let $m_a=b_a(0)$ be the midpoint splitting the two children of $I_a$.

The common prefix sends the initial ordinate to $2^{j-1}(y_w-m_a)$. The wrong next branch therefore has ratio satisfying

$$
|y_j|-1=2^j|y_w-m_a|. \tag{6.2}
$$

Its actual radius is $A_a\rho_{u_j}$, so (6.1) and (6.2) imply

$$
|y_w-m_a|
<\frac{2\delta_n}{2^j A_a\rho_{u_j}}
=\frac{\delta_n}{\rho_{u_j}e^{D_{j-1}(w)}}
\le4\delta_n. \tag{6.3}
$$

The last inequality uses $w\in\mathcal G_n$ and $\rho_{u_j}\ge1/4$. For this fixed $u,j$, all such witnesses lie in the same child opposite to $u_j$. Thus (6.3) puts them in a **one-sided** interval of length at most $4\delta_n$. Grid spacing $2\delta_n$ permits at most three witnesses in that interval. Summing over the $n$ possible first-disagreement positions, and adding the possible $w=u$, proves the asserted bound $3n+1$.

If some prefix of $u$ has $D<0$, it simply cannot be the common prefix of a member of $\mathcal G_n$ at the relevant position. There is no assumption that an arbitrary approximate control itself satisfies (5.1).

Any catalogue covering all of $Q$ covers these witnesses. Hence (5.3) yields

$$
r(n,\delta_n;Q)\ge\frac{|\mathcal G_n|}{3n+1}
\ge\frac{\binom n{j_n}}{n(3n+1)},
$$

which proves the first inequality of (1.2). This lower bound uses a necessary condition at a time $j\le n$ for every covered witness. A later return to the neighbourhood cannot erase a violation at that time. Thus it applies to the full-time constraint and all permitted approximate controls, not just to terminal states or natural feasible codings.

## 7. Taking the limit and comparing catalogues

For $q=j/n$, the elementary binomial bounds are

$$
\frac{e^{nH(q)}}{n+1}\le\binom nj\le e^{nH(q)}. \tag{7.1}
$$

For $0<j<n$, use the binomial distribution with parameter $q$: its probability at $j$ is $\binom nj e^{-nH(q)}$, at most one and at least $1/(n+1)$ because $j$ is a mode, as the ratio of neighbouring masses verifies. The cases $j=0,n$ are immediate.

Since $j_n/n\to p_*\in(0,1)$, (7.1), continuity of $H$, and (1.2) give matching lower and upper limits $H(p_*)$. Moreover $0\le j_n/n-p_*<1/n$ and $H'$ is bounded on a fixed neighbourhood of $p_*$. Therefore $n|H(j_n/n)-H(p_*)|$ is bounded for all sufficiently large $n$. Combining (7.1) with (1.2), and absorbing the finitely many smaller $n$ into a constant, proves (1.4).

The same sandwich proves the stopped tree has exponent $H(p_*)$. If one separately evaluates the R06 type-count expression, $\chi(p)=\ln4-p\ln3$ and $\chi(p_*)=\ln2$. For $p\ge p_*$, $H(p)\le H(p_*)$ because $p_*>1/2$. For $p\le p_*$, the derivative of $H(p)/\chi(p)$ has numerator $g(p)>0$ from §4, so $\ln2\,H(p)/\chi(p)\le H(p_*)$. Thus the formal tree exponent agrees with (1.3). This agreement was proved for actual approximate controls by §§5–6; it was not assumed from the old formula.

## 8. What this result does and does not explain

The branch $F_0$ multiplies transverse differences by $3/2$, so R06's contraction of every tail and its uniform stopped-cylinder length comparison are lost. The useful replacement is a family with zero asymptotic transverse logarithmic growth: its symbol-zero frequency approaches $p_*$, and cyclic rotation makes every prefix product $2^kA_k$ at least one. Its cardinality has exponent $H(p_*)$. Even controls which leave $Q$ can absorb only $O(n)$ of these actual witnesses. The fast branch still supplies a single safe tail after a small exact prefix. Together these mechanisms exclude an exponential saving over the threshold catalogue at the specified precision.

This is a new proved interface relative to the repository's R06 result. The combinatorial rotation and probability-weight counting methods are classical. We have not proved a new general pressure principle, a new phase transition, a formula at other precision exponents, or a classification of initial sets.

Also, the present system does **not** have convergence to the origin under every allowed input. For example, $F_0^k(1,1)$ has $s_k=(3/4)^k$ and $z_k=2(3/2)^k-(3/4)^k\to\infty$. Exactly feasible trajectories still approach the apex since $s_k\le(3/4)^k$ and $|z_k|\le s_k$. Consequently this example extends the finite-horizon constraint-cost analysis beyond uniformly contracting inputs; it is not a stronger instance of the original manuscript's all-input uniform-convergence claim.

The precise R07 limit is settled. No mathematical gap remains in (1.3). Whether this bounded extension materially strengthens a publishable R05–R06 package is a separate contribution/priority assessment, recorded without a journal-tier claim in REPORT and SOURCES.
