# R03：原件到位与 arXiv 查询证据

核查日期：2026-10-03（Asia/Shanghai）。以下只关闭实际完成的获取或定义接口，不关闭未读证明。没有将第三方论文全文复制进本仓库。

## 已取得的 WHS2019 原件

用户本聊天提供 `18m1197862.pdf`，400654 字节，24 页；PDF 首页、末页、作者、期刊及 DOI 核对通过，印刷页为 310–333。

SHA-256：`23330e1e34452e66919a68264d672a2d8e281b5c9bba60c07c79b53c549dc363`。

Wang, T., Huang, Y., & Sun, H.-W. (2019). Measure-theoretic invariance entropy for control systems. *SIAM Journal on Control and Optimization, 57*(1), 310–333. https://doi.org/10.1137/18M1197862

实际阅读：§2 的有限 Borel invariant partition 与 itinerary cylinder；Definitions 4.1 / 4.3（所有初始状态概率、局部质量衰减、对分划取下确界）；Definition 4.7 和 Theorem 4.8 的实际状态双可测共轭及其证明；Definition 4.9 的 maximal irreducibility；Theorems 6.4 / 7.2、Corollary 6.5 的准确陈述及 clopen 条件。PDF 页 7、17 的图像用于交叉检查公式。全篇其余技术证明尚未逐行审完。

这份原件确认优化测度为 `M(Q)`，并不要求状态不变或提升不变；也确认其共轭保留实际状态和受控实现。这些条件不能由 R01 的抽象提升图式共轭替代。本次应用完全自含，不依赖未审的变分证明。

## NWH2022：论文身份已核实，arXiv 未命中

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

## 其他全文入口与失败项

中山大学黄煜旧页面 `/node/346` 和现页面 `/teacher/HuangYu` 的索引列出该论文；网页读取工具返回 403。本次改用标准 HTTP 读取现页面，取得 49164 字节真实 HTML，核对其第 60 项书目；检查所有链接，没有发现该论文的 PDF / arXiv 链接。王涛湖南师大公开页可读，但其所列代表成果没有给这篇完整稿。ResearchGate 仅给请求全文入口，未联系作者。

Crossref 的全文链接指向 Elsevier 期刊 API，实际跟随其 `PII:S002203962200184X` 的 XML 与纯文本两种入口，均只返回 195 字节 SiteUnavailable 占位页，不是正文。出版社索引标 Open archive；OpenAlex 和 Semantic Scholar 也标 bronze，并只给 DOI / 期刊页面，本次没有列出 arXiv 外部标识或可下载的仓储版本。聚合元数据只用于寻找入口，不用于认证数学覆盖，也不能证明没有作者稿。

下一获取方向由助手继续承担：新增的合法作者公开稿、机构仓储入口或可读取的期刊正文。不能要求用户先找齐两篇才能审查已到位的 2019 原件。没有新入口时保留 2022 缺口，不循环相同失败请求、不用摘要排除覆盖。此次未重新完成勘误普查；R02 的勘误审查边界和其他版本缺口保留。
