# R06：原始来源、覆盖边界和实际阅读范围

2026-10-03。本轮只围绕 Theorem 6.1 的控制依赖收缩、有限时域精度及初始集假设核查。沿用 [R05/SOURCES.md](../R05/SOURCES.md) 的已读原件、身份和版本边界；不把复用记录写成重新全文审计。第三方全文不复制入仓库。

## 1. 复用原件与控制增长估计

**Kawan2013 — 正式原件。**

Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

项目原件 `07-pdf`，2,264,873 字节，290 页，SHA-256 `c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6`。身份沿用用户原件与 [Springer 书目](https://link.springer.com/book/10.1007/978-3-319-01288-9)。

R06 新增实际阅读：第 3 章引言；§3.1 Theorem 3.1 的假设、陈述及分解开头；§3.2 Definitions 3.1–3.2、Examples 3.1–3.2、投影体积准备段、Theorem 3.3 的完整陈述与证明及 Corollary 3.1（印刷 pp. 96–104）。没有重审书中全部引理、Selgrade 分解或附录 B 的证明；R05 已读目录和 outer 定义及 Lipschitz 覆盖范围继续有效。

逐项比较：本轮离散受控线性族属于该书的 homogeneous bilinear 框架，不能声称控制影响线性演化是新设定。Theorem 3.3 给出控制上优化的子丛体积增长下界；本轮所有输入在统一范数下收缩，其正秩子丛体积增长为负，非负化后不能给出正的精度谱下界。它没有包含本轮随 horizon 变化的 δ_n 匹配计数。其体积方法是已知工具；本轮首次偏离几何是需要另证的步骤。

**Da Silva–Kawan2016 — 作者稿复用，正式身份已核。**

Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97

[AIMS 正式条目](https://www.aimsciences.org/article/doi/10.3934/dcds.2016.36.97) 与既有 [arXiv:1408.2416v1](https://arxiv.org/abs/1408.2416v1)。本轮复读 §5.2 的完整结构假设（作者稿 pp. 38–39）、Theorem 5.7 的陈述和完整结尾证明（pp. 43–44）；未新审 volume lemma、shadowing 和周期逼近引理的全部证明，未认证正式版逐字差异。

已覆盖：控制选择与不稳定 Jacobian、周期轨道优化、正体积初始集的关系已有先例。本轮 Q 的正半径只能严格向内运动，不能近似到达更外半径，且不存在留在 Q 的正半径双向完整轨道；它不是该定理要求的双曲 chain control set 的闭包情形。不能把 R06 当该公式的反例，也不能把假设不适用本身计作重要性。

## 2. 稳定化精度与轨迹估计

**Colonius2012 — 沿用已核书目和作者稿。**

Colonius, F. (2012). Minimal bit rates and entropy for exponential stabilization. *SIAM Journal on Control and Optimization, 50*(5), 2988–3010. https://doi.org/10.1137/110829271

[SIAM 正式身份](https://epubs.siam.org/doi/10.1137/110829271)；实际已取得稿为作者 2011-12-18 机构稿，231,740 字节、23 页，SHA-256 `39f24d4ffbb2034b50bcdf37d6b7caa6b116bb06e18bd7e71978967e624f9b24`。复用 R05 对 §2 定义与 §4 Theorem 4.2 陈述、谱移位入口的实际阅读；本轮没有声称新读其余证明或取得正式 PDF。

已有指数稳定化和谱移位工具。该约束相对于原点、随当前时间衰减；R06 是实际 Q 的邻域，误差在一个 horizon 内固定。已读陈述不直接给出 (3.6) 的近似控制/停止树比较或近满面积成本分裂；这不是全篇未覆盖认证。

**Colonius–Hamzi2021 — 复用作者全文，保留正式版缺口。**

Colonius, F., & Hamzi, B. (2021). Entropy for practical stabilization. *SIAM Journal on Control and Optimization, 59*(3), 2195–2222. https://doi.org/10.1137/20M1367775

[SIAM 正式身份](https://epubs.siam.org/doi/10.1137/20M1367775)；已读 [arXiv:2009.08187v3](https://arxiv.org/pdf/2009.08187v3)，349,923 字节、27 页，SHA-256 `ea6348a73ec3bf37f55ed3a62e2dcca56c135d0cab167627b9b87f4d55cc59ac`。本轮复读 Definitions 2.1–2.2 的全时域量词与顺序极限、Theorem 3.4 的正体积假设及体积步骤、§5.1 Theorem 5.1 的完整陈述/证明与 Remark 5.2；其余使用 R05 已记录范围。

该文固定 ε 的 practical stabilization 与 R06 δ_n 的对角极限不同；§5.1 的固定 A、加性控制线性系统也不是本轮乘性控制分支。R05 记录的作者稿固定 ε 极限疑点不被当作正式期刊错误或本轮贡献。正式版差异和正式勘误状态未关闭；不重复已有失败 PDF 请求，不重复向用户索要。R06 的任何证明均不依赖疑点步骤。

**Liberzon–Mitra2018 — 本轮取得作者机构托管的期刊排版全文。**

Liberzon, D., & Mitra, S. (2018). Entropy and minimal bit rates for state estimation and model detection. *IEEE Transactions on Automatic Control, 63*(10), 3330–3344. https://doi.org/10.1109/TAC.2017.2782478

[作者机构原始文件](https://liberzon.csl.illinois.edu/research/obs-entropy-long.pdf)，1,283,368 字节、15 页，SHA-256 `1943d27d7e291343d455fb9378dcc1c1c1f10bbfe69cc31ddc95b5c3b2b18184`。首页图像确认 IEEE 卷期、正式分页与 DOI；末页为 3344，Crossref 同为 3330–3344。机构成果网页写 3330–3340，与 PDF 和 Crossref 不一致，本条采用后两者，未照抄该网页页码。

实际阅读：§II Assumption 1 与 Lemma 1 的矩阵测度界；§III 式 (5)–(6)、两种估计熵及 Theorem 1 的完整证明；§IV Proposition 2 完整证明、Remark 2、Proposition 3 陈述及末端体积比步骤。未认证其后实现算法或检测定理。

已有指数精度下的轨迹目录和增长界。其对象要逼近实际轨迹，时间零也有逼近误差；R06 不逼近初始状态，只为实际状态分配控制并保持 Q 的邻域。其谱移位不是本轮正面积分裂的现成证明，R06 也没有证明该文的信息传输实现结论。

## 3. 停止尺度与类型计数：明确归属已有工具

**Hutchinson1981 — 本轮读作者重排原文。**

Hutchinson, J. E. (1981). Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055

[作者 ANU 原文](https://maths-people.anu.edu.au/~john/Assets/Research%20Papers/fractals_self-similarity.pdf)，483,944 字节、27 页，SHA-256 `15ddd95b580b09439e1599551120a51ee5ffef43575f7f302ff35da63d3bf606`。首页明示为期刊文章的 TeX 重排版，调整格式并修正少数旧笔误，不能冒充期刊扫描件。DOI/作者/卷期/起页由 Crossref 核对，题名和完整页段由作者首页补齐；出版社网页本轮超时，不循环获取。

实际读首页说明、§2.1 的 secure/tight 前缀族、§5.1–5.3 的定义、陈述和证明；图像核对重排第 20 页停止尺度与有限重叠步骤。相似维数根式、按乘积尺度停止、分离集合的有限重叠均是先例。R06 的经典计数不主张首创；需新增证明的是实际控制容许离开 Q 时的首次分支错误界，及它对正面积初始集的影响。未读其余分形曲线或 currents 部分。

**Csiszár1998 — 仅方法归属的书目核对，不计全文审读。**

Csiszár, I. (1998). The method of types. *IEEE Transactions on Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546

本轮由 Crossref 的 DOI 记录核对身份；记录题名带有索引附注 “[information theory]”。未取得并审读该篇正式全文，不用其未读定理排除 R06。MATHEMATICS §4 的二项式类型界已给出短的自含证明；这里明确该计数方法已有，不另索原件来认证这一初等步骤。

## 4. 沿用的测度/压力与精确可行先例

以下书目和实际阅读范围复用 R03–R05 记录；本轮没有重新审计其全部证明，也不改变原件已取得的状态。

- Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862 — 项目正式 PDF 24 页，SHA-256 `23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363`。相关证明已在 R03 补核；R05 再读 Definitions 4.1/4.3。本轮没有新的测度熵结论。
- Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013 — 项目正式 PDF 31 页全文已于 R03 读完，SHA-256 `e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90`。R05 复读系统与最小目录定义；R06 不另造压力对偶，既有单位/共轭纠错不算新进展。
- Yao, S. (2026). *Invariance entropy in the dust* [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2607.02279 — 复用 R05 对官方 v1 §§3.1–3.4 的匹配图、淡出、固定前缀与 exact/approximate 分离证明范围；没有可核实期刊正式身份。晚期误差在固定容差下隐藏不是 P6 首创。R06 必须依靠正面积几何的匹配差异，不能只重述 exact/outer 分离。

## 5. 覆盖裁决的精确边界

| 对象或步骤 | 文献与本轮判断 |
|---|---|
| 控制依赖线性演化、体积增长、控制选择优化 | Kawan/Da Silva–Kawan 等已有；不能单独作为 R06 新意 |
| 精度影响信息成本、谱移位、有限时域轨迹覆盖 | Colonius/Liberzon–Mitra 等已有；误差对象和量词须逐项区分 |
| 停止前缀、相似维数根、熵与收缩之比、类型计数 | 经典内容；R06 的相关公式按已有方法应用处理 |
| 允许真实轨迹离开 Q 后，最优目录与收缩阈值树仅差多项式因子 | 在本轮明确审读的陈述/证明中未获得可直接套用的定理；R06 §3 自含证明。全库优先权未认证 |
| 同一系统、相同 exact/outer 端点下，任意近满面积紧集与含开集初始集的精度谱严格分裂 | R06 §§3–6 完成；区别于 R04 原子反例。既有多重分形方法与此受控实现是否已有等价发表仍须定向核验 |
| 非线性扰动鲁棒性、横向扩张分支、期刊档次 | 未证明/未认证，不用书目数量填补 |

本轮对 invariance entropy、contraction、precision、finite horizon、switched systems 等组合进行了有限查询，并以原始文件判断可见覆盖。检索有噪声，未命中不构成不存在证明。没有用摘要代替直接相关证明审读，也没有将正式版本缺口扩张为阻止自含数学推导的理由。本轮不需用户新增寻找原件。
