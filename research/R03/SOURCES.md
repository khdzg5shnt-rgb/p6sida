# R03：原件到位与 arXiv 查询证据

**当前状态（完成补核，2026-10-03）：WHS2019、NWH2022 两篇期刊原件均已取得并核对；NWH2022 的 31 页全文已读。** 当前身份、哈希、阅读范围与 APA 见下文“完成补核”。先前 API / 获取失败记录仅作历史保留，不再表示缺少 2022 全文，也不要求重复失败检索。

## 首次获取阶段的历史记录

核查日期：2026-10-03（Asia/Shanghai）。以下只关闭实际完成的获取或定义接口，不关闭未读证明。没有将第三方论文全文复制进本仓库。

## 已取得的 WHS2019 原件

用户本聊天提供 `18m1197862.pdf`，400654 字节，24 页；PDF 首页、末页、作者、期刊及 DOI 核对通过，印刷页为 310–333。

SHA-256：`23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363`。

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

实际阅读：§2 的有限 Borel invariant partition 与 itinerary cylinder；Definitions 4.1 / 4.3（所有初始状态概率、局部质量衰减、对分划取下确界）；Definition 4.7 和 Theorem 4.8 的实际状态双可测共轭及其证明；Definition 4.9 的 maximal irreducibility；Theorems 6.4 / 7.2、Corollary 6.5 的准确陈述及 clopen 条件。PDF 页 7、17 的图像用于交叉检查公式。全篇其余技术证明尚未逐行审完。

这份原件确认优化测度为 `M(Q)`，并不要求状态不变或提升不变；也确认其共轭保留实际状态和受控实现。这些条件不能由 R01 的抽象提升图式共轭替代。本次应用完全自含，不依赖未审的变分证明。

## NWH2022：先前身份核实与 arXiv 查询（历史）

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

作者 Xiaoxiao Nie、Tao Wang、Yu Huang，卷页和 DOI 由出版社及 Crossref 再核实。[出版社条目](https://www.sciencedirect.com/science/article/pii/S002203962200184X)。此前取得的关键正文片段保留为片段状态，读取范围仍见 R02/SOURCES.md；本次没有取得完整期刊 PDF 或 HTML。

搜索引擎对完整题名、DOI、作者组合和 arXiv 域名的查询未找到可验证编号。由于 arXiv 搜索在网页读取工具中失败，本次另外直接请求官方 API，返回有效 Atom XML，逐项解析而非只看 HTTP 状态。

| 官方 API 查询式 | 实际返回 | 本轮判断 |
|---|---|---|
| `ti:"Measure-theoretic invariance entropy and variational principles for control systems"` | 0 条 | 原题名未命中 |
| `au:"Xiaoxiao Nie"` | 0 条 | 该完整姓名写法未命中 |
| `au:Nie_Xiaoxiao` | 0 条 | 另一姓名写法未命中 |
| `au:Wang AND ti:"invariance entropy"` | 0 条 | 此作者 / 题名组合未命中 |
| `au:Nie AND all:invariance` | 共 81 条，全部条目已返回；未发现目标题名、作者组合或改题名匹配 | 不能把别的 Nie 的论文当作目标 |
| `all:"invariance entropy"` | 共 47 条，全部条目已返回；有 DSK2016、KD2018、Zhong–Huang–Zou 等，未发现目标 | 宽查询也未命中，检索接口并非一律返回空 |

可复查的官方入口：

- [完整题名查询](https://export.arxiv.org/api/query?search_query=ti%3A%22Measure-theoretic%20invariance%20entropy%20and%20variational%20principles%20for%20control%20systems%22&start=0&max_results=100)。
- [完整作者姓名查询](https://export.arxiv.org/api/query?search_query=au%3A%22Xiaoxiao%20Nie%22&start=0&max_results=100)。
- [宽主题查询](https://export.arxiv.org/api/query?search_query=all%3A%22invariance%20entropy%22&start=0&max_results=100)。

本轮完整题名 XML 的 SHA-256：`514fa71c9df9434bd9f5f2c5fcb0e7ac132cd3f6b29477d9e14700af7ed71f38`；作者完整姓名 XML：`ae6d36446ee2c2ef8eda9b3bd0b73c23974ee4f53192ef3c0ec855f1289fe5fa`。API 响应含动态时间与查询标识，哈希只识别本轮字节，不保证今后相同。

**严格结论是“本轮未找到可验证的 arXiv 版本”，不是“已证明不存在 arXiv 版本”。** 可能的改题名、未关联 DOI 或姓名索引差异未被绝对排除；没有编造编号。

## 其他全文入口与失败项（历史，勿重试）

中山大学黄煜旧页面 `/node/346` 和现页面 `/teacher/HuangYu` 的索引列出该论文；网页读取工具返回 403。本次改用标准 HTTP 读取现页面，取得 49164 字节真实 HTML，核对其第 60 项书目；检查所有链接，没有发现该论文的 PDF / arXiv 链接。王涛湖南师大公开页可读，但其所列代表成果没有给这篇完整稿。ResearchGate 仅给请求全文入口，未联系作者。

Crossref 的全文链接指向 Elsevier 期刊 API，实际跟随其 `PII:S002203962200184X` 的 XML 与纯文本两种入口，均只返回 195 字节 SiteUnavailable 占位页，不是正文。出版社索引标 Open archive；OpenAlex 和 Semantic Scholar 也标 bronze，并只给 DOI / 期刊页面，本次没有列出 arXiv 外部标识或可下载的仓储版本。聚合元数据只用于寻找入口，不用于认证数学覆盖，也不能证明没有作者稿。

下一获取方向由助手继续承担：新增的合法作者公开稿、机构仓储入口或可读取的期刊正文。不能要求用户先找齐两篇才能审查已到位的 2019 原件。没有新入口时保留 2022 缺口，不循环相同失败请求、不用摘要排除覆盖。此次未重新完成勘误普查；R02 的勘误审查边界和其他版本缺口保留。

## 完成补核：原件身份、完整性与 SHA-256

使用本项目数据源里已提供的文件，不使用搜索摘要代替全文。两篇期刊 PDF 的题名、作者、DOI、卷页、首末页、页序和参考文献结尾均核对。PDF 可解析且全部页可读；哈希标识此次实际读取的字节，不声称存在出版社公开的逐字节校验值。

| 原件 | 实际数据源文件 | 字节数 | PDF 页数 / 印刷页 | SHA-256 |
|---|---|---:|---|---|
| WHS2019 | `08-18m1197862.pdf`（用户所称 `18m1197862.pdf`） | 400654 | 24 / 310–333 | `23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363` |
| NWH2022 | `10-1-s2.0-S002203962200184X-main.pdf`（用户所称 `1-s2.0-S002203962200184X-main.pdf`） | 459673 | 31 / 318–348 | `e649c92c54fdcdb5b300ba2ce56c71299c95a23171ac1f2d1e29f5d3ef788e90` |
| Kawan2013 | `07-pdf` | 2264873 | 290；本轮使用印刷页 56–57 | `c68fe56fc0c76324bcb34a5c878c13d659741bc966a81e12f62cd3fb50c957b6` |

WHS / NWH 的期刊身份与 DOI 又用 SIAM / ScienceDirect 原始书目核对；Kawan 书名、卷号、年份及 DOI 以已到位原件的题名页和版权页核对，书 DOI 的本轮网页读取未成功，不记成成功全文来源。原稿文件的 SHA-256 仍为 `47aa42836d78fa281d1ef18e1fbb20d5d311eeab0959077f775542b61249b869`。

## 完成补核：实际全文与证明审查范围

**NWH2022：全文。** 全部 31 页自首页到参考文献末页逐页读完，包含 §§2–5 的陈述、证明和补充说明。独立影响审查包括：

- 印刷页 320–321 的系统四项转移公理、输入平移 / 拼接、admissible pair 与 `[0,n]` spanning horizon。二维反例满足这些条件；不是将 `[0,n)` 的控制计数误作少一次状态约束。
- 页 321–325 的势函数、指数权重、最小目录上确界、离散 / 连续时间 log convention，以及 Lemma 2.3 的凸性、单调性、平移和连续性证明。自然单位下的正确部分另给自含对偶推导；不认证混合单位的印刷式。
- 页 325–326 的 Definition 2.4、Proposition 2.5 与全证明；逆向 spanning 步骤不能由单向约束包含推出。页 334 的 Theorem 3.11 / 页 335 的 Corollary 3.12 的继承关系也核验。
- 页 326–337 的抽象对偶、Definition 3.4、Proposition 3.6、Example 3.8、Theorem 3.13 及 Corollary 3.15；核验零压力层与全势函数对偶的等价所需单位、负无穷余域、分离证明与最大值。
- 页 337–343 的平衡态和切线泛函证明全文已读；本轮没有独立认证其中引用的泛性 / 唯一性外部定理，也不将这些性质应用于 P6。
- 页 344–347 的 inner pressure 与固定分划补充说明全文已读；Definition 5.5 的漏 log 经图像核实，不用于 P6 结论。

NWH PDF 物理页 4、5、8、9、14、29 的图像用于关键单位、共轭和定义核对。具体错误、反证及修复边界详见 [FULLTEXT_AUDIT.md](FULLTEXT_AUDIT.md)；“全文已读”不等于“全文全部结论都正确”。

**WHS2019：相关证明补审。** 在首次范围之外，补读 Propositions 4.4–4.6、Theorem 4.8、Propositions 4.11–4.12 / Theorem 4.13，Lemma 5.1 / Theorems 5.2–5.3 的质量与 cylinder 选择证明，Proposition 6.1 / Lemma 6.3 / Theorem 6.4 的 weighted cover 与 Frostman 证明，Lemma 7.1 / Theorem 7.2 的 packing mass / weak limit 证明及相应全局推论。重点核验任意初始状态概率、分划下确界、共同块时间、实际状态共轭、generator 和 clopen 使用处。物理页 17、19 的图像确认时间因子 / 指数系数遗漏。没有声称本轮逐行认证 WHS 全部 §§2–3、§8 符号例或每个外部依赖。

**Kawan2013：共轭原始边界。** Definition 2.4 与 Proposition 2.13 在印刷页 56–57，物理 PDF 页 79–80（扫描前置页使文本分段页号不同）。已读完整证明并看这两页图像。原文在同一 forward-inclusion 条件下给 exact entropy 单向不等式；outer entropy 另用 equicontinuity。这不支持 NWH 的无条件双向等式。本轮没有审完整本 290 页书。

**R01–R03 与原稿。** 完整回读 R01 自含英文数学笔记、R02 MATHEMATICS 以及 R03 指定记录；回查原稿依赖 NWH 的相关引文位置，未重做全部 14 项原稿审查。原稿、R01–R02 内容不改。R02 所列 arXiv:2003.06935 的 v5 / 2026-09-20 元数据再次核对，但本轮没有读完整 v5 或认证其与期刊版的全部差异；不把这次元数据核查说成全文补审。

## 完成补核：核实后的 APA 与 DOI

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

Nie, X., Wang, T., & Huang, Y. (2022). Measure-theoretic invariance entropy and variational principles for control systems. *Journal of Differential Equations, 321*, 318–348. https://doi.org/10.1016/j.jde.2022.03.013

Kawan, C. (2013). *Invariance entropy for deterministic control systems: An introduction* (Lecture Notes in Mathematics, Vol. 2089). Springer. https://doi.org/10.1007/978-3-319-01288-9

## 完成补核：检索边界与无需补找

本轮只对两篇 DOI / 完整题名及 conjugacy 关键词做有界 correction / erratum / corrigendum 核验，使用出版社与官方索引，未找到匹配正式勘误；不声称绝对不存在，也不认证本轮纠正首次发现。未重复前面的失败全文获取请求，未联系作者。完整原件已经到位，历史 arXiv 未命中不再阻碍其审查。

本次提交只保存研究记录和自含推导，没有把第三方 PDF 全文复制进公开仓库。当前没有需要用户另找的文章；以后若实际证明依赖确实缺失，单独发准确题名和已核实 DOI。其他既有依赖、版本与广泛首创性范围仍未全部认证。
