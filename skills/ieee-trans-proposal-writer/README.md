# ieee-trans-proposal-writer

用于把一个 IEEE Transactions 方向的想法整理成可投稿论文的 proposal。适合 TCYB、THMS、TNNLS 风格的方法论文，尤其是领域泛化、对比学习、sEMG/EEG/IMU 时序信号、CNN/RNN/Transformer、两阶段训练和跨域实验。

## 核心用法

触发后必须先读取 `../_shared/ieee-trans-guidelines.md`。在正文起草前，先要求或协助用户建立三张表：

- Notation Table：数据、域、网络模块、损失、训练协议的符号。
- Argument Map：问题缺口、方法机制、理论/直觉、实验验证之间的映射。
- Evidence Table：每个主张对应的数据、消融、基线、统计或可视化证据。

如果用户只给出模糊想法，本 skill 先产出 proposal 骨架和缺口清单；如果用户已有实验结果，则把结果组织成 IEEE 审稿人能追踪的论证链。

## 输出

默认输出包括：

1. 研究问题与目标 venue 风险判断。
2. 必要符号表。
3. Argument Map。
4. 方法模块与目标函数草案。
5. 实验矩阵与消融矩阵。
6. 预审稿风险与下一步补证建议。
