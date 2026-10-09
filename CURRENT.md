# P6 当前状态

本轮从 main `97060923f46bc270a75637625ebe3ddf37cd6d28` 的 35 页稿继续，完成现行全文数学复核、十篇 DCDS 作者版的定向重读、必要修订及读者验收。开始时远端没有新增提交。只处理 P6，单代理，无新研究、投稿或联系他人。

唯一现行英文稿：*Precision and reliability costs in contracting control systems*。
[完整 TeX](paper/P6_PRECISION_COST.tex) 与 [35 页 PDF](paper/P6_PRECISION_COST.pdf) 对应。
[本轮修改与验收说明](research/COMBINED_PAPER/FINAL_READER_ACCEPTANCE_20261010.md) 记录前后对照、十篇原文的实际重读页段、验证范围和剩余差距；[上一轮数学复核](research/COMBINED_PAPER/FINAL_MATH_READ_20261010.md)、[DCDS 比较](research/COMBINED_PAPER/DCDS_FINAL_REVISION_20261010.md) 及 [来源记录](research/COMBINED_PAPER/DCDS_SOURCES_20261010.json) 保持历史原文。

主线仍为精度—可靠性目录率及面积失真障碍。本轮从收敛与控制选择的矛盾引入摘要，明确精确可行的含义，纠正首次退出不等于违反容差的解释和固定半径截面记号，展开面积比值、求和及平衡参数的推导，改清厚化宽度并删并重复说明。20 个正式陈述逐字保留，未缩小结论，也未把行文改善称为新数学。

| 六项结果 | 最终去向 |
| --- | --- |
| 逆面积指数下界 | §8.5，Corollary 8.2，p.24 |
| 角依赖径向例子 | Appendix C.1，pp.29–30 |
| 内部可行折叠 | Appendix C.2，Proposition C.1，pp.30–31 |
| 远处塌缩 | Appendix C.3，Proposition C.2，pp.31–33 |
| 匹配线性有限时域概率比较 | Appendix A，pp.26–27；Lemma A.1 p.27 |
| arsinh 正熵与可行状态收敛 | 37 页归档 Appendix D，pp.34–36；Proposition D.1 p.35 |

完整重读现行稿全部证明及附录，连续终读修订稿，逐页查看全部 35 页渲染图。十篇 PDF 的字节哈希与旧清单一致；本轮定向重读共 68 页，没有冒充再次全文通读 241 页。编译收敛，无未定义引用、重复标签、LaTeX 警告或 overfull/underfull 提示。重查常数依赖、紧集选择顺序、首次退出与再进入、严格指数余量、端点和极限顺序；未识别需改变正式结论的数学错误。这是 AI 辅助检查，不是独立人类数学认证。

§3.2、Lemma 4.1、Lemma 7.2、§8/Appendix D 仍有较重阅读负担。具体段落的组织可与参照比较，证据不足以认定整篇达到十篇共同水平；没有真人测试或“无法辨认 AI”的保证。Wang–Huang 2022 全文覆盖缺口未关闭，未据摘要确认新颖性。作者信息及人工审读/批准仍待确认，真实 AI 披露保持原文。本轮没有把已移入历史的 arsinh 证明计入现行稿审查。

TeX SHA-256：`fa7c4e901c29ab068e522534e667fd3176b1c357b6d8dbd31adebd3ab1bdfa5f`。
PDF SHA-256：`1f3584a20331342d4d3f551be443b0f78719841a607b87714ecab3e243b7476f`。

旧 35/37 页精确归档、原始稿、全部历史报告保持不变；本轮 35 页基线和较早 34 页稿可由相应提交恢复。恢复入口见 [RESTORE](research/COMBINED_PAPER/RESTORE.md)。完成本轮普通提交与远端逐字节回读后停止，不自动开启下一轮。
