# IEEE-skills-main

面向 IEEE Transactions on Cybernetics, IEEE Transactions on Human-Machine Systems, IEEE Transactions on Neural Networks and Learning Systems 的本地 skill 生态。

本项目从 `ieee_corpus/` 中 10 篇近年 IEEE Transactions 论文反推写作、润色、图表与预审规则。核心原则是：先建立数学对象，再写文字；先闭合实验防线，再提升语言；所有强结论都要能追溯到方法定义、消融、跨数据集验证或统计检验。

## 目录

- `ieee_corpus/`: 用户提供的 PDF 论文语料。
- `analysis/`: PDF 文本抽取与证据索引。
- `skills/_shared/ieee-trans-guidelines.md`: 所有 IEEE skills 必读的共享准则。
- `skills/ieee-trans-proposal-writer/`: 研究方案与论文 proposal。
- `skills/ieee-trans-writing/`: IEEE Transactions 论文起草与重构。
- `skills/ieee-trans-polishing/`: IEEE 风格润色、翻译与逻辑修补。
- `skills/ieee-trans-figure/`: 论文图表设计、生成与审查。
- `skills/ieee-trans-reviewer/`: 投稿前强审稿协议。

## 使用原则

每个 skill 触发后都必须先读取 `../_shared/ieee-trans-guidelines.md`。不要把 Nature 写作风格直接迁移到 IEEE；IEEE 版本更重视符号定义、目标函数、算法步骤、复杂度、可复现实验和消融链条。

如果用户材料不足，先输出缺口清单和可继续执行的最小版本；不要编造数据、实验、引用、显著性或结论。
