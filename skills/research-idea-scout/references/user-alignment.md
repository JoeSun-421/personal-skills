# User Alignment

Use this record to guide research execution within the current report or task notes. Select necessary fields based on complexity and avoid duplicate documents.

## Request Record

| Field | Record |
| --- | --- |
| Research question | Relationship or judgment to test, preserving the user's wording where possible. |
| Target setting | System, inputs/outputs, deployment conditions, task difficulty, and generalization target. |
| Chosen mechanism | Papers, algorithms, equations, and non-substitutable designs selected by the user. |
| Success evidence | Observations or comparisons that support the goal, and outcomes that refute it. |
| Deliverable | Which of research, explanation, design, editing, implementation, measurement, or full experimentation is requested now. |
| Resources and authorization | Explicit budget, permitted actions, output directory, and external saving destinations. |
| Assumptions and unknowns | Inferences, consequential unknowns, and how to obtain evidence. |

Resolve ambiguity in a named method by locating the original text and core computation first. Ask the user only when sources cannot resolve a consequential ambiguity. Do not repeatedly reopen routine decisions after an explicit user choice.

## Change Control

- On correction, record which assumption or design changes, and the affected equations, code, controls, and conclusions. Continue from the latest valid requirements.
- Preserve distinctions the user cares about. When substituting a model, input, interface, training objective, or task scope, explain what question it answers and how it relates to the original goal.
- Recommending an alternative and adopting it are different states. Complete an evaluation when asked to evaluate; complete the edit or implementation when asked to change or implement.
- Handle reversible implementation details autonomously. Label substitutions affecting the hypothesis or conclusion as recommendations or conditional plans, and adopt them only within existing authorization.
- Environment setup serves research-risk verification. Running a model with the same name cannot replace analysis of a method's transfer. Interface probes cannot replace training results or closed-loop task validation.
- When the user pauses, cancels, or switches tasks, check background jobs you started. Stop, preserve, or hand them off as directed, reporting consumed resources and recoverable state.

## Research Notes and Formulas

Preserve the author's wording, tone, mixed-language usage, and expression. Make only necessary structural changes when asked to improve organization, and separately explain evidence for technical corrections affecting meaning. Do not rewrite informal notes wholesale into paper prose.

Use one consistent index system across notation tables and prose. Check:

1. Every variable has a meaning, acquisition method, and statistical unit at first use.
2. Symbols keep their meaning across equations; trajectory, node, round, and token indices correspond consistently.
3. Every reward can be computed from real logs or a judge, with explicit training and evaluation success labels.
4. Expand controls from the same total objective, identifying enabled signals term by term. When the user chooses one form, include alternatives only where needed to explain related work.
5. Final optimization actually uses the defined signals. In reinforcement learning, trace returns, within-group statistics, advantages, and policy updates.

Cite only sources that support the equation's actual form and identify each modification. Mark empirically plausible choices as designs to test, not original-paper conclusions.

## Completion Check

Map the request to requirements, actual deliverables, evidence locations, and remaining gaps. Before finishing, return to the research question and check whether the evidence suffices.

For small tasks, a sentence or short table is enough. Results, logs, implementations, versions, and papers each support their own scope. Correct drift before continuing.

## Typical Failure Cases

| User request | Required behavior |
| --- | --- |
| "Can paper M's method work for system X? You may set up an environment to check." | Map M's mechanism to X and identify transfer risks first. Then verify relevant resources or interfaces, explicitly leaving effectiveness pending training. |
| "Keep the node-relative length reward and only one length formula." | Retain the node comparison scope and chosen formula in the main proposal, adding rewards to controls term by term. Put other length forms in related-work explanations. |
| "Write this version in without changing my style." | Read the current version, edit minimally, preserve expression, and verify the saved result. |
| "Research first; the budget is undecided." | Complete source checks, differences, and a conditional experiment plan. Unknown resources do not prevent independent research assessment. |
| "I only want to reproduce it or use it in my system." | Judge by reproduction correctness or task value and explain how existing methods can be used. |
