# 电路 symbol 视觉参考

先浏览整组例图的实际渲染结果，观察形状、端口、连线和文字如何形成一致的视觉风格，
再按当前遇到的构图问题查看细节。每种表达手法都可借鉴到不同类型的电路中。

| 观察重点 | 从图中学习什么 | 可查看的例图 |
|---|---|---|
| 比例与疏密 | 主体如何贴合内容，文字与图形如何分配空间，重复级如何保持均匀节距 | [自举采样开关](examples/bootstrap.svg)、[七位可编程延时链](examples/dcdl7.svg) |
| 对称与对齐 | 成对支路如何围绕共同轴线展开，串联图元如何形成平直、易追踪的路径 | [差分采样比较器](examples/differential-sampler.svg)、[多级比较器](examples/multistage-comparator.svg) |
| 端口与控制分组 | 控制端如何靠近作用点，长标签如何旋转摆放，主路径与辅助路径如何分区 | [差分采样比较器](examples/differential-sampler.svg)、[七位可编程延时链](examples/dcdl7.svg) |
| 重复结构的压缩 | 如何用代表性图元、重复数和位宽表达阵列，同时保留独立控制的含义 | [七位可编程延时链](examples/dcdl7.svg)、[寄存器与延时](examples/register-delay.svg) |
| 功能抽象的取舍 | 哪些关系值得展开，哪些细节可收为功能形状，抽象后的图元如何与外部路径相接 | [自举采样开关](examples/bootstrap.svg)、[差分采样比较器](examples/differential-sampler.svg) |
| 线条与局部符号 | 实线、虚线、节点和空心圆如何区分信号、控制、连接与极性；反馈交叉和时钟边沿如何保持清楚 | [多级比较器](examples/multistage-comparator.svg)、[寄存器与延时](examples/register-delay.svg) |

放大时检查节点、交叉线、开关触点和端口的连接位置；缩小时检查功能形状、主要路径、文字与控制分组是否仍清楚。
例图中的拓扑、通道数、位宽、阻值比例和端口名服务于各自的示例。目标 symbol 的这些内容由目标电路确定，
可见标签、`data-port` 和功能说明也应与目标接口一致。
