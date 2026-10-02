# P6 mathematical contribution research

基线论文：*Positive invariance entropy under uniform state convergence*。

研究目标为 Annals of Mathematics、Inventiones Mathematicae、Journal of the American Mathematical Society、Acta Mathematica。目标是寻找有实际数学分量的贡献；不承诺成功，不用扩写、加维数或小幅放宽假设代替升级，不擅自降低目标。

- [`CURRENT.md`](CURRENT.md)：最新裁决与下一入口。
- [`original/`](original/)：未经改动的原稿、SHA-256 与归档说明。
- [`research/R03/REPORT.md`](research/R03/REPORT.md)：最新原件获取、定义补核及未完成范围。
- [`research/R03/MATHEMATICS.md`](research/R03/MATHEMATICS.md)：按 WHS2019 原定义计算二进制锥体的测度熵。
- [`research/R03/SOURCES.md`](research/R03/SOURCES.md)：上传原件哈希、arXiv API 实查、APA / DOI 与获取缺口。
- [`research/R03/NEXT_COMMAND.md`](research/R03/NEXT_COMMAND.md)：完成剩余来源补核的指令。
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

R03 已取得 WHS2019 期刊原件并补核关键定义，算出二进制锥体中初始面积概率的两种测度不变熵均为 `log 2`。NWH2022 的精确题名 / 作者 arXiv 查询未命中，完整原件仍缺；查找由助手执行，无需同时取得两篇才继续独立核验。核心结构观念及压力对偶已有覆盖，当前暂停路线 A 的新证明扩展和整篇改写。新增计算按已有定义的应用处理，具体族的独立首创性未认证；原稿、R01 和 R02 均保留。

复现数学笔记 PDF：在安装 LaTeX 的环境执行 `latexmk -pdf -interaction=nonstopmode -halt-on-error research/R01/P6_R01_Mathematical_Note.tex`。原稿需单独编译，不覆盖。此仓库仅存 P6，不修改其他暂停项目。
