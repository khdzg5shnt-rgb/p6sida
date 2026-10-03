# P6 mathematical contribution research

基线论文：*Positive invariance entropy under uniform state convergence*。

研究目标为 Annals of Mathematics、Inventiones Mathematicae、Journal of the American Mathematical Society、Acta Mathematica。目标是寻找有实际数学分量的贡献；不承诺成功，不用扩写、加维数或小幅放宽假设代替升级，不擅自降低目标。

- [`CURRENT.md`](CURRENT.md)：最新裁决与下一入口。
- [`original/`](original/)：未经改动的原稿、SHA-256 与归档说明。
- [`research/R04/REPORT.md`](research/R04/REPORT.md)：路线 A 两个精确候选的有界筛选，零个通过四大门槛。
- [`research/R04/MATHEMATICS.md`](research/R04/MATHEMATICS.md)：固定状态概率反例，以及随时间优化公式的已有覆盖方法证明。
- [`research/R04/SOURCES.md`](research/R04/SOURCES.md)：实际依赖的原始证明范围和准确 APA / DOI。
- [`research/R04/NEXT_COMMAND.md`](research/R04/NEXT_COMMAND.md)：R04 完成停点；仅有具体新证据才重启评估，不自动 R05。
- [`research/R03/REPORT.md`](research/R03/REPORT.md)：两篇期刊原件补核、覆盖判断和暂停裁决；保留先前获取记录。
- [`research/R03/FULLTEXT_AUDIT.md`](research/R03/FULLTEXT_AUDIT.md)：单位反证、正面积时变共轭反例、修正后的压力对偶及证明边界。
- [`research/R03/MATHEMATICS.md`](research/R03/MATHEMATICS.md)：按 WHS2019 原定义计算二进制锥体的测度熵。
- [`research/R03/SOURCES.md`](research/R03/SOURCES.md)：原件身份、完整性、SHA-256、APA / DOI 和实际全文审查范围；历史检索保留。
- [`research/R03/NEXT_COMMAND.md`](research/R03/NEXT_COMMAND.md)：已完成的 R03 停点核验指令，保留历史；最新入口以 R04 为准。
- [`research/R02/REPORT.md`](research/R02/REPORT.md)：独立复核、已有覆盖和暂停理由。
- [`research/R02/MATHEMATICS.md`](research/R02/MATHEMATICS.md)：初始状态投影冲突与压力对偶的自含计算。
- [`research/R02/SOURCES.md`](research/R02/SOURCES.md)：本轮一手正文读取范围、APA / DOI、版本及全文失败记录。
- [`research/R02/NEXT_COMMAND.md`](research/R02/NEXT_COMMAND.md)：以新增完整原件为条件的下一指令。
- [`research/R01/REPORT.md`](research/R01/REPORT.md)：两条路线及本轮数学结果、重要性判断。
- [`research/R01/PROOF_AUDIT.md`](research/R01/PROOF_AUDIT.md)：14 项陈述的复核与未审查部分。
- [`research/R01/SOURCES.md`](research/R01/SOURCES.md)：核实的 APA、DOI、版本和全文缺口。
- [`research/R01/P6_R01_Mathematical_Note.tex`](research/R01/P6_R01_Mathematical_Note.tex)：完整自含英文数学推导。
- [`research/R01/FAILED_ATTEMPTS.md`](research/R01/FAILED_ATTEMPTS.md)：被否定目标、方法接口与适用边界。
- [`research/R01/NEXT_COMMAND.md`](research/R01/NEXT_COMMAND.md)：R01 留下的原始恢复指令；已由 R02 执行并保留历史。

R03 两篇期刊原件已到位，NWH2022 的 31 页全文及 WHS2019 的相关证明已补核。新反例否定 NWH 原文在单向约束包含下的时变共轭等式；原文混用二进制对数和指数权重也使所写变分公式失效。统一为自然单位并允许熵为负无穷后，已有压力对偶方法仍可用，R01–R03 的自含计算不因此推翻。二进制锥体的面积概率 WHS 熵仍为 `ln 2`，锥顶概率仍为零。

R04 已完成用户授权的一次有界筛选。固定初始状态概率候选被可数紧集反例否定；即使每个时间范围的整数 / 分数覆盖相等，固定概率仍不能恢复长期覆盖率。随时间优化的条件版本来自经典分数覆盖方法，不是新的四大主原理。零候选通过，路线 A 主定理扩展及整篇改写继续暂停，不自动 R05。目标不变，原稿、R01–R03 及全部历史保留；首创性未全面认证，当前没有需要用户另找的文章。

复现数学笔记 PDF：在安装 LaTeX 的环境执行 `latexmk -pdf -interaction=nonstopmode -halt-on-error research/R01/P6_R01_Mathematical_Note.tex`。原稿需单独编译，不覆盖。此仓库仅存 P6，不修改其他暂停项目。
