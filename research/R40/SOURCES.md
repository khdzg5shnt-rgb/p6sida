# R40：直接覆盖来源、正式版本与实际范围

2026-10-08 UTC；基线 `303085d3b326ea5c38db795756409be9a2c02d6f`。
本轮只新增两篇直接相关原始论文的检验对象（下述§§2–3）。
正式出版身份、作者版本阅读和未读正式范围分别记录。

## 1. WHS2019：正式原件与测度运输

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance
entropy for control systems. *SIAM Journal on Control and Optimization,
57*(1), 310–333. https://doi.org/10.1137/18M1197862

[SIAM正式页面](https://epubs.siam.org/doi/10.1137/18M1197862)再次核对身份。
复用 `18m1197862.pdf`：24页，400654字节，SHA-256
`23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363`。

本轮实际重读 PDF pp.7–11，印刷 pp.316–320：Definitions 4.1、4.3、4.7；
Propositions 4.4–4.6 及其证明；Theorem 4.8 的完整证明。
另渲染视觉核对 pp.10–11 的共轭、相同输入、柱子概率及积分运输。
p.11 随后生成分划部分不计为新审查范围；历史全文范围不冒充本轮全文。

Theorem 4.8 同时运输系统和初态测度；证明保持对应不变分划的柱子概率。
这覆盖了测度运输，但不保持两端各自的均匀面积。
本稿反例在全状态目录恒等下改变物理区域质量，和该运输结论相容。
实际双指数目录还需要正文全瞬态概率上界、正面积强制区域及完整时域比较。
所读原文步骤未直接提供它们；不是全面排除概率控制熵覆盖。

## 2. 新补核：Colonius（2018）

Colonius, F. (2018). Invariance entropy, quasi-stationary measures and
control sets. *Discrete and Continuous Dynamical Systems, 38*(4),
2093–2123. https://doi.org/10.3934/dcds.2018086

[AIMS出版页面](https://www.aimsciences.org/article/doi/10.3934/dcds.2018086)
核实卷期页码及 DOI。正式全文入口遇登录墙，机构 postprint 入口未成功；
未重试，未声称取得正式原件正文。
实际使用[作者PDF arXiv:1705.08658v2](https://arxiv.org/pdf/1705.08658v2)，
31页。版本页眉为 v2；PDF内部 Date 标为 October 11, 2018，分别保留，
不将它们视为正式版本逐字相同的证明。

实际阅读：PDF pp.3–4 的准平稳/系统定义，pp.9–11 的 Definition 2.12、
Theorem 2.13及完整证明，pp.13–16 的 coder-controller定义与
Theorem 3.4及完整证明。不写成31页全文审查。

该框架在控制概率与准平稳初态测度下，用条件柱子概率与 Shannon 率
研究测度熵、运输及 coder-controller。
正文所核不是本稿在均匀物理面积、缩小环境管带与指数失败预算下的
最少输入基数。应用仍须证明实际成功区域与所用概率过程之间的关系。
作者版已读范围没有自动给出本文物理强制质量与全瞬态 domination；
正式版未读部分不标作排除覆盖。

## 3. 新补核：Wang–Huang（2022），最直接正文缺口

Wang, T., & Huang, Y. (2022). Inverse variational principles for
control systems. *Nonlinearity, 35*(4), 1610–1633.
https://doi.org/10.1088/1361-6544/ac4f33

正式身份由出版者首页预览（印刷 p.1610）与作者机构发表表核对：
题名、两位作者、Nonlinearity 35 (2022) 1610–1633及DOI一致。
预览在[论文页面](https://www.researchgate.net/publication/358679081_Inverse_variational_principles_for_control_systems)
嵌入出版者首叶；它不是取得全文的证明。

**本轮只读出版者首页和摘要。**正式端点/正文入口未成功，
没有再尝试下载，没有读取正式定义、定理、失败参数或关键证明。
摘要明确涉及 spanning-based 测度不变熵、逆变分及线性计算，
因此是可靠性主贡献的直接覆盖风险，不能靠定义不同或检索未命中排除。

尚待原文核验：概率覆盖的失败容许和极限次序；是否提供对
随 n 改变的 δ_n、e_n 的统一估计；证明能否推出本文实际质量与
任意近似输入强制区域。这里的问题全部记为未核实，不预认答案。
已单独向用户列准确题名及 DOI；本轮自含数学及成稿继续完成。

## 4. 既有经典可靠性工具，范围复用

Csiszár, I. (1998). The method of types. *IEEE Transactions on
Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546

出版身份及既有阅读范围复用 R37–R39：作者上传文字的§II类型、
Lemma II.2及§III源块编码/Theorems III.1–III.2相关说明，主要
印刷 pp.2506–2509；电子文本缺若干数学显示，完整正式PDF未取得。
**R40没有重新获取或声称重新全文审读。**所用二项式上下界、
严格类型逼近及优化均在正文自含证明；L_a和源编码可靠性是已有工具。
没有为这项已有版本缺口重复请求原件。

## 5. 两篇 JDE 正式原件的比较证据复用

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance
entropy and variational principles for control systems.
*Journal of Differential Equations, 321*, 318–348.
https://doi.org/10.1016/j.jde.2022.03.013

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of
invariance entropy dimension. *Journal of Differential Equations, 453*,
Article 113819. https://doi.org/10.1016/j.jde.2025.113819

本轮全文读取 R35 的报告和来源记录，复用其正式审查，不写成R40
重新阅读两篇所有正文。NWH正式31页，SHA-256
`e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90`；
R35范围为PDF pp.1–7、10–26，重点 Theorem 3.13、Corollary 3.15
完整证明及§4，历史全文见R03。
CHZ正式24页，SHA-256
`8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`；
R35已读pp.1–24，重点圆柱质量、weighted covering、Frostman及逆变分。
陈虎.pdf持续记为全文已取得，卷年为2026，不以DOI年份改成2025。

NWH提供目录压力的测度对偶，须先知道实际目录；CHZ提供指定圆柱的
时间幂次及质量工具，须先把真实 A_u 与圆柱连接。
它们支持控制/动力系统方向的同刊比较，但没有代替本文双指数物理比较。
R03的归一/共轭问题不算当前竞争力依据，也未在R40重开历史反例。

## 6. 分区来源、采用链及限度

2026-10-08重开[山东工商学院机构新闻](https://sx.sdtbu.edu.cn/info/1062/7702.htm)：
新闻发布为2026-07-28，明确称JDE在**2025年中科院分区、数学大类一区TOP**。
这是大学间接来源，不是中科院官方期刊条目；不是2026分区核验。
没有完整年度学科JCR条目，不混用体系，也不以分区认证稿件。
JDE题域和两篇正式论文的比较沿R35已核记录；不是新接收门槛。

本轮采用链为现稿局部图锥/双乘积、R33有限非塌缩窗口、R37线性
可靠性、R38严格反例、R39全Q概率与加厚强制区域。
完整实际正文核查和新版标号对应见REPORT及唯一TeX。
初稿仅重读源码第15–92行作主张比较，不重新认证旧证明或初稿档位。

图变换、可求和畸变、面积公式、局部逆图、源编码可靠性和类型计数
归于经典方法。实质连接为真实物理成功集合的概率运输及任意输入
必须保留的正面积前缀，数学增量归原研究，R40整合不新增证明。
最多两篇新增原始对象，未开展广泛检索；所有未读范围保持未决。
