# ieee-trans-proposal-writer

面向 IEEE Transactions on Cybernetics、IEEE Transactions on Human-Machine Systems、IEEE Transactions on Neural Networks and Learning Systems 的 proposal-first 写作状态机。

它不是通用“帮我写论文”工具。它的核心职责是：在任何正文写作前，强制建立数学定义、目标函数、OOD 协议、消融矩阵和复杂度边界。

## 核心门控

如果缺少以下任一项，skill 必须停止正文写作，只能输出 `Blocked Math Gate` 或 `Blocked Evidence Gate`：

- 输入空间 `\mathcal{X}`、标签空间 `\mathcal{Y}`。
- 源域 `\mathcal{E}_{tr}` 和目标/OOD 域 `\mathcal{E}_{te}`。
- 编码器、投影器、分类器或预测器的形式化映射。
- 经验风险、IRM/GroupDRO/对比学习等约束项和总目标函数。
- OOD 测试协议，例如 held-out subject/session/force/load/dataset。
- 每个模块或损失项的移除/替换消融。
- 参数量、FLOPs、延迟、吞吐或训练开销等复杂度计划。

## 文件结构

保持克隆版结构不变：

```text
SKILL.md
README.md
references/
scripts/
templates/
```

其中 `scripts/build_proposal_docx.py` 只负责导出，不承载学术判断。

## 关键模板

- `templates/03_argument_map.md`: IEEE Theorem-Proof / Ablation-Defense argument map。
- `templates/04_section_contracts.md`: 每节的数学、证据、禁止主张和验证契约。
- `references/proposal-qa-rubric.md`: IEEE proposal QA 主评分表。
- `references/evaluation-rubric.md`: 兼容克隆 pipeline 的同口径评分表。

## 默认输出

- Math gate 状态。
- Notation ledger。
- Formal objective stack。
- Theorem/proof 或 mechanism-analysis 边界。
- Ablation-defense matrix。
- OOD protocol。
- Complexity and deployment contract。
- 允许写作或阻塞写作的明确结论。
