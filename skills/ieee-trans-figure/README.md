# ieee-trans-figure

用于 IEEE Transactions 论文图表的设计、生成、审查和润色。适合消融柱状图、跨域性能表图、t-SNE/PCA 特征空间、混淆矩阵、时频图、频谱图、topographic map、方法框图和多面板论文图。

## 核心原则

图不是装饰，而是证据链的一部分。每个 figure 都必须先定义：

- 核心结论。
- 对应主张。
- 数据与协议。
- 面板结构。
- 可视化不能证明的边界。

## 必读文件

触发后先读 `../_shared/ieee-trans-guidelines.md`。生成或审查图时读：

- `references/ieee-figure-contract.md`
- `references/ablation-and-feature-visualization.md`

## 默认交付

- Figure contract。
- 面板布局建议。
- 尺寸、字体、颜色、导出格式约束。
- caption/legend 草案。
- 审稿风险检查。

如果用户要求直接画图，需要先明确使用 Python、R、MATLAB 或已有脚本；不要用虚构数据生成看似真实的论文图。
