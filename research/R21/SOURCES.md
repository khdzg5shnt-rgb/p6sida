# R21: formal original, coverage, versions, and actual reading

5 October 2026. Baseline `782edf83d79d1765c1e6eb5b90f0a7951aecdb54`. One newly identified formal original was read in full. No further article was requested, no failed download was repeated, and no broad literature search was undertaken.

## 1. Correction of the original-file record

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of invariance entropy dimension. *Journal of Differential Equations, 453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

- This is the already supplied project file **陈虎.pdf**, supplied locally as `project_sources/06-pdf`. The first page names Hu Chen, Yu Huang, and Xingfu Zhong, gives the journal/volume/article number and exactly this DOI. The volume year is 2026; the 2025 in the DOI is not the reference year.
- 24 printed pages, 841,646 bytes; SHA-256 `8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`. PDF metadata agrees with the first page. All 24 pages decode to nonempty text, the text proceeds through the final acknowledgments and reference list on p. 24, and no missing page was observed. Pages 5, 12, and 20 were additionally rendered to check the critical notation and hypotheses against the printed formulas.
- The formal PDF gives received 5 May 2025, revised 2 August 2025, accepted 29 September 2025, and available online 9 October 2025. Its identity is based on the supplied journal original, not on an abstract or an author manuscript.
- **The earlier record that the project lacked this original was mistaken: the file had been supplied but was not identified in the earlier execution.** R20's historical text is preserved, with an explicit correction appended to R20/SOURCES.md. The latest full-text status is obtained and read, not missing.
- Actual reading in R21: every printed page 1–24, including all definitions, theorem statements, proofs, remarks, acknowledgments, and references. This is a full reading and a targeted coverage analysis; it is not certification that every general variational proof in the article has been independently reconstructed. No theorem from this article is needed as a correctness premise of Theorem 21.1.

## 2. The objects actually defined in the original

| Original location | Verified object and hypothesis | Relation to this project |
|---|---|---|
| §2.1, pp. 2–4; Definition 2.3 | A fixed finite measurable invariant partition, a fixed block time τ, and a specified control on each cell. Cylinders require the prescribed successive cell itinerary. | Our natural exact code gives a measurable partition, but our admissible catalogue is not restricted to its controls or itineraries. |
| §2.2, pp. 4–6; Definitions 2.5–2.7 | Bowen/packing covering and packing weights exp[−s(τN)^α]; variable cylinder lengths N are allowed. The dimension is critical in α. | α changes time normalization. It is not an exponentially decreasing Euclidean neighbourhood radius. |
| §2.3, pp. 6–7; Definition 2.9 | Local lower/upper rates of −log μ(Q_N(x,C))/(Nτ)^α. μ is a Borel probability on Q. | **μ need not be invariant.** Ordinary normalized area is a permitted measure at this level, so non-invariance of our area measure is not a novelty distinction. |
| §4.1, pp. 20–21; Definitions 4.1–4.2 | δ is permitted missing measure in a cover; the limit δ→0 is a measure-coverage limit. The stated setup uses a clopen invariant partition. | This δ is not dist₂(x,Q)<δ. Its role cannot be silently replaced by the environmental precision sequence δ_n. |

All supplied definitions and proofs were checked for a possible bridge, rather than excluded merely because their names differ.

## 3. What the proofs provide and what they do not provide

| Original result/proof | Actual supplied step | Specific missing bridge to R20/R21 |
|---|---|---|
| Lemma 2.11 and Theorems 2.12–2.13, pp. 7–9 | Selection from nested partition cylinders and measure-to-cover estimates for their time weights. | The sets V(n,δ,u) covered by arbitrary approximate inputs are not this nested cylinder family. No estimate of a wrong first branch, later reentry, moving Euclidean error band, or radial stopping witness is proved there. |
| Proposition 3.1, pp. 9–11 | Comparison of weighted and unweighted covers by the same partition cylinders, with polynomial/time-weight slack. | This is an existing weighted-cover technique. It does not compare a prescribed exact coding with the minimum cardinality of all actual Euclidean approximate controls. |
| Lemma 3.2; Theorems 3.3–3.4, pp. 11–14 | A cylinder Frostman construction and a Bowen variational principle/dimension relation; the stated invariant partition is clopen. | The construction controls measure on prescribed cylinders, not arbitrary-input physical bands. It contains no independent radial product or precision stopping comparison. |
| Lemma 3.6; Theorems 3.7–3.9, pp. 14–19 | Packing selection, an inductive measure construction, and packing variational relations; the main theorems require a clopen invariant partition. | These are fixed-partition time-complexity results, not an optimal approximate-control covering theorem at δ_n. The construction does not establish the relative prefix spacing of R21. |
| Theorems 4.3–4.7, pp. 21–24 | Inverse variational relations through full-measure subsets for Bowen/packing quantities, under a clopen invariant partition. | A full-measure infimum is not the simultaneous claim about one nearly full-area compact set for every Euclidean precision sequence. Even a typical-set application still needs our finite-time band, stopping, and full-tail comparisons. |

There is also an independently checkable hypothesis obstruction. The actual triangle Q is connected, so a finite clopen partition of Q can only have its one nonempty cell Q. No single open-loop input keeps all of Q in Q at the first discrete step: branch 0 excludes the upper open part of each fibre and branch 1 excludes the lower open part. Thus no such clopen invariant partition exists here for any positive integer block time. The main clopen variational theorems do not directly apply on this Q. This is not used to dismiss the more general measurable-cylinder estimates in §2; those were compared separately above. A lifted symbolic space would require a separately proved bridge back to actual initial states and Euclidean tolerance.

For an additional concrete test, under the natural measurable partition of our systems, assigned cylinders differ from the complete feasible strips only on null boundary curves. Their area is comparable to λ_w. Hence for area-almost every x,

−log μ(Q_N(x,C))/N → h_a.

The corresponding local time-power dimension is 1: α<1 gives infinite local rate and α>1 gives zero. This remains true while the actual precision slopes vary with β in R20, and with D and h_a/χ in R21. Thus there is no automatic identification of that dimension with our catalogue slopes. Reweighting or stopping the cylinders can supply classical counting, but **the arbitrary-input comparison (13) of MATHEMATICS.md remains an additional proof**, even granting the original's stated variational results.

**Coverage verdict:** this full formal original supplies the fixed-partition entropy-dimension and variational framework, and relevant measure/cover methods. Its statements and the complete written proofs do not already establish R20's real-catalogue threshold or R21's mismatched-rate theorem. The project main contribution is not withdrawn on this evidence. This is a precise comparison with this article, not a claim of whole-field priority or a quartile certificate. No correction of the external article is claimed as a research contribution.

## 4. Reused sources and attribution

Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen’s equations for invariance pressure of control systems. *SIAM Journal on Control and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

- Formal identity and DOI were already verified in R20. Actual read body remains arXiv:2309.01628v3 (28 January 2025), with the R20 recorded scope: introduction/Theorems 1.1–1.4, §3.1 cost-threshold definitions, and the complete Proposition 3.5 proof; earlier §2/§§3.2–3.3 scope is reused. R21 does not newly claim a full formal-version comparison or another reading of that entire article.
- Its given-address stopping/pressure methods cover the familiar role of D and the stopped product count. They do not provide our arbitrary-input physical comparison. The root formula itself is not new.

Chen, Z., & Zhong, X. (2024). Invariance complexity and equi-invariability for control systems. *Journal of Mathematical Analysis and Applications, 539*(2), Article 128533. https://doi.org/10.1016/j.jmaa.2024.128533

- Formal project original and identity/ranges remain those recorded in R20/SOURCES.md: Definitions 2.10–2.11, Theorem 2.12 and its complete written proof; relevant Examples 4.1–4.2 from R18–R19. No new full review is claimed here.
- The actual finite-horizon outer catalogue is an existing definition, with n+1 constrained times in this project. Fixed-tolerance complexity does not establish the diagonal precision-rate separation.

Hutchinson, J. E. (1981). Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055

- Identity and the previously read author TeX version/ranges are retained from R20: §2.1 prefix families and the relevant §§5.1–5.3 statements/proofs. No formal scanning or new full reading is claimed.
- Complete stopping families, product weights and separation are classical. The finite binary stopped-count proof in R21 §4 is self-contained and does not depend on an unexamined theorem.

Csiszár, I. (1998). The method of types. *IEEE Transactions on Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546

- Reuse the previously checked bibliographic identity. Formal body still not read; no exclusion of its content is claimed. R21 supplies the elementary binomial and relative-entropy arguments it uses. Type counting is not a new technique.

R17 and R19 complete mathematical notes were restored and their adopted chain independently checked against the whole current manuscript. R06 §§2–6 were recovered for the actual-input, prefix-relative packing and compact typical-set mechanisms. The key relative-spacing architecture was **already** explicit in R06 §3.2; R21 does not claim it as a new method. The R19 matched identity R=P^β has been replaced by two derived comparisons and the actual conditional spacing check.

The Mauldin–Urbański formal-body gap remains as recorded in R20; it is not a premise of the present self-contained proof and no repeated retrieval was made. R09–R14 remain paused. No unpublished or unread source is used to certify novelty. No journal quartile, TOP label, or acceptance probability is asserted.
