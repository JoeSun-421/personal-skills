# Research Report

按用户当前阶段选取必要内容。结论先行，避免空模板和机械扩充候选数量。用户研究一个具体方法时，围绕它完成判断。

## Request and Decision

简要写出用户的问题、目标系统、所选方法、本次交付和已知资源。列出影响结论的假设与未知项。

给出推荐验证、条件性保留或停止／转向的决定，并分别说明实际价值、贡献空间、资源可行性和证据强度。标明哪些结论来自文献、实测或推断。

## Problem and Hypothesis

说明谁在什么条件下发生哪种失败、代价或测量缺口。附直接来源、版本和适用范围。

写出原因假设、竞争解释和预期变化。作者列出的 limitation 可以提供问题线索，机制是否能改善该问题仍由实验检验。

## Related Work and Baselines

| Work and version | Problem and setting | Inputs, outputs, supervision and mechanism | Existing evidence | Our difference and its test |
| --- | --- | --- | --- | --- |
| 最近工作 | 与本问题的关系 | 影响可比性的关键条件 | 对应章节、实验或代码及缺口 | 改了什么，以及怎样测其独立作用 |

| Baseline | Role | Availability and protocol | Explanation it can rule out |
| --- | --- | --- | --- |
| 原系统、强近邻或简单替代方案 | 为什么比较 | 可运行性与公平性 | 哪项结果可以排除哪种解释 |

论文之间的整体结果用于背景参照。条件一致的实验用于支撑改进主张。逐项标出数据、计算或部署信息的差异。

## Method and Claimed Improvement

将核心机制写为输入、改动、信号或运算、输出以及预期作用。公式符号沿全文统一，注明来源与改写。

| Baseline component | Proposed change | Intended benefit | Added cost or risk | Supporting comparison |
| --- | --- | --- | --- | --- |
| 被改变的环节 | 当前明确采用的改动 | 可观测收益 | 新数据、计算、信息和失败条件 | 能支持或否定该收益的实验 |

用户尚未采用的替代建议应明确标记。保持作者原有表达，按授权编辑。

## Minimal Experiment

| Hypothesis | Comparison and controlled factor | Data split and budget | Metric and uncertainty | Refuting result | Next decision |
| --- | --- | --- | --- | --- | --- |
| 要检验的主张 | 哪两个配置及唯一改动 | 防泄漏划分与全部成本 | 目标指标、独立样本单位和估计方式 | 何种结果否定假设 | 继续、修改或停止依据 |

说明正式训练前需要验证的协议、baseline、资源或方差。给出能消除主要竞争解释的消融和同成本对照。数值阈值写来源，未知时记录先导如何测得。

## Resources and Execution Evidence

| Dependency or action | Exact source and version | Evidence level | Measured or estimated cost | Scope and remaining gap |
| --- | --- | --- | --- | --- |
| 代码、权重、数据、运行或训练 | 可定位的来源 | 公开存在、用户可访问、已运行验证 | 分别标明估计与实测 | 当前证据能证明到哪一步 |

仅在执行已获授权并实际完成时填写运行结果。给出关键命令、结果文件和必要版本。接口连通、模型加载、梯度通过和完整任务效果分别注明。

## Results and Improvement

| Comparison | Quality | Total cost | Uncertainty and regressions | Mechanism interpretation | Next action |
| --- | --- | --- | --- | --- | --- |
| 已跑的公平比较 | 实际指标 | 包括失败、重试及额外模块 | 实测边界 | 支持哪种解释 | 下一项有判别力的修改或停止 |

只有方案时省略结果表。迭代时记录改了哪一项及依据，不将预期收益写成已取得的结果。

## Sources and Coverage

列关键来源的题名、稳定标识、版本、正文位置、官方实现与访问范围。来源链接附在相应主张或表格行。

简记检索日期、代表性检索式、已核对近邻和剩余范围。新颖性结论限定于已检索与核验的来源。

## Requirement Audit

| User requirement | Delivered result | Authoritative evidence | Remaining gap |
| --- | --- | --- | --- |
| 用户要求及最近纠正 | 实际交付 | 来源、文件或结果 | 待完成或无法核验的部分 |

小任务可压缩为一段。用户要求执行时，未完成的独立步骤继续推进。最终报告明确结论覆盖的系统、任务和预算，以及建议投入的下一项最小实验。
