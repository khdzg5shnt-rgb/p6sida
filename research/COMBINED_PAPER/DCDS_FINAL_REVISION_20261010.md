# P6：十篇 DCDS 全文对照与实质修订

本轮基线：`f510c91c5baadab6149bbca8d81bcb487c957cbf`（37 页）。现行文件仍为 `paper/P6_PRECISION_COST.tex` 及对应 **34 页 PDF**。单代理完成，只处理 P6；没有新研究、投稿或联系他人。文件名沿用此前轮次的日期标记。

本稿的中心是指定二分支收缩系统中的**精度—可靠性目录率，以及面积失真使该率转移失败的机制**。全覆盖谱、固定初态集与全体初态的差别提供精度侧基础；无临界点的概率上界、正面积强制前缀和单射 Cantor 反例构成可靠性侧的主要内容。二元类型计数、相对熵优化和体积下界方法是经典工具，不因本轮行文改进变成新的数学贡献。旧熵—混沌问题只保留为问题来源。

**判断：本轮解决了几项明确的阅读障碍，不能据此宣布“超过十篇”或导师的问题已经解决。** 新稿的线性模型入口具体；§3.2、Lemma 4.1、Lemma 7.2 及 §8 与 Appendix D 的连接仍需要专注阅读。没有真人读者测试，也没有 AI 检测分数。

## 内容取舍及完整性

| 内容 | 37 页基线位置 | 本轮去向与理由 |
| --- | --- | --- |
| 逆面积指数下界 | §8.5，Corollary 8.1，p.25 | **保留正文 §8.5，Corollary 8.2，pp.23–24，陈述 p.24**。它解释固定面积损失为何不能替代指数失败预算，直接支撑主线。 |
| 角依赖径向例子 | §9.2，p.27 | **Appendix C.1，pp.29–30**。检验几何估计并未假设径向独立，但不是推导目录率的步骤。 |
| 内部可行折叠 | §9.3，Proposition 9.1，pp.27–29 | **Appendix C.2，Proposition C.1，pp.30–31**。保留临界集假设的真实适用范围；不把未证的折叠可靠性写成结论。 |
| 远处塌缩 | §9.4，Proposition 9.2，pp.29–30 | **Appendix C.3，Proposition C.2，pp.31–33**。保留说明局部线性数据不足的反例及完整证明，与主定理的正向证明分层。 |
| 匹配线性有限时域概率比较 | Appendix C，pp.33–34，Lemma C.1 p.34 | **Appendix A，pp.26–27，Lemma A.1 p.26**。保留为联合预算的有限时域解释，常数不依赖两个预算及 horizon 的结论未删。 |
| arsinh 正熵与可行状态收敛 | Appendix D，pp.34–36，Proposition D.1 p.35 | **移出现行稿，完整保存在 37 页归档的原 Appendix D**。它只要求可行轨迹收敛，采用不同径向收缩及三种固定容差熵定义；不是当前全输入共同收缩类的概率结论或证明依赖。 |

此外，旧 Appendix B 的控制字母表比较移入同一完整归档：它比较改变控制集合后的有限时域计数，另起一个模型，不能回答当前固定二分支的两个预算。摘要、引言、结尾及交叉引用同步撤去对这两部分的承诺。它们不是因页数或难度被删。

主线顺序改为：具体模型 → 定义与结果 → 局部几何 → 强制前缀 → 全覆盖谱 → 面积与固定初态集 → 概率率 → 反例。原面积 Theorem 4.1 改为工具 Proposition 6.1，假设、量词及估计不变。Corollary 2.2 的重复分段差值式合并为 `Δ=S−min{h,γ/β}` 并保留零区间、严格正区间、饱和值。匹配判据仍完整位于 Appendix B：它说明主线所用匹配假设的作用，不是另开问题。

Cantor 插值由旧 §8.2 提炼为 Lemma 8.1（p.22），完整证明移到 Appendix D（p.33）。正文先给所需区间对应、导数性质，再检查平面控制和概率质量；附录保留间隙积分、两阶导数识别及端点拼接。正文没有省去调用条件。向内变形例子保留为 §9（pp.24–25），因为它直接检验区间可截断、固定半径截面可空的主证明情形。

精确归档位于 `paper/archive/`：35 页文件对应 `4daf068c7d31a245a6406b504ddbf4e1249a0761`，37 页文件对应本轮基线，均与祖先提交逐字节一致。原始稿及各轮数学笔记、旧报告没有改动。

## 十篇正式身份与实际阅读版本

以下均为 **Discrete and Continuous Dynamical Systems 主刊，ISSN 1078-0947**。正式卷页与作者次序核对出版社记录；实际阅读全文的是以下明确身份的作者版本，**不声称与出版终版逐字相同**。共 241 个 PDF 页面，逐篇从头至尾阅读，并精读下一表所列证明。页码均指所读 PDF 页码；Kawan 的正文印刷页码比 PDF 页码少 2。全文阅读不等于对十篇所有数学论证进行了独立审稿。

选择含三篇直接控制熵工作，以及七篇熵、尺度增长、饱和集或构造性反例工作；后者发表于 2017–2026 年，体量 12–29 个作者版页面。直接控制文献较早但不可用近期的泛相关论文代替。部分初选全文地址失效后选取了范围内替代文献，没有把摘要或局部可读的候选计入十篇。URL、完整出版社元数据、版本备注和文件 SHA-256 见 [来源记录](DCDS_SOURCES_20261010.json)。

1. Kawan, C. (2011). Upper and lower estimates for invariance entropy. *Discrete and Continuous Dynamical Systems, 30*(1), 169–186. https://doi.org/10.3934/dcds.2011.30.169 。所读：[作者预印本 Nr. 30/2009](https://d-nb.info/1077698828/34)，28 页（含 2 页封面）；封面 2009-11-04、正文日期 2009-09-21。它早于正式版，不能据此声称读过终版增加的内容。
2. Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97 。所读：[arXiv:1408.2416](https://arxiv.org/pdf/1408.2416)，45 页；页边标 v1、2014-08-11，内文标题日期为 2018-07-18。保留这两个实际日期，不自行解释版本冲突。
3. Colonius, F. (2018). Invariance entropy, quasi-stationary measures and control sets. *Discrete and Continuous Dynamical Systems, 38*(4), 2093–2123. https://doi.org/10.3934/dcds.2018086 。所读：[arXiv:1705.08658](https://arxiv.org/pdf/1705.08658)，31 页；页边 v2、2017-11-27，内文日期 2018-10-11。正文引用明确标为作者版的定理编号。
4. Dou, D., Fan, M., & Qiu, H. (2017). Topological entropy on subsets for fixed-point free flows. *Discrete and Continuous Dynamical Systems, 37*(12), 6319–6331. https://doi.org/10.3934/dcds.2017273 。所读：[南京大学作者 PDF](https://math.nju.edu.cn/DFS/file/2020/02/24/20200224190353307hud9hh.pdf)，15 页，无版次日期；以作者出版目录核实身份。
5. Wolf, C. (2020). A shift map with a discontinuous entropy function. *Discrete and Continuous Dynamical Systems, 40*(1), 319–329. https://doi.org/10.3934/dcds.2020012 。所读：[arXiv:1803.02440v1](https://arxiv.org/pdf/1803.02440)，2018-03-06，12 页。
6. Wang, Y., Chen, E., & Zhou, X. (2022). Mean dimension theory in symbolic dynamics for finitely generated amenable groups. *Discrete and Continuous Dynamical Systems, 42*(9), 4219–4236. https://doi.org/10.3934/dcds.2022050 。所读：[arXiv:2103.14817v1](https://arxiv.org/pdf/2103.14817)，2021-03-27，21 页。
7. Hou, X., Tian, X., & Zhang, Y. (2023). Topological structures on saturated sets, optimal orbits and equilibrium states. *Discrete and Continuous Dynamical Systems, 43*(2), 771–806. https://doi.org/10.3934/dcds.2022169 。所读：[arXiv:2012.09482v2](https://arxiv.org/pdf/2012.09482)，2021-07-27，29 页。
8. Zhang, W., Ren, X., & Zhang, Y. (2023). Upper capacity entropy and packing entropy of saturated sets for amenable group actions. *Discrete and Continuous Dynamical Systems, 43*(7), 2812–2834. https://doi.org/10.3934/dcds.2023030 。所读：[arXiv:2112.07425v1](https://arxiv.org/pdf/2112.07425)，页边 2021-12-14、内文 2021-12-15，25 页。预印本作者次序为 Ren–Zhang–Zhang，上述 APA 采用正式版次序。
9. Kucherenko, T. (2024). Nonlinear thermodynamic formalism through the lens of rotation theory. *Discrete and Continuous Dynamical Systems, 44*(12), 3760–3773. https://doi.org/10.3934/dcds.2024077 。所读：[作者网站 PDF](https://tamara.ccny.cuny.edu/publications/Nonlinear%20Thermodynamic%20Formalism.pdf)，17 页，无版次日期；从作者出版目录核实身份。
10. Burgos, S. (2026). On the structure of the Birkhoff-irregular set for subshifts of finite type. *Discrete and Continuous Dynamical Systems, 49*, 248–265. https://doi.org/10.3934/dcds.2025167 。所读：[arXiv:2410.23487v2](https://arxiv.org/pdf/2410.23487)，2025-03-13，18 页。正式卷年为 2026，在线发表为 2025-10-17；不把出版社元数据的占位 issue 0 写成期号。

## 逐篇比较如何落实

表中同时考察摘要与引言、定义与结果安排、证明动机与符号、例子与收束。比较的是可观察的表达和阅读负担，不是期刊身份带来的评分。旧稿指 37 页基线，新稿指本轮 34 页稿。

| 参照与具体依据 | 旧稿障碍、已落实修改、仍有差距 |
| --- | --- |
| **1 Kawan**：摘要/引言 PDF pp.3–5 先给上下界及各自工具；Theorem 12 pp.16–21 分局部化、覆盖、缩放；Theorem 14 pp.22–24 从一个控制服务的集合估体积；Remarks 16–17 pp.24–25 紧邻估计说明适用边界。例子检验界，预备符号较长。 | 旧 §4 先进入逆像与典型频率，读者尚未见完整全覆盖证明。新 §6 先说明“单输入最多服务多少面积，便至少需要多少输入”，推迟概率工具；§5 先完成全覆盖。新引言的数值词例比该文的抽象入口更具体，但本稿双预算与所有可行编码的一致性仍更费力；不能因预印本较长就认定本稿更清楚。 |
| **2 Da Silva–Kawan**：pp.1–2 摘要/引言先区分上界改进和体积下界；p.7 解释为何近似一般轨道；Volume Lemma pp.19–30 分九步，pp.27–30 图像、体积、Fubini 的作用清楚；Theorem 4.8 pp.32–35 先固定初始时间再取率。pp.3–5 符号表及 p.21 常数仍重，末尾未给工作数值例。 | 旧稿也有分段，但常数与目标联系弱。新 §3.2 解释径向图为何进入角导数，Lemma 4.1 先解释耦合算子；§6.3 先按首次退出分类。没有仿照其大符号表。P6 的可算线性/非线性例子是入口优势，证明分层较接近；该文一般双曲理论任务不同，不能总体排序。 |
| **3 Colonius**：pp.1–2 区分状态准平稳测度和控制分布；定义集中于 pp.3–8，Theorem 2.13 pp.9–11 保持运输测度；coder-controller pp.13–16 是另一任务；Lemma 4.2 / Theorem 4.3 pp.16–20 先把状态送入内部集合；Examples 5.12–5.13 pp.29–30 对应控制集结论，结尾问题具体。 | 旧文献段把多种概率熵并列，未充分解释不可直接套用之处。新 §1.3 明确本稿比较两个系统各自的均匀面积，非运输后同一测度；§2.4 只说明一次索引，删除重复解释。定义入口比其完整准平稳框架轻，但本稿移动失败预算需要额外一致性，仍不能由这些比较确认新颖性。 |
| **4 Dou–Fan–Qiu**：p.2 引言区分已有四步证明与流的时间重参数化困难；Lemmas 3.2–3.5 pp.5–9 逐步建立球的变换与覆盖；§4 pp.9–14 在使用时引入加权熵、Frostman 工具。摘要集中于变分原理，例子不是主线，结束于证明。 | 旧稿重复说明几何“将被用于”多个后续部分。新 §3.3 直接说明只在首次实际退出前可用图像估计，§6.3 接着把三个面积项逐一对应。P6 有直观例子优势，定义与用途的连接改善；源文单一目标的证明链更紧，本稿尚有两个目录问题和一个反例，不能靠减少标题消除其数学负担。 |
| **5 Wolf**：pp.1–3 的摘要/引言聚焦一个连续性失败及两项结论；pp.4–7 先造目标旋转集几何再造势；Proposition 3 pp.7–9 的刚性接到 pp.9–11 的质量分解。简单几何先导与最后证明都围绕同一反例；索引仍密。 | 旧稿 Cantor 动机之后很快进入平滑拼接，机制被暂时打断。新 §8 先写出 `2^k` 个质量约 `b^k` 的区域为什么迫使目录增长，插值实现完整移入附录。新旧稿的例子都可算；新结构更聚焦，但源文围绕一个反例的紧凑性仍明显优于本稿两条正向率与反例并行的任务。 |
| **6 Wang–Chen–Zhou**：pp.1–3 从整数作用的熵—维数公式引向群推广，§2.3 p.7 陈述结果；pp.9–13 区分覆盖及模式数估计；Lemma 4.2 pp.15–16 用误差坐标集解释信息估计；pp.18–19 例子算同一常数。率失真符号正式定义较迟（pp.13–14），不宜照搬。 | 新摘要删去未解释的 `h,β` 固定集公式，新 §1 直接解释每个预算约束什么；§7.5 把物理余量与不可丢弃质量的两条严格不等式分开解释。线性入口与其先讲基例的做法相当；本稿概率失败不是平均失真，不能移植其解释或结论。原稿及新稿的常数层次仍较多。 |
| **7 Hou–Tian–Zhang**：pp.1–5 摘要/引言已有大量公式和应用，并非简洁模板；pp.6–10 定义多种熵及轨道性质。§3.2 pp.11–14 按所构集合的三项性质组织检验，§4 pp.15–19 用嵌套闭集承载极限测度；应用都接同一理论，§6.3 p.27 收束到水平集。 | 旧 P6 末尾把不同收缩体制的 arsinh 比较也并列，统一性更差。移出该体制及字母表例，保留检验当前假设的例子；Lemma 7.2 按可行性、错误控制、面积与分离组织。新稿入口较轻，但该文应用数量来自同一理论，不能把其广度当成可删冗余；高密度构造各有实际数学原因。 |
| **8 Zhang–Ren–Zhang**：pp.1–3 用两个主结果提出群作用问题；pp.3–10 定义长，p.10 交代拼接目标；p.16 解释为何重复最大熵测度以适配两层铺砌，pp.17–18 从分离族到极限测度；§4 pp.20–21 只有相应水平集应用，技术工具证明置于 pp.21–24 附录。 | 新 Lemma 4.2 在组合数前说明固定首尾数字是为了不产生长同符号串；新 §8.2 先给插值工具的全部性质，附录供核算。主干/工具分层较接近。其预印本也有句法和符号负担，不能作为英文质量的统一上限；新 P6 的双预算比较仍需跨节追踪，未因移附录自动变容易。 |
| **9 Kucherenko**：§2.2 pp.3–4 先说明用旋转集把测度优化转成有限维问题；Theorem 1 pp.5–7 把连续性和局部化分开；Lemma 1 pp.8–10 明确边界连续性失效后需要哪种较弱结论；Examples 1–2 pp.12–16 专门检验假设及极限顺序，最后停在反例。 | 旧 P6 限制散见多个总结，例子目的容易混杂。新 §6.2 强调为什么必须先选同一个紧集，§8.5 只问逆面积常数能否次指数，§10 集中列尚未确定的率。例子作用更明确，但源文“一个障碍—所需工具”的连接仍更短；本稿图像估计与两类下界之间尚不如它顺畅。 |
| **10 Burgos**：pp.1–2 从测度零与满熵的反差进入一个四项定理；pp.3–8 定义较长；§4 pp.8–17 逐项验证同一构造，尤其 §4.5 / Lemma 4.7 p.12：双 Lipschitz 不是动力共轭，熵需另证。摘要末尾泛化评价不值得模仿，例子/结尾均服务该构造。 | 新 §1.3 与 §8.3 更明确：全覆盖对应不等于重置均匀面积后的概率对应。旧稿多个末尾主题的聚焦性逊于该文；移出后有所改善。新稿具体初态例更易进入，但尚有强制区域及 Cantor 两套对象，逻辑负担仍大；不宣称其研究任务或数学贡献可用文字风格排名。 |

上述参照落实为内容和证明顺序的改变，没有仿写原句。只有直接影响文献定位的 Kawan 与 Da Silva–Kawan 加入论文参考文献；其余写作参照留在本说明，未为凑十篇扩充论文书目。原先仅作宽泛方法背景的两条引用随相应段落删除。

## 四处关键前后对照

以下英文均取自自己的两版稿，省略部分以省略号表示；不代表源论文原文。

1. **引言的“一条输入服务什么”**。旧 §1.1：“These two scales explain the counting problem. Long words serve narrow angular intervals, but their states are also close to the origin.” 新 §1.1：“the word 01 serves precisely −7/9 ≤ y ≤ −1/3 on each fibre. After two steps these states fill the angular range again, at radius 4s/81.” 原文解释并非错误，但要求读者自己将两个抽象乘积还原成区域；改后可直接核算一条输入的服务范围，四列表同时列可行初始角区间。

2. **面积工具的出场理由**。旧 §4：“The estimates of Section 3 apply near the origin, but a catalogue must serve initial states throughout Q.” 新 §6：“To prove a lower bound on an arbitrary positive-area set K, estimate the area that one input can serve. If this is at most b_n on a fixed subset T ⊂ K of positive area, every cover needs at least area(T)/b_n inputs.” 旧段先解释技术覆盖范围，新段先给最终要用的不等式；移动整个面积部分使全覆盖证明不被暂时无用的 Egorov/逆图工具打断。

3. **耦合轨道为何能构造**。旧 Lemma 5.1 已解释先从候选角序列产生半径、再修正角度，并写道：“The resulting operator will be a contraction.” 但读者要进入估计式才能看出为什么小半径有用。新 Lemma 4.1：“Given a candidate angle sequence, first solve its forward radial recursion. Substitute those radii into the inverse angular equations. The dependence of the radii on the candidate has size O(s_*²), which will make this combined operation a contraction when the initial radius s_* is small.” 公式仍完整保留；补上的理由解释了为何要先求半径，以及两项 Lipschitz 误差中平方量的作用。

4. **Cantor 部分避免先陷入实现细节**。旧 §8：“The total source mass will be too large to discard, while the target dynamics force different prefixes on different intervals.” 新 §8：“If their total mass (2b)^k decays more slowly than e_n, almost all 2^k prefixes are required.” 新正文先给这条定量机制及 Lemma 8.1 的性质，再用它构造控制；旧 §8.2 的光滑拼接全部进入新 Appendix D。相比泛称“质量太大”，读者现在知道比较哪两个量；仍需回附录核对 C²，不能宣称这一困难已消失。

另删除了通信含义的连续重复句、重复差值分段式及结尾对已证公式的再总结；把不必要的 “regular window” 改为普通的 set/compact set。并非统一缩短句子或机械换词。保留必要的首次退出、再进入和测度运输限制，避免删掉真实数学边界。

## 验证范围与剩余判断

从定义重新核对保留定理及证明，重排后连续阅读全部正文和附录。重点核对：同一紧集先于精度指数/序列的选择；有限瞬态中每个导数输入仍在 Q；固定损失与移动失败预算不能交换；强制区域厚化的延拓论证和全点分离；先固定块长再取 horizon 极限；端点用严格类型逼近；Cantor 间隙积分确实给出导数；任意近似输入的首次错误不能由后续再进入补救。

保留陈述的假设、量词及结论逐项与基线对照：未发现需改变正式数学结论的错误，没有缩小结果来换取简短。提炼出的 Lemma 8.1 是原构造性质的集中陈述，不是新增研究。重排时恢复了 §6.4 的匹配参数声明，补回 transient 的首次定义，纠正一处拼接语病和指向前文的错误将来时。证明核查是本轮 AI 辅助核查，不是独立人类数学认证。

编译收敛，无未定义引用、重复标签、LaTeX 警告或 overfull/underfull 提示。**全部 34 页均查看渲染图**，核对正文、公式、页边界、附录、作者状态及参考文献；未发现越界、遮挡或缺字。没有缩小字号、修改页边距来压缩篇幅。页数变化不是可读性证据。

仍然困难的地方：§3.2 的角坐标和移动径向图同时出现；Lemma 4.1 的无限序列不动点需要熟悉一致范数；Lemma 7.2 调用前述图像失真且须处理截断像；§8 的两组区间、质量与径向误差有不同尺度。新稿给了用途与证明分层，但这些段落尚未达到“无需往返”的程度；至少 Kucherenko 的单障碍叙述、Wolf 的单构造聚焦仍更顺。作者需判断目标读者是否接受这组技术负担，以及附录 C 的三个假设测试是否都值得出版篇幅。

**文献限制未关闭**：Wang–Huang (2022), DOI 10.1088/1361-6544/ac4f33，仍未取得可核全文。本轮有界补查后停止重复检索；论文 §1.3 明写这一限制。不能据摘要或十篇 DCDS 的写作比较宣布同时预算结果的新颖性已确认。一般临界集情形的可靠性、Cantor 例准确率及极限、任意固定正面积集高精度率、失配高精度率仍是既有未决边界，没有开启求解。

作者姓名、单位、人类数学审读及稿件/AI 披露的批准仍待真实确认。原有完整 AI 使用披露保留。本次完成普通提交与远端逐字节回读后停止，不自动开启下一轮润色或研究。
