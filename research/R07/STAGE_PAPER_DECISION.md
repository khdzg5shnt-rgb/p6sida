# 阶段论文主贡献整合与成稿裁决

2026-10-04（北京时间）。本文件记录用户明确授权的“阶段论文主贡献整合与条件式成稿”，不启动 R08。恢复基线及开始时最新 main 均为 `b71661c178668a93328ce9742aa7d80c19b72539`。实际仓库为 `khdzg5shnt-rgb/p6sida`；指令中的 `khdzzg5shnt-rgb` 是多一个 z 的历史转写错误。未发现适用 AGENTS.md 或更晚完成项。

## 1. 裁决：通过成稿，形成可评估稿件

拟收入论文的证明链经重新推导，未发现需要撤下的结论。现有结果足以支持一篇范围有限、具有独立专业用途的阶段论文。唯一主线是：**实际受控可行性怎样使初始集几何影响精度—时域成本**。最有分量的结果是 R06 的同系统成本分裂，不是 exact/outer 分离本身，不是停止尺度公式或压力对偶。

已完成唯一英文稿：

- [`paper/P6_PRECISION_COST.tex`](../../paper/P6_PRECISION_COST.tex)
- [`paper/P6_PRECISION_COST.pdf`](../../paper/P6_PRECISION_COST.pdf)

题名：*Precision-dependent invariance costs and the geometry of initial sets*。PDF 为 14 页，页数由内容自然决定。正文含完整假设、证明、两个必要例子、直接文献比较和局限；不写研究轮次或审计历史，不把未解猜想列作贡献。作者栏沿用原稿空白，不擅自填写姓名、单位或联系资料。

这次实质新增是经过裁决的完整论文及明确的贡献边界，没有另行获得超过 R05–R07 的一般数学定理。不能把成稿、编译或本文件当作又一次数学突破。

## 2. 主结果及定理关系

所有目录都为实际初始状态分配控制，使用欧氏距离；一个 horizon 内使用同一容差，要求时刻 0,…,n 全部合格。允许实际轨迹离开 Q，不用参考点替换初始状态。

| 稿件位置 | 完整主张的要点 | 作用及贡献归属 |
|---|---|---|
| Theorem 2.2、Proposition 3.1、§§3–5 | 二进制平面系统 `F_i(s,z)=(ρ_i s,ρ_i(2z+v_i s))`，`v_0=1,v_1=−1`，`0<ρ_i<1/2`。每个含开集紧初始集的任意对角精度序列都有率 `F(γ)=max_p H(p)min(1,γ/χ(p))`；每个 ε 有一个面积大于 `1−ε` 的紧集，对所有精度序列都有率 `G(γ)=ln2 min(1,γ/c̄)`。不同收缩率时在 `0<γ≤min(c_i)` 严格分裂；相同 exact/outer 端点仍为 ln2/0。 | 唯一主结果。其用途是给出“正面积能否替代非空内部”的精确边界反例，且不是零测度或原子造成的差别。任意近似控制与停止树的比较、近满面积集上每个任意控制的面积上界，是需要实证的几何步骤。 |
| Theorem 6.1、§6 | R05 的共同 R(s)、有限字母严格内向余量、二阶小横向非线性项。在其完整假设下，对每个正面积紧 K，率为 `max_{0≤a≤1}[a ln q−(a(−lnρ)−γ)_+]`。允许 γ=0、∞，精度序列不要求单调。 | 比较定理：说明正面积统一律在哪个独立假设类成立。正文保留所有实际使用条件。它与二进制无余量模型互不包含，不能称 R06 为它的无条件推广。 |
| Proposition 7.1、§7 | 固定 `ρ_0=3/4,ρ_1=1/4,K=Q,δ_n=2^(−n)`，率为 `H(ln2/ln3)`；真实目录与所构造停止目录至多差 `C n^3`。 | 补充案例。循环移位本身经典；新增接口是临界词实际初态对任意近似控制的 `3n+1` 覆盖上界。该系统存在发散输入，不保留所有输入一致收敛，不宣称一般扩张精度谱。 |

文内 Example 2.3 取 `ρ_0=1/4,ρ_1=1/16,δ_n=2^(−n)`，给出精确差别 `lnφ/2 > ln2/3`，其中 `φ=(1+√5)/2`。Example 6.3 用实际满足假设的 tanh 非线性项说明决定下界的时间可以是 `n/2`，只检查终点会丢掉正成本。

原稿主轴是锥体可行性转移、谱率及熵与状态收敛的分离。阶段稿新增的数学内容来自 R05–R07：完整对角精度律、控制依赖收缩下的初始集成本分裂、扩张分支的匹配案例。没有重启纯提升公式或共同输入混沌；原稿的高维叙述、tracking、提升和文献纠错均不纳入这篇稿件的主贡献。

## 3. 实际核验的证明链

完整读取 CURRENT.md、R07 的 REPORT/MATHEMATICS/SOURCES/NEXT_COMMAND，以及准备采用的 R05、R06 完整数学证明。原稿回查限于共同径向可行性、精确目录和截面估计等依赖；未重新审计无关混沌或提升结论。

1. **R05 全时域下界。** 固定半径和输入时，所有中间状态的垂直坐标对初始 z 严格单调；凸邻域的全时域可行初值交集是区间。导数乘积在该整个区间上统一受控，不只沿一个可行参考点。先用 R^j(1)→0 和 δ_n→0，再使晚期横向导数接近 q；早期有限乘积吸收为统一常数。截断 `s≥s_0` 后保留正面积，由 Fubini 得目录下界，最后选择所有时间比例 a。未交换 n 与精度的顺序极限。
2. **R05 全尾部上界。** 恢复小半径精确控制块和统一精确目录指数。固定前缀后，有限控制族在原点有共同局部 Lipschitz 常数；分别处理 L>1 和 L≤1，证明尾部始终留在所用局部球及 Q 的容差邻域。达到 n 的情形使用精确目录，避免越过时域。ρ=1 与 γ=∞ 单独由精确上界配合截面下界处理。
3. **R06 真实目录比较。** 恢复二进制完整可行圆柱、共同收缩范数。第一次选错控制时，欧氏邻域给出 `|z|<s+2δ`，继而是一侧狭带；`ρ_i<1/2` 才允许把停止尺度变成圆柱长度下界。每个实际输入至多覆盖 O(n) 个叶中点。含开集初始集包含固定半径完整子树，固定前缀及阈值常数不改变指数。
4. **R06 近满面积分裂。** 从 Lebesgue 编码的等频率及 Egorov、内正则性得到一个固定紧 E，而非假设所求覆盖率。E 对每个 ζ 有统一前缀收缩界；再用首次偏离的截面测度估计覆盖任意输入。K 的选择先于 γ、δ_n 和 ζ；同一 K 对全部精度序列成立。相似维数根和严格 AM–GM 只负责求值及比较，归于经典方法。
5. **R07 临界词。** 取零数 `ceil(n ln2/ln3)` 的词，累计对数总增量非负；从循环最低点之后开始即可保持全部前缀非负。每个循环轨道至多 n 个词，不使用整数步长 cycle lemma 的精确计数。固定一条任意输入，在每个首次偏离位置只覆盖一侧宽 `4δ_n` 内的至多三个格点；另加一个完全匹配词。上界使用快尾部 `1^∞`，没有用已经失效的“所有尾部收缩”。

正文核验中仅补清零时域目录、类型估计的 `k≥1`、词的父前缀和 N_0 记号、范数收缩方向及常数的量词，没有更改历史定理的结论。正文保留 C¹ 共轭的简短谱障碍说明，未收入不服务主线的更长 bi-Lipschitz 论证。

## 4. 直接文献、版本及实际阅读范围

以下 APA 与 DOI 同稿末参考文献。复用的阅读只按历史实际范围记载，不冒充本轮重新逐页全文审读。没有重新下载失败原件，也没有把检索未命中当作首创认证。

**Colonius, F. (2012).** Minimal bit rates and entropy for exponential stabilization. *SIAM Journal on Control and Optimization, 50*(5), 2988–3010. https://doi.org/10.1137/110829271

正式书目身份已核；实际正文为 2011-12-18 作者机构稿。复用 R05 §2 定义、§4 Theorem 4.2 陈述与谱移位入口，不声称正式版逐页比对。已有随当前时间衰减的稳定化精度；不把这种先例改写为本稿新概念。

**Colonius, F., & Hamzi, B. (2021).** Entropy for practical stabilization. *SIAM Journal on Control and Optimization, 59*(3), 2195–2222. https://doi.org/10.1137/20M1367775

正式身份与 arXiv:2009.08187v3 已核，期刊 PDF 差异仍未关闭。本轮复读 Definitions 2.1–2.2、§5.1 Theorem 5.1 的陈述和完整证明、Remark 5.2；R05–R06 已读其余相关范围沿用。其约束含 KL 函数与固定 ε，线性应用为固定 A、加性控制；本稿是全时域固定 δ_n 的 Q 邻域和乘性控制分支。本稿不依赖其有争议的固定 ε 下界步骤，不把作者稿疑点写成正式刊物错误。

**Csiszár, I. (1998).** The method of types. *IEEE Transactions on Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546

沿用 Crossref 身份核验，仅作已有方法归属；未声称读完原件。正文 Lemma 4.1 自含证明所用二项式上下界，不以未读定理作覆盖排除。

**Da Silva, A., & Kawan, C. (2016).** Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97

本轮重新核对 [AIMS 正式记录](https://www.aimsciences.org/article/doi/10.3934/dcds.2016.36.97)。复用作者稿 arXiv:1408.2416v1 §5.2 完整结构条件、Theorem 5.7 及其结尾证明（pp. 38–39、43–44）；未重审全部 volume lemma、shadowing 和周期逼近，也未认证正式版逐字差异。控制选择、正体积与不稳定 Jacobian 已有理论；本稿向内单向径向系统不满足其控制集假设，不能作为该理论的反例。

**Dershowitz, N., & Zaks, S. (1990).** The cycle lemma and some applications. *European Journal of Combinatorics, 11*(1), 35–40. https://doi.org/10.1016/S0195-6698(13)80053-4

复用 R07 的作者机构托管期刊扫描件及 Crossref。已读 §1、§§1.1–1.3 的证明及末尾参考文献，未审全部树应用。循环移位归于经典；本稿直接证明所需非负实数部分和的最低点旋转，不借用不适用的整数精确计数。

**Huang, Y., & Zhong, X. (2018).** Carathéodory–Pesin structures associated with control systems. *Systems & Control Letters, 112*, 36–41. https://doi.org/10.1016/j.sysconle.2017.12.009

本轮新增核对出版社可检索摘要/引言与 SIAM 2025 原文参考文献中的作者、卷页、DOI。实际范围仅摘要及引言片段；全文页面未成功打开，未声称审读各 C–P 结构定理。仅支持“控制熵的维数型构造已有”这一背景归属，不用于认证不存在等价覆盖。

**Hutchinson, J. E. (1981).** Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055

复用作者 TeX 重排原件（注明更正旧笔误，并非期刊扫描件），已读 §2.1、§§5.1–5.3 的定义、陈述和证明。停止尺度、有限重叠、相似维数根属于已有方法。真正需要本稿证明的是容许离开 Q 的控制所覆盖的实际状态。

**Kawan, C. (2013).** *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

用户正式原件 290 页，SHA-256 `c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6`。复用 §2.1 目录/outer 定义，§3.2 Definitions 3.1–3.2、Examples 3.1–3.2、Theorem 3.3 完整证明与 Corollary 3.1，以及 R05 §4.1 的相关覆盖范围。体积增长和控制优化已有；在本稿全输入共同收缩情形，已读体积增长下界的非负化不提供这里的正对角成本。未声称重读全书。

**Liberzon, D., & Mitra, S. (2018).** Entropy and minimal bit rates for state estimation and model detection. *IEEE Transactions on Automatic Control, 63*(10), 3330–3344. https://doi.org/10.1109/TAC.2017.2782478

复用机构托管期刊排版原件及 R06–R07 对 §II、§III 定义和 Theorem 1 证明、§IV Proposition 2 证明和 Remark 2 等的读取。分页以原件/Crossref 为准。其精度约束是逼近轨迹，时间零也有逼近误差；本稿初始状态不被替代，故不能直接搬用估计熵率，亦不宣称实现其通信结论。

**Nie, X., Wang, T., & Huang, Y. (2022).** Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

用户正式原件 31 页，SHA-256 `e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90`。R03 已全文阅读，R05 复读系统与最小目录定义；全文已取得的状态不变。本稿只引用测度与变分背景，不依赖其单位或共轭争议步骤；不另造压力对偶或把纠错作为主贡献。

**Wang, T., Huang, Y., & Sun, H.-W. (2019).** Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

用户正式原件 24 页，SHA-256 `23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363`。R03 补核的相关证明、R05 Definitions 4.1/4.3 范围沿用。本稿没有新测度熵或测度变分主张，正文只作已有背景引用。

**Yang, R., Chen, E., Yang, J., & Zhou, X. (2025).** Bowen’s equations for invariance pressure of control systems. *SIAM Journal on Control and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

本轮核对 [SIAM 正式条目](https://epubs.siam.org/doi/10.1137/23M1607684) 和 [arXiv v3](https://arxiv.org/html/2309.01628v3) 的引言、Theorems 1.1–1.4、§2 设定入口；复用 R01 的 partition/cylinder 定义及变分证明入口范围。正式逐字差异未审。它明确覆盖按不变分划的诱导压力、Bowen 方程和相应维数/变分原则。本稿不以这些公式为新意；待证的是全部实际近似控制与特定符号树的比较。作者版 Theorem 1.4 的 clopen 假设不能自动由二进制锥体的普通 Borel 分支满足。

**Yao, S. (2026).** *Invariance entropy in the dust* (Version 1) [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2607.02279

本轮核对官方版本记录（仍为 2026-07-02 v1，未见期刊身份）及 [官方正文](https://arxiv.org/html/2607.02279v1)。在 R05 已读主要分离证明基础上，复读匹配图、有限骨架与 §4.1–4.3 的匹配/淡出步骤，未重审全部 Hausdorff 附录。正 exact、零 outer 和晚期误差隐藏已有直接先例；本稿只能以正面积条件下的完整对角精度律及严格成本分裂主张区别。

上述版本、源文件哈希与更细阅读记录仍保留在 R03–R07/SOURCES.md。本轮没有要求用户再次获取已有原件。未读或仅摘要的文献不能被写成“已排除全部覆盖”；例如 R01 已记录的零熵复杂度/entropy dimension 文献，不能按题名就排除其细节。有限定向检索和当前直接阅读支持的是上述具体差别，而不是全库首创证明。

## 5. 成果分量与期刊判断

**数学核验通过。** 这是本轮对实际写入证明链的结论，未经过外部同行评审，也不是形式化证明证书。没有以有限数值计算替代证明。

**形成可评估稿件。** 已有独立用途：在一个全部输入共同收缩的正面积系统内，给出仅靠正面积条件会失效的定量定理，并将失效定位到可行分支与收缩的绑定。共同径向定理与扩张案例帮助界定用途。它超过再举一个熵分离例子，但仍依赖特殊平面比值几何；不是一般控制理论、一般分形理论或四大级结果。

**是否值得向某刊尝试，是有风险的专业判断。**

| 对象 | 证据与本轮判断 |
|---|---|
| DCDS | 可作为阶段稿的首个条件性尝试对象。Da Silva–Kawan2016 的直接相关论文表明，受控几何、正体积初始集与熵率之间的定理联系是该刊实际发表过的内容。本稿有精确的新几何限制及完整证明，因此不只因题域匹配而建议尝试；但其适用范围与一般性明显较窄，编辑认为分量不足的风险仍实在。 |
| SIAM Journal on Control and Optimization | 有 Colonius2012、Colonius–Hamzi2021、WHS2019、Yang 等2025 的直接主题证据，可作更有挑战性的备选。现稿没有普遍最优控制/通信实现结论，不能据相似词汇认证其贡献达到该刊要求。 |
| JDE、ETDS | 有相关熵/测度文献，不足以支撑当前这组特定系统结果已达到其录用标准。没有本轮可据以作出的强推荐，更不能报告“已达一区/TOP”。 |
| Annals、Inventiones、JAMS、Acta | 继续保留长期目标；这篇特定模型的阶段稿尚无四大重要性依据，不因成稿而上调判断。 |

这些判断不是期刊承诺或录用概率。本轮不使用未经核实的分区标签。也不承诺通过累积模型、加维数或多写几轮可逐级到达四大。

## 6. 编译、正文一致性与下一入口

已全文核对生成稿的定义、定理、实际证明和 PDF 提取文本；补清符号和边界时域，逐项核对 13 条引文身份及其使用范围。使用 `latexmk -pdf -interaction=nonstopmode -halt-on-error` 编译；交叉引用及引用均解析。完成 14 页逐页渲染检查，正文与公式清晰，无溢出、未定义引用或 LaTeX 警告。编译通过仅说明技术完整，不替代上文的数学和发表裁决。

从仓库根目录复现：

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=/tmp/p6-paper-build paper/P6_PRECISION_COST.tex
```

阶段稿的已陈述主定理没有本轮已知未解步骤；实际局限是系统类有限、一般正面积集尚未分类、控制依赖非线性未获一般公式、全部文献等价覆盖未认证。本轮无需新增一个缺失命题来勉强成稿。

下一入口是对**现稿**作一次提交前的有限审阅和定位修订：只处理具体反例、直接等价文献或确切行文问题，不自动另开数学轮次，不添加模型，不重复 R01–R07 全部审计。若无实质问题，保留这份稿件供作者评估；是否投稿另由用户决定。可直接使用：

> $github 继续 khdzg5shnt-rgb/p6sida。先核对最新 main、CURRENT.md 和 research/R07/STAGE_PAPER_DECISION.md，全文阅读 paper/P6_PRECISION_COST.tex。对这份已完成阶段稿做一次有界的提交前审阅：只解决会改变主贡献裁决的直接文献等价覆盖、具体证明漏洞或专业行文问题；发现问题给出精确原句、理由和必要修订，未发现则明确维持已有裁决，不重复开轮、不自动增加定理。以 DCDS 为条件性定位核对贡献表达，不承诺录用。只操作 p6sida，保留 original/ 与全部历史，不投稿、不联系他人、不分派代理；仅有实质修订才提交并全文回读。

保存边界：只新增本裁决与 paper/ 中的唯一阶段稿，简短更新 CURRENT.md、README.md；不改 original/ 和 R01–R07 的既有文件。原稿 SHA-256 仍为 `47aa42836d78fa281d1ef18e1fbb20d5d311eeab0959077f775542b61249b869`。
