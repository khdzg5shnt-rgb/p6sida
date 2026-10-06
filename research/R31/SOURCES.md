# R31：来源、实际读取与覆盖范围

2026-10-06 UTC。基线
`134b7f949173a3182795db449ffa0247e1954c89`。
证明自含；没有新增第三方论文下载或广泛检索。两项直接比较
对象沿用R21/R30，其余仅为既有方法背景。未读正式正文不记为
已排除覆盖，不认证全领域首创。

## 1. 项目内实际读取和归属

全文读取CURRENT、paper/P6_PRECISION_COST.tex、R30的REPORT/
SOURCES/NEXT_COMMAND，以及R21、R27、R29完整相关数学笔记。
采用文件按R30最终SHA远程取回，实际推导用完整正文核对，
历史PASS等判断不作为正确性前提。

| 来源 | 实际采用及边界 |
|---|---|
| R21 §§2–8 | 两乘积、典型面积、停止长度及相对熵；其半径自主、满像区间和中点树比较不能直接推广 |
| R27 §§2–7；现稿 §§3–5 | Taylor、图锥、截断区间、首真越界、有限瞬态、全部可行前缀典型性及耦合有界串；按不同径向常数逐项验证 |
| R29 §§2–4；现稿 §6 | 完整尾部、固定L后取时域极限的较短物理前缀；只证明授权低精度范围，不另攻完整失配谱 |
| 现稿Theorem2.1 | 同一全域条件下的匹配正向结果，与Corollary31.3充分侧对照；该充分侧也由本轮估计直接推出，R31尚未收入论文 |

图变换、Taylor误差求和、Borel–Cantelli、Egorov、停止尺度、
类型计数和相对熵均为经典工具。本轮新增是这些工具在指定
实际反馈假设下的加权连接及一般类失配结论。

## 2. 两项直接原文比较

### Chen–Huang–Zhong：已取得的正式原件

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of
invariance entropy dimension. *Journal of Differential Equations,
453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

原件为陈虎.pdf，附件路径project_sources/06-pdf。本轮核对封面、
24页、841646字节及SHA-256：
`8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`。
作者、卷年2026、文章号和DOI与封面一致；DOI中的2025不是引用
年份。所有页可提取非空文本，已取得的正式全文状态不变。

R21已全文读取1–24页；本轮定向重读第1页、7–14及20–24页，
不冒充重新完成整篇独立证明重建。具体比较如下。

| 原文位置 | 已有内容 | R31仍需证明的连接 |
|---|---|---|
| Lemma2.11、Theorems2.12–2.13，pp.7–9 | 指定圆柱的选取及局部测度到覆盖比较，所印证明已读 | Au来自任意近似输入；须先推出δλ_w/P_w实际越界带，才能应用质量到覆盖逻辑 |
| Proposition3.1，pp.9–11 | 同一圆柱家族的加权和普通覆盖比较 | 不比较实际角向/径向双尺度，不证明近似输入可以换成精确控制词 |
| Lemma3.2、Theorems3.3–3.4，pp.11–14 | clopen分划Frostman和变分方法及所印相关推导 | 不给耦合半径的图结构、物理错控制余量或完整尾部 |
| §4，pp.20–24 | 允许遗漏测度的覆盖及逆变分关系 | 原文δ不是欧氏容差；未给先于全部δ_n选定的物理紧集及这里的准确成本 |

不只凭定义不同排除覆盖：本轮确实采用同类“质量约束目录数”
逻辑和经典典型集方法。额外的动力学事实是MATHEMATICS中的
(31.12)、(31.15)、(31.25)–(31.29)。所读原文没有这些物理几何
估计；先独立证明它们才连接实际目录。测度不必不变不是区别。
没有要求用户再找原件。网页访问限制不改变已取得PDF的状态。

### Yang–Chen–Yang–Zhou：压力背景

Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen’s equations
for invariance pressure of control systems. *SIAM Journal on
Control and Optimization, 63*(2), 1104–1128.
https://doi.org/10.1137/23M1607684

本轮核对[SIAM官方记录](https://epubs.siam.org/doi/10.1137/23M1607684)：
Rui Yang、Ercai Chen、Jiao Yang、Xiaoyao Zhou四位作者、63(2)、
1104–1128、DOI及2025年一致。当前网页题名、摘要和元数据已读，
不把此页面记作正式正文全文。

正文复用已读作者稿arXiv:2309.01628v3的介绍、Theorems1.1–1.4、
§3.1成本阈值定义及Proposition3.5所印证明，其他既有范围沿
R21/R30。本轮没有下载或扩大正式主文阅读范围，正式全文未读
的限制保留。

指定不变分划的成本压力及Bowen方程是已有框架。D和停止树
P_w^D恒等式不声称新颖；有限二子权重证明自含。已读范围不
替代Au的实际越界带和正半径错输入余量，未读正式部分不作
等价覆盖已排除的结论。

## 3. 其他复用背景及准确APA

1. Chen, Z., & Zhong, X. (2024). Invariance complexity and
   equi-invariability for control systems. *Journal of Mathematical
   Analysis and Applications, 539*(2), Article 128533.
   https://doi.org/10.1016/j.jmaa.2024.128533
   已有16页正式原件；Definitions2.10–2.11、Theorems2.12–2.13、
   Corollary2.14的实际范围沿R28/R30，本轮未重新全文读。
   outer catalogue是已有对象，固定容差框架不自行量化联合率。
2. Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class
   of partially hyperbolic sets. *Mathematics of Control, Signals,
   and Systems, 30*, Article 18.
   https://doi.org/10.1007/s00498-018-0224-2
   图变换、锥和体积归已有方法。正式附录及作者稿
   arXiv:1711.01181v2真实范围沿R30；本轮无新正文读取。
   正式主文未全文读取，未读部分不记为已排除覆盖。
3. Hutchinson, J. E. (1981). Fractals and self-similarity.
   *Indiana University Mathematics Journal, 30*(5), 713–747.
   https://doi.org/10.1512/iumj.1981.30.30055
   作者文本§2.1、§§5.1–5.3范围沿R30，正式全文未全部审查。
   停止尺度及乘积权重为经典；仅使用自含二子恒等式。
4. Csiszár, I. (1998). The method of types. *IEEE Transactions on
   Information Theory, 44*(6), 2505–2523.
   https://doi.org/10.1109/18.720546
   身份和DOI沿已核记录，正式正文未全文读取。二项式界和相对
   熵在本轮自含证明，不以未读正文证明新颖性。

WHS2019/NWH2022原件与真实范围按R30保留，没有重新审计或标
缺失。没有依赖有问题的时变共轭公式。四大研读无新增阅读或
逆熵定理调用，其启发不等于四大成果分量。

## 4. 覆盖和定位边界

已读材料提供经典工具和目录框架，尚未直接给出本轮任意近似
输入的反馈几何。完成范围比较不等于认证全库首创。R31是
R21与R27–R29的实际加权结构连接，没有新增热力学原理。
没有核实分区体系或年份，也未作一区/TOP声明或给录用概率。
