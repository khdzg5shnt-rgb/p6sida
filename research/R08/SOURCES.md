# R08：原始来源、准确书目与覆盖边界

2026-10-04。只核查重叠控制与成本分离的实际依赖，第三方全文不复制入仓库。书目身份、阅读范围和覆盖判断分开记录。

## 新补核的最近原文

**Lu, J., Steiner, W., & Zou, Y. (2026).** Hausdorff dimension of double-base expansions and binary shifts with a hole. *Bulletin of the London Mathematical Society, 58*(4), Article e70344. https://doi.org/10.1112/blms.70344

Wiley 正式全文页与 Crossref DOI 记录交叉核对作者、题名、卷期、文章号。在线日期2026-03-31，印刷期2026-04，不是仅以 arXiv 日期代替期刊身份。

[正式原文](https://londmathsoc.onlinelibrary.wiley.com/doi/full/10.1112/blms.70344)。实际阅读：引言、Theorems 1.1–1.6 陈述；§2 Lemmas 2.1–2.3 的陈述和证明，Lemma 2.4 陈述与构造开头；§3.8 部分证明和相关书目。未审完全部连续性证明。网页检索工具读取正式全文，独立 HTML 请求403，未重试，不声称取得期刊 PDF。

其唯一编码、避洞子移位、熵/维数和加权词根式均为直接先例。R08 受限编码和熵/收缩计数不作首创主张。已读对象是唯一展开集合及符号语言，不直接含实际正面积初态、控制半径乘积、全时域容差与同一近满面积紧集的目录分离；后者在 MATHEMATICS 中自含证明。这不是全库非覆盖认证。

**Komornik, V., Kong, D., & Li, W. (2017).** Hausdorff dimension of univoque sets and Devil's staircase. *Advances in Mathematics, 305*, 165–196. https://doi.org/10.1016/j.aim.2016.03.047

Crossref 精确题名查询与上述正式论文 reference 29 交叉核对，DOI采用登记结果。本轮未取得并审读正文；作者机构PDF入口404，出版社与arXiv PDF网页入口未成功读取，未循环。仅记历史归属，不能据此排除技术覆盖，不为这个背景工具要求用户补找原件。

## 复用的控制与精度原文

**Chen, Z., & Zhong, X. (2024).** Invariance complexity and equi-invariability for control systems. *Journal of Mathematical Analysis and Applications, 539*(2), Article 128533. https://doi.org/10.1016/j.jmaa.2024.128533

正式原件09-1-s2.0-S0022247X24004554-main.pdf，16页，SHA-256 62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc。复用 R07/DCDS_FINAL_REVIEW 对 Definitions 2.10–2.11、Theorem 2.12、§3.1 的审读范围，没有重审 mean 类型证明。同一目录定义和固定容差有界性已有；该刻画没有直接给出本轮对角指数分离。

**Kawan, C. (2013).** *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

项目正式原件07-pdf，290页，SHA-256 c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6。复用 R05–R07 的 §2.1 目录/outer、§3.2 体积增长和 §4.1 Lipschitz覆盖实际范围，未重读全书。双线性控制、输入优化和覆盖方法已有；本轮全部输入共同收缩，正增长下界不会自动给出正联合精度成本。

**Yang, R., Chen, E., Yang, J., & Zhou, X. (2025).** Bowen's equations for invariance pressure of control systems. *SIAM Journal on Control and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

正式身份和作者版范围沿用 R07/STAGE_PAPER_DECISION：引言、Theorems 1.1–1.4、partition/cylinder 入口，未新增正式版逐字比对。分划压力、Bowen根式和维数已有；R08 不提出新压力公式，实际目录与完整符号树的比较必须另证。

**Hutchinson, J. E. (1981).** Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055

复用 R06 已读的作者TeX重排修订稿 §2.1、§§5.1–5.3，不冒充期刊扫描版。前缀停止、相似维数和分离计数已有；本轮根式与全树上界按经典应用处理。

**Csiszár, I. (1998).** The method of types. *IEEE Transactions on Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546

仅复用既有 Crossref 身份核对，仍不计正式全文已读。R08 所需二项式界已有自含证明，不依赖未读定理。

WHS2019、NWH2022 的正式原件及 R03 全文补核状态不变。本轮没有新测度熵或变分主张，也不依赖争议步骤。Colonius–Hamzi2021 等作者稿与正式版缺口按 R05/SOURCES 保留，未重复失败获取，不因此阻塞自含推导。

## 逐项覆盖

| 内容 | 归属和边界 |
|---|---|
| 目录定义、固定精度有界性 | Chen–Zhong / Kawan 等已有。 |
| 重叠中保留唯一编码、词熵和维数 | 唯一展开/避洞理论已有，最近直接原文为 Lu–Steiner–Zou2026。 |
| 类型法、禁长串的并集界、Borel–Cantelli、内正则性 | 已有工具的应用。 |
| 根 \(\rho_0^D+\rho_1^D=1\)、加权停止 | 已有方法，不作为新主定理。 |
| 首次偏离造成实际锥外距离，对任意近似控制强制长字块，后期重返也不能修复 | R08 完成的控制几何接口，限于所构造见证子集。 |
| 非独立数字的频率带、同一近满面积紧集、真实前缀及完整尾部 | R08 完成，没有假设不变测度或等频数字。 |
| 每对不同收缩率下，正重叠与严格余量仍有严格指数分离 | 本轮新证于项目；已读结果未提供可直接套用的同量词结论，全库优先权未认证。 |
| 完整重叠精度谱、较大重叠分类、期刊档次 | 未证明或未认证。 |

不以检索未命中认证首创，不将未读正文标为已排除覆盖。APA 与明确身份记录对应。现有材料足以支持本轮自含证明，不需要用户寻找新原件。
