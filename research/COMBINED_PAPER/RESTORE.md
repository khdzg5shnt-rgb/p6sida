# P6 当前稿与历史恢复入口

截至 2026-10-10（Asia/Shanghai）。唯一现行英文稿：
[paper/P6_PRECISION_COST.tex](../../paper/P6_PRECISION_COST.tex) 和
[35 页 PDF](../../paper/P6_PRECISION_COST.pdf)。
先读 [CURRENT.md](../../CURRENT.md) 和
[最新终读记录](FINAL_READ_20261010.md)。本轮基线为 `b7d5336746a074689c5e4b3d4b94ce4af10a92ba`。
四处定点修订不改变正式数学陈述；全部六项结果保留。最新位置及页码见 CURRENT 和 FINAL_READ。
上一轮 [完整数学与行文记录](MATH_STYLE_REVIEW_20261010.md) 及所有更早记录保留历史身份，其旧页码不覆盖当前页码。
任务已完成并停止，没有自动新研究轮或投稿指令。

恢复层次与用途：

| 入口 | 身份 |
| --- | --- |
| [最新终读记录](FINAL_READ_20261010.md) | 当前核查范围、四处修改、五篇定向比较、最终页码和未决事项 |
| [上一轮数学与行文记录](MATH_STYLE_REVIEW_20261010.md) | 上一轮完整修订、五篇文献身份及当时页码 |
| [上一轮采用记录](CONTENT_RESTORATION_20261009.md) | 六项补回、完整可见轮次对应及真实限制；保留历史页码 |
| [历史索引](P6_Research_History_Audit_20261009.md) | 修订前 609bdffd 基线的来源索引，不能作为证明正确性的前提 |
| [原始稿](../../original/P6_LIYO_Manuscript_SUBMISSION.tex) | 完整初稿，文件不覆盖；高维、lift、反馈、连续时间等成果继续保存 |
| [R01 笔记](../R01/P6_R01_Mathematical_Note.tex)／[PROOF_AUDIT](../R01/PROOF_AUDIT.md) | 早期独立成果及其真实核验范围 |
| [旧 RESULT_COVERAGE](RESULT_COVERAGE.md)／[FINAL_SELECTION](FINAL_SELECTION.md) | 历史合并稿对应与其后取舍，不是当前全轮采用表 |
| R36 提交 `221376684d9b0476b4a2c7be2f09e22f50097bb7` | 当时折叠、塌缩及反馈成熟正文的 Git 历史快照 |
| 49 页稿提交 `22e9716c3fc656ac71029cbac566dd93ac56c04e` | 原稿与可靠性主线的旧完整合并版本 |
| 补回前提交 `609bdffd3e25f3a86231b450b1c0edb67e7bd766` | 27 页集中主线修订前稿；上传 P6_1009.tex 与此稿字节相同 |

上一轮修订基线为 `fea87f320bd4b1ea8c64ef7dbc1e8809378f4ac2`，对应六项补回后的35页稿。
该轮中断前已有未提交修订，续接采用后完成。当时位置：§9.2径向角依赖、§9.3折叠；
附录C pp.31–33，附录D pp.33–35。

历史源码在对应提交的 `paper/P6_PRECISION_COST.tex` 路径恢复，
不要用旧快照覆盖现行稿。各 R 目录的数学笔记和 NEXT_COMMAND 是历史记录，
读取它们不自动授权继续其暂停研究。

复现当前 PDF：在仓库根执行
`latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=/tmp/p6-paper-build paper/P6_PRECISION_COST.tex`。
出版前的人类作者与证明审读事实仍待确认；本轮没有选刊或投稿。
