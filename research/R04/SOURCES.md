# R04：原始来源、阅读范围与覆盖证据

2026-10-03（Asia/Shanghai）。本轮使用已经提供的 NWH2022、WHS2019、Kawan2013 原件，不重新获取，不重复 R03 的失败检索。原件身份与完整性记录沿用 [R03/SOURCES.md](../R03/SOURCES.md) 的“完成补核”部分；其前面的失败记录只是历史。

## 已到位的三份原件

| 原件 / SHA-256 | 本轮实际依赖及回读范围 |
|---|---|
| WHS2019；`23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363` | Definition 4.1 的状态概率 / 局部 cylinder 域；§6.1 Proposition 6.1 的加权覆盖比较完整证明，§6.2 Lemma 6.3、Theorem 6.4 的完整证明及 Corollary 6.5 的条件（印刷页 324–327）。核对同层 cylinder 不交、开性与概率极限使用处。Theorem 7.2 只复查陈述，不再重审完整 packing 构造；其 R03 全证明补核记录保留。 |
| NWH2022；`e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90` | 印刷页 320–321 的 admissible pair、shift / concatenation、公理和 `[0,n]` horizon，Definition 2.1 的最小目录压力；页 331 的 Definition 3.4 测度域 M(U)，及页 346–347 的固定分划补充说明。全文已由 R03 读完，本轮没有把这些局部复读说成新一轮全文审查，不依赖混合单位式或错误共轭等式。 |
| Kawan2013；`c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6` | §2.1，印刷页 44–45：Definitions 2.1–2.2 的紧 admissible pair、完整 `[0,τ]` 状态约束、离散单位。任意紧初始集不要求正体积，也不要求 K = Q。没有重做 R03 的共轭证明核验或本书其余几何定理。 |

本轮自然对数计数相当于原书 / NWH 离散 bit 单位乘以 ln 2；不存在混用指数权重的压力步骤。R04 的反例采用全输入空间、紧凸 Q、全局光滑可逆控制映射和无限向前可行性。它没有强制 K 的正体积或 backward viability 条件，也没有冒称反驳带这些附加条件的结果。

准确 APA 与 DOI：

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

## C2 的经典原始覆盖来源

Chvátal, V. (1979). A greedy heuristic for the set-covering problem. *Mathematics of Operations Research, 4*(3), 233–235. https://doi.org/10.1287/moor.4.3.233

身份与 DOI / 卷页核对：[INFORMS 原始出版社条目](https://pubsonline.informs.org/doi/10.1287/moor.4.3.233)。实际正文来源为 [机构托管的三页期刊 PDF](https://people.stfx.ca/tjsmith/lec/W23CSCI435/Chv79.pdf)，不是讲义中的二手定理转述。在线 PDF 的三页文本已读，包括 pp. 234–235 以任意分数可行向量比较的证明；公式提取有局部缺损，未将缺损文字当作完整公式认证。故 [MATHEMATICS.md](MATHEMATICS.md) §3 另给有限对偶和无权舍入界的完整自含证明。未成功取得本地原始 PDF 字节，不虚列 SHA-256，也未上传第三方原件到仓库。

从此原文采用的内容仅为有限 set-cover 的经典分数比较 / 舍入方法；模式约化及其渐近应用在本项目中独立写出。这里足以证实方法已有覆盖，不需要靠“检索没找到”来认证新颖性。

Lovász, L. (1975). On the ratio of optimal integral and fractional covers. *Discrete Mathematics, 13*(4), 383–390. https://doi.org/10.1016/0012-365X(75)90058-8

这项只核对了出版社索引题名、摘要、卷页和 DOI；本轮未读其完整原件，不把它作为已审完的证明依赖。Chvátal 原文及上面的自含证明已足够支持本轮 C2 覆盖判断，不要求用户补找该文。

## 仓库依赖与检索边界

先全文读取 CURRENT.md、R03/FULLTEXT_AUDIT.md、REPORT.md、SOURCES.md、NEXT_COMMAND.md。R03 原件补核与停点核验已经完成，其暂停判断作为历史出发点而非数学正确性前提。

回读 R01 自含数学笔记的二进制归一化、逆分支和有限可行前缀证明，以及 R02/MATHEMATICS.md §§1–2 的投影 / 目录识别论证。R04 对自己使用的这些步骤重新推导，不依赖尚未复核的其他历史证明；没有重算面积熵、二进制压力、提升因子熵、outer / tracking 熵或混沌部分。

对 fractional covering / state-measure variational 关键词做过两组有界检索；只将原始出版社 / 原文用于覆盖结论。检索中的其他元数据没有作为全文证据，未找到精确结果也不据此声称首次发现。本轮没有据零散元数据扩成维数或第三路线。

未完成其他模型类别、版本、全部外部依赖或首创性的普查；R04 不产生新文献勘误主张，也不重复 R03 勘误核验。C1 用完整反例直接排除，C2 用完整已知方法推导排除升级资格。目前没有需要用户补找的文章。
