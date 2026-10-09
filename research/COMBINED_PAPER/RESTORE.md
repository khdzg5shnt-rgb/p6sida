# P6 当前稿与历史恢复入口

截至 2026-10-09。唯一现行英文稿：
[paper/P6_PRECISION_COST.tex](../../paper/P6_PRECISION_COST.tex) 和
[35 页 PDF](../../paper/P6_PRECISION_COST.pdf)。
先读 [CURRENT.md](../../CURRENT.md) 和
[本轮实际采用与补回记录](CONTENT_RESTORATION_20261009.md)。
任务已完成并停止，没有待自动执行的新研究轮或投稿指令。

恢复层次与用途：

| 入口 | 身份 |
| --- | --- |
| [本轮采用记录](CONTENT_RESTORATION_20261009.md) | 当前六项补回、完整可见轮次对应及真实限制 |
| [历史索引](P6_Research_History_Audit_20261009.md) | 修订前 609bdffd 基线的来源索引，不能作为证明正确性的前提 |
| [原始稿](../../original/P6_LIYO_Manuscript_SUBMISSION.tex) | 完整初稿，文件不覆盖；高维、lift、反馈、连续时间等成果继续保存 |
| [R01 笔记](../R01/P6_R01_Mathematical_Note.tex)／[PROOF_AUDIT](../R01/PROOF_AUDIT.md) | 早期独立成果及其真实核验范围 |
| [旧 RESULT_COVERAGE](RESULT_COVERAGE.md)／[FINAL_SELECTION](FINAL_SELECTION.md) | 历史合并稿对应与其后取舍，不是当前全轮采用表 |
| R36 提交 `221376684d9b0476b4a2c7be2f09e22f50097bb7` | 当时折叠、塌缩及反馈成熟正文的 Git 历史快照 |
| 49 页稿提交 `22e9716c3fc656ac71029cbac566dd93ac56c04e` | 原稿与可靠性主线的旧完整合并版本 |
| 本轮父提交 `609bdffd3e25f3a86231b450b1c0edb67e7bd766` | 27 页集中主线修订前稿；上传 P6_1009.tex 与此稿字节相同 |

历史源码在对应提交的 `paper/P6_PRECISION_COST.tex` 路径恢复，
不要用旧快照覆盖现行稿。各 R 目录的数学笔记和 NEXT_COMMAND 是历史记录，
读取它们不自动授权继续其暂停研究。

复现当前 PDF：在仓库根执行
`latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=/tmp/p6-paper-build paper/P6_PRECISION_COST.tex`。
出版前的人类作者与证明审读事实仍待确认；本轮没有选刊或投稿。
