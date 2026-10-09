# P6 最终数学复核与读者验收

基线为 main `97060923f46bc270a75637625ebe3ddf37cd6d28` 的 35 页稿。开始时远端没有后续提交。本轮单代理，只处理 P6；完整重读现行 TeX 全部证明，连续终读最终 PDF，并逐页查看全部 35 页渲染图。旧报告只用于定位，没有作为证明正确的前提。

**判断：问题引入和部分证明段落已有可与参照比较的具体优点，但证据不足以认定整篇达到十篇文章的共同水平。** 没有识别出需要改变现行定理的证明断裂；修正了首次退出的错误解释和两处易误解的表述，展开了面积界的关键代入。数学审查由 AI 辅助完成，不是独立人类验证，也没有真人读者测试。

## 实际修改及理由

| 位置（最终 PDF） | 改前 | 改后与作用 |
| --- | --- | --- |
| 摘要，p.1 | 从 catalogue 定义进入较长的假设清单；用 source-coding rate 解释尚未熟悉的量 | 先提出“所有输入都使状态趋零，为什么控制选择仍增长”的问题，再说明观察一次初态的操作；用线性模型需要保留多少可行词解释 `L_a`。匹配、临界集和概率定理的较强条件均保留。 |
| §2.1，p.3 | 再次提醒覆盖必须检查再进入前的时刻，但 exactly feasible 尚无直接定义 | 定义为前缀的每个中间状态都在 Q 中；全部时刻的要求已由式 (2.1) 和 §1.2 明确，不再重复。 |
| §3.2，p.8 | “There is no positive lower bound on \(|I_w|\)” | 写为固定半径截面 \(|I_w(s_0)|\)，并指明该截面可能为空，避免与整个物理区域及附录 A 的线性区间混淆。 |
| §3.3，p.9 | “Reentry cannot undo a violation at this first exit.” | “An exit from Q may still respect the tolerance.” 随后说明式 (3.8) 包含所有首次退出仍满足容差的状态，后续约束只会缩小集合。离开 Q 不等于违反 δ 约束；原面积上界不变。 |
| §6.3–6.4，p.16 | 依次引用条带界、词乘积和逆面积界后直接给出指数；用一句话宣布各项均被控制 | 区分存活与首次退出，写出 \(\lambda_w/P_w\le D_\eta^2 e^{(\chi_R-h+2\eta)(j-1)}\)、几何级数以及选择 \(m_n\) 后的两个不等式。读者可在证明现场检查指数符号和常数归属。 |
| §7.1–7.2，pp.17–18 | 相邻段落两次解释为何用精确可行词 | 合并；直接写出“未覆盖状态包含于被丢弃词区域的并集”，说明有重叠时为什么仍可用并集上界。 |
| §7.4，pp.18–19 | “Expansion through any prefix then changes that width by at most a fixed factor”容易被理解为相对于初始宽度的固定倍数 | 先给出扩张尺度 \(\lambda_w^{-1}\)，再解释初始宽度取 \(\lambda_w\) 的小倍数，使各步的角偏差小；保留端点延拓及错误控制的完整证明。 |
| §5、§7、§8 | 已由计算说明的“实际区域／全部时刻／不能靠再进入”反复补一句保证；反例未知精确率说两遍 | 删除这些重复句，保留它们真正参与论证的地方；未知范围集中留在 §10。没有删除计算或历史成果。 |

## 十篇原文的本轮比较

恢复的十个 PDF 均与 [既有来源清单](DCDS_SOURCES_20261010.json) 的 SHA-256 和页数相符。以下是**本轮定向重读的全部页段，共 68 个 PDF 页**；不是再次完整通读全部 241 页。页码均指所读作者版的 PDF 页，不能当作正式刊物页码。只读了证明片段的项目不称为完整重核该证明。正式身份与完整版本说明沿用来源清单；本轮没有重新检索出版社。

| 文献／所读版本 | 本轮页段与具体比较点 | 本稿处理及比较判断 |
| --- | --- | --- |
| Kawan (2011)，2009 年作者预印本，28 页 | 3–4、22–25；Theorem 14 的成功集合→单输入体积→目录数，尤其 PDF 23 | §6.3–6.4 现在展示这一转换的中间代入。结构可以直接比较；本稿仍多出首次退出和固定紧集两层，不能声称同样简洁。 |
| Da Silva & Kawan (2016)，arXiv:1408.2416v1，45 页 | 1–2、19–20、32–35、43；精读 Theorem 4.8 三步证明，尤其 PDF 34 的固定初始时间逆像 | 保留 §6.2 的“先选同一紧集”和全部逆图，再在 §6.3 明写乘以 \(L_T\)。其 Volume Lemma 只重读陈述与第一步，不声称本轮精读九步全文。它的技术设置更广，不能比较整体难度。 |
| Colonius (2018)，arXiv:1705.08658v2，31 页 | 1、3、9–11、30；Definition 2.12 明列推前测度，Theorem 2.13 实际运输集合和概率 | §1.3、§8.3 已清楚区分推前测度与两边都取均匀面积，保留。这种区别是必要说明，不按“去 AI 感”删除。两文的概率对象不同。 |
| Dou, Fan, & Qiu (2017)，南京大学作者 PDF，15 页 | 1–2、9–11、14；PDF 9 在证明需要时引入加权熵，PDF 2 交代沿用的四步方法及新障碍 | 保留本稿在 §2.4 才定义 \(I_a,L_a\)，在 §7.4 才引入厚化常数；增加 exactly feasible 的直接解释。不添加全局术语表。本文的局部常数仍比该方法概述更重。 |
| Wolf (2020)，arXiv:1803.02440v1，12 页 | 1–2、7–9、11；Proposition 3 的三个质量断言分开建立，Theorem 1 再调用 | 保留 §8.1–8.4 的区间→映射→轨迹→面积顺序，删去证明末尾的防御式复述。其单一反例主线更集中；本稿没有同等紧凑。Theorem 1 本轮只重读首尾，不冒充全文证明核验。 |
| Wang, Chen, & Zhou (2022)，arXiv:2103.14817v1，21 页 | 1–2、7、15–16、19；Lemma 4.2 先定义错误坐标，再以条件信息分解说明误差代价 | 改写 §7.2 为具体的“丢弃词→未覆盖集合→面积”链，保留 §1.2 对两个预算的分工。这里是初态失败概率，不是该文的平均失真；只比较解释方式。 |
| Hou, Tian, & Zhang (2023)，arXiv:2012.09482v2，29 页 | 1–2、11–14、27；§3.2 在构造后列出需验证的三项性质，再逐项证明 | 保留 Lemma 4.1、7.2 按数学任务分段；改清 §7.4 开头宽度选择的目的。其摘要和主结果也有较高符号密度，不能把“短句少符号”当作统一期刊标准。 |
| Zhang, Ren, & Zhang (2023)，arXiv:2112.07425v1，25 页 | 1–3、10、16–18、21；PDF 16 用一句具体原因解释为何重复最大熵测度两次，随后才选择参数 | 本稿固定块首尾字母、限制游程的理由已经明确，保留；在面积证明展开真正需要解释的代入，而非再添加段首预告。该文准铺砌结构不能直接用来比较本稿篇幅。 |
| Kucherenko (2024)，作者 PDF，17 页 | 1、3–4、8–10、16；PDF 8 说明边界连续性不可用，但较弱结论足以处理所需上确界，然后引出 Lemma 1 | 保留 §7.5–7.6 的严格频率→逼近端点及 §10 的未知范围；删除 §8 重复的未知率声明。其“障碍为何需要这个引理”衔接更紧，本稿跨 §3/4/6/7 的调用仍较多。 |
| Burgos (2026)，arXiv:2410.23487v2，18 页 | 1–2、8、11–13、17；§4.5 在 entropy 论证前指出 bi-Lipschitz 映射不交换动力学，不能直接保熵 | 保留 §8.3 的实际轨迹等式 (8.3) 与全覆盖集合对应，不凭 homeomorphism 宣称概率成本相同。本轮 Lemma 4.7 只读了开头。其首页也有宽泛评价，未将这类措辞作为模仿目标。 |

以上作者版不保证逐字等同正式版。Kawan 的 PDF 有两页封面；Da Silva–Kawan 和 Colonius 的页边版本日期与内部日期并不相同；S2023 预印本署名顺序是 Ren–Zhang–Zhang，正式引用使用 Zhang–Ren–Zhang；Burgos 正式卷年为 2026，不能以 arXiv 年份替代。

准确发表引用（期刊均为 *Discrete and Continuous Dynamical Systems* 主刊）：

1. Kawan, C. (2011). Upper and lower estimates for invariance entropy. *Discrete and Continuous Dynamical Systems, 30*(1), 169–186. https://doi.org/10.3934/dcds.2011.30.169
2. Da Silva, A., & Kawan, C. (2016). Invariance entropy of hyperbolic control sets. *Discrete and Continuous Dynamical Systems, 36*(1), 97–136. https://doi.org/10.3934/dcds.2016.36.97
3. Colonius, F. (2018). Invariance entropy, quasi-stationary measures and control sets. *Discrete and Continuous Dynamical Systems, 38*(4), 2093–2123. https://doi.org/10.3934/dcds.2018086
4. Dou, D., Fan, M., & Qiu, H. (2017). Topological entropy on subsets for fixed-point free flows. *Discrete and Continuous Dynamical Systems, 37*(12), 6319–6331. https://doi.org/10.3934/dcds.2017273
5. Wolf, C. (2020). A shift map with a discontinuous entropy function. *Discrete and Continuous Dynamical Systems, 40*(1), 319–329. https://doi.org/10.3934/dcds.2020012
6. Wang, Y., Chen, E., & Zhou, X. (2022). Mean dimension theory in symbolic dynamics for finitely generated amenable groups. *Discrete and Continuous Dynamical Systems, 42*(9), 4219–4236. https://doi.org/10.3934/dcds.2022050
7. Hou, X., Tian, X., & Zhang, Y. (2023). Topological structures on saturated sets, optimal orbits and equilibrium states. *Discrete and Continuous Dynamical Systems, 43*(2), 771–806. https://doi.org/10.3934/dcds.2022169
8. Zhang, W., Ren, X., & Zhang, Y. (2023). Upper capacity entropy and packing entropy of saturated sets for amenable group actions. *Discrete and Continuous Dynamical Systems, 43*(7), 2812–2834. https://doi.org/10.3934/dcds.2023030
9. Kucherenko, T. (2024). Nonlinear thermodynamic formalism through the lens of rotation theory. *Discrete and Continuous Dynamical Systems, 44*(12), 3760–3773. https://doi.org/10.3934/dcds.2024077
10. Burgos, S. (2026). On the structure of the Birkhoff-irregular set for subshifts of finite type. *Discrete and Continuous Dynamical Systems, 49*, 248–265. https://doi.org/10.3934/dcds.2025167

## 数学核查与六项去向

逐步复核了：§3 图像斜率不变、截面端点和长度、径向与角向乘积、首次退出条带；§4 耦合收缩映射、统一小半径和错误控制余量；§5 停止树的全部状态覆盖与计数；§6 零集拉回、所有瞬态逆分支、Egorov 紧集先于参数选择及面积平衡；§7 无例外面积运输、厚化区间端点延拓、失败比例、严格指数余量和边界逼近；§8/附录 D 全区间压缩、两次积分确认 C²、真实面积、物理距离及逆面积指数；§9/附录 A–C 各例的全局收缩、可行性、Jacobian、概率比较和失配判据；附录 E 的 Taylor/商求导常数。各结论的范围、有限瞬态、端点、再进入、先固定块长后取 horizon 极限及交叉引用一并检查。

未暗中加强假设或削弱结论。20 个正式陈述与基线逐字一致只是防止误改的附加核对，不是正确性证据。实际数学性修订是纠正退出／容差的混淆、修正截面记号和宽度解释，并写出原有面积论证省略的中间步骤；没有新增定理。本轮没有留下已识别但未处理的现行证明缺口，仍可能存在本次审读未发现的问题。

| 历史结果 | 本轮最终去向与核查范围 |
| --- | --- |
| 逆面积指数下界 | §8.5，Corollary 8.2，p.24；保留并复核完整证明 |
| 角依赖径向例子 | Appendix C.1，pp.29–30；保留并复核 |
| 内部可行折叠 | Appendix C.2，Proposition C.1，pp.30–31；保留并复核 |
| 远处塌缩 | Appendix C.3，Proposition C.2，pp.31–33；保留并复核 |
| 匹配线性有限时域概率比较 | Appendix A，pp.26–27；Lemma A.1 p.27；保留并复核 |
| arsinh 正熵与可行状态收敛 | 继续留在 `paper/archive/P6_PRECISION_COST_37p_f510c91`，Appendix D pp.34–36，Proposition D.1 p.35；本轮不放回正文，也不声称重新核验其证明 |

## 验收判断与剩余限制

- **问题引入**：§1.1 的数值词 `01`、角区间和面积解释，比 H2023/S2023 所读开头更少依赖该方向的先验术语；K2011、F2020 对贡献的定位仍更快。本稿摘要依然容纳多项结果，不能称为同样集中。
- **定义安排**：初态随机性、两种预算、精确可行和概率对象现在可在使用处理解；这与所读参照“先说明用途再定义”的局部组织相当。§2.2 同时设置一般幂次及匹配子类，§3 保留两套乘积，仍增加记忆负担，因附录 B 实际使用而保留。
- **证明衔接**：§6.3 的三类状态和 §7.4 的宽度选择已可直接跟随；K2011 的单输入体积链是具体参照。§3.2→Lemma 4.1→Lemma 7.2 仍需回查图像估计，§8.2 与 Appendix D 仍跨正文和附录。前者兼有符号组织负担，后者的分层有明确数学理由；都不能据新增导读宣布轻松易读。
- **英文表达**：删掉了相邻重复保证和报告式自我辩护；保留自然的完整论证句，没有机械统一句长。证据支持这些局部缺陷已减轻，不支持“英文整体至少超过十篇”或任何 AI 来源不可辨认的结论。

Wang–Huang (2022), DOI 10.1088/1361-6544/ac4f33 的完整覆盖缺口仍在；本轮没有借摘要确认新颖性，也没有重复搜索拖延修改。作者身份、实际人工贡献、数学审读和署名批准仍须人类作者确认。现有真实 AI 披露保持逐字原文。

最终稿重新编译为 **35 页**，连续终读并逐页检查 1–35 页；没有发现裁切、重叠、缺字、公式越界或失效引用。编译日志无未定义引用、重复标签、LaTeX 警告及 overfull/underfull 提示。没有改变字号或以省略证明压缩篇幅。旧原稿、基线和历史报告保留，完成普通提交及远端回读后停止。

TeX SHA-256：`fa7c4e901c29ab068e522534e667fd3176b1c357b6d8dbd31adebd3ab1bdfa5f`。  
PDF SHA-256：`1f3584a20331342d4d3f551be443b0f78719841a607b87714ecab3e243b7476f`。
