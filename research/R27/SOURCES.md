# R27：来源、实际读取与覆盖边界

2026-10-05 UTC。本轮没有新增第三方论文下载；复用已取得原件。
未增加名单外论文，未重复失败获取，也不以检索未命中认证首创。
新证明自含。完整来源清单及此前阅读范围保留在
[四大研读 SOURCES.json](../FOUR_JOURNAL_STUDY/SOURCES.json) 和
[R26/SOURCES.md](../R26/SOURCES.md)。以下区分重新阅读与沿用范围。

## 1. 四大研读的实际使用

Hochman, M. (2014). On self-similar sets with overlaps and inverse
theorems for entropy. *Annals of Mathematics, 180*(2), 773–822.
https://doi.org/10.4007/annals.2014.180.2.7

- [正式记录](https://annals.math.princeton.edu/2014/180-2/p07)本轮核对；
  已有正式 PDF 50 页、668014 字节，SHA-256
  `e50bcf12c8d854286031b108b47c36be281b8632c5041a471221293fd99287d0`。
- 本轮重读 PDF 页1–2、5–7：自相似对象、Theorems 1.3–1.4 的
  非等收缩率处理、§1.3 的卷积分解。其余已读页3–4、14–18、
  37–40按研读记录复用，没有宣称本轮全文重审。
- 不同平移可以有不同收缩率，原文同时保留这些信息；本轮据此
  在局部真实条带中同时追踪径向与初态尺度。
- 不能直接调用：本轮 A_u 是状态反馈下的全时域可行区域，未
  建立原文的自相似卷积分解或概率测度平稳恒等式。其逆定理
  不给首次真正不可行的面积带，也不保证任何预选控制目录最优。
- Theorem 2.8 的阈值修正仍按研读中记录的正式脚注提示保留。
  本轮没有调用该定理，因此没有借用未经核准的熵阈值。

Shmerkin, P. (2019). On Furstenberg’s intersection conjecture,
self-similar measures, and the L^q norms of convolutions.
*Annals of Mathematics, 189*(2), 319–391.
https://doi.org/10.4007/annals.2019.189.2.1

- [正式记录](https://annals.math.princeton.edu/2019/189-2/p01)本轮核对；
  已有正式 PDF 73 页、656730 字节，SHA-256
  `00b0a8cc5d02434672018e0d0e40386e5971739ef2b9e536ade9d7592feab3d3`。
- 本轮重读 PDF 页9–12：Lemmas 1.7–1.8 的局部质量/纤维计数
  证明，以及动态模型(1.3)–(1.5)、pleasant model及其分离条件。
  原有页1–4、13–17、21–22、41–42、47–48按记录复用。
- 实际启发：先证明全部 A_u 的质量上界，再用覆盖不等式；
  同时另处理稀少但决定全 Q 成本的物理状态。
- 覆盖边界：本轮没有对应动态卷积模型、L^q 维数或所需投影
  Frostman 数据。Lemma 1.8 在已有质量假设下计数纤维，不能
  自行给出本轮式(4)。必须先证明截断可行区域和首次越界的
  物理控制；这些步骤在 R27 自含完成，而不是从其定理直接套出。

没有把其余八篇再次列为必需依赖；它们的版本和真实范围原样
保留，没有扩大为全篇覆盖审计。四大方法学习不是期刊档位证据。

## 2. 与实际目录和图几何直接比较的已有原文

Kawan, C., & Da Silva, A. (2018). Invariance entropy for a class of
partially hyperbolic sets. *Mathematics of Control, Signals, and
Systems, 30*, Article 18.
https://doi.org/10.1007/s00498-018-0224-2

- [Springer正式页面](https://link.springer.com/article/10.1007/s00498-018-0224-2)
  本轮再次核对身份，并重读可见正式附录 §1.2 的开头、Lemma 6.5
  及 Lemma 6.6 的陈述和完整证明。Formal主文全篇仍未通读。
- 已有作者稿 arXiv:1711.01181v2，403967字节，SHA-256
  `f7041c7fa49d498e632141febdc234ab6b3c6a37a8a7ee4c28aca6acf45eda1f`。
  本轮重读印刷页4–5的 P1–P4/主结果范围、页10–11的 Lemma3.6
  与固定半径 Bowen-ball，以及页25的图变换设置；完整 §6.2 的
  既有读取按 R26 复用，未宣称新增正式全文。
- 图变换、导数锥和体积工具是已有方法。本轮不将(11)的新对象
  当作新发明的图变换。
- 原文 all-time lift 的 P1 要求双向 Q 内轨迹；(3)使有界双向
  轨迹只能为原点：V(x₀)≤θ^j sup_QV 对所有j，故x₀=0。
  因此不能以同一个有正面积Q直接使用其主定理。物理平面在
  公共原点的两个导数特征值都小于1；吹起角向坐标中的扩张
  也不能冒充原文的物理不稳定丛。
- 不只靠假设不同排除覆盖：已读图证明可用来控制光滑图和
  固定半径 Bowen-ball，但其 C_δ 常数没有给出本轮随时域缩小
  容差的联合估计。还需从实际约束推出截断可行像、首次真越界
  带、所有可行前缀典型性及式(24)物理余量；本轮逐项证明。
  未读正式主文不记作已排除覆盖。

Chen, Z., & Zhong, X. (2024). Invariance complexity and
equi-invariability for control systems. *Journal of Mathematical
Analysis and Applications, 539*(2), Article 128533.
https://doi.org/10.1016/j.jmaa.2024.128533

- 使用用户已提供的正式原件
  `1-s2.0-S0022247X24004554-main.pdf`，441166字节，SHA-256
  `62e442a6c2bd78b01b623fe4a2d7c46bcc65587a7714003ea7df9eaf7250ffcc`。
  本轮重读封面和正式页6–7的 Definitions2.10–2.11、Theorem2.12
  及印刷证明（包括(1)引用旧证明的事实，不能称原文在此详证）。
  Examples4.1–4.2等此前范围复用。DOI在线重定向本轮返回错误，
  没有因此将已经取得的正式PDF标缺失或重复下载。
- 本轮目录与原文 outer complexity 是同类真实对象，仅采用
  0,…,n和联动δ_n；不是新定义。Theorem2.12 给每个固定容差下
  的有限目录等价性质，未量化该目录常数随容差缩小的增长。
  其证明不能自行推出式(4)、γ/β的联合极限或全Q的稀少见证。
- (18)本身给固定δ下统一有界目录，这与原文性质相容。
  正的指数精度成本不与固定容差的有界复杂度矛盾。

这两项均为已有正文的定向复核，未补找新的第三方原件。没有
将它们的未读部分或领域内其他论文写为全面排除。

## 3. 其他已核原件保持原状态

Chen, H., Huang, Y., & Zhong, X. (2026). Variational principles of
invariance entropy dimension. *Journal of Differential Equations,
453*, Article 113819. https://doi.org/10.1016/j.jde.2025.113819

陈虎.pdf已在R21全文核验：24页、841646字节，SHA-256
`8a431cc9d2668c84464205ae30eed7c2bdeedb42c44e265aed2657dea8bccd7c`。
本轮再次核对文件哈希，复用R21的全文范围，未声称再次全文重读。
指定分划、圆柱和时间α次归一的变分方法不能省去这里的实际
初态约束证明。正文与证明覆盖裁决见R21，不以改换术语否定它。
不再标缺失、不要求用户重找。

Yang, R., Chen, E., Yang, J., & Zhou, X. (2025). Bowen’s equations
for invariance pressure of control systems. *SIAM Journal on
Control and Optimization, 63*(2), 1104–1128.
https://doi.org/10.1137/23M1607684

复用R26记录的作者稿 arXiv:2309.01628v3 §3.1及其余已读范围；
正式主文未全文读取的限制保留。指定分划/停止权重和压力工具
不证明实际重叠下哪条目录最优，本轮也没有新增压力根计算。

Hutchinson, J. E. (1981). Fractals and self-similarity.
*Indiana University Mathematics Journal, 30*(5), 713–747.
https://doi.org/10.1512/iumj.1981.30.30055

Csiszár, I. (1998). The method of types.
*IEEE Transactions on Information Theory, 44*(6), 2505–2523.
https://doi.org/10.1109/18.720546

经典停止权重和类型方法沿用R26的来源与版本范围。
Hutchinson作者重排稿既有§2.1、5.1–5.3范围保留；Csiszár正式
全文未读状态保留。本轮所用树加法、类型界和熵差均自含给出。
没有因为这些经典公式另写一次便声称原创。

## 4. 覆盖归属与判断限度

| R27步骤 | 归属 | 本轮真实增量 |
|---|---|---|
| 局部Taylor、图锥、可求和畸变 | 经典光滑/图方法 | 在仅有匹配一阶矩阵且可行像截断的约束下，证明实际词区间与面积上界。 |
| 边界管与有限逆映射 | 经典几何和变量代换 | 对任意近似输入给早期真越界 O(δ) 损失，接入全时域下界。 |
| 全部可行前缀典型集 | R26逻辑与经典概率/测度工具 | 缺词/截断情形仍成立，有限非塌缩外部动力学不改变统一紧集量词。 |
| 有界串轨迹实现 | 经典压缩映射工具 | 不预设全词可行，在实际耦合径向递推下构造困难状态并证明错控制物理余量。 |
| 边界率结论 | 新几何接口后的R26式成本推导 | 转移到只有局部匹配jets的新类；没有另称类型优化是新理论。 |
| 非化约实例 | 基本共轭不变量 | 两点边界像交集与旧类连续集不相容，仅限保持Q的同时控制共轭。 |

已读原文没有直接给出这里完整的式(4)、缺词情况下的实际见证
及二者合成的边界。此判断限于实际读取范围，不是全领域首创
认证；正式未读范围及其他可能相关文献继续限制更高期刊评估。
本轮不需要用户补找原件，没有一区、TOP或四大的自动认证。
