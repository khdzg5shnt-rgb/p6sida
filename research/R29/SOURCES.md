# R29：来源、实际范围与公式归属

2026-10-06 UTC。本轮复用 R28 已核原件及阅读范围；没有新增
论文下载或原文补核，没有重复失败获取。以下 APA/DOI 沿用已
核正式身份，不把以前读过的部分改写成本轮全文阅读。
本轮新计数和优化全部自含，未发现必须追加原文的直接依赖。

## 1. 项目内实际证明来源

基线 `503801f1b028316159cf78aa63fae3ed35120e1c`：

- CURRENT.md、paper/P6_PRECISION_COST.tex、R28 的 REPORT.md、
  SOURCES.md、NEXT_COMMAND.md，全文读取。唯一稿是 R28 整合稿。
- R27/MATHEMATICS.md 全文恢复；实际采用并独立复核 §§2–3 的
  局部径向比较、§6 的参考停止树真实上界、§7 Lemma 27.2 的
  有界串物理实现及错控制余量、§8 的首次错误约束。与现稿
  §§3、5–6 完整证明对照，不将历史核验作为正确性前提。
- R27 的同一个典型近满面积紧集及低侧定理用于结果对照和
  Corollary 29.2 后的差距推论，不重新制造一次全面审计。
- R26 不新增正文复读：R29 必需的几何已在 R27 与现稿中完整
  陈述及证明。原有正式文献阅读范围继续保留。

R27 数学文件 SHA-256：
`210ce8688e7e60d865f409c6c47e5cb0847d44992482906a87e6c45fd4089b07`。
唯一论文的源码/PDF 哈希见 REPORT；本轮不改这些文件。

## 2. 经典计数与直接压力背景

Csiszár, I. (1998). The method of types. *IEEE Transactions on
Information Theory, 44*(6), 2505–2523.
https://doi.org/10.1109/18.720546

- 正式身份/卷期页码沿用 R28；正式全文未读状态不变。本轮没有
  将该文当作已全面排除覆盖的文献。
- 使用的是经典二进制类型上、下界，R29 §4 给出 binomial 法的
  独立证明；它不是新贡献。有限块计数与频率优化不能自行
  提供正半径物理实现和任意近似输入下界。

Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen’s equations
for invariance pressure of control systems. *SIAM Journal on Control
and Optimization, 63*(2), 1104–1128.
https://doi.org/10.1137/23M1607684

- 正式身份已经核实。沿用作者稿 arXiv:2309.01628v3 的 §3.1
  及 R25–R28 的已记录压力/停止范围；正式主文未全文读的限制
  保留。本轮无新的正文审查。
- 指定分划、成本阈值和压力公式为已有方法。R29 没有把最大
  熵表达或压力根式主张为新定理，也不靠该文断言参考停止树
  必要。真实目录的上界分配和下界物理强制由 R27 提供。

Hutchinson, J. E. (1981). Fractals and self-similarity.
*Indiana University Mathematics Journal, 30*(5), 713–747.
https://doi.org/10.1512/iumj.1981.30.30055

- 作者重排稿 §§2.1、5.1–5.3 的既有范围沿用，正式全文不改称
  已读。本轮不追加阅读。
- 辅助二叉树的乘积尺度及权重加法是经典背景，非物理初态
  的实际分划。R29 的几何论证没有要求所有固定半径词截面非空。

## 3. 真实目录与体积框架的覆盖范围

Chen, Z., & Zhong, X. (2024). Invariance complexity and
equi-invariability for control systems. *Journal of Mathematical
Analysis and Applications, 539*(2), Article 128533.
https://doi.org/10.1016/j.jmaa.2024.128533

- 沿用正式 PDF 16 页、441166 字节、SHA-256
  `62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc`。
  R28 重读 §2.2、页6–7 Definitions 2.10–2.11、Theorems 2.12–2.13、
  Corollary 2.14 及印刷证明；2.12(1) 指向旧证明，不改称本文
  完整逐步推导。本轮复用该范围。
- A_u/真实最小目录是其 outer complexity 同类对象，非本项目
  新定义。固定 δ 的有界性不自行量化 δ_n→0 的准确谱；已读
  证明仍需实际径向比较、全时域尾部和物理错控制余量的连接。

Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class of
partially hyperbolic sets. *Mathematics of Control, Signals, and
Systems, 30*, Article 18. https://doi.org/10.1007/s00498-018-0224-2

- 沿用 R28 的正式可见附录 Lemmas 6.5–6.6、Proposition 6.7 与
  Lemma 3.6 收束范围；6.7 下估计援引 analogous argument，
  不写成该处完整详证。作者稿 arXiv:1711.01181v2 印刷页4–5、
  10–11 及此前 §6.2 实际范围不扩大。正式主文仍未全篇读取。
- 图变换与体积方法是已有工具，原文双向受控不变集、固定容差
  体积框架不自行给出本稿收缩至一点时随时域变化容差的谱。
  本次未新用图变换结果；R27 实际几何已在采用链中证明。

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of
invariance entropy dimension. *Journal of Differential Equations,
453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

- **陈虎.pdf 已在 R21 全文核验**，24 页、841646 字节，SHA-256
  `8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`。
  全文取得状态不变，本轮不再要求寻找，不重复读取整篇。
- 沿用指定不变分划、圆柱、时间 α 次归一、测度变分原理及
  R21 的逐项证明比较。改变时间归一的覆盖结论不自行给出
  任意近似输入下 δ_n 精度与真实初态的相等关系；R29 需要的
  物理连接由 R27 已证。并非仅凭术语不同排除覆盖。

## 4. 本轮增量与新颖性边界

| R29 内容 | 覆盖/归属 |
|---|---|
| 有限叶词的频率—成本约束 | 经典停止尺度及类型计数；自含上界。 |
| 正半径、全部中间时刻与首次真错控制 | R27 已证实际几何；本轮恢复并核验实际依赖。 |
| 较短前缀匹配任意精度指数 | R27 物理引理的新推论推导，非新结构机制。 |
| 三段谱及 ln2 饱和点 | 经典熵优化；本轮完成求值，不主张计算工具首创。 |
| 任意近似输入的准确真实率 | 由以上受控几何与计数合成；已读外部范围未自行提供这一连接。 |

这份记录没有认证全领域首创。正式未读范围继续限制全面覆盖
及更高期刊判断。没有新增原件需求或具体覆盖风险，故不为
本次自含计数追加两篇论文，也不重做广泛检索。
四大研读未在 R29 调用逆熵/卷积定理；其记录原样保留。
不使用未核实的分区体系、年份或成功率。
