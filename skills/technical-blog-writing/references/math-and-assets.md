# Mathematics and Local Figures

## Preserve Mathematical Source

Markdown 中行内数学用单美元符号，展示公式用独立成行的双美元符号。代码区域的美元符号仍按代码处理。表格里的条件概率使用 \mid，范数使用 \lVert 与 \rVert，避免未转义的竖线拆开表格。

转换 HTML 时先让数学插件识别公式，或先将数学区域替换为占位符。普通 Markdown 解析器可能吞掉 LaTeX 反斜线，再做 auto-render 会得到错误结果。

统一上下文、轨迹、外部轮次与内部 token 索引。重命名原论文符号时保留其数学意义，例如区分模式成本与 RL 折扣。

## Render and Inspect

使用项目既有引擎；没有时可在隔离临时目录使用固定版本 KaTeX，避免全局安装和修改站点。[KaTeX API](https://katex.org/docs/api) 的 renderToString 支持服务端渲染。校验启用 throwOnError，明确 displayMode，可输出 htmlAndMathml 兼顾可访问性。

实际打开生成结果，检查数学元素数量、错误标记、残留源码、上下标、分段条件和对齐。浏览桌面与窄屏，确认图片加载，页面无意外横向溢出，必要的横向滚动限制在公式块中。

LaTeX 配对检查和数值计算是补充；没有完成浏览器检查时不声称显示已验证。

## Source Figures

原 PDF 保持不变，图资源使用稳定的本地相对路径。提取图的内容区域，检查标签完整，数据曲线保留坐标和图例。

图注就近标作者、论文、版本和 Figure 编号；素材说明记录源 PDF 页码、URL、许可、裁剪情况和校验和。遵守对应转载或改编许可。

图可以链接到原始分辨率版本。避免整页 PDF 缩略图，也避免用生成式重绘冒充原图。
