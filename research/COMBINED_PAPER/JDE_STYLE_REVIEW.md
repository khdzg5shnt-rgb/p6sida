# 五篇 JDE 原文参照与 P6 行文修订

日期：2026-10-09（UTC）。开始及提交前 main：`7f6324f013e59af0eee946c36d785e94ec854ef4`。
未发现后续完成项或适用仓库指令。只操作 p6sida；未分派代理、联系他人或投稿。
本次采用26页稿为基线，修改现有唯一 TeX/PDF；结果为27页，不以页数决定取舍。

## 1. 五篇文献、版本和实际阅读

以下均为 JDE 原始论文。前两篇复用正式原件，其余三篇使用核实对应关系的作者稿。
正式书目信息依据出版方记录，并与原件首页、作者稿和作者机构发表目录交叉核对。
作者稿的页码只指实际阅读文件，不冒充正式版页码；未取得的正式正文不记为已读。
各篇均读摘要、完整引言、主要结论及说明、组织安排和末节；没有独立结语的文章不虚构结语。

**NWH2022**

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

- 来源：[出版方](https://www.sciencedirect.com/science/article/pii/S002203962200184X)；仓库已有 `project_sources/10-1-s2.0-S002203962200184X-main.pdf`，正式31页。
- 本次实际全文读PDF pp.1–31（刊页318–348）。重点完整链为§3 Theorems 3.1–3.2、Proposition 3.6、Theorem 3.13及Corollary 3.15，PDF pp.9–20；也读§4平衡态与§5补充讨论。学习从既有控制熵问题进入压力/测度对象，以及技术工具的引入次序；不重新认证该文全部数学结论。
- SHA-256：`e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90`。

**CHZ2026**

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of invariance entropy dimension. *Journal of Differential Equations, 453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

- 来源：[出版方](https://www.sciencedirect.com/science/article/abs/pii/S0022039625008460)；已有“陈虎.pdf”，仓库路径 `project_sources/06-pdf`，正式24页，卷453 Part 1。
- 本次读PDF pp.1–14、19–24。完整核心链：§2.4 Theorems 2.12–2.13，§3.1 Proposition 3.1、Frostman Lemma 3.2、Theorems 3.3–3.4（pp.7–13）；主定理、§4逆变分结论及末尾亦读。**本次未重读pp.15–18的packing构造中段**，不以摘要或既往全文记录替代此次范围。其局部质量到覆盖下界的组织与P6相关。
- SHA-256：`8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`。

**CCS2020**

Colonius, F., Cossich, J. A. N., & Santana, A. J. (2020). Bounds for invariance pressure. *Journal of Differential Equations, 268*(12), 7877–7896. https://doi.org/10.1016/j.jde.2019.11.091

- 来源：[出版方记录](https://www.sciencedirect.com/science/article/pii/S0022039619306254)；[可访问作者稿](https://d-nb.info/1248483715/34)，首页注明2019-09-10、提交JDE，24页。题名、三位作者及主结果与正式发表记录对应；未逐字核正式20页版本。
- 本次全文读作者稿pp.1–24。完整核心链：§4 Theorem 14体积下界（pp.11–12），§5 Lemma 15到Theorem 16线性精确式（pp.13–17）；同时读§3上界、§6应用及末例。单控制实际集合的体积界与P6最直接可比。
- SHA-256：`79d2aee0b11e293f3d3a4eea6eebacceb32b0c1a68eb00d91248de22edebd39d`。

**WCLW2020**

Wang, Y., Chen, E., Lin, Z., & Wu, T. (2020). Bowen entropy of sets of generic points for fixed-point free flows. *Journal of Differential Equations, 269*(11), 9846–9867. https://doi.org/10.1016/j.jde.2020.07.008

- 来源：[出版方](https://www.sciencedirect.com/science/article/pii/S0022039620304022)、[作者机构发表目录](https://www2.scut.edu.cn/ma_en/2025/1113/c5918a609443/page.htm)、[arXiv:1901.02135v2](https://arxiv.org/pdf/1901.02135v2)，2019-10-03，19页。正式版作者顺序为Wang–Chen–Lin–Wu；作者稿首页为Wang–Chen–Wu–Lin，明确保留这一版本差异，不把两者说成相同排版正文。
- 本次全文读作者稿pp.1–19。完整链包括§3非遍历Brin–Katok公式（pp.5–11），§§4–5的泛点集上下界（pp.12–16），以及§6 Theorem 1.4的Billingsley型两向覆盖证明（pp.16–18，覆盖引理按文中引用使用）。参考价值是局部质量、实际覆盖和熵上下界的衔接，不是其流系统直接包含本控制问题。
- SHA-256：`174bdd62ce54444ad7948987c205310d6285701ae8d69c5179651c4fb2091b1d`。

**CDZ2022**

Chen, E., Dou, D., & Zheng, D. (2022). Variational principles for amenable metric mean dimensions. *Journal of Differential Equations, 319*, 41–79. https://doi.org/10.1016/j.jde.2022.02.046

- 来源：[出版方](https://www.sciencedirect.com/science/article/pii/S0022039622001449)、[作者机构发表目录](https://math.nju.edu.cn/en/People/Faculty/20200501/i74445.html)、[arXiv:1708.02087v4](https://arxiv.org/pdf/1708.02087v4)，2020-08-09，36页。题名、作者和变分主结果对应；正式39页版本未取得，不主张正文逐字相同。
- 本次全文读作者稿pp.1–36。完整核心链为§2 Lemmas 2.6、2.8，§3 Propositions 3.2、3.4、3.9，§4 Lemma 4.2、Propositions 4.3–4.4及Claims 4.5–4.6到Theorem 4.1（pp.18–25）；§5和Appendix A结尾亦读。选择它是因为其信息论量必须通过实际几何构造才进入动力学结论，与P6的写作难点相近；并非一般PDE题域凑数。
- SHA-256：`7540008223c2894945c329da6819b9141e8907dc7dd36c4ede5fe600783821f5`。

## 2. 具体参照与已经落实的位置

下表页码为上述阅读版本；P6页码为本次27页PDF。每条记录对应实际正文修改，不仅是建议。

| 参照 | 原文中的具体做法与位置 | P6已落实的两项修改 |
|---|---|---|
| NWH2022 | 引言及§3开头先交代所需测度性质（pp.3、9）；Theorem 3.13证明先说明要建立的对偶关系再作分离构造（pp.18–20） | §1.1（p.2）把两种目录上界和不能仅用指定编码的困难分开解释；Lemma 5.1证明开头（p.11）先说明角向参考轨道、耦合递推与错控制余量各自的任务，再进入不动点计算。 |
| CHZ2026 | 定义后即说明柱集嵌套/分离性质（p.4）；Remark 2.14、Frostman引理前说明及Remark 3.8明确工具来源（pp.9、11、19） | §2.2（p.4）在定义λ_w、P_w后立刻解释其几何职责，并指向§3的实际证明；§1.2（p.3）明确体积目录下界已有归属，区分经典计数与本稿首次真越界、失败质量比较。 |
| CCS2020 | 将构造上界、任意目录的体积下界与相等式分节（§§3–5，pp.9–17）；Theorem 14先定义被单控制服务的实际集合再估体积（pp.11–12） | §7总述及§7.2（pp.15–17）解释S与L_a来自两个可选构造、下界另需质量区域；Theorem 2.5证明开头（pp.10–11）将实际覆盖集分成瞬态退出、精确存活和局部首次退出三类，对应面积式的三个项。 |
| WCLW2020 | 引言指出上下界各自的几何难点（pp.3–4）；§6先保留正质量集合，再把逐球质量转换成任意覆盖下界（pp.16–18） | §7.4（p.17）说明单点见证为何不足、必须加厚成所有点共享强制前缀的区域；§7.5（p.18）解释χ(p)<γ/β控制物理可区分性、I_a(p)<α控制不能丢弃的总质量，再进行块计数。 |
| CDZ2022 | 引言明确旧证明可复用部分和额外铺砌接口（p.3）；定义按使用次序分组，先证明L¹主链、再把平行L∞证明放附录（§§3–5、Appendix A） | §3开头（p.7）直接给出将要证明的两个实际面积尺度，并解释小误差为何可求和；将仅用于失配的γ₀、D移到附录A入口（pp.24–25），主文保留真正反复使用的双产品与χ_R。 |

此外，摘要明确均匀面积及“一次初态选择”的对象；§8开头及§8.1（p.20）先解释双射瞬态为何保全覆盖、为何改变质量，以及λ<b²与(2b)^k在反例中的不同作用；§9（p.23）先说明重叠与截断实例针对的证明假设；§10（p.24）用固定面积损失与指数失败预算解释差异，删去重复公式总结。

没有套用五篇的固定文风。它们某些宏观开场、英文语病或重复不适合照搬；本稿没有移植原句，也没有为了写作学习将五篇全部加入参考文献。

## 3. 三个修改前后片段

以下仅引用P6自身文字，完整差异由本提交保存。

1. §1.1原来只说：
   > The spectrum S combines angular entropy with radial stopping cost.

   现在先给构造意义：
   > The two terms come from different constructions. Covering all initial states at the prescribed tolerance gives the precision spectrum S.

   随后解释稀有词删去给L_a、二者择小、实际区域下界排除任意近似输入的进一步节省。

2. §7.4原来直接从节标题进入Lemma 7.2。现在补上：
   > The witnesses in Lemma 5.1 distinguish control words, but individual states have zero area.

   接着说明要构造有已知质量、每个点均强制同一前缀的区域；原有加厚、面积和错控制估计全部保留。

3. 原§2.2在主定理前同时定义χ_R、γ₀、D。现将γ₀和D的定义及根唯一性原样移到附录A，前置解释：
   > The geometric estimates already retained the two products λ_w and P_w separately; only the stopping count changes when the powers differ.

   定理范围和数值定义没有改变，减少首次阅读可靠性定理时无用的符号负担。

## 4. 直接覆盖与数学边界

- CCS2020作者稿Theorem 14已经采用“单控制实际集合体积—任意目录数量”方法。本次因此新增正文引用 `CCS2020`，不把这一通用原则认作本稿首创。该证明用连续时间流、终点Jacobian和Liouville估计；所读范围没有给P6首真越界的δλ_w/P_w带、全可行瞬态概率界及指数失败预算下的正面积强制区域。不能仅因对象名称不同排除覆盖；这里缺的是这些定量步骤。正式版本正文未读限制仍保留。
- NWH2022的压力对偶、CHZ2026的分划柱子与时间幂次变分链提供框架和工具；CHZ §4也有高概率集合覆盖，概率覆盖本身不算本稿新概念。所读证明依赖相应柱子/局部质量，并未建立任意近似控制在两项指数预算下的物理比较。既往对原文具体命题的审查不因写作参照而被撤销。
- WCLW2020的重参数化流球局部质量与CDZ2022的互信息/平均失真、铺砌和不变测度极限各有实际几何连接。不能把它们直接替代A_u的全时域约束或精确失败预算；本次未发现需要撤回P6结论的直接覆盖证据，不据此认证首创。
- **Wang–Huang2022，Nonlinearity，DOI10.1088/1361-6544/ac4f33**不属于五篇JDE。其正式全文覆盖缺口仍在，限制对spanning测度熵和可靠性主贡献的完整新颖性判断。未重复失败获取，也没有用本次行文研读宣布缺口关闭。陈虎.pdf始终按已取得原件处理。

本轮未改变数学主张，未发现改写实际涉及部分的实质数学错误。15项正式结果和结构假设逐字保留；12段proof中原有全部数学表达按原顺序保留；109个label不变。新增解释与正文计算逐项对应。γ₀、D只迁移定义位置，附录B全部内容及其2到1有限计数反例原样保留，AI披露逐字保留。这些一致性核对不能替代独立人工证明审阅。

## 5. 完成状态及仍有负担的位置

- 已更新唯一TeX及对应27页PDF；latexmk/pdflatex正常收敛，最终日志无warning、未定义引用或overfull/underfull提示。全部27页经渲染目视检查，公式、编号、分页和文献可读；13条参考文献均有实际引用。
- 阅读负担仍主要在§3的图导数常数、Lemma 5.1的耦合不动点、Lemma 7.2的全点余量，以及§8的C² Cantor插值。已增加用途说明，但这些估计承担主定理，不能为“自然”删除。剩余负担主要来自技术依赖；本文仍需要相应动力系统/控制背景。
- JDE继续为**B：合理冲刺**。本次改善呈现与方法归属，没有新增数学或扩大用途。指定二进制平面一阶几何、三角约束和共同原点收缩仍限制范围；Wang–Huang正式正文覆盖核验仍待完成。没有因行文更顺而提高定位，也没有发现必须再添一项定理的理由。
- 作者姓名/顺序、单位/邮箱、通讯作者、资助与利益冲突、实际人工审读范围、稿件及AI披露批准、稿件发表/在审状态仍待真实确认；JDE专属作者指南的前轮访问缺口未在本次处理。正文改写完成不等于已经可直接执行投稿。

最终文件SHA-256：

```text
TeX 5daf164992f063f304641e7059b4533ce05cab57165588a6c9a30cab949b1645
PDF cbe2459dc66d94149e9b8d765028bac41aec8023e05f15e8afe17e5e26ff955c
```

提交仅涉及唯一TeX/PDF、本记录、CURRENT和README。提交前重核main，使用expected-SHA更新；随后按提交SHA完整回读五个文件并逐字节核对PDF，核对其他树项不变。实际提交SHA在交付中给出，避免记录对自身提交的循环引用。完成后停止，不自动新研究轮；R09–R14继续暂停。
