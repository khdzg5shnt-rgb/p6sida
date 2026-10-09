# P6 当前状态

本轮完成“十篇 DCDS 主刊全文对照、内容取舍与最终实质修订”。基线 main 为 `f510c91c5baadab6149bbca8d81bcb487c957cbf`；开始及提交准备时回查均无新增远端工作。只处理 P6，单代理执行，没有新研究、投稿或联系他人。

唯一现行英文稿：*Precision and reliability costs in contracting control systems*。
[完整 TeX](paper/P6_PRECISION_COST.tex) 与 [34 页 PDF](paper/P6_PRECISION_COST.pdf) 对应。
[本轮修改说明](research/COMBINED_PAPER/DCDS_FINAL_REVISION_20261010.md) 包含十篇准确引用、实际版本、逐篇比较、关键前后对照、取舍及剩余困难；[来源记录](research/COMBINED_PAPER/DCDS_SOURCES_20261010.json) 保存 URL、页码与哈希。

主线为精度—可靠性目录率及面积失真障碍。全覆盖证明前移，面积工具放在固定初态集与概率证明之前；Cantor 插值完整证明移至附录 D。控制字母表比较和 arsinh 比较移出现行稿，完整保存在 37 页归档，未删除历史成果。其他保留结论的假设、量词和证明范围没有缩小。

| 六项结果 | 最终去向 |
| --- | --- |
| 逆面积指数下界 | §8.5，Corollary 8.2，pp.23–24；陈述 p.24 |
| 角依赖径向例子 | Appendix C.1，pp.29–30 |
| 内部可行折叠 | Appendix C.2，Proposition C.1，pp.30–31 |
| 远处塌缩 | Appendix C.3，Proposition C.2，pp.31–33 |
| 匹配线性有限时域概率比较 | Appendix A，pp.26–27；Lemma A.1 p.26 |
| arsinh 正熵与可行状态收敛 | 37 页归档 Appendix D，pp.34–36；Proposition D.1 p.35 |

重新核读当前完整 TeX/PDF，连续终读最终稿并逐页查看全部 34 页渲染图。编译收敛，无未定义引用、重复标签、LaTeX 警告或 overfull/underfull 提示。重查局部几何、首次退出/再进入、紧集先选、常数依赖、严格指数余量和极限顺序；未识别需改变保留正式结论的数学错误。此为 AI 辅助核查，不替代独立人类数学审读。

十篇主刊论文均取得并阅读全文作者版本（共 241 个 PDF 页面），具体版本差异如实记录。比较没有给出“超过十篇”认证：§3.2、Lemma 4.1、Lemma 7.2、§8 与 Appendix D 仍较难读。无真人测试。Wang–Huang 2022（10.1088/1361-6544/ac4f33）全文覆盖缺口仍未关闭，未据摘要确认新颖性。真实作者信息、人工数学审读及稿件/AI 披露批准仍待确认。

TeX SHA-256：`aa2dc07baf0871cc707119ae496ff08b504754d65751373361335d956101be4b`。
PDF SHA-256：`3544384e3d3a62e6bd890a0a167e0a0c32de42703c6d5321e6e6125568f51a7c`。

35 页和 37 页 TeX/PDF 已精确归档于 [paper/archive](paper/archive/README.md)，并与祖先提交逐字节核对。原稿、旧报告、R01–R40 和所有历史记录保持历史身份。恢复见 [RESTORE](research/COMBINED_PAPER/RESTORE.md)。完成本轮普通提交与远端逐字节回读后停止，不自动开启下一轮。
