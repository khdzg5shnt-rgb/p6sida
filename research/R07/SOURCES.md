# R07：直接来源、阅读范围与覆盖边界

2026-10-04（北京时间）。本轮只围绕指定扩张分支的精度成本。复用 [R06/SOURCES.md](../R06/SOURCES.md) 与 [R05/SOURCES.md](../R05/SOURCES.md) 的原件、身份及已读范围；未把复用写成再次全文审计，未重新获取先前失败的全文。第三方全文不复制入仓库。

## 1. 新用的循环移位方法：经典工具

**Dershowitz–Zaks1990，作者机构托管的期刊排版扫描全文。**

Dershowitz, N., & Zaks, S. (1990). The cycle lemma and some applications. *European Journal of Combinatorics, 11*(1), 35–40. https://doi.org/10.1016/S0195-6698(13)80053-4

- [作者原始 PDF](https://www.cs.tau.ac.il/~nachumd/papers/CL.pdf)，271,312 字节，6 页，SHA-256 `5d830ea85a471d2bdeace1c7cd633fcd92900e7d6933b655a741f35be06caee3`。图像核对首页期刊题名/年份/卷号/页段及第 36 页路径证明；PDF 完整到第 40 页。
- DOI、作者、卷期、页段由 Crossref 的 DOI 登记和[作者机构成果页](https://cris.tau.ac.il/en/publications/the-cycle-lemma-and-some-applications/)交叉核对。ScienceDirect 条目检索命中，直接打开 403；已有期刊扫描及身份核对，不再重试该入口。
- 实际审读 §1 的循环引理、§§1.1–1.2 两个完整证明、§1.3 的非整数/实数增量归属说明（pp. 35–37），以及 pp. 39–40 相关参考书目；没有核验 §2 树高应用的全部推导。

该文整数步版本计数精确的有效循环位置；§1.2 已使用重新选择路径起点的机制。R07 只需更弱的实数增量事实：总和非负时，在前缀最低点切开可以得到全部前缀非负的一个旋转。因此 MATHEMATICS §5 给出直接证明，没有把整数精确计数公式套到 `ln(3/2),−ln2`，也不宣称新循环引理。

**Dvoretzky–Motzkin1947，仅历史原始归属与书目核对，不计全文已读。**

Dvoretzky, A., & Motzkin, Th. (1947). A problem of arrangements. *Duke Mathematical Journal, 14*(2), 305–313. https://doi.org/10.1215/S0012-7094-47-01423-3

作者/题名/卷期/日期/DOI 由 Crossref 核对；页段由上述 Dershowitz–Zaks 期刊原文 reference 9 核对，Crossref 当前返回未列 page。DOI 网页本轮无法打开，未取得并审读 1947 全文，未循环下载。这里只注明历史来源；实数旋转步骤自含，不依赖未读定理，不要求用户为此找原件。

## 2. 控制增长下界与精度成本

**Kawan2013，复用项目正式书籍原件。**

Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

项目原件 `07-pdf`，2,264,873 字节，290 页，SHA-256 `c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6`。[Springer 正式条目](https://link.springer.com/book/10.1007/978-3-319-01288-9)本轮再次核对身份。

本轮复读 §3.2 Definitions 3.1–3.2、Examples 3.1–3.2、Theorem 3.3 完整陈述/证明及 Corollary 3.1（相关印刷 pp. 96–104）。投影体积准备引理沿用 R06 已读范围，未重新审计附录 B 或全书。离散受控线性族在其 homogeneous bilinear 框架中，不能以切换收缩/扩张作为设定首创。

该下界对输入取 inf 的增长率；本轮允许 `1∞`，对应矩阵特征值 `1/4,1/2`，在这个固定输入上任何正秩不变子空间的体积增长率均为负。因此该具体公式不能直接给出 R07 的正临界精度下界。它研究的目录量、固定 Q 和极限也没有自动包含 `δ_n=2^(−n)` 下的首次偏离见证论证。这是对已读公式的适用判断，不是宣布一般体积方法无效。

**Liberzon–Mitra2018，复用作者机构托管的期刊排版全文。**

Liberzon, D., & Mitra, S. (2018). Entropy and minimal bit rates for state estimation and model detection. *IEEE Transactions on Automatic Control, 63*(10), 3330–3344. https://doi.org/10.1109/TAC.2017.2782478

[原始 PDF](https://liberzon.csl.illinois.edu/research/obs-entropy-long.pdf)，1,283,368 字节，15 页，SHA-256 `1943d27d7e291343d455fb9378dcc1c1c1f10bbfe69cc31ddc95b5c3b2b18184`。正式分页和 DOI 的图像/Crossref 核对沿用 R06；未照抄机构网页的错误末页 3340。

本轮复读 §III 式 (5)–(6) 的全时域精度量词、Theorem 1 的陈述与直接证明，以及 §IV Proposition 2 的完整证明和 Remark 2（pp. 3332–3334）；其余 Lemma/体积/算法审查范围沿用 R06，不新增认证。

已有指数精度、轨迹目录和谱移位方法。其误差为轨迹相互逼近、随当前时间衰减；R07 为给实际初态分配控制，在同一 horizon 内使用固定的 `2^(−n)` 邻域约束。其线性谱移位结论并非本轮全控制可行性下界，但也不能把“精度造成正成本”本身说成新现象。

## 3. 其余直接背景：复用范围，不重复审查

| 核实后的 APA 与 DOI | 版本、范围及本轮边界 |
|---|---|
| Colonius, F. (2012). Minimal bit rates and entropy for exponential stabilization. *SIAM Journal on Control and Optimization, 50*(5), 2988–3010. https://doi.org/10.1137/110829271 | 2011-12-18 作者机构稿；复用 R05–R06 的 §2 定义与 §4 Theorem 4.2 陈述/谱移位入口。没有取得正式 PDF 或新增全篇覆盖认证。 |
| Colonius, F., & Hamzi, B. (2021). Entropy for practical stabilization. *SIAM Journal on Control and Optimization, 59*(3), 2195–2222. https://doi.org/10.1137/20M1367775 | 已读 arXiv:2009.08187v3；复用 Definitions 2.1–2.2、Theorem 3.4 及 §5.1 Theorem 5.1/Remark 5.2 的 R05–R06 范围。固定误差与对角精度的量词不同。正式 PDF 差异/勘误缺口保留，不重试、不重复索要；R07 不依赖既有疑点。 |
| Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97 | 作者稿 arXiv:1408.2416v1，正式 AIMS 身份已核；复用 R06 对 §5.2 完整假设和 Theorem 5.7 结尾证明的范围。Q 的半径沿正向严格减小，不具该内点双曲 chain control set 的完整近似可控性；不把此假设差别本身当新意。 |
| Hutchinson, J. E. (1981). Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055 | 作者 TeX 重排修订稿，非期刊扫描。复用 R06 的 §2.1 前缀族与 §§5.1–5.3 停止尺度/分离计数。乘积尺度停止是已有工具；本轮只换用了能容许横向扩张的见证族。 |
| Csiszár, I. (1998). The method of types. *IEEE Transactions on Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546 | 仅沿用 R06 已核 Crossref 书目，不计全文审读。二项式界在 R07 §7 自含证明。 |

WHS2019 / NWH2022 的正式原件及既有阅读记录继续有效：

- Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862 — R03 已补核相关证明，R07 不新增测度熵命题。
- Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013 — 31 页全文已取得并在 R03 审读，绝不重新标为未取得。R07 不依赖其压力变分公式，不重新开既有纠错。

两篇 SHA-256、版本和详细审查范围见 R03/FULLTEXT_AUDIT、R03/SOURCES 及 R06/SOURCES。本轮的普通计数概率不是这些论文的受控不变测度对象，不以换名生成新变分结论。

## 4. 逐项覆盖裁决

| 本轮内容 | 已有方法或新增接口 |
|---|---|
| 控制依赖线性演化、收缩和扩张、体积增长、指数精度 | 已有理论背景，不能作为单独新意。 |
| 二进制编码、精确前缀接尾部、首次偏离带宽 | 仓库 R06 已有，参数适用条件重新核验。 |
| 循环最低点、类型数量、停止树概率权重 | 经典方法的具体应用，完整归属并自含证明。 |
| 临界频率词经旋转后，每个前缀横向乘积至少为一；任意近似控制只能覆盖其中 O(n) 个实际初态 | R07 新完成的控制几何接口，取代失效的统一停止圆柱比较。已读直接陈述没有提供可直接代入的同量词结论；全库优先权未认证。 |
| 指定系统在 `δ_n=2^(−n),K=Q` 下精确率及总目录多项式比较 | 本轮新证明的完整结果，限于一个明确边界案例；不主张普适扩张分支理论或新的压力对偶。 |

本轮有限检索围绕 invariance entropy、switched/expanding branches、precision，以及循环移位原始归属；新方法原文和已存控制原文用于直接核验。检索未命中不等于证明无人发表。没有需要用户新增寻找的原件，也没有因正式版本缺口搁置自含证明。
