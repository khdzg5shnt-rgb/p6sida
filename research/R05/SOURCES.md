# R05：直接文献、版本和实际审查范围

2026-10-03（Asia/Shanghai）。以下分开记录数学原件、作者稿和正式版本身份。书目核对不等于正式全文已读；未读技术证明不用于认证其全部结论。本轮没有重开 NWH2022 / WHS2019 的获取任务，也未把所有原稿引文标为核实。

## 1. 用户已提供的原件

R03 的两篇期刊原件及 Kawan2013 原件继续使用。此次身份与字节采用已有文件，数学比较只复读所需部分；R03 的完整阅读和证明补核记录保留在 [R03/SOURCES.md](../R03/SOURCES.md) 与 [FULLTEXT_AUDIT.md](../R03/FULLTEXT_AUDIT.md)。

| 原件 | 实际文件 | 字节 / 页数 | SHA-256 |
|---|---|---|---|
| WHS2019 | 项目数据源 08-18m1197862.pdf | 400654 / 24，印刷页 310–333 | 23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363 |
| NWH2022 | 项目数据源 10-1-s2.0-S002203962200184X-main.pdf | 459673 / 31，印刷页 318–348 | e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90 |
| Kawan2013 | 项目数据源 07-pdf | 2264873 / 290 | c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6 |

**WHS2019 — APA**

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

正式身份：SIAM 出版社条目与已提供期刊 PDF；[出版社](https://epubs.siam.org/doi/10.1137/18M1197862)。R05 实际复读 Definitions 4.1/4.3：状态概率、局部 itinerary-cylinder 质量、积分以及 invariant partition 下确界。其余证明使用 R03 已记录范围，不声称本轮又全文审了一遍。

覆盖判断：该对象不是 R04 的 max_w μ(V_n(w))，也不是 R05 收紧环境误差的目录计数。全库首创性不能由这一区别单独认证；有限块、质量及覆盖方法属于先例。

**NWH2022 — APA**

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

正式身份：[ScienceDirect](https://www.sciencedirect.com/science/article/pii/S002203962200184X) 与 31 页期刊原件。全文已在 R03 阅读。本轮复读 §2.1 的系统公理、§2.2 的闭时域 spanning 与 minimum-cardinality catalogue 的加权上确界；R03 已审单位/共轭问题不重开。R02 原有“全文未取得”句子是保留的历史，不是当前状态。

覆盖判断：已有压力/输入值概率对偶不能因抽象形式相似就作为 R05 的计算。R05 不使用该论文的混合单位式，也不提出另一种压力对偶。

**Kawan2013 — APA**

Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

正式身份：[Springer 原始书目](https://link.springer.com/book/10.1007/978-3-319-01288-9) 与用户原件。R05 实际复读 §2.1 约印刷页 45–49 的 finite catalogue、拼接/次可加与 outer 先时间后误差定义，§4.1 约 pp. 108–110 的 tracking 和 Lipschitz 覆盖证明相关段落。R03 的共轭原始证明审查不重做，没有阅读全文 290 页。

覆盖判断：这些是目录量词、局部 Lipschitz 估计的既有出处。R05 的 δ_n 在一个 horizon 内固定、在 horizons 之间变化；传统 outer 的顺序极限不会自动给出整条对角精度谱。

## 2. 本轮直接相关的稳定化论文

**Colonius2012 — APA**

Colonius, F. (2012). Minimal bit rates and entropy for exponential stabilization. *SIAM Journal on Control and Optimization, 50*(5), 2988–3010. https://doi.org/10.1137/110829271

正式题名、作者、卷期页码、DOI 由 [SIAM](https://epubs.siam.org/doi/10.1137/110829271) 与 Crossref 核对。实际取得的是作者机构公开稿，日期 2011-12-18：

[作者原始稿](https://scwww.math.uni-augsburg.de/~colonius/downloads/2011_12_18DataRates_revised.pdf)，231740 字节，23 页，SHA-256 39f24d4ffbb2034b50bcdf37d6b7caa6b116bb06e18bd7e71978967e624f9b24。

实际阅读：§2 式 (2.9)–(2.10)、Definition 2.4、Remark 2.5，§4 Theorem 4.2 的完整假设/陈述和开头谱移位步骤。未逐行认证该论文剩余证明；正式 PDF 的机构入口未取得，不把作者稿叫正式 PDF。

比较：指数稳定化约束是随当前时间 t 衰减的原点目标界，误差在指数因子内；R05 是原始前向锥体 Q 的环境邻域，其 δ_n 只依赖总 horizon n 并在每个 k≤n 使用同一值。标准正谱移位是既有内容，不能作为新意。R05 的收缩情形斜率 α/c 及中间时刻瓶颈不由该已读陈述直接给出。尚未完成正式版全文差异认证。

**Colonius–Hamzi2021 — APA**

Colonius, F., & Hamzi, B. (2021). Entropy for practical stabilization. *SIAM Journal on Control and Optimization, 59*(3), 2195–2222. https://doi.org/10.1137/20M1367775

正式身份：[SIAM 书目及摘要](https://epubs.siam.org/doi/10.1137/20M1367775)、Crossref 的正式版 DOI/卷期/页码/全文链接。实际全文是 arXiv:2009.08187v3（2021-02-03，稿面日期 2021-02-04）：

[arXiv 作者稿](https://arxiv.org/pdf/2009.08187v3)，349923 字节，27 页，SHA-256 ea6348a73ec3bf37f55ed3a62e2dcca56c135d0cab167627b9b87f4d55cc59ac。

实际阅读：摘要/引言、§2 Definitions 2.1–2.2 与 Remarks 2.4–2.6；§3 Theorem 3.1 的假设与参考控制/Lipschitz 上界构造相关步骤；Theorem 3.4 完整陈述与证明；§4.3 线性反馈比较；§5.1 Theorem 5.1 完整陈述与证明及 Remark 5.2。没有阅读并认证所有后续非线性例和附录。PDF 第 12 页图像用于交叉检查公式。

直接差别：实用稳定化式 (2.3) 使用 ζ(d(x₀,Λ)+ε,t)+ε，先固定 ε 后取时间极限；R05 的 δ_n 随总时域变化，且约束仍为整个 Q，不能把 Λ=Q、ζ 任意代入就得到 Theorem 5.1 的匹配律。

**必须保留的版本疑点。** 作者稿 Theorem 3.4(ii) 的第 12 页出现如下极限步骤：固定 ε>0 时将 τ^{-1}ln[e^{-aτ}M(κ₀+ε)+ε] 的极限写成 −a。独立算得该极限为零。图像确认这不是文本抽取漏掉指数；κ₀ 是该文初始距离界，不是 R05 的扰动范数。因而不能依此作者稿步骤排除 R05 或认证实用稳定化的所有谱移位式。正式期刊版是否修正、是否存在正式勘误尚未关闭，不能把作者稿问题直接定性为期刊正式结论错误。

获取/核验边界：出版社 PDF 返回 403，机构 OPUS 的 deliver/files 两种合法公开入口返回 502；已记录，不循环。ResearchGate 作者上传全文仍标明同一 arXiv v3，不能冒充正式版。对准确 DOI/题名加 correction、erratum 的有限查询未得到可核实正式修正条目；这不是“证明没有勘误”。已另发独立消息请用户补找正式 PDF。R05 自含证明不依赖这一步，也不把本疑点另立为主贡献候选。

## 3. 专业期刊及结构先例

**Colonius2018（ETDS）— APA**

Colonius, F. (2018). Metric invariance entropy and conditionally invariant measures. *Ergodic Theory and Dynamical Systems, 38*(3), 921–939. https://doi.org/10.1017/etds.2016.72

正式身份：[Cambridge 原始条目](https://www.cambridge.org/core/journals/ergodic-theory-and-dynamical-systems/article/abs/metric-invariance-entropy-and-conditionally-invariant-measures/18CB177E231E9164002893D0BB18B851)、Crossref。在线发布 2016-10-20，卷期年份为 2018，APA 使用后者。

实际原文：[作者机构稿，2016-04-26](https://scwww.math.uni-augsburg.de/~colonius/downloads/2016_04_26MetricInvarianceEntropy.pdf)，217458 字节，18 页，SHA-256 67797077a5842ab97df2663cf869c44875d88d7759b293bba45c7cac726146aa。

实际阅读：§1–2 的 conditionally invariant / quasi-stationary measure 定义及支持边界相关证明；§3 Definition 3.1 的 invariant partition 与 admissible words，Definitions 3.5–3.6、3.9–3.11，Theorem 3.12 的共轭证明与 Definition 3.13/Theorem 3.14 的目录接口。未认证全篇技术引理，未取得正式 PDF 与作者稿的完整逐字差异。

覆盖判断：条件不变测度和实际受控状态共轭是已有研究；“所有不变提升测度在 apex”不等于所有这些控制测度熵为零。该文是专业期刊贡献形式的先例，不能据其刊名替 P6 评级。

**Da Silva–Kawan2016（DCDS）— APA**

Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97

正式身份：[AIMS 原始条目](https://www.aimsciences.org/article/doi/10.3934/dcds.2016.36.97)。沿用已取得 [arXiv:1408.2416v1 作者稿](https://arxiv.org/abs/1408.2416v1)，没有重复获取。

实际复读：§5.2 的双曲 chain control set、内点可达性与每输入唯一全时状态的假设，Theorem 5.7 的公式陈述与结尾证明，以及 graph lift 的说明。没有在 R05 重审 volume lemma/shadowing 的所有技术证明，不认证全部正式版差异。

覆盖判断：共轭为输入图式仍需保留不稳定 Jacobian 的思想已经存在。P6 的正半径不存在全时可行轨道，R=arsinh 的 apex 又有中心导数，不能直接套用该公式。假设不适用只是非覆盖证据，不能单独作为独立重要性依据。

**Kawan 当前 v5 — APA**

Kawan, C. (2026). *Control of chaos with minimal information transfer* (Version 5) [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2003.06935

[arXiv 官方记录](https://arxiv.org/abs/2003.06935) 确认最初 2020、最新 2026-09-20 v5；[实际正文](https://arxiv.org/html/2003.06935v5)。本轮读取摘要、相关引言、§4.2 的条件熵/pressure 解释、A1–A3 及 Theorem 4.7 陈述。不声称阅读全文 v5，也未确认期刊正式版。

覆盖判断：不稳定体积增长减内部条件熵以及全时双曲的几何接口已有先例；P6 不拥有这个一般机制的新证明。R05 不把裸图式与该保留 cocycle 的理论混为一谈。

**Yao2026 — APA**

Yao, S. (2026). *Invariance entropy in the dust* [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2607.02279

[arXiv 官方记录](https://arxiv.org/abs/2607.02279) 确认 2026-07-02 v1，无在该记录中可核实的期刊正式身份；[原始正文](https://arxiv.org/html/2607.02279v1)。实际复读 §§3.1–3.4，匹配图、指数淡出、固定前缀目录、Theorem 1 的精确/近似熵分离及相应估计；不重做其整个构造认证。

覆盖判断：信息成本可以来自精确可行几何，晚期符号错误可在固定容差下隐藏，以及前缀截断法，都不是 P6 首创。R05 需要以全精度律、真实正面积约束及非线性统一匹配证明为新增内容，不能只写“正成本而没有状态混沌”。当前正文 Theorem 1 位于 §3.4，不机械沿用原稿的 Theorem 3.1 编号。

## 4. 精确的覆盖结论与残余缺口

| 内容 | 已有覆盖/方法 | R05 状态 |
|---|---|---|
| finite catalogue、拼接、outer 顺序极限、Lipschitz/体积估计 | Kawan2013、稳定化理论等 | 既有工具，明确归属 |
| 压力对偶、分划质量熵、条件不变控制测度 | NWH/WHS/Colonius | 已有对象；未另造普适变分原理 |
| exact 成本与内部动力复杂度不同、丢失几何信息危险 | 双曲 Jacobian 理论、Yao 薄几何 | 概念已有先例，S1 不据此独占重要性 |
| 原稿固定 first jet 非线性 exact/outer/tracking 端点 | 项目已有完整证明；组合优先权仍须审查 | 本轮重推，不计作新增 |
| 任意 δ_n→0、给定极限指数 γ 的非线性实际时间极限及早期/末端匹配律 | 本轮所读直接原文未提供同量词结论或直接套用定理 | Theorem 5.1 新增于项目；全库首创性未认证 |
| 阶段稿录用、“一区/TOP”、四大重要性 | 没有可据以认定的证据 | 不作肯定判断，不给成功率 |

必须先关闭 Colonius–Hamzi2021 的正式版本差异，再加强“确未覆盖”的发表叙述。其余作者稿与正式版的未审差异仍明确保留，若影响主定理覆盖则按实际需要补审。不能用搜索未命中证明首创性，也不能因这项具体版本缺口而否认已经给出的自含数学证明。

第三方论文全文不复制进仓库；这里只保存书目、实际阅读范围、来源身份及覆盖判断。
