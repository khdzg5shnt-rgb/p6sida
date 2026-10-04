# DCDS 终稿审阅与条件式投稿准备

2026-10-04。执行用户本轮明确授权；开始时最新 main 为 `06744e0feb17c2f4dbd88abb966fc638c2586586`，与恢复点一致。本地 40 个仓库文件逐一与远端 Git blob 核对一致，未发现适用 AGENTS.md 或后续完成项。全文读取 CURRENT、STAGE_PAPER_DECISION 和唯一论文源码，并检查对应 PDF。没有启动 R08、分派代理、投稿或联系他人。

## 裁决和实际变化

**维持可向 DCDS 作条件性尝试的判断。** 这次有界核验未发现需要撤下主贡献的数学错误，也未在实际审读的直接文献中发现等价覆盖。具体贡献仍是 Theorem 2.2 的精度成本分裂及其真实控制几何证明。有限系统类和一般初始集未分类，仍使成果分量存在编辑判断风险；数学核验不等于录用判断。

本轮新增了一项直接文献归属：Chen–Zhong 2024 已经使用同一种有限时域近似控制目录，并研究固定容差下的有界复杂度。正文现在明确写出两套记号的精确对应，不能把目录定义、允许离开 Q 或固定精度的有界性当作首创。这项补核没有提供本文的匹配对角极限、任意近似控制的停止树比较或近满面积紧集的严格成本分裂。

已在同轮完成实用投稿准备：唯一稿改用 `amsart`，标题按句式大小写、公式编号置右，增加首页 MSC2020 和关键词，参考文献依 AIMS 样式按作者排序，压缩重复限制说明，加入真实 AI 用途披露；另有完整附信草稿和简短材料清单。**没有新增数学定理，也没有借格式修订上调期刊档次。**

## 证明核验的具体边界

实际重新检查的是稿件 §§2–7 的完整证明链，不以历史记录代替推导：

- **Proposition 3.1 / Theorem 2.2(ii)：** 任意控制第一次选错分支时，由欧氏邻域得到单侧带；停止叶尺度和 `ρ_i<1/2` 给中点间距，所以每个控制仅覆盖 `1+Bn` 个见证。下界只用必要条件，不要求近似轨迹继续精确可行。上界的共同范数收缩覆盖整段尾部；含开集 K 内使用固定半径的完整子树。
- **Theorem 2.2(iii)：** 先从几乎处处等频率，经 Egorov 与内正则性选定一个紧 E，再对每个 ζ 取得统一前缀界。K 的选择不依赖 γ、精度序列或 ζ。对每条任意控制，首次偏离带的总截面测度满足式 (5.5)，Fubini 与匹配前缀上界给 G；没有把随 n 变化的高测度集合替代同一个 K。
- **Theorem 6.1：** 共同半径使全时域可行初值截面为区间；导数乘积下界在整个区间上成立。先截断 `s≥s_0` 保留正面积，再对任意中间时间作估计。精确控制块、统一小半径入口和局部共同 Lipschitz 常数一起控制完整尾部；`ρ=1`、临界 `ρq=1`、`γ=0,∞` 均在证明中处理。
- **Proposition 7.1：** 循环最低点旋转只使用总增量非负，不套用整数循环引理的精确计数。临界前缀保证任意控制在每个首次偏离位置只覆盖至多三个格点；快尾部 `1^∞` 给全时域上界。`0^∞` 的实际发散仍明确展示，不能把此例说成保留所有输入收敛的推广。

Theorem 6.1 的严格内向余量、共同 R 和小非线性项，与 Theorem 2.2 的不重叠二进制分支及控制依赖收缩没有互相包含关系。完整假设和所有结论保持原样。源码逐段比较确认：§§2–7 除新增的文献记号对应及末尾范围说明两段外，与恢复点一致；本轮的正确性判断来自上述重推，而不是“没有改动”这一事实。

## 直接覆盖补核与来源

本轮补核对象不超过两篇：一篇使用数据源中已提供的正式 PDF，另一篇仅更新正式摘要/引言范围的检查。其余文献复用 [STAGE_PAPER_DECISION.md](STAGE_PAPER_DECISION.md) 所列 13 条 APA、DOI、版本和实际阅读范围，未重复获取失败原件。

**Chen, Z., & Zhong, X. (2024).** Invariance complexity and equi-invariability for control systems. *Journal of Mathematical Analysis and Applications, 539*(2), Article 128533. https://doi.org/10.1016/j.jmaa.2024.128533

正式身份由出版社条目与用户原件第一页交叉核对。原件 `1-s2.0-S0022247X24004554-main.pdf`，16 页、441166 字节，SHA-256 `62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc`。实际审读：引言；§2 系统和 admissible pair；§2.1 Definitions 2.1–2.2、Theorem 2.3 陈述与证明；control set 定义及相关条件；§2.2 Definitions 2.10–2.11、Theorem 2.12 陈述与证明、Theorem 2.13/Corollary 2.14/Theorem 2.15 的适用条件；§3.1 Definitions 3.1–3.2、Theorem 3.3 陈述与完整证明；Remark 3.7；§4 两个例子及证明。未重审全部 mean 类型的证明，也不对那些证明作正确性认证。

| 对应位置 | 精确覆盖及限制 |
|---|---|
| 本稿 Definition 2.1 | 其 §2.2 的 `r_inv(n+1,δ,K,Q)` 就是本稿 `r(n,δ;K)`；差一源于 `[0,n)` 与 `0,…,n`。实际初始状态、环境邻域及任意控制均已包含。正文已明确引用。 |
| 本稿 Theorem 2.2(i) 的固定精度行为 | 本系统满足其 Theorem 2.12 的有限字母连续性、紧 K 和 admissible pair 条件。本稿固定 δ 的目录统一有界属于其 bounded outer invariance complexity 框架。该定理没有控制有界常数随 δ 的增长率。 |
| 本稿近满面积 K | 其 Theorem 3.3 刻画有界的测度 exact complexity 与高测度等不变集合。按本稿时域约定，一条 exact 词覆盖面积 `2^(-n)`，覆盖面积大于 `1−ε` 必须至少 `(1−ε)2^n` 条，故这里不满足其有界 exact complexity 前提。它不直接给出本稿较低但仍可为正的对角成本 G。 |
| 非空内部条件 | 其若干进一步等价和二分结论要求 Q 为 control set。本稿半径只能下降，Q 不满足其 Definition 2.4 的近似可达条件。本文也不是这些定理的反例。 |

**Chen, H., Huang, Y., & Zhong, X. (2026).** Variational principles of invariance entropy dimension. *Journal of Differential Equations, 453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

本轮读取 [出版社摘要、引言及分节摘要](https://www.sciencedirect.com/science/article/abs/pii/S0022039625008460)，核对正式卷年及身份。其公开内容说明研究零不变熵系统的 Bowen/packing α-invariance entropy、dimension 与局部测度变分关系。**没有取得和审读本文完整正文，不能写成已经排除其全部覆盖。** 本稿不依赖其定理，也不主张新熵维数或新变分原理；这项有限范围不阻塞已经自含的几何证明。本轮未重复全文下载，亦不以未检索到等价定理认证首创。

对既有最近相关结果的使用保持以下边界：Da Silva–Kawan 2016（DOI `10.3934/dcds.2016.36.97`）提供控制几何、正体积与不稳定增长率的直接专业背景；其正式记录本轮复核，正文范围仍按既有作者版阅读记录。Yang 等 2025（DOI `10.1137/23M1607684`）的分划压力和维数公式、Hutchinson 的停止尺度、Csiszár 的类型方法、Dershowitz–Zaks 的循环方法均属已有工具。Yao 的 exact/outer 分离、Colonius–Hamzi 的稳定化精度、WHS/NWH 的测度框架也不改写为本文发明。WHS2019、NWH2022、Kawan2013 原件仍已取得；已知作者稿与正式版差异缺口保持原记录，没有把它们抹去。

## 官方适配、材料与完成停点

读取 [DCDS 官方入口](https://www.aimsciences.org/DCDS/submitapaper)、其导航指向的 [Guide for Authors](https://www.aimsciences.org/index/GuideforAuthors)、[AI Policy](https://www.aimsciences.org/index/AIpolicy)、[编委页](https://www.aimsciences.org/DCDS/editorialboard) 及 AMS 的 MSC2020。正文动态加载，已读取页面实际调用的公开接口：`/data/news/news-detail-data?newsId=3109`、`3730`、`3881`；编委为 `/editor/editor-list?publisherId=DCDS`。这是核对日的网页内容，不宣称存在单独的“2026 版指南”。

初次投稿无需套录用后的出版社 class；采用其推荐的 amsart 并保留自含源码。附信强调数学问题、主定理、首次偏离几何的用途，没有虚构独占首创或录用把握。官方要求的生成式 AI 披露已如实覆盖证明开发、核查、全文起草与修订，不只写语言润色；没有声明作者已经人工审阅、全体批准或无利益冲突。未知事实集中在 [SUBMISSION_CHECKLIST.md](../../paper/SUBMISSION_CHECKLIST.md)，候选编辑及两篇/12 个月规则也在其中。

最终唯一 PDF 为 12 页。LaTeX 编译无警告、无未定义引用和溢出；59 个标签与 14 条文献全部解析，文献均有正文引用，摘要 148 词。完成全文文本对应与逐页图像检查，公式右编号、主结果、证明续页和末尾声明/文献均可读。数学段落差分用于防止适配时意外改动，不能代替证明。PDF SHA-256：`d076182f38ba39aabedb293b821ee9e2cdda56249c9566cd948c566cb5a88471`。

本轮停在**作者信息及真实声明待确认的投稿准备稿**。下一步只补齐清单里的事实、完成人工审读、在同一源码中定稿并重新核对 PDF；不需要再造一轮审计或扩展模型。是否实际投稿仍由用户另行决定。original/、原阶段裁决及 R01–R07 既有文件保留，原稿 SHA-256 仍为 `47aa42836d78fa281d1ef18e1fbb20d5d311eeab0959077f775542b61249b869`。提交后回读全部修改文件和完整 PDF，并与本次核验的本地文件逐字节比对。
