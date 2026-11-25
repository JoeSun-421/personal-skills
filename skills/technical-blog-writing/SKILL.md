---
name: technical-blog-writing
description: Turn papers, mathematical methods, and experiments into concise technical blog posts, paper explainers, or research meeting notes, checking original sources, figures, and equation rendering. Use for article writing and rewriting, not ordinary chat answers or direct website deployment.
---

# Technical Blog Writing

Help readers explain the problem, why the method works, and how far the evidence reaches. Remove redundancy while retaining necessary derivations and causal connections.

## Argument before Structure

Identify the one question readers need to understand and the article's central judgment before selecting material. Introduce background when needed rather than opening with a collection of terminology and paper titles.

A useful progression is concrete difficulty, core idea, necessary mechanism, evidence and limits, then transfer. Adapt to the material without fixed length or section counts. When rewriting, retain useful conclusions and sources, moving repeated derivations, general algorithm manuals, and implementation inventories into linked detailed notes.

Keep user instructions, execution plans, self-check results, and commentary about the writing process out of the article. Place limitations beside the conclusions they affect. Put tool-access gaps in maintenance records or delivery notes.

For a multi-paper review, read [research-reviews.md](references/research-reviews.md). Select distinct, transferable mechanisms and honor the requested year, algorithm preference, paper count, heading language, and structure without lowering evidence standards to fill a quota.

## Make the Mechanism Legible

- Advance one judgment per section and explain its relationship to the preceding section. Establish an understandable situation before introducing the terminology needed to address it.
- Resolve shared names with different meanings, such as short/long text modes versus text/continuous-latent switching. Compare methods around the same problem, specifying inputs, outputs, supervision, and optimization targets.
- Before an equation, explain which step it solves; afterward, explain why each new term appears. Keep outer-round, inner-token, and trajectory indices consistent. Define each variable's meaning and acquisition method at first use.
- Retain derivations and numerical examples that can change a reader's judgment. Expand full training scripts, large notation tables, and general background only when readers actually need them.
- Naturally distinguish original-paper results, your own derivations, teaching examples, and transfer proposals. Do not describe an unexecuted design as an established capability.
- Avoid posing questions only to answer them and corrective constructions such as "not X, but Y." Remove empty transitions, repeated disclaimers, and closing slogans.

## Evidence and Figures

Check original papers, fixed versions, and official implementations first. Keep citations near claims, including section or equation numbers when needed. Describe paper/code differences separately; abstracts, titles, and demonstrations cannot establish training details.

Tell readers which relationship to inspect in a figure before using it to advance the explanation. For source figures, preserve local assets, figure numbers, authors, versions, provenance, and license information. Crop unrelated text while retaining labels, axes, and legends. When clean original figures are requested, add no overlays, source labels, or image hyperlinks; keep paper references in the text or at the end and individual figure provenance in a separate asset record. Figures should serve the argument and cannot replace experimental controls.

Read [editorial-patterns.md](references/editorial-patterns.md) as needed when using writing references. Learn how information is organized without copying voice, signature phrasing, or paragraphs. Choose techniques suited to the current article rather than mechanically combining every reference style.

## Markdown to Blog

Store prose, figure assets, and source notes separately, using stable relative paths. For site transfer, use neutral metadata such as title, date, description, and tags. Writing Markdown does not authorize automatic publication or website changes.

Read [math-and-assets.md](references/math-and-assets.md) when equations or figures are involved. Render mathematics with actual KaTeX/MathJax and inspect it in a browser; LaTeX delimiter checks alone do not establish correct display. Prefer splitting long expressions into meaningful equations over reducing font sizes.

Read the finished article independently: can readers follow the problem into the method, do figures explain equations, can training signals be traced to parameter updates, and do conclusions stay within evidence? Then verify citations, local links, numerical examples, and rendering.

## Meeting Notes

Start meeting notes with the actual topic, materials, and progress, followed by key discussion, decisions, and open questions. Separate paper claims, the group's observations, and new proposals.

Record owners, deadlines, experimental results, and decisions only when actually supplied; omit missing fields. Link to background and mechanisms in blog posts rather than copying full derivations into every meeting record.
