# Personal Skills

个人维护的 agent skills，按研究和技术写作工作流组织。

| Skill | 用途 | 入口 |
| --- | --- | --- |
| research-idea-scout | 核验研究问题、最近工作与 baseline，设计可证伪实验，按证据改进方案 | [SKILL.md](skills/research-idea-scout/SKILL.md) |
| technical-blog-writing | 把论文、公式与实验写成清晰博客和组会记录，检查来源、图片与数学渲染 | [SKILL.md](skills/technical-blog-writing/SKILL.md) |

## Structure

每个 skills/ 子目录是一项独立 skill：SKILL.md 是入口，references/ 保存按需阅读的资料，agents/openai.yaml 保存显示信息与默认调用提示。

写作 skill 的[编辑方法](skills/technical-blog-writing/references/editorial-patterns.md) 整合 PI、苏剑林、Distill、Lilian Weng、Karpathy、Jay Alammar、Sebastian Raschka 与 Simon Willison 的具体文章观察；直接访问受限的资料单独注明。学习其信息组织，不复制作者口吻。

## Usage

在支持 SKILL.md 的 agent 中安装对应子目录后，可使用 $research-idea-scout 或 $technical-blog-writing 调用。维护时同步入口与相对引用，并重新验证 skill 结构。

本仓库收录个人维护的 skill，不包含工具自带的 .system 或插件缓存。论文 PDF、实验数据、模型权重和凭据保留在各自项目。
