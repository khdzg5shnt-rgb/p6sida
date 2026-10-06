# R33：直接来源、真实范围及方法归属

2026-10-06 UTC。基线 a8712bcbcffd3d1983e37cb9eb195a8906a858c2。
本轮是有限可行瞬态的非塌缩结构推论，不是新不变熵定义、
面积公式或谱。只有两篇已有正式控制论文作定向正文复核，
没有新获取论文或重复失败下载。

## 1. 实际采用的项目证明

| 已全文读取文件 | 实际依赖 |
|---|---|
| CURRENT、R32 REPORT/SOURCES/NEXT_COMMAND | 最新成稿量词、文献边界和暂停问题 |
| 唯一 paper/P6_PRECISION_COST.tex | 全文1567行；§§2–7采用链，§9正面积塌缩，其余检查范围一致性 |
| R31/MATHEMATICS.md | 全文641行；两乘积、首真越界、典型性、完整尾部、物理下界与失配 |
| R27/MATHEMATICS.md | 全文663行；Taylor/图锥、截断闭区间、旧有限瞬态和实际有界串 |

旧局部几何无需全域逆。R33 独立证明可行域内零集/临界拉回、
固定紧集多逆分支界及任意输入早期越界。
采用旧结果定位其完整推导，不将历史通过裁决当作前提。
未重审无关历史，也未重开 R09–R14。

## 2. 两篇正式正文与逐项覆盖

### Chen–Zhong 2024

Chen, Z., & Zhong, X. (2024). Invariance complexity and
equi-invariability for control systems. *Journal of Mathematical
Analysis and Applications, 539*(2), Article 128533.
https://doi.org/10.1016/j.jmaa.2024.128533

项目已有16页正式原件，SHA-256：
62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc。
本轮重读 p.2 离散系统/连续 F_u 与 admissible pair 定义，
§2.2 pp.6–7 outer spanning 对象、Definitions 2.10–2.11、
Theorems 2.12–2.13、Corollary 2.14 与所印证明。
Theorem 2.12(1) 转引未当作另读完整被引证明。

公理已允许非单射连续映射。R33 目录是既有 outer catalogue，
仅时域写为0,…,n，删除单射要求不是对象首创。
Theorem 2.12 是每个固定容差各有一个对全部时域有效的
目录常数，有限覆盖/Baire证明不量化该常数随δ→0的速度。
它不给全部可行前缀的实际典型性或固定物理 T 的早期
C_Tδ面积界。推出联合时域—精度率，仍需 R33 Lemmas
33.2–33.5、旧局部 λ_w/P_w 带及物理困难状态。
这是具体定理/证明缺口，不是仅凭定义区别排除覆盖。

### Chen–Huang–Zhong 2026

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of
invariance entropy dimension. *Journal of Differential Equations,
453*, Article 113819.
https://doi.org/10.1016/j.jde.2025.113819

陈虎.pdf 是 R21 已全文审查的24页正式原件，841646字节，
SHA-256：
8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c。
本轮定向重读 §2.1 pp.2–4 连续控制系统、admissible pair、
指定 invariant partition/圆柱；§2.3–2.4 pp.6–9 的
Lemma 2.11、Theorems 2.12–2.13 及所印质量证明；
§3.1 pp.9–11 的加权覆盖/Proposition 3.1 及完整所印证明。
其余全文范围复用 R21，不写成本轮重新全文阅读。

它同样不要求单射。圆柱式中逆像符号是集合拉回，不能误读
为全域逆映射；测度无需不变也不是我们的区别。
Lemma 2.11 的不交抽取来自指定分划的嵌套同编码圆柱，
不经实际比较不能用于任意 A_u 的重叠覆盖。
Theorems 2.12–2.13 从已知圆柱质量转成时间 α 次权重，
Proposition 3.1 处理指定圆柱加权/整数覆盖。
它们未从临界集零面积导出全部可行瞬态零集拉回、固定 T
多逆分支δ管带或任意近似输入的首真越界 λ_w/P_w 面积。
这些连接先独立证明后，质量比较逻辑才可应用。
不直接以变分原理认定目录最优率，不将已取得全文标缺失。

两篇已读范围内没有省去该物理连接的等价定理；
这是有限范围比较，不是全领域首创或新颖性认证。

## 3. 经典工具、复用范围及版本边界

| 来源/工具 | 实际采用和限制 |
|---|---|
| 局部逆函数、C¹换元、局部Lipschitz零集保持 | 经典；R33 完整证明可数逆图、可行域归纳及有限紧集应用，无新工具主张 |
| Egorov、紧内逼近 | 经典；构造一个先于所有精度的 T，不让初态随 n 变化 |
| Borel–Cantelli、Bernoulli尾界、类型计数 | 现稿自含步骤；针对全部可行前缀而非指定编码 |
| Kawan–Da Silva 2018 | 正式附录及作者稿的既有体积/图变换范围沿R32；正式主文未全文读，不记为新补核或整体无覆盖 |
| Yang–Chen–Yang–Zhou 2025 | 正式身份/DOI已核，作者稿arXiv:2309.01628v3已读定理、成本阈值/Proposition3.5沿R32；正式主文未全文读。压力/停止工具不算新颖 |
| R18 饱和反例 | 现稿§9完整证明复核；正面积区域临界并映到射线，违反本轮条件 |

已有准确APA：

- Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class
  of partially hyperbolic sets. *Mathematics of Control, Signals,
  and Systems, 30*, Article 18. https://doi.org/10.1007/s00498-018-0224-2
- Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen's equations
  for invariance pressure of control systems. *SIAM Journal on Control
  and Optimization, 63*(2), 1104–1128. https://doi.org/10.1137/23M1607684

另核 Springer 官方书目页：
Federer, H. (1996). *Geometric measure theory* (Classics in
Mathematics reprint). Springer.
https://doi.org/10.1007/978-3-642-62010-2
该DOI对应1996再版，不写成已核1969原版DOI。
只读官方元数据/目录，正式章节未读；换元证明不依赖未读
正文，不据此排除覆盖。AMS原文页和Stanford讲义的一次
访问未成功，没有重试或记为已读；它们不是证明依赖或
用户补件要求。狭窄检索未给新直接覆盖定理，未命中不认证首创。

未新增分区体系/年份核验或选刊建议。经典有限瞬态工具的
结构应用扩大适用范围，不单独认证一区、TOP或四大分量。
