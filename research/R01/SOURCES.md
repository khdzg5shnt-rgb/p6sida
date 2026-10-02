# R01：关键文献、版本与覆盖核查

检索截至 2026-10-02（UTC）。依据出版社、arXiv 正式记录、作者提供的论文全文或学位论文原件；没有把 P6 自述或二手论文摘要当作原创性证据。下面只给实际核实过的书目信息。全文未取得、只读相关部分、只读摘要，均分别记录。未检索到勘误不等于不存在勘误。

## 阅读范围及对升级目标的影响

| 文献 | 实际取得和核查范围 | 核实的假设、定义或结论 | 与 P6 / R01 的关系及缺口 |
|---|---|---|---|
| Kawan，2009 学位论文 | 德国国家图书馆全文；读 Definition 3.1.1、Theorem 4.1.2、Proposition 4.1.9、Theorem 4.1.10 的定义与相关陈述 | tracking 用可行参考状态和输入对；线性谱公式需要其控制/约束条件和正体积初始集；不齐次双线性结果另有自身条件 | 定义及谱/体积工具已有先例；未逐行审完 177 页全文，未确认缩时域上界的优先权 |
| Da Silva & Kawan，2016 | 出版社元数据；作者版 arXiv:1408.2416；读 control set 定义、双曲图性质及 Theorem 5.7 和证明 | 双曲 chain control set、非空内部、相应局部可达/Lie rank 条件及 singleton input fibers；完整时间提升可与输入移位共轭，熵仍由不稳定 Jacobian 给出 | 直接说明“提升与输入移位共轭”并非新现象。P6 满锥体是前向约束，不能当成该文的 full-time 控制集；本轮未逐行审完作者版全部证明，也未完成作者版与期刊版逐页差异 |
| Kawan & Da Silva，2018 | 出版社元数据及摘要；arXiv:1711.01181v2 的主定理 2.1 和相关定义 | compact all-time controlled invariant Q；连续不变 splitting `E+⊕E0-`，`E+` 统一扩张、`E0-` 至多子指数增长；隔离、输入纤维 lower semicontinuity；下界含不稳定 determinant 和相对压力/条件状态熵 | 已有“总不稳定性与内部复杂度分开”的结构解释。不是所有系统的等式。前向锥体的正体积初始集不在 full-time core 内，不能直接套用该公式 |
| Kawan，arXiv:2003.06935v5 | 正式版本记录；v5 HTML 中系统设定、双曲/隔离/lsc 条件、§4.2 压力下界、§4.6–4.7 相关证明与条件熵、achievability 的范围 | 双向离散控制系统、光滑可逆状态映射、紧连通输入空间；compact all-time invariant hyperbolic Q、isolated lift、lsc fibers、正体积 K；下界为 `infμ[∫log J+ dμ−hμ(state|input)]`；一般上界仍未给出，仅两个极端情形得到匹配 | 原稿引用的是 v4（2021-05-19）；最新为 v5（2026-09-20）。有限离散字母不满足该设定的连通输入条件；中性径向 P6 也不是统一双曲 full-time Q。不能把该论文当作未有人解释信息成本/内部复杂度的证据 |
| Yao，arXiv:2607.02279v1 | 正式版本记录；主系统、薄图构造、finite matching、fading estimate、主要熵计数证明（§3、§4.2–4.5） | 连续时间 `zdot=−z, cdot=0, ydot=−y+zu`，Cantor 指令图约束；exact/strict 计数 `2^ceil(T)`、熵 `log 2`，固定容差近似熵为零 | 最接近的新竞争预印本确实存在，2026-07-02 v1。由其方程独立推得任意可行两轨道距离趋向 `|c1−c2|`，故“正 exact 成本且无状态 Li–Yorke”这个弱命题不能作为 P6 的首创。它未给 P6 的正 outer/tracking 联合现象；本轮没有审完其全部 Hausdorff 扰动附录 |
| Wang, Huang, & Sun，2019 | SIAM 元数据、摘要；全文付费，公开全文检索未取得 | 摘要确认两种 measure-theoretic invariance entropy、控制共轭不变性及指定情形的变分原理 | **未核验其完整定理假设与证明**。不能由 P6 的条件 KS 熵为零推断这些熵为零。此缺口阻止全面原创性认证 |
| Nie, Wang, & Huang，2022 | ScienceDirect 出版条目及卷目录的索引结果，另由 SIAM 2025 论文参考文献交叉核对 DOI/页码；全文未取得 | 只能确认书目信息、研究主题为测度不变熵及变分原理 | **定理覆盖未核验**。不根据题名排除其与拟议一般原则的重合 |
| Colonius，2018 | 出版社元数据；arXiv:1705.08658 作者全文相关 §2 定义、Theorems 2.15–2.16、§3讨论 | 先给输入值分布 ν 和 quasi-stationary η，`μ=ν^N×η` 条件不变；优化 invariant `(Q,η)` partitions，定义并非普通 lift KS entropy；有 `hμ(Q)≤hinv(Q)` | 历史上的“measure-theoretic invariance entropy”已有不同定义。R01 的 no-go 不否定其可测状态变换不变性或 partition 优化。其后全部控制集定理未审完 |
| Zhang，2006 | Cambridge/Wiley 元数据、摘要；论文全文未取得 | 摘要确认 positive conditional entropy 推出相对渐近对与混沌 | **尚未逐项验证原稿所列 Theorems 3.9、3.10、4.2 和 Lemma 4.3**；原稿关于 homeomorphism 的范围描述未以全文完成认证。P6 本轮独立证明条件状态熵为零，故不能用正条件熵的入口 |
| Blanchard, Glasner, Kolyada, & Maass，2002 | 出版社 DOI 元数据；Kolyada 作者全文，读 compact continuous surjection 的设定、Li–Yorke 定义及正熵结论 | 正紧状态系统 topological entropy 给不可数 scrambled set；必须在实际状态映射/实现因子上有正熵 | R01 零成本反馈例在状态 Cantor 子系统上真的实现双符号满移位，故可以使用；P6 的输入满移位不能替代该假设。未审完该文所有后续结构定理 |
| Liu, Tan, & Zhang，2024 | ScienceDirect 元数据与摘要；arXiv:2207.08505 最新 v3 的摘要/版本记录；PDF读取失败 | injective continuous infinite-dimensional RDS，底为 invertible ergodic Polish system，invariant random compact K 有正状态 topological entropy；得到沿任意趋∞整数序列的 mean Li–Yorke | 输入熵并非其正状态熵条件。**全文证明和更细假设未审** |
| Yang, Chen, Yang, & Zhou，2025 | SIAM 元数据；arXiv:2309.01628v3 主定理、partition/cylinder 定义及相应变分证明入口 | 上容量和 Pesin–Pitskel invariance pressure 的 Bowen equation；Theorem 1.4 要求 clopen invariant partition、compact nonempty K、正连续权重；测度取 `M(Q)` 且 `μ(K)=1`，并非必须 F-invariant | 原稿连通锥体只有平凡有限 clopen 分划；一般 Borel 分划不能自动满足此条件。R01 恢复有限可行覆盖的恒等式与该文压力定理不同，不能把恒等式包装成新变分原理 |
| Chen, Huang, & Zhong，2026 | ScienceDirect 元数据与摘要索引 | invariance entropy dimension、α-invariance entropy 及对应局部测度熵的变分/逆变分原则，针对零不变熵系统的复杂度尺度 | 文献确实存在，DOI 年份 2025、卷年份 2026；**全文具体假设与定理覆盖未审**，不按题名排除 |
| Sibai & Mallada，2026 | 出版社条目、作者大学出版记录与作者网站 18 页全文；读 Definitions 4–5 和 recurrence catalogue 定义 | 每个初始状态存在一个控制使轨道在每个长度 τ 时间窗返回 Q；catalogue 计数刻画该控制任务；返回 Q 不等于返回初始点，不等于两轨道 proximality | 原稿把 recurrence entropy 当补充背景合理；此复现定义本身不产生状态 scrambled set。全文全部上下界和 finite alphabet 定理未逐行审完 |
| Colonius & Fabbri，2026 | Springer 出版全文、设定与 control set 的相关 Proposition 29 | 非自治 control-affine 系统、紧凸输入范围、最小连续外部底流；多个 skew product 与可达/chain controllability 关系 | 正式发表，online 2025-12-22、卷年份 2026；不是待审新预印本。未给出用输入 entropy 替代状态混沌的结论；本轮未审完全文全部控制集定理 |

### 单位、版本与勘误记录

P6 和 R01 用自然对数；Kawan v5 和 Sibai–Mallada 的信息速率用以 2 为底的对数。比较公式时需统一单位：自然单位的熵率等于 bit 熵率乘以 `ln 2`。数值单位差不构成新的数学现象。

Kawan v5 的当前文本必须用于后续比较。此轮 v4 PDF 获取失败，未作完整 v4/v5 diff，不能声称版本变化不影响 P6。Yao 的正式历史目前只有 v1。arXiv:1711.01181 当前为 v2（2018-05-09），2309.01628 当前为 v3（2025-01-28），2207.08505 当前为 v3（2022-11-29）。

核查上述主要出版社条目、arXiv 历史并检索 correction/erratum，未确认与本轮使用的主结论有关的独立勘误。作者出版页搜索摘要曾显示未定位的 “Erratum” 字样，但回读页面未定位到对应项目，不能推定属于任何这里的论文。各原件版本差异仍按表内范围保留缺口。

原稿 Yao 引用写作 “Theorem 3.1”，当前 HTML 主结果显示为 Theorem 1，并位于 §3；后续正文应按版本直接核对引用编号。原稿保持原样，未在 `original/` 修订。

## 已核实的 APA 引用

Blanchard, F., Glasner, E., Kolyada, S., & Maass, A. (2002). On Li-Yorke pairs. *Journal für die reine und angewandte Mathematik, 547*, 51–68. https://doi.org/10.1515/crll.2002.053

Kawan, C. (2009). *Invariance entropy for control systems* [Doctoral dissertation, Universität Augsburg]. German National Library. https://d-nb.info/1000462749/34 （本轮未核实论文专属 DOI，不编造。）

Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97

Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class of partially hyperbolic sets. *Mathematics of Control, Signals, and Systems, 30*, Article 18. https://doi.org/10.1007/s00498-018-0224-2

Kawan, C. (2026). *Control of chaos with minimal information transfer* (Version 5) [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2003.06935 （初次上传 2020；这里标注所核查的 2026-09-20 v5。该 DOI 是 arXiv DOI，不是期刊 DOI。）

Yao, S. (2026). *Invariance entropy in the dust* (Version 1) [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2607.02279 （2026-07-02；arXiv DOI。）

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

Colonius, F. (2018). Invariance entropy, quasi-stationary measures and control sets. *Discrete and Continuous Dynamical Systems, 38*(4), 2093–2123. https://doi.org/10.3934/dcds.2018086

Zhang, G. (2006). Relative entropy, asymptotic pairs and chaos. *Journal of the London Mathematical Society, 73*(1), 157–172. https://doi.org/10.1112/S0024610705022520

Liu, C., Tan, F., & Zhang, J. (2024). Mean Li-Yorke chaos along any infinite sequence for infinite-dimensional random dynamical systems. *Journal of Differential Equations, 403*, 548–575. https://doi.org/10.1016/j.jde.2024.05.035

Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen’s equations for invariance pressure of control systems. *SIAM Journal on Control and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of invariance entropy dimension. *Journal of Differential Equations, 453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

Sibai, H., & Mallada, E. (2026). Recurrence of nonlinear control systems: Entropy, bit rates, and finite alphabet controllers. *Nonlinear Analysis: Hybrid Systems, 59*, Article 101649. https://doi.org/10.1016/j.nahs.2025.101649

Colonius, F., & Fabbri, R. (2026). Nonautonomous control systems and skew product flows. *Journal of Dynamical and Control Systems, 32*, Article 3. https://doi.org/10.1007/s10883-025-09750-3

## 可回读的一手正文入口

- [Kawan v5 正文](https://arxiv.org/html/2003.06935v5)；[正式版本历史](https://arxiv.org/abs/2003.06935)。
- [Yao v1 正文](https://arxiv.org/html/2607.02279v1)；[正式版本历史](https://arxiv.org/abs/2607.02279)。
- [Da Silva & Kawan 作者版](https://arxiv.org/pdf/1408.2416)；[部分双曲作者版](https://arxiv.org/pdf/1711.01181)。
- [Colonius 作者版](https://arxiv.org/pdf/1705.08658)；[Yang 等作者版](https://arxiv.org/pdf/2309.01628v3)。
- [BGKM 作者全文](https://www.imath.kiev.ua/~skolyada/LY.pdf)。
- [Sibai & Mallada 作者全文](https://mallada.ece.jhu.edu/pubs/2026-NAHS-SM.pdf)。
- [Nie 等正式卷目录](https://www.sciencedirect.com/journal/journal-of-differential-equations/vol/321/suppl/C)。

## 原稿其余条目的状态

原稿共 28 条引用。`CK2009, K2011, KStrict2011, CH2021, KD2016, CST2023, CCS2021, ZCH2021, ZC2023, CZ2024, WH2024, ZH2025, ZHZ2023` 本轮未完成独立全文核验。不得把它们的原稿元数据复制后标作本轮已核实 APA；也不得用原稿关于其范围的说明排除竞争覆盖。Lie-group 公式、稳定化 data-rate、复杂度与不确定控制相关的新颖性风险仍未全面消除。

优先缺口：WHS2019 与 NWH2022 原文的定义、控制共轭关系、变分原则假设及所优化测度类别；其次核对 Zhang2006 原稿指定编号与 Kawan 完整版本差异。只有补齐这些，才可能负责任地区分 R01 的结果究竟是已知事实的具体实现、可发表的独立限制定理，还是更深一般问题的可靠起点。
