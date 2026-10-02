# R02：一手文献、阅读范围与未闭合缺口

核查日期：2026-10-03（Asia/Shanghai；UTC 2026-10-02）。以下以出版社、arXiv 作者原件和 Crossref 元数据为依据。书目信息核实、取得完整文件、读过相关正文、独立核验全部证明是四个不同状态。本轮没有用原稿的文献说明认证原创性，没有用摘要排除覆盖。

## 1. 阅读与定义对照

| 文献 | 实际取得、阅读位置 | 对本轮判断有用的定义与假设 | 未完成项 |
|---|---|---|---|
| Wang–Huang–Sun 2019 | SIAM 出版条目、摘要与作者元数据；未取得全文 | 摘要只确认两种测度不变熵、控制共轭不变性及特殊情形的变分原则。NWH2022 引言对它的介绍不是 WHS 原文审查 | 测度类别、分划要求、全部定理与证明仍未核验；不能排除覆盖 |
| Nie–Wang–Huang 2022 | 从出版社页面的检索索引取得实际正文片段：§2 压力、Definition 2.4、Proposition 2.5、Definition 3.4、Theorems 3.11 / 3.13、Corollary 3.15；没有完整 HTML 或 PDF | 修订压力对最小基数 spanning families 的加权和取上确界，区别于既有的加权和下确界；测度取输入值空间的 `M(U)`。Def. 3.4 用压力零水平集上的积分下确界定义熵；3.13 / 3.15 给相应变分公式 | 系统公理、§2.3 及证明中间部分未连续取得。索引转写及离散时间势函数的单位须由完整原件补核。本轮自己的有限字母计算不依赖这些未读证明 |
| Da Silva–Kawan 2016 | 完整作者 PDF（45 页），arXiv:1408.2416v1；阅读 Proposition 4.7、§5.2、Theorem 5.7 及相关证明 | 光滑 control-affine 系统，双曲 chain control set，非空内部、相应 Lie rank / 可达性与单点输入纤维条件；正体积紧 `K⊂D`。提升图共轭输入移位，精确成本由不稳定 Jacobian 给出 | 所列编号按作者 v1；未逐行审完其全部证明，也未逐页比较 2015 修订后的期刊原件 |
| Kawan–Da Silva 2018 | 完整作者 PDF（31 页）及 HTML，最新 arXiv:1711.01181v2；读 §2 的 P1–P4、条件熵与 Theorem 2.1 | `C²` control-affine 系统；无限紧凸输入范围；全时间 controlled invariant 紧 `Q`；常维 splitting `E+⊕E0−`，前者统一扩张、后者至多子指数增长；纤维下半连续、隔离，`K` 正体积。结论是膨胀积分减条件状态熵的下界 | 不是一般等式；全部技术证明及作者版与期刊版差异未完成审查 |
| Kawan 2003.06935 最新版 | 正式版本历史及 v5 完整 HTML 可读；核查 §3.1、A1–A3、Theorem 4.7、Corollary 4.9、§4.6–4.7 适用范围及 §7 | 双向离散控制系统；紧连通可度量输入空间、联合连续的状态微分同胚及逆/导数；全时间双曲紧 `Q`，隔离提升、纤维下半连续，`K` 正体积；相应下界还用 `C²` 正则性。一般匹配上界仍是问题 | 没有逐行审完全部证明；未完成 v4/v5 全文 diff；两个已处理极端情形不能被改写成一般等式 |

NWH2022 的 Def. 2.4 明确使用实际状态映射 `π_t` 和输入值映射 `H`，满足 `π_t φ₁(t,x,ω)=φ₂(t,π₀x,h_Hω)`。Proposition 2.5 的正文陈述另列 `π_t(Q)⊂π₀(Q)` 和每个时域 spanning count 有限。它不是任意可行提升的抽象共轭。相关证明尚未全文审完；R02 只独立使用固定状态映射、初始投影交换的较窄情形。

三种测度对象必须分开：WHS2019 的原文类别尚未确认；NWH2022 定义的对象是输入**值**上的概率；部分双曲论文的条件熵对象是全时间提升上的不变概率及其输入过程边缘。不得把它们互相代换。R01 的所有条件 KS 熵为零没有排除控制测度熵为正。

## 2. 核实后的 APA 与版本

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

出版社核实作者 Tao Wang、Yu Huang、Hai-Wei Sun；2019-01-22 在线发表。原文入口：[SIAM 条目](https://epubs.siam.org/doi/10.1137/18M1197862)。

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

出版社、卷目录和 Crossref 核实 Xiaoxiao Nie、Tao Wang、Yu Huang 及卷页 DOI。[出版社正文入口](https://www.sciencedirect.com/science/article/pii/S002203962200184X)；[本轮取得索引正文片段的同一出版社页面](https://www.sciencedirect.com/science/article/abs/pii/S002203962200184X)。页面索引标作 Open archive；访问失败不能据此归因为必须付费。

Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97

[期刊条目](https://www.aimsciences.org/article/doi/10.3934/dcds.2016.36.97)显示 2015-03 修订、2015-06 在线发表，卷年 2016。[作者版历史](https://arxiv.org/abs/1408.2416)本轮只见 v1（2014-08-11）；[所读作者 PDF](https://arxiv.org/pdf/1408.2416v1)与[HTML](https://arxiv.org/html/1408.2416v1)均固定版本。不能把 v1 与最终期刊版未经比较就称为逐页相同。

Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class of partially hyperbolic sets. *Mathematics of Control, Signals, and Systems, 30*, Article 18. https://doi.org/10.1007/s00498-018-0224-2

[Springer 条目](https://link.springer.com/article/10.1007/s00498-018-0224-2)核实 2018-10-30 发表。[作者版历史](https://arxiv.org/abs/1711.01181)当前最新 v2（2018-05-09）；[PDF](https://arxiv.org/pdf/1711.01181v2)；[HTML](https://arxiv.org/html/1711.01181v2)。

Kawan, C. (2026). *Control of chaos with minimal information transfer* (Version 5) [Preprint]. arXiv. https://doi.org/10.48550/arXiv.2003.06935

[正式历史](https://arxiv.org/abs/2003.06935)核实首版 2020-03-15，最新 v5 为 2026-09-20；[本轮正文](https://arxiv.org/html/2003.06935v5)。这是 arXiv DOI，未据此虚构期刊发表。P6 原稿所列 v4（2021-05-19）不再是最新版。

## 3. 全文获取失败的可复查记录

| 对象 / 入口 | 本轮实际响应或检索结果 | 裁决 |
|---|---|---|
| WHS2019 SIAM 条目、`/doi/pdf/10.1137/18M1197862`、电子 PDF 入口 | 条目可读，列出 Get Access；PDF 请求 403 或转入访问/购买页，未返回论文 PDF | 未取得全文；没有购买、借用凭据或联系作者 |
| WHS2019 作者公开页面及题名 / DOI / arXiv 检索 | 王涛湖南师大页面列出书目；其余公开入口没有取得可验证全文 | 此结果只说明本轮没有找到，不证明不存在公开作者版 |
| NWH2022 出版社文章 / 摘要页面 | 直接读取 403；标准下载返回 HTTP 200，但只有 195 字节 SiteUnavailable 占位内容 | HTTP 200 不是取得论文；未把该文件算作完整 HTML |
| NWH2022 `pdfft` 下载入口 | 返回错误占位页 / 工具访问失败，无有效 PDF | 完整原件缺口保留；索引中的正文片段单独标记为已读 |
| NWH2022 其他公开全文检索 | 未取得可验证完整作者稿 | 未排除其定理、例子或后续覆盖；没有以摘要作排除依据 |

已成功取得的作者 PDF 仅用于本地阅读，不把第三方全文复制进仓库。获取文件的 SHA-256：

- DSK2016v1（463523 字节，45 页）：`2d4cb7ea8ddb59c7cbccae6f5534cf5d98b76b48f9afbfc687c48a8865b2185b`。
- KD2018v2（403967 字节，31 页）：`f7041c7fa49d498e632141febdc234ab6b3c6a37a8a7ee4c28aca6acf45eda1f`。

这些哈希只识别本轮下载字节；arXiv 重新构建文件时字节可能改变。

## 4. 单位、勘误和剩余审查边界

R02 自含计算明确采用自然对数及 `exp(S_n g)`。KD2018 作者版也明确用自然对数。Kawan v5 的 bit 速率换为自然单位需乘 `ln 2`。NWH2022 索引显示离散时间对数约定与指数权重；在未取得完整原件前，不认证转写后所有势函数单位完全一致，不由此宣布论文有错。R02 计算与其定义的结构对应已明确，逐字数值归一仍须补核。

对四篇期刊论文的 DOI 结合 erratum / correction 检索，并核查当前出版社条目；本轮没有确认与所用主结论相关的独立勘误。Crossref 对前三篇的关系字段没有列出更新关系；2018 条目 Crossref 请求受限，元数据改由 Springer 核实。Springer 的 2018 页面 Notes 另有 Lemma 3.6 的符号替换说明（ε 对应 η，δ₀ 对应 ρ₀）；这不是本轮找到的独立勘误论文。未发现不等于证明没有勘误。

仍未完成：WHS2019 全文；NWH2022 连续完整原件及全部证明；两篇作者版与期刊版差异；Kawan v4/v5 全文差异。R01 其他文献缺口不因 R02 被自动关闭。精确族的首创性仍未认证，不能把这个事实改写成已有覆盖已全部排除。
