# R34：实际来源、覆盖与方法归属

2026-10-07 UTC；基线 `aa59d61301e4951914ee49ce3b7b3a7c5fe599ee`。
本轮复用 R33 结果，未获取新论文或重复失败检索。
两篇已有正式控制论文定向复核；历史范围不改写成本轮重新全文阅读。

## 1. 项目采用链

完整读取 CURRENT、R32唯一TeX（1567行）、R33四份文件，
恢复R31数学641行、R27数学663行；最终唯一源码全文回读。
关键链为R27局部几何与物理见证、R31双乘积失配、现稿匹配停止计数、
R33非塌缩可行瞬态。未以历史通过判断代替本轮核验。
原稿仅回看标题、摘要和开篇主张（源码15–126行），未重审全部原稿。
旧R32 TeX SHA-256为
`0128a95c6e3b2bdb75754fb3870c921ca36d64fb1fd03033f7599c339bdfc595`；
旧18页PDF和全部证明由Git历史保留。新稿哈希见REPORT。

## 2. 两篇正式正文

### Chen–Zhong（2024）

Chen, Z., & Zhong, X. (2024). Invariance complexity and
equi-invariability for control systems. *Journal of Mathematical
Analysis and Applications, 539*(2), Article 128533.
https://doi.org/10.1016/j.jmaa.2024.128533

已有16页正式原件 `1-s2.0-S0022247X24004554-main.pdf`，本轮再次核对SHA-256：
`62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc`。
实际重读pp.1–2身份及连续控制映射框架，§2.2 pp.6–7，
Definitions2.10–2.11、Theorems2.12–2.13、Corollary2.14及所印证明。
Theorem2.12(1)转引未当作另读被引完整证明。

框架已允许非单射；本稿目录属于已有outer spanning，时刻编号为0,…,n。
固定容差的有限覆盖/Baire论证不量化目录常数在容差—时域联合极限的速度。
仍需实际双尺度带、固定紧集瞬态面积和物理下界连接；已读证明没有从
零面积临界建立这些连接。非单射与outer catalogue不作为对象首创。

### Chen–Huang–Zhong（2026）

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of
invariance entropy dimension. *Journal of Differential Equations,
453*, Article 113819.
https://doi.org/10.1016/j.jde.2025.113819

陈虎.pdf是R21已全文核验的24页正式原件，841646字节。
本轮再次核对SHA-256：
`8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`。
不得标缺失或再次索取。
本轮重读pp.1–2身份和引言、系统框架开头，pp.7–9的
Lemma2.11、Theorems2.12–2.13及所印证明、加权覆盖定义开头。
指定分划完整定义及§3.1 Proposition3.1 pp.9–11所印证明复用R33；
其余全文复用R21，未声称本轮重新全文阅读。

该文允许非单射连续映射；逆像是集合拉回，测度无需不变。
Lemma2.11抽取使用指定分划的嵌套同编码圆柱；Theorems2.12–2.13
从圆柱质量得到时间α次权重，Proposition3.1处理圆柱加权/整数覆盖。
它们不能未经物理比较用于任意近似输入A_u。
本稿额外证明全部可行瞬态零集拉回、固定紧集多逆图δ管带及局部
首真越界`δλ_w/P_w`。不是仅凭定义不同排除覆盖，或以变分原理代替目录证明。
两篇上述范围未给省略物理连接的等价结果；不是全领域首创认证。

## 3. 既有版本范围

Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class of
partially hyperbolic sets. *Mathematics of Control, Signals, and
Systems, 30*, Article 18. https://doi.org/10.1007/s00498-018-0224-2

正式图变换附录及作者稿arXiv:1711.01181v2的既有范围沿R32/R33；
正式主文未全文读。本轮不新增阅读或声称正式整篇已排除覆盖。
固定半径lift体积估计不直接给收缩原点附近联合容差—时域率；
本稿局部图锥和真越界面积自含证明。

Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen's equations
for invariance pressure of control systems. *SIAM Journal on
Control and Optimization, 63*(2), 1104–1128.
https://doi.org/10.1137/23M1607684

正式身份/DOI与作者稿arXiv:2309.01628v3的引言、Theorems1.1–1.4、
§3.1 Proposition3.5等范围沿R32/R33；正式主文未全文读。
成本阈值和压力是计数背景，不能取代任意近似输入物理比较。
没有新增正式全文获取或把未读版本记为已排除。

其余七条既有参考文献的准确APA、DOI、版本及真实范围沿
[R32/SOURCES](../R32/SOURCES.md)，正文保留同一11条参考文献。
WHS2019、NWH2022既有全文审查不变；陈虎正式全文没有缺口。
Federer1996再版仅是R33官方书目/目录记录，未读章节不是本稿证明依赖，
没有新增到参考文献或用于排除覆盖。

## 4. 方法归属

| 步骤 | 归属与用途 |
|---|---|
| 局部逆函数、C¹换元、Lipschitz零集保持 | 经典；Lemma4.1自含可数逆图及可行域归纳，无新面积公式 |
| Egorov、紧内逼近 | 经典；同一物理紧集同时处理全部前缀典型性、有限临界删除，先于所有精度 |
| 固定窗口多逆图与早期面积 | R33非塌缩结构推论；允许实际折叠，无全Q逆Jacobian下界 |
| Taylor、图锥、畸变 | 经典方法和R27/R31几何；完整截面及实际λ_w/P_w带自含陈述 |
| 类型、停止权重、相对熵 | 经典；完整谱归R29，失配结构归R31，不是R34新证明 |
| 实际可行折叠 | R33范围实例，证明确有非单射成员；非单射本身不是新对象 |

未新增分区体系/年份核验或选刊，不认证一区/TOP。
具体独立用途、适用限制和阶段定位见REPORT。
