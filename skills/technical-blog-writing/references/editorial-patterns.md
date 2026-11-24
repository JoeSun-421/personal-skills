# Editorial Patterns

核对日期：2026-11-24。以下是对具体文章信息组织的观察及可迁移做法，不是作者制定的规则。

## Physical Intelligence — Task, Mechanism, Evidence

已读：[Teaching Robots to Listen and Think Harder](https://www.pi.website/research/hirobot)、[A VLA that Learns from Experience](https://www.pi.website/blog/pistar06)。

Hi Robot 从做饭时的具体决策引出分层策略，紧接系统图和交互示例，再交代训练数据与指标。借鉴其“可感知的困难—结构改动—训练信号—验证”的链条。演示建立直觉，量化结果支持结论，两者分工清楚。

使用时控制类比篇幅，及时回到真实模型。分层 VLM／VLA 也不能泛称为单模型连续 latent。

## 苏剑林 — Derive the Missing Connection

原始入口：[从瞬时速度到平均速度](https://kexue.fm/archives/10958)、[将步长作为条件输入](https://kexue.fm/archives/10617)。

访问情况：原站及其官方域名本轮返回 HTTP 403，只取得原站搜索缓存中的标题、章节与部分推导，未完整阅读全文。

已获取段落先指出平均速度与现有训练目标之间缺少连接，再用定义和恒等变换建立联系。可借鉴这种推导组织：先交代缺什么，再解释新项如何由已知量得到。写 RL 时，把奖励、优势、概率比与梯度连成可追踪的一条线。

关于作者风格的观察限于上述段落，不补造未读内容。

## Chris Olah and Distill — A Figure as an Argument

已读：[Feature Visualization](https://distill.pub/2017/feature-visualization/)。

先分清 visualization 与 attribution，再把优化目标与可视化结果对应，读者可以通过对照理解目标变化。借鉴一图一关系、标出观察位置、保留失效对照，让图承担推理。

只有交互能揭示规律时才增加控件。静态图片足以解释时保持静态。

## Lilian Weng — A Map before the Details

已读：[LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)。

先给系统总图，再逐步讲规划、记忆、工具和案例，每个局部都有全局位置及来源。借鉴概念边界、导航与就近引用。短博客只保留主线需要的模块，避免照搬长综述的百科式范围。

## Andrej Karpathy — Concrete Failure before Abstraction

已读：[A Recipe for Training Neural Networks](https://karpathy.github.io/2019/04/25/recipe/)。

文章从看似正常却训练失败的实际现象进入，说明抽象接口遮住的细节，再给从简单设置建立可信结果的路径。借鉴具体故障、最小例子和逐步增加复杂度。

写算法时至少给一个可以手算或复现的小例子，解释每个量从哪里来。避免把所有工程经验扩写成统一检查表。

## Jay Alammar — Zoom in without Losing the Whole

已读：[The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)。

先把模型当作输入输出黑箱，再逐层打开模块和内部计算，图示保持连续。借鉴由外到内的缩放顺序，让读者每一步都知道当前层次。

解释 gate、token 概率或 latent 递归前先画完整数据流；颜色与符号跨图一致，避免一开始就铺满矩阵细节。

## Sebastian Raschka — Separate Routes, Compare Assumptions

已读：[Understanding Reasoning LLMs](https://magazine.sebastianraschka.com/p/understanding-reasoning-llms)。

先限定 reasoning model 的含义，再组织不同构建路径和各自代价。借鉴明确分类轴、对照方法的条件及资源口径，避免把推理时控制、SFT 和 RL 混成同一机制。

压缩时保留决定方法选择的差异，删去仅展示覆盖广度的罗列。

## Simon Willison — Reproducible Claims and Scoped Experience

已读：[Here’s how I use LLMs to help me write code](https://simonwillison.net/2025/Mar/11/using-llms-for-code/)。

用具体使用过程解释能力边界，给实际例子和验证习惯。借鉴经验结论的适用范围及失败记录。文章展示了某个工具能做什么，还需要读者看见它如何被检验。

学习证据安排，不直接复制其模型判断、时效信息或个人口吻。

## Integrated Editing Method

1. 用一个具体困难建立阅读动机，留下一个核心问题。
2. 给完整数据流，再逐层打开真正发生变化的模块。
3. 用统一符号推导关键连接，每个新项都有作用说明。
4. 接一个最小例子，检查机制是否落到可观察的行为。
5. 用同条件对照给证据，指出仍然解释不了的部分。
6. 删除对主张没有贡献的背景、重复定义和过程记录。

可按任务选择侧重：架构文章多用图与数据流；算法文章多用推导和例子；迁移文章明确假设变化与判别实验；组会记录围绕实际进展、讨论和决定。
