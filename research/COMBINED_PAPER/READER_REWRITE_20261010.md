# P6 面向读者的全文结构性改写

基线为 main `4daf068c7d31a245a6406b504ddbf4e1249a0761`。开始及提交前回查均未见后续远端提交。本轮按用户授权单代理执行，只处理 P6；没有新研究、投稿或对外联系。唯一现行稿为 [完整英文 TeX](../../paper/P6_PRECISION_COST.tex) 和 [37 页 PDF](../../paper/P6_PRECISION_COST.pdf)。

## 实际改动

摘要及引言围绕精度—可靠性问题重写。§1.1 先用已有线性模型说明三角形、斜率坐标、两个控制的可行区间，以及“一个词服务的角区间变窄，但半径同时缩小”；随后区分沿整条轨迹的距离限制与初态集合的失败概率。原来的熵—混沌问题在引言交代关联，在附录 D 保留完整比较，不再与正文主线争夺中心。

§2 先定义目录及假设，再给全覆盖谱与可靠性定理。原 Theorem 2.3、Corollary 2.4 改为 Theorem 2.1、Corollary 2.2；原 Theorems 2.1、2.2 改为 2.3、2.4。原面积工具 Theorem 2.5 移至 §4，现为 Theorem 4.1。词的两种乘积推迟至 §3；Taylor 常数的具体选择完整移到附录 E，正文保留可调用估计及条件。

§§3–7 按各步承担的数学任务重写叙述：移动曲线及链式求导、首真越界、固定紧集选择、任意输入面积界、耦合角径向构造、停止树、概率运输、正面积强制区域和罕见词族。§8 拆成源/目标区间、光滑插值、平面控制、不可舍弃质量、逆面积成本五步，解释构造参数为何同时服务于质量差异和二阶光滑性。§9 与附录保留实例及证明，讨论集中说明已经证明的范围及尚无答案的范围。

## 几处关键前后对照

以下均摘自本稿自己的旧、新版本；省略号表示只展示相关片段。

| 位置 | 旧文片段及具体障碍 | 新文片段及改动作用 |
| --- | --- | --- |
| 引言 → §1.1 | “Their first derivatives induce complementary angular branches of relative lengths…”：读者尚不知道角坐标及哪个输入服务哪个状态，就要理解分支和匹配条件。 | “For s>0, write y=z/s.” 随后给两个控制的坐标变化表及区间，再解释 “Long words serve narrow angular intervals, but their states are also close to the origin.” 用实际模型建立两种尺度的关系。 |
| §3.2 | “Consider a radial graph s=S(y)…”：直接引入图，未说明原来的直纤维为什么不够。 | “An initially horizontal fibre usually becomes curved after one control.” 先说明对象为何出现，再解释对数斜率及链式求导各项的用途。 |
| Lemma 5.1 证明 | “We then solve the perturbed angular and radial recursions together…”：只预告操作，未解释为何需要联立。 | “The radius depends on the candidate angular sequence, so an angular inverse iteration alone is insufficient.” 接着按候选角序列生成半径，再说明修正算子及收缩估计。 |
| §8.1–8.2 | 旧文虽说明第一步改变质量，但立即进入 B₀、B₁、端点及两套收缩比例；比例和 C² 要求的关系要读者自行回推。 | “The target lengths must also decrease fast enough, relative to the source lengths…” 提前说明比例选择的两个任务；积分段再说明连续候选导数为何还必须确认为 g 的导数。 |

这些修改解决具体的阅读入口和逻辑衔接；并不构成新增数学贡献，也不能据此宣称真人读者已经读懂。

## 五篇 JDE 原文的具体参照

沿用已取得并核过身份的全文副本：前两篇正式版，后三篇作者版本。本轮定向回读下列段落，不冒称重新通读五篇全文。页码均为这些副本的 PDF 页码；完整版本来源与身份记录见 [此前报告](MATH_STYLE_REVIEW_20261010.md)。没有仿写原句。

| 文章及 DOI | 本轮回读位置与组织特点 | 落实到 P6 的改写 |
| --- | --- | --- |
| Nie–Wang–Huang (2022), *Measure-theoretic invariance entropy and variational principles for control systems*；10.1016/j.jde.2022.03.013 | pp.3、9：先交代研究对象与问题关系，再引入支持目标公式的工具。 | §1 具体控制任务先行；面积工具移出主结果区，置于 §4 的实际用途旁。 |
| Chen–Huang–Zhong (2026), *Variational principles of invariance entropy dimension*；10.1016/j.jde.2025.113819 | pp.4、11：定义后紧接所用划分性质；Frostman 工具的任务与来源明确。 | §3 词乘积出现时交代几何作用；§5 先说强制输入的用途，再给引理和构造。 |
| Colonius–Cossich–Santana (2020), *Bounds for invariance pressure*；10.1016/j.jde.2019.11.091 | 作者稿 pp.2、11：区分上下界的任务；先明确单个输入服务的集合，再作体积估计。 | §§4.3、7.3–7.5 围绕“一个任意输入能覆盖多少”解释下界，不从公式堆叠开始。 |
| Wang–Chen–Lin–Wu (2020), *Bowen entropy of sets of generic points for fixed-point free flows*；10.1016/j.jde.2020.07.008 | arXiv v2 pp.3、17–18：问题与已知结果先于定理；下界先固定正质量集合再处理任意覆盖。 | §4.2 解释先选同一紧集的必要性；§§6.3、7.3 区分固定质量与随时间变化的失败集合。 |
| Chen–Dou–Zheng (2022), *Variational principles for amenable metric mean dimensions*；10.1016/j.jde.2022.02.046 | arXiv v4 pp.3、18、26、29：交代技术障碍，区分主证明和附录计算，并将覆盖具体用于编码。 | §1.2 说明非线性困难；§§6–7 解释停止词如何成为实际目录；常数核算移至附录 E。 |

具体差距仍在：本稿同一套几何需同时处理半径、角度、实际越界和覆盖质量，§3.2、Lemma 5.1、§8.2 仍比上述选读段落更密。此次增加了作用说明和分段，但未删掉必要推导；这些段落是否达到导师要求，仍需作者按目标读者标准判断。

## 六项结果完整保留

旧位置指本轮 35 页基线，新页码指当前 37 页 PDF。

| 结果 | 旧位置 | 新位置与适用范围 |
| --- | --- | --- |
| 逆面积指数下界 | §8.4 / Cor.8.1，p.23 | §8.5 / Cor.8.1，p.25；固定 Cantor 反例与指定指数失败预算，对任意满足条件的可测窗口。 |
| 角依赖径向例子 | §9.2，p.25 | §9.2，p.27；非奇异例子，匹配时适用两条主定理，失配时保留附录 A 范围。 |
| 内部可行折叠 | §9.3 / Prop.9.1，pp.25–27 | §9.3 / Prop.9.1，pp.27–29；真实内部可行碰撞，零面积临界集；不声称可靠性公式。 |
| 远处塌缩 | §9.4 / Prop.9.2，pp.27–28 | §9.4 / Prop.9.2，pp.29–30；正面积初态集零成本，全 Q 低精度准确率及高侧上下界。 |
| 匹配线性有限时域概率比较 | App.C，pp.31–33；Lemma C.1，p.32 | App.C，pp.33–34；Lemma C.1，p.34；匹配线性系统，常数独立于时域和两项预算。 |
| arsinh 正熵与可行状态收敛 | App.D，pp.33–34；Prop.D.1，p.33 | App.D，pp.34–36；Prop.D.1，p.35；固定容差的精确、外及跟踪熵；只断言无限可行状态一致收敛。 |

## 验证及剩余限制

从定义、假设及量词连续核读完整 TeX 和最终正文，重点重查：同一紧集在精度及序列之前选择；固定块长后取时域极限；常数对词、时域及两预算的一致性；首真越界与再进入；概率下界不能将 O(δ) 误差直接当成允许的失败概率；Cantor 强制性覆盖整个物理区间；正文与附录的调用范围。未识别出需要改变正式数学结论的证明错误。发现并修正一处真实记号冲突：Cantor 根区间与第一层地址 0 的区间原同写 J₀，根现写 J∅。另补明坐标分量及最终角映射的定义。

20 项正式陈述的数学正文保持原文；只改三项引理的说明性标题并调整位置。保留 17 段 proof、全部 136 个旧标签及 13 条文献，新增一个附录标签。上述计数仅是遗漏检查，不代替证明核查。编译收敛，无未定义引用、LaTeX 警告或 overfull/underfull 提示；对 37 页逐页查看了渲染图，未见溢出、遮挡、缺字或错误引用。未做真人读者测试，不给 AI 检测分数。

Wang–Huang (2022), DOI 10.1088/1361-6544/ac4f33 的直接全文覆盖缺口仍在。本轮有限次重查未取得正式 PDF 或身份明确的作者全文，没有根据摘要确认新颖性，也没有以继续检索拖延改写。一般失配高侧、任意正面积紧集高侧、折叠可靠性、塌缩高侧及 Cantor 准确可靠性谱/极限仍保持原限制；未重启暂停研究。真实作者信息、人工数学复核、稿件及 AI 披露批准仍待作者确认，原 AI 披露逐字保留。

35 页基线的 [TeX](https://github.com/khdzg5shnt-rgb/p6sida/blob/4daf068c7d31a245a6406b504ddbf4e1249a0761/paper/P6_PRECISION_COST.tex) 与 [PDF](https://github.com/khdzg5shnt-rgb/p6sida/blob/4daf068c7d31a245a6406b504ddbf4e1249a0761/paper/P6_PRECISION_COST.pdf) 保留在 Git 历史中；原稿、研究目录与旧报告均未覆盖。完成普通提交、远端回读后停止。

最终文件 SHA-256：

- TeX：`487dad7c8e349a893cb4f04a499898d409019d1ac2c954bb074833af242b3b07`
- PDF：`adc825c49ac728ea4e72367a63fdb5acddb2c7ba97e88842c8aaa08436e471ad`
