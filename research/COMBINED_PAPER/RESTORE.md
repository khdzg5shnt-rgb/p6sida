# P6 当前稿与历史恢复入口

唯一现行英文稿为 [完整 TeX](../../paper/P6_PRECISION_COST.tex) 和 [35 页 PDF](../../paper/P6_PRECISION_COST.pdf)。先读 [CURRENT.md](../../CURRENT.md) 及 [本轮数学与读者验收说明](FINAL_READER_ACCEPTANCE_20261010.md)。本轮基线为 `97060923f46bc270a75637625ebe3ddf37cd6d28` 的 35 页稿；重新核查全部现行证明，并恢复十篇 DCDS 作者版定向重读。历史报告保留各自的旧页码，不以旧结论替代本轮核查。

控制字母表及 arsinh 比较已移出现行稿，但完整数学内容保存在 37 页归档。其他五项指定结果仍在现行稿，位置见 CURRENT。没有新增研究命题。历史 NEXT_COMMAND 不构成自动续研授权。

| 入口 | 身份 |
| --- | --- |
| [本轮验收说明](FINAL_READER_ACCEPTANCE_20261010.md) | 当前 35 页稿的必要修订、十篇原文比较位置及尚存差距 |
| 35 页稿提交 `97060923f46bc270a75637625ebe3ddf37cd6d28` / [当时说明](FINAL_MATH_READ_20261010.md) | 本轮基线；在该提交的 paper/P6_PRECISION_COST.tex 及对应 PDF 恢复 |
| 34 页稿提交 `ea9577ed24ceebed452179d586e5c1350346020b` | 较早 DCDS 取舍后的完整稿；在该提交的同一路径恢复 |
| [DCDS 修订说明](DCDS_FINAL_REVISION_20261010.md) / [来源记录](DCDS_SOURCES_20261010.json) | 上一轮 34 页稿的十篇全文比较、取舍、验证与限制 |
| [归档说明](../../paper/archive/README.md) | 35/37 页 TeX/PDF 精确快照及哈希 |
| [37 页 TeX](../../paper/archive/P6_PRECISION_COST_37p_f510c91.tex) / [PDF](../../paper/archive/P6_PRECISION_COST_37p_f510c91.pdf) | `f510c91` 历史基线的逐字节副本；旧 Appendix B / D 的完整内容可在此恢复 |
| [35 页 TeX](../../paper/archive/P6_PRECISION_COST_35p_4daf068.tex) / [PDF](../../paper/archive/P6_PRECISION_COST_35p_4daf068.pdf) | `4daf068c7d31a245a6406b504ddbf4e1249a0761` 的逐字节副本 |
| [上一轮结构改写说明](READER_REWRITE_20261010.md) | 37 页历史稿的改动、五篇 JDE 参照和当时验证范围 |
| [上一轮终读记录](FINAL_READ_20261010.md) | 当时四处定点修改、35 页位置与限制 |
| [较早数学与行文记录](MATH_STYLE_REVIEW_20261010.md) | 五篇文献身份及当时核查，不代替本轮核读 |
| [内容恢复记录](CONTENT_RESTORATION_20261009.md) | 六项补回及完整轮次去向，保留历史页码 |
| [历史索引](P6_Research_History_Audit_20261009.md) | 修订前来源索引，不作为正确性前提 |
| [原始稿](../../original/P6_LIYO_Manuscript_SUBMISSION.tex) | 完整初稿，文件不覆盖；高维、lift、反馈、连续时间等历史内容保留 |
| [R01 笔记](../R01/P6_R01_Mathematical_Note.tex) / [PROOF_AUDIT](../R01/PROOF_AUDIT.md) | 早期成果及其真实核验范围 |
| [旧 RESULT_COVERAGE](RESULT_COVERAGE.md) / [FINAL_SELECTION](FINAL_SELECTION.md) | 历史合并稿对应及其后取舍 |
| R36 提交 `221376684d9b0476b4a2c7be2f09e22f50097bb7` | 当时折叠、塌缩及反馈正文快照 |
| 49 页稿提交 `22e9716c3fc656ac71029cbac566dd93ac56c04e` | 原稿与可靠性主线的旧完整合并版本 |
| 补回前提交 `609bdffd3e25f3a86231b450b1c0edb67e7bd766` | 27 页集中主线修订前稿 |

较早终读轮的修订基线为 `fea87f320bd4b1ea8c64ef7dbc1e8809378f4ac2`，对应六项补回后的35页稿。
该轮中断前已有未提交修订，续接采用后完成。当时位置：§9.2径向角依赖、§9.3折叠；
附录C pp.31–33，附录D pp.33–35。

历史源码在对应提交的 `paper/P6_PRECISION_COST.tex` 路径恢复，
不要用旧快照覆盖现行稿。各 R 目录的数学笔记和 NEXT_COMMAND 是历史记录，
读取它们不自动授权继续其暂停研究。

复现当前 PDF：在仓库根执行
`latexmk -pdf -interaction=nonstopmode -halt-on-error -outdir=/tmp/p6-paper-build paper/P6_PRECISION_COST.tex`。
出版前的人类作者与证明审读事实仍待确认；本轮没有选刊或投稿。
