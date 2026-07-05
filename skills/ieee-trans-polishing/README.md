# ieee-trans-polishing

用于 IEEE Transactions 论文的英文润色、中文到英文改写、段落结构修补和结果分析收紧。它优先保护科学主张和证据边界，而不是把句子改得更夸张。

## 适用场景

- 润色 abstract、introduction、method、experiments、discussion。
- 将中文科研笔记翻译成 IEEE 论文英文。
- 降低 AI 味、口语化、空泛夸张和重复表达。
- 修补结果分析中过度解读、证据不足或逻辑跳跃的问题。

## 使用方式

触发后必须先读取 `../_shared/ieee-trans-guidelines.md`。根据任务读取：

- `references/claim-calibration.md`: 主张强度、动词、hedging。
- `references/structural-repair.md`: 段落结构、中文式逻辑、方法段顺序。
- `references/result-analysis-tightening.md`: 结果分析、消融解释、可视化解读。

默认输出“润色后文本 + 关键修改说明 + 风险提示”。如果原文有不被证据支持的主张，会保留技术边界而不是强行美化。
