# Research Report

Select only what the user's current stage needs. Lead with the conclusion; avoid empty templates and mechanically increasing candidate counts. Center the assessment on the specified method when the user is studying one.

## Request and Decision

Briefly state the question, target system, chosen method, deliverable, and known resources. List assumptions and unknowns that affect the conclusion.

Recommend validation, retain conditionally, or stop/redirect. Explain practical value, contribution opportunity, resource feasibility, and evidence strength separately. Identify conclusions from literature, measurements, and inference.

## Problem and Hypothesis

Explain who experiences which failure, cost, or measurement gap under what conditions. Include direct sources, versions, and scope.

State the causal hypothesis, competing explanations, and predicted change. An author's limitation can motivate the problem; experiments must still establish whether the proposed mechanism improves it.

## Related Work and Baselines

| Work and version | Problem and setting | Inputs, outputs, supervision, and mechanism | Existing evidence | Our difference and its test |
| --- | --- | --- | --- | --- |
| Closest work | Relationship to this problem | Conditions affecting comparability | Relevant sections, experiments, code, and gaps | What changes and how to test its independent effect |

| Baseline | Role | Availability and protocol | Explanation it can rule out |
| --- | --- | --- | --- |
| Original system, strong neighbor, or simple alternative | Reason for comparison | Availability and fairness | Which outcome excludes which explanation |

Overall results across papers provide context. Experiments under matched conditions support improvement claims. Identify differences in data, compute, and deployment information explicitly.

## Method and Claimed Improvement

Express the core mechanism through inputs, intervention, signal or computation, outputs, and intended effect. Use consistent notation and identify sources and modifications.

| Baseline component | Proposed change | Intended benefit | Added cost or risk | Supporting comparison |
| --- | --- | --- | --- | --- |
| Component changed | Intervention currently adopted | Observable gain | Extra data, compute, information, and failure conditions | Experiment that supports or refutes the gain |

Clearly mark alternatives the user has not adopted. Preserve the author's expression and edit within authorization.

## Minimal Experiment

| Hypothesis | Comparison and controlled factor | Data split and budget | Metric and uncertainty | Refuting result | Next decision |
| --- | --- | --- | --- | --- | --- |
| Claim to test | Two configurations and their single difference | Leakage-resistant split and all costs | Target metric, independent sample unit, and estimator | Outcome that refutes the hypothesis | Criteria to continue, revise, or stop |

State which protocols, baselines, resources, or variance estimates must be checked before formal training. Include ablations and equal-cost controls that eliminate major competing explanations. Cite numeric thresholds, or explain how a pilot will estimate them.

## Resources and Execution Evidence

| Dependency or action | Exact source and version | Evidence level | Measured or estimated cost | Scope and remaining gap |
| --- | --- | --- | --- | --- |
| Code, weights, data, execution, or training | Traceable source | Publicly listed, accessible to the user, or verified by execution | Separate estimates and measurements | What current evidence establishes |

Include execution results only when authorized and actually completed. Provide key commands, result files, and required versions. Distinguish interface connectivity, model loading, gradient flow, and full-task effectiveness.

## Results and Improvement

| Comparison | Quality | Total cost | Uncertainty and regressions | Mechanism interpretation | Next action |
| --- | --- | --- | --- | --- | --- |
| Fair comparison actually run | Actual metrics | Failures, retries, and extra modules included | Measured limits | Explanation supported | Next decisive revision or stopping decision |

Omit the results table for a proposal alone. During iteration, record what changed and why. Do not present expected gains as obtained results.

## Sources and Coverage

List key source titles, stable identifiers, versions, text locations, official implementations, and access scope. Attach links to the relevant claim or table row.

Briefly record the search date, representative queries, checked neighbors, and remaining coverage. Limit novelty conclusions to searched and verified sources.

## Requirement Audit

| User requirement | Delivered result | Authoritative evidence | Remaining gap |
| --- | --- | --- | --- |
| Requirement and latest correction | Actual deliverable | Source, file, or result | Incomplete or unverifiable work |

For small tasks, use a paragraph. When execution is requested, continue independent unfinished steps. State which systems, tasks, and budgets the final conclusion covers and the next minimal experiment worth funding.
