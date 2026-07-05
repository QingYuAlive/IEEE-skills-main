# ieee-trans-reviewer

用于 IEEE Transactions 投稿前的强审稿模拟。它从审稿人视角检查 novelty、数学定义、实验协议、基线公平性、消融链条、复杂度和结论边界。

## 适用场景

- 投稿前预审。
- 检查方法是否像“模块堆叠”。
- 找实验设计漏洞。
- 找理论/公式/符号问题。
- 审查图表和结果分析是否过度解读。

## 必读文件

触发后必须先读 `../_shared/ieee-trans-guidelines.md`。根据稿件类型读取：

- `references/aggressive-review-protocol.md`
- `references/empirical-defense-checklist.md`
- `references/theory-loophole-checklist.md`

## 输出

默认输出包括：

1. 审查边界。
2. 总体风险等级。
3. Major concerns。
4. Minor concerns。
5. 必须补的实验/公式/文字。
6. 是否建议继续投稿、重写或补实验。

该 skill 不写作者回复信；它先把问题挖出来。
