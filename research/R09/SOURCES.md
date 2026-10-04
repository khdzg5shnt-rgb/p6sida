# R09：原文、方法归属与实际阅读范围

2026-10-04（Asia/Shanghai）。本轮直接对象是首次越界修复、实际停止覆盖及改变精度后的时间极限。自含证明不以历史文献裁决为前提。原始来源与正式身份分开核对，不将未读版本记作已排除覆盖。

## 本轮复读与补核

**Kawan, C. (2013).** *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

沿用项目正式原件07-pdf，SHA-256 c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6。本轮实际复读§2.1，约印刷pp.44–48：Definitions 2.1–2.3、Proposition 2.3及完整拼接证明；Appendix B，p.252，Lemma B.3及完整证明。没有重读全书。

目录量词、拼接/次可加和极限等于确界是经典内容。R09停止目录的拼接按同一方法证明；新工作的所在是将允许离开Q的对角精度目录转成精确停止目录，不能仅由固定时域的Proposition 2.3直接得出。

**Yang, R., Chen, E., Yang, J., & Zhou, X. (2025).** Bowen’s equations for invariance pressure of control systems. *SIAM Journal on Control and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

[SIAM正式身份](https://epubs.siam.org/doi/10.1137/23M1607684)核对作者、卷期、页码、DOI和2025-04-10在线日期。本轮新读[出版者提供的第一页预览](https://www.researchgate.net/publication/390679689_Bowen%27s_Equations_for_Invariance_Pressure_of_Control_Systems)，印刷p.1104；这不是取得25页正式全文。

实际技术正文复读[arXiv:2309.01628v3](https://arxiv.org/html/2309.01628v3)，日期2025-01-28：Theorems 1.1–1.4陈述，§2 invariant partition、地址和柱子集，§3.1 Definitions 3.2–3.3、Proposition 3.5完整证明，§3.2开头至式(3.3)及其邻近步骤。其余定理的全部证明没有本轮重审。未完成与正式全文的逐字差异认证，也未重试既有失败PDF入口。

正输入势、停止成本、诱导压力与Bowen根式已有。所读技术对象依赖预先给定的不变分划及其地址；R09的N_m允许重叠的实际可行区间并优化控制词，没有固定地址。将任意近似越界区间修复为精确停止覆盖的比较未由上述陈述直接提供。未经证明，不能把R09未知常数等同某个分划压力或已有根。

## 复用原件和阅读记录

**Chen, Z., & Zhong, X. (2024).** Invariance complexity and equi-invariability for control systems. *Journal of Mathematical Analysis and Applications, 539*(2), Article 128533. https://doi.org/10.1016/j.jmaa.2024.128533

项目正式原件09-1-s2.0-S0022247X24004554-main.pdf，16页，SHA-256 62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc。沿用R08记录的Definitions 2.10–2.11、Theorem 2.12、§3.1范围；本轮复查稿首页题名、作者及DOI，未重审全部技术证明。实际作者为Zhijing Chen、Xingfu Zhong。

同一环境邻域目录及固定精度有界性已有。它们不自动给出 \(\delta_n=2^{-n}\) 的增长极限；R09局部参考控制覆盖采用既有连续性/Lipschitz思路，不独占这种方法。

**Lu, J., Steiner, W., & Zou, Y. (2026).** Hausdorff dimension of double-base expansions and binary shifts with a hole. *Bulletin of the London Mathematical Society, 58*(4), Article e70344. https://doi.org/10.1112/blms.70344

复用R08已核Wiley正式全文身份、Crossref及阅读记录：引言与Theorems 1.1–1.6；§2 Lemmas 2.1–2.3完整证明、Lemma 2.4陈述和构造开头；§3.8部分证明。没有在R09又审全篇。唯一编码、避洞语言和加权词熵均有先例；R09最长串19的具体几何验证、最长串21的安全策略及实际目录比较另作自含推导，不以该文代替覆盖证明。

**Hutchinson, J. E. (1981).** Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055

复用R06/R08作者TeX重排修订稿§2.1、§§5.1–5.3记录，仍非期刊扫描版。加权停止、相似维数及有限词概率方法已有。R09有限状态概率的全部公式在MATHEMATICS §7直接验证，不依赖未读命题。

WHS2019、NWH2022正式原件及R03补核状态保持；本轮不用其争议步骤。Komornik–Kong–Li2017未取得正文、Colonius–Hamzi2021正式版与作者稿的差异，以及其他既有版本缺口均保持，不循环获取。本轮推导不依赖这些缺口。

## 逐项判断

| 陈述或步骤 | 判断 |
|---|---|
| 目录定义、完整时域、参考控制邻域覆盖 | 已有定义和方法。 |
| 停止成本、压力/维数根式、有限状态加权计数 | 既有工具及已有方法应用。 |
| 精确停止目录的拼接和次可加极限 | 经典方法的具体应用，非新一般原理。 |
| 实际初态顶截面与全锥体目录相等、包含全部时刻的区间表达 | 固定系统的自含几何推导，保留半径与可行性。 |
| 任意近似目录按首次越界修复，以线性损失转成最优精确停止覆盖 | R09实际完成的核心接口；已读文献没有可直接套用的同对象结论。 |
| 指定系统真实率极限存在、两侧严格收紧 | 新增于项目；准确常数仍未知，全库优先权未认证。 |
| 显式准确值、最优策略、一般参数分类、期刊档位 | 未完成或未认证。 |

正式版本缺口限制非覆盖与发表叙述，不否认本轮独立证明。没有以检索未命中认证首创，也没有把一份只读第一页的正式版本列作全文排除。无需用户补找原件来完成此次自含推导。
