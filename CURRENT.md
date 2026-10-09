# P6 当前状态

截至 2026-10-10（Asia/Shanghai），已完成用户授权的一次“完整终读与定点修订”。基线 main 为 `b7d5336746a074689c5e4b3d4b94ce4af10a92ba`；恢复时无后续提交。

唯一现行稿：*Precision and reliability costs in contracting control systems*。
[TeX](paper/P6_PRECISION_COST.tex) 与 [35 页 PDF](paper/P6_PRECISION_COST.pdf) 对应。
最新记录：[FINAL_READ_20261010](research/COMBINED_PAPER/FINAL_READ_20261010.md)。
上一轮完整数学与行文记录：[MATH_STYLE_REVIEW_20261010](research/COMBINED_PAPER/MATH_STYLE_REVIEW_20261010.md)；保留历史身份，不覆盖。

本轮全文终读正文与四个附录，从定义核查证明链，未识别出需撤回正式结果的必要证明缺口。只改四处：收紧 S 与 L_a 的公式形式说明；删除两处重复总结/证明预告；纠正附录 D 对固定容差零率条件的解释——指数收缩足够，但关键是所有输入的一致趋零，不能与仅可行轨迹趋零混淆。

20 项正式陈述逐字保留，136 个唯一标签、17 个 proof 环境及 13 条文献保留；作者字段与 AI 披露不变。最终 35 页编译收敛，交叉引用、全文抽取及所有页面渲染检查完成。本轮定向回读同五篇 JDE 的具体段落；两篇正式版、三篇已核作者稿，不冒称本轮重新全文阅读外部五篇。

| 六项保留结果 | 当前最终位置 |
| --- | --- |
| 逆面积指数下界 | §8.4 / Corollary 8.1，p.23 |
| 角度影响径向收缩 | §9.2，p.25 |
| 内部可行折叠 | §9.3 / Proposition 9.1，pp.25–27 |
| 局部一致与远处塌缩 | §9.4 / Proposition 9.2，pp.27–28 |
| 匹配线性有限时域概率比较 | Appendix C，pp.31–33；Lemma C.1，p.32 |
| arsinh 正熵与可行状态收敛 | Appendix D，pp.33–34；Proposition D.1，p.33 |

Wang–Huang 2022 书目信息及 DOI 重新核实；正式下载实际返回验证码 HTML，未取得可核全文，直接覆盖缺口仍在。未解决范围仍包括反例准确可靠性谱及极限、折叠可靠性、塌缩高侧准确谱、一般失配高侧、任意正面积紧集高侧及暂停的策略最优问题。

真实作者信息、人工数学审读及稿件/披露批准仍待确认。AI 辅助复核不是独立人类同行认证；没有 AI 概率分数或不可检测承诺，没有提高既有期刊定位。

TeX SHA-256：`81b7aa9ce6a56f6a294c5eac94fbfa9af1a7c88f1c213864d26e04b9ebc0d18c`。
PDF SHA-256：`a405ab69c70f96e643b9d668186353afedeabfba4edf746095fe40eed6dc7384`。

原稿、旧稿、R01–R40 和旧报告均保留。六项采用来源见 [CONTENT_RESTORATION_20261009](research/COMBINED_PAPER/CONTENT_RESTORATION_20261009.md)，当前页码以上表为准；历史研究不构成自动续研授权。完成后停止，不自动 R41，不重启暂停问题，不投稿。
