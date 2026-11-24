---
name: research-idea-scout
description: "Assess research questions, search recent work, select baselines, design falsifiable experiments, and use evidence to refine proposals and decide whether to continue. Use for topic selection, method transfer, experimental design, and research reviews while respecting the user's target, mechanism, budget, and deliverables. Use separate workflows for explaining a single paper or simply downloading literature."
---

# Research Workflow

Make research decisions traceable to the user's question, existing evidence, and experiments that could refute the hypothesis. Use Chinese by default unless the user requests another language. Follow the current request for domain, method, budget, and writing format. Preserve this skill's original invocation name.

## Start with the Research Request

Briefly establish the research question, hypothesis to test, target system, and current deliverable. Examine an existing proposal in depth when one is specified; compare candidate directions when the user asks to find a direction.

Read [user-alignment.md](references/user-alignment.md) and keep a compact request record. Distinguish explicit user choices, working assumptions, unknowns, and authorization. Apply the latest corrections throughout subsequent equations, code, experiments, and conclusions.

When the user names a paper or algorithm, verify its primary source, version, and core mechanism before deciding how to transfer it. Assess whether the method can solve the target problem before downloading models, setting up environments, or probing APIs. Code and resource checks should address identified technical risks.

Match the depth of work to the user's current stage. Research exploration may end with an evidence-backed experimental design. When implementation or experiments are authorized, complete the corresponding setup, execution, diagnosis, and verification. If key resources remain unknown, complete independent analysis and state conditional conclusions.

## Establish That the Problem Matters

Describe a measurable failure of a specific system under explicit conditions, including the affected people, tasks, or costs. Record the source of the observation and its scope.

- Separate observed failures from proposed causes, and list competing explanations.
- Check official protocols, implementations, initialization, and budgets to rule out problems caused by configuration differences.
- Assess value against the research goal. Method innovation, application transfer, evaluation findings, reliability measurement, and reproduction can each be worthwhile.
- Define an observable improvement, such as lower cost at equal quality or higher task completion under a fixed budget. Derive metrics and acceptable regressions from task requirements or pilot measurements.

## Find the Closest Work and Baselines

Read [evidence-and-screening.md](references/evidence-and-screening.md) when searching, checking sources, or assessing research value.

Develop evidence for the problem, runnable foundations, closest competing methods, and negative findings alongside one another. Expand through references, citations, authors' follow-up work, and synonymous mechanisms. Record the search date, representative queries, and access gaps.

For the few closest works that affect the decision, compare the problem, inputs and information available at deployment, output interface, supervision and training, core mechanism, and evaluation conditions. Identify the closest mechanistic precedent before stating the remaining measurable difference.

Choose baselines for the question being answered. Usually include the main system, the strongest fairly comparable neighbor, and a simple alternative that might explain the same gains. State each one's role, availability, protocol differences, and selection rationale. Similar names or datasets alone do not justify a central comparison.

## Form a Falsifiable Mechanism

Connect the proposal through a complete chain:

**Observed failure → causal hypothesis → intervention point → added signal or computation → predicted behavior change → observable outcome.**

For every substantial change, explain what differs from the baseline, what is retained, what extra cost it adds, and when it might fail. Choose changes that best distinguish competing explanations; stacking modules is not itself a contribution.

Use the user's chosen mechanism as the basis of the current proposal. If evidence shows it is infeasible or already covered, present the specific evidence and possible revisions, and clearly mark proposal changes. Alternatives the user has not chosen remain recommendations.

Use consistent notation in equations. Define inputs, statistical scope, computation order, and boundary cases. Optimization objectives, training signals, advantages or losses, and evaluation metrics should correspond explicitly. Cite each borrowed equation and identify the exact modifications.

## Design the Smallest Decisive Experiment

Read [experiment-design.md](references/experiment-design.md) when designing or running experiments.

Start with a refutable claim and the smallest experiment that distinguishes explanations. Let its result determine whether to scale up. For each comparison, state the single factor to isolate, primary metric, budget accounting, predicted observation, and refuting outcome.

Use pilots to verify protocols, estimate variance, and determine the formal sample size. Separate training, development, and testing by potential leakage units. Account for failures, filtered samples, retries, and the costs of additional modules.

Set criteria for continuing, improving, stopping, or changing direction before running. After results arrive, diagnose protocol issues and confounds before updating the mechanism hypothesis. Test every revision against the same fair baseline, retaining negative results and tuning history.

## Verify Resources and Execute Within Scope

Record resources at three distinct evidence levels: publicly listed, accessible to the user, and verified by execution. State the scope of each verification.

Check models, data, code, licenses, environment versions, devices, GPU memory, disk, and runtime. Account separately for inference, parameter-efficient training, and full fine-tuning, including activations, optimizers, caches, sampling, and verifiers.

Resource probes should verify the required interface, peak usage, or training path. If a probe covers only one forward pass, limit the conclusion accordingly. Treat substitute models, quantization, privileged state, and shorter tasks as experimental conditions, and check whether they still answer the original question.

Build and execute within the current authorization. Use project conventions for directories, and preserve reproducible commands, versions, seeds, and result evidence. Handle external saving destinations, expensive services, and new persistent jobs according to the user's authorization.

## Assess and Improve

Assess research value, differences from the closest work, resource feasibility, and evidence strength separately. Decide investment against the corresponding goal; strengths in one area cannot cancel a critical gap elsewhere.

| Decision | Required reason |
| --- | --- |
| Recommend validation | The problem is supported, baselines are comparable, and key resources and a decisive experiment are viable. State which mechanisms still require experimental confirmation. |
| Retain conditionally | Identify missing evidence or dependencies and explain how resolving them would change the decision. |
| Stop or redirect | Show evidence that the core claim is covered, a key hypothesis is refuted, value is insufficient, or resources do not fit. Distinguish stopping this mechanism from abandoning the whole problem. |

Report effectiveness, cost, regression conditions, and uncertainty together. Limit conclusions to the tasks, models, data, and budgets actually covered. If an existing method supports an application goal, explain its reuse value. A methodological paper needs an additional testable difference.

## Deliver and Audit

Read [report-template.md](references/report-template.md) for delivery, selecting only the sections needed now. The core conclusion should answer whether the problem is worth pursuing, what specifically changes, what prior work already covers, how to test fairly, and how far current evidence reaches.

Respect the user's wording, writing habits, language, equations, and file destinations. Make the smallest changes that satisfy a request to edit an existing proposal, then read back and verify.

Before finishing, map user requirements to evidence. Check for requirement drift, accurate nearest-work comparisons, alignment between method and experiments, and resource claims that match the verification performed. Identify blockers and completed scope for unmet requirements, and continue work that remains authorized and feasible.
