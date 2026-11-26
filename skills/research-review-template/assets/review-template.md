---
title: "[Paper-style title]"
date: "[Date]"
description: "[Mechanisms, evidence and target scope]"
tags: [research-review]
---

# [Paper-style title]

## Why [Target System] Needs [Capability]

[Describe the concrete system, its input/output and feedback loop. Establish the cost or failure that motivates the review.]

## [Number] Routes to [Capability]

1. **[Mechanism Class A]：** [Paper A1]、[Paper A2]。[Primary intervention.]
2. **[Mechanism Class B]：** [Paper B1]、[Paper B2]。[Primary intervention.]
3. **[Mechanism Class C]：** [Paper C1]、[Paper C2]。[Primary intervention.]
4. **[Optional Mechanism Class D]：** [Paper D1]、[Paper D2]。[Primary intervention.]

## [Mechanism Class A]

[One sentence defining the shared intervention and the papers' distinct roles.]

### [Paper A1 — Specific Mechanism]

#### Problem

[The source paper's concrete problem.]

<!-- Insert the original method figure with a stable local path and descriptive alt text. -->

#### Method and Training Recipe

[Follow the paper's actual input, operation, execution and learning order.]

1. [Data or initialization.]
2. [Sampling or runtime decision.]
3. [Verification and reward/label.]
4. [Advantage or supervised target and its statistical scope.]
5. [Loss, masks and parameters updated.]

[Use only the equations needed to explain the mechanism. Define each new symbol next to its first use. For inference-only work, replace training steps with its execution protocol.]

#### Results

<!-- Insert an original evidence figure. -->

[State the matched comparison, metric, actual cost boundary and material limitation.]

<!-- Repeat the paper block, then the class block, to the requested counts. -->

## Transfer to [Target System]

[Consolidate the transferable mechanisms, changed assumptions and evaluation requirements. Label untested design as proposed. Keep the target discussion here when a single final transfer section is requested.]

## References

- [Authors]. **[Exact title].** [Original release and reviewed version]. [Primary source link]. [Method/appendix/table locations].

[Add a supplied taxonomy survey separately from the main method-paper count.]
