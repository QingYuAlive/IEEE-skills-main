# ieee-trans-writing

用于起草、重构或补写 IEEE Transactions 风格论文段落和章节。它不是通用英文写作工具，而是把作者材料组织成“问题定义 -> 数学方法 -> 实验防线 -> 受限结论”的论文写作流程。

## 适用场景

- 写 abstract、introduction、related work、method、experiment、discussion、conclusion。
- 把中文实验笔记改写成 IEEE 论文段落。
- 把已有方法说明重构为公式先行的 Method。
- 把实验结果组织成审稿人能接受的 Results 分析。

## 必读共享准则

触发后必须先读 `../_shared/ieee-trans-guidelines.md`。如果要写方法，继续读 `references/equation-first-methods.md`；如果要写实验或结果，读 `references/bulletproof-results.md`；如果要写具体章节，读 `references/section-patterns.md`。

## 默认输出

除非用户只要最终段落，否则先给出：

1. 检测到的章节与论文类型。
2. 一句话 thesis。
3. 公式/实验/证据骨架。
4. 正文草稿。
5. 未支撑主张与需要补的材料。
