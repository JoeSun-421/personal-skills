# Editorial Patterns

Review date: 2026-11-24. These are observations about the organization of specific articles and transferable techniques, not rules prescribed by their authors.

## Physical Intelligence — Task, Mechanism, Evidence

Read: [Teaching Robots to Listen and Think Harder](https://www.pi.website/research/hirobot), [A VLA that Learns from Experience](https://www.pi.website/blog/pistar06).

Hi Robot introduces hierarchical policies through concrete cooking decisions, followed immediately by a system diagram and interaction examples, then training data and metrics. Learn from the chain of observable difficulty, structural change, training signal, and validation. Demonstrations build intuition; quantitative results support conclusions.

Keep analogies brief and return to the actual model. Hierarchical VLM/VLA systems should not be described generically as a single model with continuous latents.

## Jianlin Su — Derive the Missing Connection

Original sources: [From Instantaneous Velocity to Average Velocity](https://kexue.fm/archives/10958), [Conditioning on Step Size](https://kexue.fm/archives/10617). Link labels are English translations.

Access status at the review date: the original site and its official domain returned HTTP 403. Only titles, headings, and partial derivations from search-cached original-site content were obtained; the full articles were not read.

The available passages first identify the missing connection between average velocity and existing training objectives, then build it through definitions and algebraic identities. Use this derivation structure: explain what is missing, then how new terms follow from known quantities. In RL writing, connect rewards, advantages, probability ratios, and gradients into a traceable chain.

Observations about the author's style are limited to the accessed passages. Do not invent unread content.

## Chris Olah and Distill — A Figure as an Argument

Read: [Feature Visualization](https://distill.pub/2017/feature-visualization/).

The article distinguishes visualization from attribution before linking optimization objectives to visual results, letting readers compare changes in the objective. Use one relationship per figure, identify where to look, and retain failure controls so the figure contributes to reasoning.

Add controls only when interaction reveals a pattern. Keep figures static when a static image explains enough.

## Lilian Weng — A Map before the Details

Read: [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/).

An overall system diagram precedes planning, memory, tools, and examples, giving each component a place in the whole and a source. Learn from conceptual boundaries, navigation, and nearby citations. A short post should retain only modules needed for its argument rather than adopting a long survey's encyclopedic scope.

## Andrej Karpathy — Concrete Failure before Abstraction

Read: [A Recipe for Training Neural Networks](https://karpathy.github.io/2019/04/25/recipe/).

The article begins with apparently normal training that nevertheless fails, explains details hidden by abstract interfaces, and offers a path from simple setups to trustworthy results. Use concrete failures, minimal examples, and gradual increases in complexity.

For an algorithm, include at least one small example readers can compute by hand or reproduce, explaining where each quantity comes from. Avoid turning every engineering observation into a universal checklist.

## Jay Alammar — Zoom in without Losing the Whole

Read: [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/).

The article starts with the model as an input/output black box, then opens its modules and internal computations with visual continuity. Use this outside-in progression so readers always know the current level of explanation.

Show the complete data flow before explaining gates, token probabilities, or latent recursion. Keep colors and symbols consistent across figures rather than opening with dense matrix detail.

## Sebastian Raschka — Separate Routes, Compare Assumptions

Read: [Understanding Reasoning LLMs](https://magazine.sebastianraschka.com/p/understanding-reasoning-llms).

The article bounds the meaning of a reasoning model before organizing construction routes and their costs. Use explicit classification axes, method assumptions, and resource accounting; distinguish inference-time control, SFT, and RL.

When shortening, retain differences that determine method choice and remove lists whose only purpose is breadth.

## Simon Willison — Reproducible Claims and Scoped Experience

Read: [Here's how I use LLMs to help me write code](https://simonwillison.net/2025/Mar/11/using-llms-for-code/).

Concrete workflows establish capability boundaries through examples and verification habits. Scope experiential conclusions and retain failure records. Readers need to see how a tool's claimed capability was checked.

Learn from the arrangement of evidence without copying model judgments, time-sensitive claims, or personal voice.

## Integrated Editing Method

1. Establish motivation through one concrete difficulty and retain one central question.
2. Show the whole data flow, then open the modules that actually change.
3. Derive key connections with consistent notation, explaining the role of every new term.
4. Follow with a minimal example to check that the mechanism produces observable behavior.
5. Supply evidence through matched controls, identifying what remains unexplained.
6. Remove background, repeated definitions, and process notes that do not advance the claim.

Adapt the emphasis: architecture posts benefit from figures and data flow; algorithm posts from derivations and examples; transfer posts from changed assumptions and decisive experiments; meeting notes from actual progress, discussion, and decisions.
