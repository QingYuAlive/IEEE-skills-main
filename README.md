# IEEE Skills

一组面向 IEEE Transactions 写作流程的 Codex skills，覆盖研究方案设计、论文起草、语言润色、图表生成和投稿前审稿。

目标场景包括 IEEE Transactions on Cybernetics、IEEE Transactions on Human-Machine Systems、IEEE Transactions on Neural Networks and Learning Systems，以及相近的机器学习、神经网络、时间序列、生物信号、工业诊断和 domain generalization 论文。

## Skills

- `skills/ieee-proposal-writer/`: 研究方案、符号体系、方法公式化、实验矩阵和投稿前 proposal 审查。
- `skills/ieee-writing/`: Abstract、Introduction、Method、Experiments 等论文部分的起草与结构重写。
- `skills/ieee-polishing/`: IEEE 风格英文润色、中文到英文改写、claim calibration 和逻辑修补。
- `skills/ieee-figure/`: IEEE 栏宽、字体、配色、LaTeX 数学标注和可复现实验图代码生成。
- `skills/ieee-reviewer/`: 模拟严苛审稿人，对数学定义、理论漏洞、实验协议、消融和表述边界做投稿前审查。

共享规则位于 `skills/_shared/ieee-guidelines.md`，由各个 skill 在运行时按需读取。

## Installation

将需要的 skill 目录复制到本地 Codex skills 目录即可，例如：

```powershell
Copy-Item -Recurse .\skills\ieee-writing $env:USERPROFILE\.codex\skills\
Copy-Item -Recurse .\skills\ieee-polishing $env:USERPROFILE\.codex\skills\
```

也可以整体复制 `skills/` 下的所有 `ieee-*` 目录。

## Usage Examples

```text
Use ieee-proposal-writer to turn my sEMG force-domain generalization idea into a rigorous proposal.
```

```text
Use ieee-writing to draft the Method section from this notation ledger and objective function.
```

```text
Use ieee-reviewer to audit this manuscript before TCYB submission.
```

```text
Use ieee-figure to generate a double-column ablation figure from these arrays.
```

## Repository Notes

This repository is intended to store reusable skill instructions and templates. Do not commit private PDFs, proprietary datasets, generated model outputs, or large local analysis artifacts unless they are explicitly meant to be public.
