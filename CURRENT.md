# P6 当前状态

截至2026-10-10（Asia/Shanghai），已完成一次授权的“完整稿数学正确性复核、五篇同方向 JDE 原文对照与专业行文修订”，含中断续接。基线 main 为 `fea87f320bd4b1ea8c64ef7dbc1e8809378f4ac2`；恢复时远端没有后续提交，采用本地已有英文修订继续完成。

唯一现行稿：*Precision and reliability costs in contracting control systems*。
[TeX](paper/P6_PRECISION_COST.tex) 与 [35页PDF](paper/P6_PRECISION_COST.pdf) 对应。
完整数学与行文记录见 [MATH_STYLE_REVIEW_20261010](research/COMBINED_PAPER/MATH_STYLE_REVIEW_20261010.md)，恢复见 [RESTORE](research/COMBINED_PAPER/RESTORE.md)。

本轮复核20项正式陈述、全部采用证明和六项补回接口，未发现需撤回主定理或限制既有六项陈述的实质错误。英文修订重写摘要、引言和结论，明确两种预算与物理覆盖接口，按无临界点、零面积临界、正面积塌缩组织例子。五篇相关JDE原文均全文阅读，其中两篇正式版、三篇身份已核作者稿；每篇至少两项具体写法对照已落实。未新增引用、研究命题或系统类。

| 六项保留内容 | 最终位置 |
| --- | --- |
| 固定反例的逆面积指数下界 | §8.4，Corollary 8.1，pp.23–24 |
| 角度影响径向收缩 | §9.2，pp.25–26 |
| 内部可行折叠 | §9.3，Proposition 9.1，pp.26–27 |
| 局部一致与远处塌缩 | §9.4，Proposition 9.2，pp.27–29 |
| 匹配线性有限时域概率比较 | Appendix C，pp.31–33；Lemma C.1 在 p.32 |
| arsinh 正熵与可行状态收敛比较 | Appendix D，pp.33–35；Proposition D.1 在 p.34 |

20项正式陈述按label逐字保留，136个唯一标签、17段proof；附录B的2到1有限计数反例、13条文献、作者字段及真实AI披露不变。编译、交叉引用、全文抽取与最终35页全部渲染检查完成。

[CONTENT_RESTORATION_20261009](research/COMBINED_PAPER/CONTENT_RESTORATION_20261009.md) 保留上一轮六项补回及39个可见目录的采用表，原页码由本轮记录更新；成果去向不变。旧JDE_STYLE_REVIEW与全部既有研究记录不覆盖。R01–R09独立保存，R09真实率极限存在已证但准确常数未知；R10–R13不是策略最优定理。

未解决范围仍包括反例准确可靠性谱及极限、折叠可靠性率、塌缩高侧准确谱、一般失配高侧、任意正面积紧集高侧及暂停的策略最优问题。Wang–Huang2022正式全文的直接覆盖核验、真实作者信息与人工数学审读/批准仍待完成。AI复核不是独立人类同行认证，不承诺无法识别AI使用。

TeX SHA-256：`25215530f4926e42bbbc9d07fb05112fc2ae9492e4182e975e979c25208f4e40`。
PDF SHA-256：`c03c5df6ca45c9d85db310bd2ee98a09e943a4f151d0a95bc81c9aab721195de`。
本轮只处理P6，未分派代理、读改P3/P4、选刊、投稿、联系他人或提高期刊定位。
完成后停止，不自动开启R41或重启暂停问题。
