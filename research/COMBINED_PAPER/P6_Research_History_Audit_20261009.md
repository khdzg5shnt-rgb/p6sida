# P6修订记录与内容补回核查

当前稿确实没有收录 p6sida 中所有已证成果。最值得补回的是 R38 的逆面积常数量化下界、R33 的实际可行折叠例子和 R18 的局部完全一致但全局塌缩反例。这三项都服务于现稿的非塌缩与可靠性问题，已有证明可用。R01 至 R09 中另有独立成果未收入当前稿，应继续保存，不能统称为已被新主定理吸收。

现稿的可靠性正反定理、匹配精度谱、面积估计、有限瞬态证明和失配判据已保留。当前问题主要是成果取舍和例证缺失；本次未识别出“少了这些例子就无法证明现稿主定理”的依赖缺口。

## 核查对象与范围

核查基线为仓库 [p6sida 的 609bdffd 提交](https://github.com/khdzg5shnt-rgb/p6sida/tree/609bdffd3e25f3a86231b450b1c0edb67e7bd766)，核查日期为 2026 年 10 月 9 日。

| 对象 | 核对结果 |
| --- | --- |
| 本次上传的 P6_1009.tex | 与该提交的 paper/P6_PRECISION_COST.tex 逐字节相同，均为 103686 字节 |
| 数据源中的原始 P6 TeX | 与 original/P6_LIYO_Manuscript_SUBMISSION.tex 逐字节相同，均为 95642 字节 |
| 可见提交历史 | 52 个提交；当前分支及其可追溯历史已纳入版本与路径核查 |
| 研究轮目录 | R01 至 R13、R15 至 R40，共 39 个目录 |
| R14 | 没有独立目录或成果提交；README 记载只核验端点递推与贪心工具，没有比较增量 |
| R00 与 R41 至 R100 | 当前仓库及可追溯文件路径中没有这些轮次的独立记录；原始稿承担起始基线的作用 |
| 当前文件与历史路径 | 当前跟踪文件 168 个，历史出现过的不同文件路径也为 168 个；数学内容的删节主要发生在同一论文文件的改写中 |

本次逐轮核对数学产出、适用条件、成果状态与终稿采用位置，并重新检查了拟补回三项的构造和证明。这里的“逐轮核查”是成果保留关系审计，不等于对所有历史证明逐行作形式化认证，也不等于重新完成全部外部文献的新颖性核查。

两个身份校验值如下：

```text
当前稿 SHA256
ae63f015a8a7ac7b91b21087808896a9b68cbc3ba64b1a758a831b91c67f75a0

原始稿 SHA256
47aa42836d78fa281d1ef18e1fbb20d5d311eeab0959077f775542b61249b869
```

## 内容在哪些版本中退出了正文

当前稿不是所有轮次的累积合集。至少存在三种情况：研究笔记从未整合进论文；已被后来的定理覆盖，因而不再重复；有效成果曾进入正文，随后因选定主线而撤下。

| 版本变化 | 实际发生的取舍 | 证据 |
| --- | --- | --- |
| R07 阶段稿至 R20 整合 | R05 共同径向精度公式、R07 横向扩张实例退出论文；R06 的主线转向几何匹配问题 | [R20 报告](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R20/REPORT.md)，尤其采用范围和删除范围 |
| R36 稿至 R40 稿 | 曾有完整构造的折叠、角度影响径向的特定反馈、正面积塌缩例子退出正文 | [R36 论文快照](https://github.com/khdzg5shnt-rgb/p6sida/blob/221376684d9b0476b4a2c7be2f09e22f50097bb7/paper/P6_PRECISION_COST.tex)；[R40 报告](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R40/REPORT.md)第一节明确记录移出 |
| 原始稿加 R40 的 49 页合并稿至集中主线稿 | 高维锥体、共同径向谱、熵与混沌分离、真实 lift、反馈与标量基线等退出本篇 | [49 页论文快照](https://github.com/khdzg5shnt-rgb/p6sida/blob/22e9716c3fc656ac71029cbac566dd93ac56c04e/paper/P6_PRECISION_COST.tex)；[取舍提交](https://github.com/khdzg5shnt-rgb/p6sida/commit/3e08c9992426d4cdea887c9e0cb595f43918d285)；[FINAL_SELECTION](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/COMBINED_PAPER/FINAL_SELECTION.md) |
| 集中主线稿至本次上传版本 | 后续证明表述与行文修订，当前 PDF 为 27 页 | [CURRENT](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/CURRENT.md)与当前论文 |

因此，“当前比某个版本少内容”有真实的版本依据。不过，页数减少本身不能区分合理去重和有价值内容的退出。原始 TeX 的字节数还少于当前 TeX，不能用文件长度判断数学包含关系。

## 优先补回的三项

| 内容 | 为什么值得补回 | 建议位置 |
| --- | --- | --- |
| R38 逆面积常数必须指数增长 | 将可靠性反例的机制量化，直接说明固定面积损失的规则窗口不能自动用于指数失败预算 | 第 8 节反例证明后，增加一个短推论及证明 |
| R33 实际可行折叠 | 显示精度定理确实适用于非单射控制，且临界集零面积条件有超出微分同胚的实际例子 | 第 9 节增加一个例子，或放入短附录 |
| R18 局部完全一致但全局塌缩 | 说明共同一阶数据、甚至原点邻域内全部动力学一致，加上所有输入收敛，仍不能决定全局正面积初始集成本 | 第 9 节之后的反例比较，或与折叠例子一起放入短附录 |

这三项的价值在于把现稿条件的区别说透，不是用命题数量证明期刊档次。补回时无需开启新的研究轮，也无需重写现有主证明。

### R38 逆面积常数的量化结论

来源为 [R38 数学笔记第 6 节](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R38/MATHEMATICS.md)。当前稿保留了该反例及严格可靠性率差，但没有保留这个独立的量化结论。

使用当前第 8 节已经定义的同一个系统、$H$、$b=2/5$、$\lambda=a_0a_1$、目标区间长度 $\ell$ 和 $\mathsf A_0$。设

$$
e_n=\exp\{-n/8+o(n)\},\qquad k_n=\lfloor n/2\rfloor.
$$

对任意可测 $T_n\subset Q$，若 $\mu(T_n)\ge1-e_n$，并且某个有限常数 $L_n$ 满足

$$
\mu\bigl(T_n\cap F_0^{-1}(B)\bigr)
\le L_n\operatorname{area}(B)
\quad\text{对所有可测 }B\subset\mathbb R^2,
$$

则对所有充分大的 $n$，

$$
L_n\ge\frac{1}{2\ell\det\mathsf A_0}
             (b/\lambda)^{k_n},\qquad
\liminf_{n\to\infty}\frac{\log L_n}{n}
\ge\frac12\log(b/\lambda)>0.
$$

证明直接使用现稿的物理区域 $E_{\sigma,k}$。取首个块地址为零的区域之并 $E_k^0$，则

$$
\mu(E_k^0)=\frac3{16}(2b)^k,
\qquad
\operatorname{area}\bigl(H(E_k^0)\bigr)
=\frac3{16}\ell(2\lambda)^k.
$$

因为 $\tfrac12\log(5/4)<1/8$，在 $k=k_n$ 时，$e_n/\mu(E_k^0)\to0$。所以任意这样的 $T_n$ 最终至少保留 $E_{k_n}^0$ 的一半面积。第一控制零在这些区域上真实可行，且

$$
F_0(E_{k_n}^0)=\mathsf A_0H(E_{k_n}^0)\subset Q.
$$

将 $B=\mathsf A_0H(E_{k_n}^0)$ 代入逆面积不等式，用 $\det\mathsf A_0=a_0^{2\beta-1}>0$，即得上述下界。如果根本没有有限 $L_n$，更不可能得到次指数常数。

这个结论针对 R38 的固定反例和指定失败序列，覆盖所有符合面积损失限制的窗口选择。它不是“任意系统一旦有指数失败预算，逆面积常数都会指数增长”的一般断言。它也没有求出该反例的准确可靠性谱或证明其可靠性极限存在。

### R33 真正发生在可行分支上的折叠

来源为 [R33 数学笔记第 7 节](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R33/MATHEMATICS.md)。该例曾进入 R34 和 R36 正文，R40 明确移出；当前第 9 节的向内边界例子是微分同胚，不能代替它对非单射适用范围的展示。

取 $c=1/5$，取光滑截止函数 $\psi$，使其在 $s\le1/4$ 为零、在 $s\ge1/2$ 为一。定义

$$
H(s,z)=
\begin{cases}
(s,z),&s\le1/4,\\
(s,z+c\,s\psi(s)\sin(2\pi z/s)),&s>1/4,
\end{cases}
\qquad F_i=\mathsf A_i\circ H.
$$

它在原点邻域恒为线性对照，因而所有局部导数一致。$H(Q)\subset Q$，线性控制的可行域覆盖保证 $Q$ 受控可行。设

$$
m_* =\max_i\{r_i,t_i\}<1,
\qquad
\Lambda=1+\frac{2m_*(1+2c)}{1-m_*}.
$$

由 $|H^z-z|\le c|s|$，现稿范数 $V=\max\{\Lambda|s|,|z|\}$ 满足

$$
V(F_i x)\le
m_*(1+1/\Lambda)(1+c/\Lambda)V(x)
<\frac{1+m_*}{2}V(x).
$$

此界在全平面成立。临界集由

$$
\det DH=1+2\pi c\psi(s)\cos(2\pi z/s),
\qquad
\det DF_i=(r_i^2/a_i)\det DH
$$

给出。每个固定正半径上的临界角有限，故 $Q$ 内临界集面积为零；但临界点确实存在。

在 $s_0=3/4$，令 $g(y)=y+(1/5)\sin(2\pi y)$。有

$$
g(1/4)=9/20<1/2,
\qquad g(2/5)>1/2,
\qquad g(1/2)=1/2.
$$

所以存在 $y_1\in(1/4,2/5)$，使两个不同内部状态 $(s_0,s_0y_1)$ 与 $(s_0,s_0/2)$ 在两个控制下分别具有相同输出，且至少一个控制的这个共同输出在 $Q$ 内。这是实际可行分支中的非单射，不能由保持 $Q$ 的同时状态共轭化成单射控制。

精度结论 Theorem 2.3 适用于匹配参数；附录 A 的失配结论适用于失配参数。该例存在临界点，不能用 Theorem 2.1 给它宣称指数可靠性公式。补回时必须保留这个区别。

### R18 局部完全一致仍不能防止正面积塌缩

来源为 [R18 数学笔记](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R18/MATHEMATICS.md)。该例曾在 R20 至 R36 的正文中出现，目前没有保留。

固定匹配参数 $r_i=a_i^\beta$、$t_i=a_i^{\beta-1}$ 和 $0<\sigma<1/2$。取光滑 $\psi$，在 $s\le\sigma$ 为零、在 $s\ge2\sigma$ 为一。定义

$$
G_0(s,z)=\bigl(r_0s,
(1-\psi(s))t_0(z+a_1s)-\psi(s)r_0s\bigr),
$$

$$
G_1(s,z)=\bigl(r_1s,
(1-\psi(s))t_1(z-a_0s)+\psi(s)r_1s\bigr).
$$

两者为全局 $C^\infty$ 映射，在原点的整个开邻域内与线性控制相同。它们是线性控制与收缩射线映射的逐点凸组合，所以存在一个共同范数，使所有输入在全平面向原点一致指数收敛。逐半径计算可行域还能验证 $Q$ 受控可行。

固定紧集

$$
K_\sigma=Q\cap\{s\ge2\sigma\},
\qquad \operatorname{area}(K_\sigma)=1-4\sigma^2
$$

被控制零一步送到下边界射线，之后输入 $0^\infty$ 一直恰好可行。因此

$$
r_G(n,\delta;K_\sigma)=1
\quad\text{对全部 }n\ge0,\ \delta>0.
$$

另一方面，小核心 $Q_{\sigma/2}$ 的全部输入轨迹，包括离开 $Q$ 后的轨迹，仍与线性系统完全相同。它是正面积初始集，故对于有限 $\gamma>0$ 和现稿使用的精度序列，

$$
\liminf_n\frac{\log r_G(n,\delta_n;Q)}n
\ge\min\{h,\gamma/\beta\}>0.
$$

一个固定长度的恰好可行前缀又把全 $Q$ 送入线性区，停止目录给出上界 $\min\{\log2,\gamma/\beta\}$；所以在 $0\le\gamma\le\beta h$，全 $Q$ 率准确等于 $\gamma/\beta$。

其雅可比为

$$
\det DG_i=(1-\psi(s))a_i^{2\beta-1},
$$

在饱和区的正面积集合上为零，因而不满足现稿的零面积临界集假设。这个例子说明不能仅凭局部数据和共同收敛删掉全局非塌缩控制，不是说零面积临界集条件对每一个有效系统都必要。减小 $\sigma$ 可以让 $K_\sigma$ 面积接近一，但会改变系统，不能改写为同一个固定系统拥有任意接近满面积的零成本紧集。

## 各轮成果与现稿对应

下表中的“覆盖”只指注明的数学结论及适用范围。成本定理被覆盖，不表示其特殊实例、非共轭性质或所有边界参数也自动保留。整合、文献评估和行文修订不单独计为新数学定理。

### 原始稿与早期轮次

| 轮次及来源 | 实际产出 | 现稿情况 | 处理意见 |
| --- | --- | --- | --- |
| [原始稿](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/original/P6_LIYO_Manuscript_SUBMISSION.tex) | 高维锥体谱、共同径向扰动、有限字母族、任意有序熵率、Lyapunov 与混沌分离、真实 lift、分划及标量基线 | 大部分撤下；控制集合扩大的已修正计数保留在附录 B，固定容差连接保留短论证 | 整稿继续归档；不是新稿的无用旧版本 |
| [R01](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R01/P6_R01_Mathematical_Note.tex) | 固定字母表实现有序控制熵；抽象 lift 及其不变测度不能恢复初态投影下的控制成本；熵与状态混沌分离例子 | 未整合为现稿的定理；可靠性定理不能推出这些结构结论 | 保存为独立的熵与投影问题，不整段塞入本篇 |
| [R02](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R02/MATHEMATICS.md) | 同符号 lift 不对应同初态投影的具体冲突；最小目录压力与凸对偶计算 | 未整合；当前物理初态定义与这一辨别一致，但没有收录证明 | 需要讨论 lift 时简短引用；不恢复整套压力章节 |
| [R03](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R03/FULLTEXT_AUDIT.md) | 历史笔记对对数单位与时变共轭范围的反证；另算二进制锥体的面积测度熵和锥顶测度熵 | 没有收录为现稿结果；现稿也没有采用被笔记否定的单向包含共轭等式 | 保留引文审查；不要把与主证明无关的纠错材料整章加入 |
| [R04](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R04/MATHEMATICS.md) | 固定状态概率公式的计数紧集反例；随时间优化概率的经典分数覆盖比较 | 未整合；反例是零面积可数初始集，不在当前均匀面积可靠性问题中 | 保存为独立变分公式反例，不当作当前概率定理的反例 |
| [R05](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R05/MATHEMATICS.md) | 共同径向、有限控制和严格内向余量下的完整容差时域公式，含 $\rho=1$ 与 $\gamma=\infty$ | 曾入阶段稿，R20 撤下；系统类并非当前共同指数收缩二分支类的子类 | 有完整独立价值；可做简短比较或另存完整成果包 |
| [R06](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R06/MATHEMATICS.md) | 等角宽、不同径向收缩下的完整精度谱；每个有内部紧集与固定近满面积紧集的不同率；含无限精度指数 | 现稿排除 $a_0=a_1$，失配附录只给低精度范围，不能称完整覆盖 | 保留完整比较；若要本篇体现失配全谱，需要单独明确该特殊类 |
| [R07](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R07/MATHEMATICS.md) | 一个横向特征值大于一的系统在 $\delta_n=2^{-n}$ 下的准确率 | 曾入阶段稿，R20 撤下；不满足当前所有输入共同范数收缩 | 独立例子继续保存；放正文会扩大论文的问题范围 |
| [R08](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R08/MATHEMATICS.md) | 固定归一化角向重叠和内向余量仍允许全 $Q$ 与近满面积紧集成本分裂 | 没有整合；R26 的趋零重叠和现稿局部一阶分支不能覆盖固定角向重叠 | 保存持续重叠这条独立研究线 |
| [R09](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R09/MATHEMATICS.md) | 同一重叠系统真实目录率极限存在；等于最优停止覆盖指数的一半；准确常数有严格两侧根界 | 没有整合；极限存在已证明，准确常数尚未求出 | 必须保存为已完成成果，不能与后续未解策略问题一起标为未完成 |
| [R10](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R10/MATHEMATICS.md) | 重叠区两个强制块的 81 与 24 不同成本、非零平移，以及同后缀删词的反例 | 未整合；是持续重叠研究的已证技术接口 | 保留笔记；不宣称由此已求出最优率 |
| [R11](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R11/MATHEMATICS.md) | 几何重编码及残余预算界；给出策略与最优指数比较的充分条件 | 未整合；关键次线性预算控制未证明 | 保留条件式结论，不恢复为策略最优定理 |
| [R12](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R12/MATHEMATICS.md) | 达标区间最多相交三个最优目录区间；端点残余指数差的刻画和预算界 | 未整合；仍没有证明固定策略达到最优指数 | 保留已证界，明确尚未闭合的比较 |
| [R13](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R13/MATHEMATICS.md) | 具体选择器的有限精确端点闭合与有限状态捷径排除 | 未整合；不是新准确率或最优策略证明 | 留作方法边界，不作为正文新主结果 |
| R14 | README 记录了工具核验，没有独立成果文件或提交 | 无可核查的新已证产出 | 不虚构一轮结果，不自动重开问题 |

R05 的公式与 R06 的谱有相似的停止尺度表达，但假设、初始集量词和允许参数不同。两者不能因形式相似而归入现稿的一条公式。

R09 的固定系统为 $q=2-2^{-20}$、$\rho_0=1/4$、$\rho_1=1/256$、$\delta_n=2^{-n}$。已证

$$
H=\lim_n\frac{\log r(n,2^{-n};Q)}n
=\frac12\lim_m\frac{\log N_m}{m},
$$

并有两个不同根给出的界，约为 $0.16102194$ 至 $0.16107928$。这些数是边界的近似展示，不是 $H$ 的准确值。R10 至 R13 没有把这一区间收敛成一个准确常数。

### 匹配与非线性推广轮次

| 轮次及来源 | 实际产出 | 现稿情况 | 处理意见 |
| --- | --- | --- | --- |
| [R15](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R15/MATHEMATICS.md) | 线性几何匹配的所有正面积紧集共同低精度率和一般上下界 | 不等分支、有限精度指数的成本结论已由 Theorem 2.3 覆盖并加强；旧等分支情形和无限指数不在现稿正式范围内 | 不重复旧证明；若恢复边界参数应单独写清范围 |
| [R16](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R16/MATHEMATICS.md) | 同一匹配系统的高精度成本分裂及具体参数例子 | 被 Theorem 2.3、Corollary 2.4 和第 9 节实例覆盖 | 不重复 |
| [R17](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R17/MATHEMATICS.md) | 所有正面积紧集共同成本的准确边界 $\beta h$ | 已保留，且现稿给出完整全 $Q$ 谱和准确差距 | 不重复编号 |
| [R18](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R18/MATHEMATICS.md) | 原点邻域动力学完全相同、所有输入收敛，却在远处正面积塌缩并出现零成本紧集 | 曾入正文，R40 撤下；当前没有等效例证 | 优先补回短构造和证明 |
| [R19](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R19/MATHEMATICS.md) | 指定状态依赖、径向自主可逆系统的匹配边界转移 | 成本结论被一般一阶结构类覆盖；具体公式及限定的非共轭证明没有原样保留 | 不重复成本证明；实例按需要择一 |
| [R20](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R20/REPORT.md) | R15 至 R19 主线整合 | 属整合记录；主要率后来保留，R18 例子后来移出 | 作为采用与删除依据 |
| [R21](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R21/MATHEMATICS.md) | 径向自主类低精度失配双率与匹配判据 | 成本结论被附录 A 的更一般反馈类覆盖 | 不重复 |
| [R22](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R22/MATHEMATICS.md) | 角度影响可行分支和径向轨迹的匹配推广；特定范围的坐标化约排除 | 成本结论被 Theorem 2.3 覆盖；特定实例和非共轭结论未整体保留 | 可补简短反馈实例，不能扩大其非共轭范围 |
| [R23](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R23/REPORT.md) | 失配与角向反馈整合 | 率保留在一般定理和附录 A；独立实例后来删节 | 不作为额外新定理 |
| [R24](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R24/MATHEMATICS.md) | 分支和径向可独立扰动，只要求渐近一阶匹配 | 成本结论由一般一阶定理覆盖；长的具体小扰动类未原样保留 | 不恢复重复证明 |
| [R25](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R25/REPORT.md) | R24 与既有结果整合 | 属整合记录，没有另一个独立数学结果需加入 | 保留历史 |
| [R26](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R26/MATHEMATICS.md) | 归一化重叠趋零、物理重叠为二阶小量时的精度边界 | 成本结论已覆盖；不能据此覆盖 R08 的固定归一化重叠 | 不重复证明，不恢复已修正的旧截止支撑条件 |
| [R27](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R27/MATHEMATICS.md) | 一般局部几何、真实面积和物理见证；允许空、单点、截断的可行截面 | Theorem 2.5、第 3 至第 6 节和向内例子保留；有限瞬态条件由 R33 加强 | 主证明链已保留 |
| [R28](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R28/REPORT.md) | R27 实际面积与边界整合 | 属整合记录，核心内容仍在正文 | 不重复 |
| [R29](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R29/MATHEMATICS.md) | 全 $Q$ 完整匹配谱和三段闭式，两个准确阈值 | Theorem 2.3、Corollary 2.4、第 6 节完整保留 | 已采用 |
| [R30](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R30/REPORT.md) | R29 完整谱整合 | 属整合记录，谱和证明保留 | 已采用 |
| [R31](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R31/MATHEMATICS.md) | 一般反馈类低精度失配双率和匹配判据，分开角向与径向乘积 | 附录 A 与面积证明保留，有限瞬态范围由 R33 扩大 | 已采用 |
| [R32](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R32/REPORT.md) | 一般反馈匹配与失配整合 | 属整合记录，主要率保留 | 已采用 |

### 非塌缩与可靠性轮次

| 轮次及来源 | 实际产出 | 现稿情况 | 处理意见 |
| --- | --- | --- | --- |
| [R33](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R33/MATHEMATICS.md) | 不要求全局单射，零面积临界集下的可行有限瞬态转移；一个实际可行的光滑折叠例子 | 定理与局部逆图证明保留在 Theorem 2.3、2.5、Lemmas 4.1、4.2 及附录 A；折叠例子退出正文 | 定理不重复，折叠例子优先补回 |
| [R34](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R34/REPORT.md) | 非塌缩推广整合，同时保留折叠、塌缩和角度影响径向的例子 | 主证明保留；上述特殊例子于 R40 移出 | 作为恢复实例的成熟正文来源 |
| [R35](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R35/REPORT.md) | 对照正式论文的 JDE 竞争力评估 | 没有新增数学定理 | 不将期刊评估当作待补数学内容 |
| [R36](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R36/REVISION_NOTES.md) | 匹配判据和初始集成本论文的行文修订；当时仍有完整折叠与塌缩证明 | 无新数学定理；其成熟实例正文可用于恢复 | 选取已完成的证明，不把旧摘要整段搬回 |
| [R37](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R37/MATHEMATICS.md) | 匹配线性系统的联合精度可靠性率；固定失败率；停止树概率覆盖与实际目录的有限时域比较 | 率与一次初态索引用途保留在 Theorem 2.1、Corollary 7.3 和定义后说明；线性有限时域比较未单独收录 | 主要率已采用；有限时域比较可选放附录 |
| [R38](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R38/MATHEMATICS.md) | 单射且零面积临界的瞬态反例：全 $Q$ 所有有限时域计数不变，可靠性下极限严格增大；窗口逆面积常数必须指数增长 | Theorem 2.2 与第 8 节保留反例及率差；逆面积常数下界没有保留 | 优先补回量化短推论；不声称反例准确谱已求出 |
| [R39](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R39/MATHEMATICS.md) | 全 $Q$ 无临界点时，物理均匀面积的概率运输和正面积强制词给出联合率 | Theorem 2.1、Lemmas 7.1、7.2 与第 7 节完整保留 | 已采用；无临界点是充分条件，不是必要充分分类 |
| [R40](https://github.com/khdzg5shnt-rgb/p6sida/blob/609bdffd3e25f3a86231b450b1c0edb67e7bd766/research/R40/REPORT.md) | R37 至 R39 可靠性主线整合，并撤下旧特殊实例 | 15 项现行正式陈述来自这一主线的取舍与后续修订 | 整合本身不是又一项新定理 |

## 现稿主链的实际保留情况

将 R40 的 25 页 TeX 与当前 TeX 按正式陈述标签和内容对照，R40 有 16 项正式陈述，当前有 15 项。唯一退出编号的是匹配线性谱的 cor:linear，结论已作为一般精度定理的线性特例包含。其余 15 项共有陈述中，12 项除空白外一致；3 项的修改是如下澄清，而不是减少成本结果。

| 陈述 | 当前修改 |
| --- | --- |
| thm:area | 小误差参数改用 $\eta$，明确可用 $m$ 为整数及其与时域的范围 |
| lem:regularwindow | 小误差参数改用 $\eta$，避免与失败概率混用 |
| cor:failure | 明确固定失败结论仍要求匹配幂次 |

这个对照支持“R40 主线的正式结果基本保留”，不能支持“R01 至 R40 的全部成果都保留”。R38 的量化窗口下界本来就没有成为 R40 的独立正式陈述，R18 与折叠例子更早已退出。

当前对应关系如下：

| 现稿位置 | 保留的内容 |
| --- | --- |
| Theorem 2.1 与第 7 节 | 无临界点的联合精度可靠性公式 $\min\{S(\gamma),L_a(\alpha)\}$ |
| Theorem 2.2 与第 8 节 | 零面积临界但可靠性转移失效的反例；全状态有限时域计数恒等 |
| Theorem 2.3、Corollary 2.4 与第 6 节 | 匹配完整全 $Q$ 谱、同一个固定近满面积紧集的率、共同边界与饱和边界 |
| Theorem 2.5 与第 3 至第 5 节 | 任意近似输入的真实面积、首真越界、有限可行瞬态、固定规则窗口和物理见证 |
| Corollary 7.3 | 线性可靠性特例与匹配类固定失败比例率 |
| 附录 A | 一阶匹配判据与一般反馈的低精度失配双率 |
| 附录 B | 控制集合扩大后的全 $Q$ 计数和内部初始集率界；保留内部有限时域计数可能下降的修正 |

可靠性函数 $L_a$ 的闭式在当前第 7 节、eq:reliabilityclosed 中已经写出，不能再列为遗漏。角向乘积 $\lambda_w$ 与径向乘积 $P_w$、所有中间时刻、任意近似输入和之后重入的处理也已保留。

## 可选补充与不宜直接拼回的内容

| 内容 | 有什么额外价值 | 对本篇的取舍 |
| --- | --- | --- |
| R34 角度影响径向的简短反馈实例 | 显示现稿不假设半径自主，不只适用于向内径向模型 | 可在附录 A 或例子节用一段公式展示；优先级低于三项核心补回 |
| R37 线性有限时域概率目录比较 | 给出比渐近率更具体的停止树目录上、下界，并控制任意近似输入 | 若强调有限时域操作用途可放短附录；一般非线性率定理并不自动给此比较 |
| R05 完整共同径向公式 | 包括弱径向收缩、临界乘积和不同字母表，扩大比较范围 | 与现稿系统类不同，整套证明宜独立保存；正文只给有条件的短比较 |
| R06 等角宽失配完整谱 | 比当前失配附录的低精度双率更完整，并有“每个有内部紧集”的结论 | 若要增加完整失配比较可另设附录；不把它包装成一般反馈的高精度谱 |
| 原稿 arsinh 共同径向例子 | 所有正控制熵与无状态 Li–Yorke 混沌可同时出现 | 可在讨论中简述；其 $R'(0)=1$ 不满足当前统一指数收缩，不称现稿特例 |
| 原稿高维、lift、反馈、分划和连续时间标量章节 | 有独立的熵结构问题和证明 | 保存完整旧稿；整体回填会改变本篇问题与证明范围 |
| R08 至 R13 持续重叠研究 | 已有分裂、真实率存在、严格根界和技术障碍 | 保存为独立研究记录；准确常数与策略最优问题尚未闭合，不迁入现稿作为已解决主定理 |

例如 R37 的有限时域比较是：对固定匹配线性系统、$n\ge1$、$0<\delta<1$ 和 $0<e<3/4$，若 $C(n,t;e)$ 表示权重覆盖至少 $1-e$ 的最少停止树叶数，则存在固定 $B,M$，使

$$
\frac1B C(n,\delta^{1/\beta};4e/3)
\le r_e(n,\delta;Q)
\le C\bigl(n,(\delta/M)^{1/\beta};e\bigr).
$$

它有独立的有限时域用途，但恢复时需要保留树、权重和阈值的定义；不能只加这个公式而省略任意输入的比较证明。

## 两处记录需要更正

第一，README 末段仍说“当前唯一论文为初始 P6 与 R40 的完整合并稿”。这对应旧 49 页版本，与顶部和 CURRENT 所指的 27 页集中主线稿不一致。建议改为“当前唯一论文为精度与可靠性主线稿；原始稿和完整合并稿由原文件及历史版本保存”。

第二，research/COMBINED_PAPER/RESULT_COVERAGE.md 是 49 页合并稿的历史对应表，记录的是原始稿与 R40 的正式陈述，不是 R01 至 R40 每轮产出的完整采用表。CURRENT 与 FINAL_SELECTION 已说明它的历史身份；仍不能用它推断目前没有遗漏。

现稿保留的附录 B 也不应恢复旧的“扩大控制集合后所有有限时域计数不变”说法。原始内部集的具体计数可下降，当前已有 $q=2,n=1$ 从 2 降至 1 的反例；这项修改应继续保留。

## 对投稿稿的具体建议

保留当前精度与可靠性主线。先将 R38 的短推论补在反例后，再加入 R33 折叠与 R18 塌缩作为对照：正面积塌缩会破坏精度转移；零面积临界允许精度结论，但不足以保证指数可靠性；全 $Q$ 无临界点给出已证可靠性充分条件。三种现象的条件、成本对象和强弱关系要分别写清。

对于 R01 至 R09 和原始稿，继续保存原证明和历史，不按“旧版”整体删除。已经被一般定理覆盖的成本证明无需重复；独立系统类和独立问题不能以“新版更强”为由丢弃，也不必全部并入这一篇投稿稿。

本次交付的是核查与补回方案，没有修改论文、提交 GitHub 改动或重新开启未解研究问题。
