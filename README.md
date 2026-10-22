# Analog Artist Skills

用于模拟电路 symbol 与原理图绘制的 agent skills，包含绘图流程、几何检查方法和 SVG 例图。

| Skill | 用途 |
|---|---|
| [circuit-symbol-svg](circuit-symbol-svg/SKILL.md) | 根据电路接口与功能绘制、修改和审阅 SVG symbol，从例图学习构图与视觉风格 |
| [virtuoso-drawing](virtuoso-drawing/SKILL.md) | 在 Cadence Virtuoso 中绘制、重排和审阅 schematic 与 symbol，保存手工调整并重建视图 |

## 使用

将所需 skill 的完整目录安装到 agent 支持的 skills 目录，保留其中的 `references/` 与 `agents/`。
任务中指定 skill 名称，并提供目标电路的接口、网表或原理图，以及希望修改的范围。

- `circuit-symbol-svg` 需要 SVG 编辑能力，以及浏览器或 Inkscape 等渲染工具。
- `virtuoso-drawing` 需要可访问目标 OA 库的 Cadence Virtuoso 环境与操作工具。
  具体调用遵循所用工具的 API 文档；环境中安装了 `virtuoso` skill 时，可配合使用。
  字体、格距、图层显示与配置存放方式由目标项目确定。

## 例图

[视觉参考索引](circuit-symbol-svg/references/symbol-style-reference.md)涵盖自举采样开关、
可编程延时链、差分采样比较器、多级比较器，以及寄存器与延时电路。
例图用于学习绘图表达；绘制目标电路时按其实际接口与拓扑确定内容。
