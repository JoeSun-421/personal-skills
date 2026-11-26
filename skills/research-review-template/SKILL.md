---
name: research-review-template
description: Build or extend a mechanism-grouped research review from a user-supplied Markdown template, preserving required papers, source-faithful training recipes, original figures and a consolidated transfer discussion. Use for template-based literature reviews and reusable Markdown review scaffolds.
---

# Research Review Template

Produce a research review readers can follow from a target problem through distinct mechanisms and their original training recipes. This is a Markdown writing template; it does not create a Template Gallery artifact or authorize publication.

## Read the User's Template First

Read the current draft and its inline annotations before applying the generic structure. Preserve intentional edits, required papers, terminology, output location and the latest title. Keep frontmatter and H1 consistent. Save the original annotated draft outside the delivery file before replacing placeholders.

The user's current request controls paper count and grouping. For this personal template, use 6–8 main papers in 3–4 mechanism classes by default, with clear representation rather than a quota per class. A classification survey is a supporting reference, not an additional main method paper.

## Establish the Classification

Start from what each method changes: retained context, generated computation, reasoning reuse, model selection, verification, or execution scheduling. Put an approach in the class of its primary mechanism and explain overlaps briefly. When adapting a supplied taxonomy, preserve its attribution and distinguish the new grouping from the source taxonomy.

Preserve explicitly required papers. Prefer recent original releases, complete recipes, meaningful controls, measurable costs and stated limits. Record preprint release, reviewed version and acceptance separately. Verify critical mechanisms in the paper or official implementation; a survey's optimizer label is not sufficient evidence.

## Fill the Review

Use [the Markdown scaffold](assets/review-template.md) and [the source-reading checklist](references/paper-reading.md). Adapt their wording and section count to the user's draft rather than replacing it mechanically.

Default structure:

1. The target system's concrete problem and feedback loop.
2. A short numbered overview of the mechanism classes and papers in each.
3. One H2 per class, one H3 per paper, and H4 sections for problem, method/training and evidence where useful.
4. One final transfer section, followed by references.

Default prose is Chinese and all titles/subtitles are English unless the user requests otherwise. Keep original-paper content in paper sections. When transfer is consolidated at the end, remove per-paper target-domain scenarios and speculative adaptation proposals from the main review.

Follow the source argument and actual operation order. For RL, connect data, sampling, verifier/reward, advantage statistics, loss masks and updated parameters. For supervised or inference-only work, describe its actual training or runtime protocol without inventing an RL stage. Keep source limitations beside the claims they qualify.

Use equations for mechanism-critical decisions and updates. Define symbols locally and specify normalization populations, token/turn granularity, frozen parameters and approximations. Do not substitute a proposed PPO adaptation for a paper's GRPO recipe. A loss mask does not freeze shared parameters.

## Figures and Rendering

Prefer original method and evidence figures. Keep PDFs unchanged; record version, figure/page, crop and checksum separately. Check beyond the crop boundaries before extraction so headings, axes, legends and small labels remain complete. Remove unrelated text and excess whitespace, preserving aspect ratio and modest consistent padding.

Match figure and prose widths when requested. Clean original figures receive no added source overlays or image hyperlinks; keep paper references in text or the references section. Do not replace figures with generated imitations.

Preserve Markdown mathematics before conversion and render with the existing KaTeX/MathJax engine. Inspect desktop and mobile output for missing images, equation errors, overflow and column alignment. Delimiter checks alone cannot establish correct display.

## Edit and Deliver

Remove template notes, search history, selection narration, self-posed questions and drafting instructions from the article. State the mechanism directly; avoid rhetorical corrections such as “不是……而是……”. Keep necessary scientific assumptions and measured limitations.

Check the requested number of actual paper sections and actual classes, required-paper retention, a single final transfer section, original-source consistency, references and rendered assets. Report only the artifacts and verification actually completed. Updating a local Markdown draft does not imply publishing the site or synchronizing an external workspace.
