# R30 来源、实际范围与方法归属

2026-10-06 UTC。本轮是 R29 准确谱的英文稿整合，不开展广泛检索。
复用 R28–R29 原件、来源记录及更早实际阅读范围，未新增论文下载，
未重复失败获取，也未把旧阅读改记为本轮重新全文阅读。
正式身份与 DOI 沿用已核官方版本和仓库记录；没有以检索未命中
认证首创。未读正式主文仍限制新颖性判断。

## 1. 本轮实际读取及证明依赖

完整读取开始 SHA `726ab9434154cde63dab6fa378a5b8dd1d0463af` 下的
CURRENT、唯一论文 TeX、R29/MATHEMATICS、REPORT、SOURCES、NEXT_COMMAND；
对照 R27/MATHEMATICS §§2–3、6–8 的真实采用依赖及 R28 稿的完整
对应证明。原稿题名、摘要、引言及开头定理只用于版本贡献比较，
不重做历史全稿审计。

R27 给实际图结构、径向尺度、任意输入面积及物理错控制余量；
R29 给按全部停止叶长和词频计数、较短实际前缀强制、三段优化。
R30 §6 将其统一写入正文，没有加入新的动力学假设或待证引理。

| 来源 | 版本与已经实际读取的范围 | 对正文的关系、未解决的覆盖范围 |
|---|---|---|
| Chen–Zhong 2024 | 已取得 16 页正式 PDF。R28 直接读取 §2.2 pp.6–7，Definitions 2.10–2.11、Theorems 2.12–2.13、Corollary 2.14 及所印证明；2.12(1) 的转引不能算成另有全文证明 | 同一有限外目录对象的定义覆盖；固定容差有界性及等度框架不直接给随 n 改变容差的准确常数。本稿需另证真实面积和物理见证，不能只凭定义差异排除其方法覆盖 |
| Chen–Huang–Zhong 2026 | 陈虎.pdf 已在 R21 核验正式身份与完整性并全文读取，共 24 页；本轮复用，不标缺失 | 指定不变分划圆柱、时间 α 次归一、非必需不变的测度及变分原理；R21 已对照证明，未给任意近似输入集合 A_u 的所需几何比较。本轮新计数没有令其变成真实目录定理 |
| Kawan–Da Silva 2018 | 正式可见附录 Lemmas 6.5–6.6、Proposition 6.7 及 Lemma 3.6 闭包论证；作者稿 arXiv:1711.01181v2 的相关体积/图变换部分、P1–P4 和 Lemma 3.6，实际页码范围沿 R22/R28。正式主文未全文读取；转引或“类似证明”不记作已读完整自含证明 | 图变换和体积畸变背景，不认证首创方法。已读部分围绕部分双曲全时域 lift；本类向原点收缩且有奇异角向 blow-up，仍需实际有限时域与 δ_n 桥接。未读正式部分不记为已排除覆盖 |
| Yang 等 2025 | 正式身份、页码、DOI 已核；采用作者稿 arXiv:2309.01628v3 的相关成本阈值/压力部分（含 §3.1）；正式正文未全文读取。范围沿 R21–R29 | 指定不变分划的压力与 Bowen 方程是已有方法；不能替代任意近似输入真实几何。没有宣称正式版本已被逐页排除等价覆盖 |
| Csiszár 1998 | 正式身份和 DOI 已核；正文未全文读取。本轮不增记阅读范围 | 类型计数归于经典方法；§6 自含证明所用两条二项式界，不依赖未读命题 |
| Hutchinson 1981 | 已有重排作者文本的 §2.1、§§5.1–5.3；正式全文未全部审查 | 分支乘积和停止尺度属经典工具。本稿二子权重和为一只是辅助树恒等式，不是实际初态分划假设 |
| Wang–Huang–Sun 2019 | 正式原件 18m1197862.pdf。相关正文和证明已在 R03 补核；本轮仅重读正式封面确认作者姓名、卷期页码与 DOI | 测度不变熵背景，没有把其测度对象当成所有实际近似输入的目录。第三作者必须写 Sun, H.-W. |
| Nie–Wang–Huang 2022 | 正式原件 1-s2.0-S002203962200184X-main.pdf，31 页全文已在 R03 读取；本轮复用原有审查范围 | 测度不变熵与变分方法背景；原文历史纠错由 R03 保留，不依赖有问题的时变共轭公式推出本稿谱 |
| Kawan 2013；Colonius 2012；Colonius–Hamzi 2021 | 正式身份、DOI 和已有定义/相关稳定化部分的实际范围沿 R03/R05/R28；本轮无新增正文阅读 | 不变熵、指数稳定化及实际稳定化背景。未把衰减要求与约束邻域全时域可行性混为一谈，也未标为全文排除覆盖 |

上述记录不是完整领域新颖性综述。陈虎正式全文已经取得；需要
真实目录的受控几何桥接，并不等于宣布所有既有方法都无法延伸。

已核复用原件的身份记录（不冒充本轮重新全文阅读）：

| 原件 | 字节数 | SHA-256 |
|---|---:|---|
| Chen–Zhong 2024 正式 PDF | 441166 | 62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc |
| 陈虎.pdf / CHZ2026 正式 PDF | 841646 | 8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c |
| Kawan–Da Silva 作者稿 v2 | 403967 | f7041c7fa49d498e632141febdc234ab6b3c6a37a8ee4c28aca6acf45eda1f |

## 2. 方法与新增内容逐项归属

| 步骤 | 已有工具 | 本项目内的实际桥接 |
|---|---|---|
| 截断可行图及径向/角向比较 | Taylor 估计、图锥、可求和畸变 | R27 从指定导数及向原点收缩推出完整闭截面，允许空/单点/截断；不假设末端映满 |
| 任意输入覆盖面积 | 测度管带、有限 Jacobian、几何级数 | R27 区分编码变化与首次真正不可行，保留早期 O(δ) 损失和全部中间约束；重新进入不移除首次约束 |
| 固定典型物理紧集 | Bernoulli 大偏差、Borel–Cantelli、Egorov、紧内逼近 | R27 对全部可行前缀统一典型，故同一集先于全部精度指数与序列 |
| Full-Q 上界 | 停止尺度、类型计数 | R29 使用 R27 实际前缀与共同尾部；控制不同叶长成本后只得到构造上界，不认定树最优 |
| Full-Q 下界 | 固定频率块计数 | R27 真实正半径见证的错误控制余量；R29 用严格较短前缀与 δ_n 作物理比较。符号词数本身不足够 |
| 三段闭式与差距 | 熵不等式、单变量比值导数 | R29 统一推论与评价，R30 完整整合；不是新压力或反熵定理 |

四大研读的实际作用沿 R27：学习典型质量与全部初态的区别、以及
从符号量到真实几何的桥接要求。本轮没有调用 Hochman 或 Shmerkin
反定理推出控制目录，也没有因此宣称同样的成果分量。

## 3. 核实后的 APA 与 DOI

1. Chen, Z., & Zhong, X. (2024). Invariance complexity and equi-invariability for control systems. *Journal of Mathematical Analysis and Applications, 539*(2), Article 128533. https://doi.org/10.1016/j.jmaa.2024.128533
2. Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of invariance entropy dimension. *Journal of Differential Equations, 453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819
3. Colonius, F. (2012). Minimal bit rates and entropy for exponential stabilization. *SIAM Journal on Control and Optimization, 50*(5), 2988–3010. https://doi.org/10.1137/110829271
4. Colonius, F., & Hamzi, B. (2021). Entropy for practical stabilization. *SIAM Journal on Control and Optimization, 59*(3), 2195–2222. https://doi.org/10.1137/20M1367775
5. Csiszár, I. (1998). The method of types. *IEEE Transactions on Information Theory, 44*(6), 2505–2523. https://doi.org/10.1109/18.720546
6. Hutchinson, J. E. (1981). Fractals and self-similarity. *Indiana University Mathematics Journal, 30*(5), 713–747. https://doi.org/10.1512/iumj.1981.30.30055
7. Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class of partially hyperbolic sets. *Mathematics of Control, Signals, and Systems, 30*, Article 18. https://doi.org/10.1007/s00498-018-0224-2
8. Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9
9. Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013
10. Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862
11. Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen's equations for invariance pressure of control systems. *SIAM Journal on Control and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

更正说明：R28/SOURCES 中 WHS2019 的 “Sun, S.” 是错误缩写。
R30 重核官方原件封面为 “HAI-WEI SUN”，当前 APA 使用 H.-W.。
论文原有署名正确；R28 历史来源文件不覆写。此身份更正不是数学增量。

## 4. 覆盖裁决与未读边界

在上述实际读取范围内，采用链仍需独立的任意近似输入面积界及
物理错控制余量，没有发现可直接删除这些步骤的等价已读定理。
R29 谱优化本身由经典计数完成，不能被当作首创公式框架。
未读正式版本范围保留；不以“定义不同”或“检索未命中”宣称完整
覆盖排除。这些限制影响新颖性和定位证据，不把已自含的证明
变成依赖未读文献的证明计划。

本轮没有核实分区体系和年份，也没有作一区/TOP 档位声明。
对已发表论文的比较只用于具体对象、方法和证明接口，不据刊名
倒推当前稿竞争力。不要求用户再找已经取得的原件。
