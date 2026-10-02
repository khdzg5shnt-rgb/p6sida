# WHS2019 entropy in the binary cone

3 October 2026. This is an application of Definitions 4.1 and 4.3 of Wang–Huang–Sun (2019), checked in the supplied journal original. It is not claimed as a new variational principle. All logarithms are natural.

## Definitions and model

Let

$$
Q=\{(s,z):0\le s\le1,\ |z|\le s\},\qquad
f_j(s,z)=\left(R(s),\frac{R(s)}s(2z+sv_j)\right),
\quad v_0=1,\ v_1=-1.
$$

Use the smooth extension at zero from R01. Assume R is the same increasing radial diffeomorphism as there, R(0)=0 and 0<R(s)<s for 0<s≤1. Inputs are all binary sequences. Every f_j fixes the apex a=(0,0). At positive radius y=z/s evolves by y⁺=2y+v_j.

An invariant partition C=(A,τ,υ) consists of a finite Borel partition A of Q, an integer τ≥1, and an assigned length-τ input word υ(A) that keeps every state in its atom inside Q during the block. The itinerary cylinder Q_N(x,C) consists of states having the same first N atom names as x under these successively assigned controls. In the WHS definitions, for any Borel probability µ on Q,

$$
\underline h_\mu(Q,C)=\int_Q\liminf_{N\to\infty}
\frac{-\log\mu(Q_N(x,C))}{N\tau}\,d\mu(x),\qquad
\overline h_\mu(Q,C)=\int_Q\limsup_{N\to\infty}
\frac{-\log\mu(Q_N(x,C))}{N\tau}\,d\mu(x).
$$

The global quantities are the respective infima over all invariant partitions C. No invariance assumption on µ appears in these definitions. Denote planar Lebesgue measure restricted to Q by λ; its total mass is already one because ∫₀¹2s ds=1.

## Lower bound for every partition

For an input word w of length n, the feasible normalized initial interval is

$$
I_w=\psi_{w_0}\cdots\psi_{w_{n-1}}([-1,1]),\qquad
\psi_0(y)=(y-1)/2,\quad \psi_1(y)=(y+1)/2.
$$

Its length is 2^{1−n}. Each inverse branch preserves [-1,1], so membership also guarantees feasibility at all intermediate times. Its feasible initial set V_w has vertical section sI_w and hence

$$
\lambda(V_w)=\int_0^1s\,|I_w|\,ds=2^{-n}.
$$

Fix an arbitrary invariant partition C and x∈Q. Every state in Q_N(x,C) has the same sequence of assigned control blocks. Concatenating the blocks gives one word w of length Nτ. Each intermediate block is feasible by the partition property, including the last block. Therefore Q_N(x,C)⊂V_w and

$$
\lambda(Q_N(x,C))\le2^{-N\tau}.
$$

The local liminf and limsup are both at least log 2, with −log 0=+∞. Integrating and then taking the infimum over **all** C gives lower bounds log 2 for both global quantities. This argument does not assume a generator or maximal irreducibility.

## One partition attains the bound

Take τ=1 and

$$
A_0=\{(s,z)\in Q:s>0,\ z\le0\}\cup\{a\},\qquad
A_1=\{(s,z)\in Q:s>0,\ z>0\},
\qquad \upsilon(A_j)=j.
$$

For y≤0, 2y+1∈[-1,1]; for y>0, 2y−1∈(-1,1]. At the apex either input is feasible. Thus C₀ is a finite Borel invariant partition. Its normalized closed-loop map is the two-branch map T(y)=2y+1 for y≤0 and T(y)=2y−1 for y>0.

At depth N, each binary name corresponds, up to the finitely many branch endpoints, to a dyadic interval of length 2^{1−N}. This follows inductively by applying the inverse branch ψ_j to each depth-(N−1) interval. The intervals have disjoint interiors; assigning the endpoint y=0 to A₀ chooses an itinerary without changing any interval length. At zero radius the extra apex also has area zero. Consequently every positive-area cylinder has λ-mass 2^{-N}; for λ-almost every x the local liminf and limsup both equal log 2. Hence

$$
\boxed{\underline h_\lambda(Q)=\overline h_\lambda(Q)=\log2.}
$$

For µ=δ_a, the cylinder containing a has probability one for every N and every partition. Both integrated local quantities, and both global infima, are zero:

$$
\underline h_{\delta_a}(Q)=\overline h_{\delta_a}(Q)=0.
$$

λ is not invariant under the displayed closed-loop map: the integral of s−R(s) with respect to λ is strictly positive, whereas invariance of a probability would force it to be zero. Thus λ is not the state marginal of an invariant feasible lift. The latter marginals are all δ_a, as also follows directly by integrating s−R(s). There is no identification of λ with those lift measures. The positive control measure entropies above and the zero conditional KS entropy of every invariant feasible lift are statements about distinct domains.

## Why two WHS variational hypotheses fail here

Q is connected. A finite partition of Q by nonempty clopen atoms must therefore have the sole atom Q. Such an atom would require one fixed length-τ word feasible for every state in Q. Already its first letter has feasible normalized interval of length one, strictly smaller than [-1,1], so no such word exists. Therefore there is no clopen invariant partition of Q.

There is also no maximally irreducible invariant partition in the sense of WHS Definition 4.9. For any C, let A be the atom containing a. Since τ≥1, choose a binary word different from υ(A). The alternative word keeps a in Q at every time. It therefore cannot send the whole atom A outside Q at any time, as maximal irreducibility requires. This contradicts that requirement, regardless of endpoint conventions for the control horizon.

Theorems 6.4 and 7.2 of WHS use a clopen invariant partition; their global Corollary 6.5(iii) additionally uses a maximally irreducible one. These are not direct theorems for this full cone. The computation above instead uses their entropy definitions and the elementary word-area formula. Nonapplicability of a theorem is not a novelty claim, and this application supplies no new major upgrade interface.
