# Mathematics and Local Figures

## Preserve Mathematical Source

Use single dollar signs for inline mathematics and double dollar signs on separate lines for display equations in Markdown. Dollar signs in code remain code. In tables, write conditional probabilities with \mid and norms with \lVert and \rVert so unescaped vertical bars do not split cells.

When converting to HTML, let a mathematics plugin recognize equations first, or replace math regions with placeholders. A plain Markdown parser can consume LaTeX backslashes, leaving incorrect source for later auto-rendering.

Keep context, trajectory, outer-round, and inner-token indices consistent. When renaming a paper's symbols, preserve their mathematical meaning; distinguish mode costs from RL discounts, for example.

## Render and Inspect

Use the project's existing engine. If none exists, use a pinned KaTeX version in an isolated temporary directory, avoiding global installation and website changes. The [KaTeX API](https://katex.org/docs/api) supports server-side rendering through renderToString. Enable throwOnError for validation, set displayMode explicitly, and consider htmlAndMathml output for accessibility.

Open the actual rendered output. Check math-element counts, error markers, leftover source, subscripts/superscripts, piecewise conditions, and alignment. Inspect desktop and narrow layouts, image loading, and unintended horizontal overflow. Limit necessary horizontal scrolling to equation blocks.

Delimiter checks and numerical calculations are supplements. Do not claim verified display without completing browser inspection.

## Original Scientific Figures

Use an original diagram when a proposed mechanism or experiment needs a visual explanation. Mark diagrams of proposed work as such. When plotting reported measurements, preserve the units, experimental setting, aggregation, and source location. Keep incomparable quantities on separate axes and avoid implying matched controls beyond the source. Retain the figure inputs and source in a companion provenance note, then inspect the actual article at desktop and mobile widths.

## Source Figures

Keep source PDFs unchanged and use stable local relative paths for figure assets. Extract the figure content region, checking that labels are complete and data curves retain axes and legends.

Honor the requested caption style. For clean original figures, keep existing labels without adding watermarks, source captions, or image hyperlinks. Put paper citations in the text or references, and retain the source PDF page, figure number, URL, license, crop, and checksum in a separate asset record. Follow the applicable reproduction or adaptation license.

Figures may link to full-resolution originals. Avoid whole-page PDF thumbnails and never present generative redraws as original figures.
