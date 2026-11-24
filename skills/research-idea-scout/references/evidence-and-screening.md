# Evidence Search and Screening

Use for literature searches, baseline verification, novelty reviews, and resource screening. Retain evidence that can change a research decision; search volume is not a completion criterion.

## 1. Build Search Axes

Derive separate query groups from the user's problem rather than packing every constraint into one query:

| Search axis | What to find |
| --- | --- |
| System/task + failure conditions | Who measured the failure, and under which settings? |
| Problem + existing methods | Main baselines, simple alternatives, and strongest competitors |
| Proposed supervision signal/mechanism | Does the same approach exist under another name? |
| Adjacent field + similar problem | Has another field solved it using different terminology? What remains substantive in the transfer? |
| Recent citation chains and author projects | New versions, follow-up work, code, counterexamples, and retractions/corrections |
| Implementation + weights/data + hardware | Are core dependencies actually available, and is the target scale affordable? |

Choose a recent window based on the field's pace, such as the last 6–12 months, then trace foundational work. Year filters, keyword matches, and leaderboards do not establish exhaustive coverage. Coverage is sufficient when closest competitors are identified, core differences are compared explicitly, and key problem and resource claims have support. If further independent queries mainly repeat known neighbors, converge and disclose the remaining gaps.

## 2. Sources and Versions

Prefer original papers and supplements, official conference/journal pages, author projects, and official code/model/data releases. Search snippets, surveys, aggregators, and posts are leads; they cannot alone support a key recommendation.

For each work used in a conclusion, keep a source record:

| Field | Content |
| --- | --- |
| Identifier | DOI, arXiv ID, or normalized title |
| Bibliographic details | Title, authors, first release date, version read, and version date |
| Status | Preprint, published/accepted, corrected, or another verified status |
| Direct location | Method section, experimental setup, table/figure, appendix, or repository path |
| Supported judgment | Which problem, limitation, mechanism, or resource conclusion does it support? |
| Implementation match | Official/third-party, commit/tag, weights or data version; mark unverified items |
| Access level | Full text read, partial text, abstract only, or inaccessible |

Deduplicate versions using stable identifiers. Preserve differences when titles, numbers, conclusions, or implementations change; do not combine old experiments with a new method. A search crawl date is not the paper's first publication date. Do not infer acceptance from submission, OpenReview discussion, or an author's CV without official confirmation.

Check each named method's model/system type, inputs, outputs, actual training target, and optimization procedure. Assess shared names separately from shared mechanisms. Identify domain-specific differences that affect comparability, such as high-level skill calls, text-based end-effector commands, and continuous action heads in robotics.

## 3. Connect Sources to Claims

Use three evidence labels in prose, tables, or research cards:

- **Source-confirmed:** Directly measured or explicitly stated in the source. Still identify author-reported versus independently reproduced results and the applicable setting.
- **Research hypothesis/inference:** A proposed cause or mechanism inferred from observations. State its basis and alternative explanations.
- **Unverified:** Missing full text, experimental conditions, implementation, version, or access. Explain how the gap affects the conclusion.

A paper reporting failure and a claim about its cause are separate statements: the former may be factual while the latter requires a discriminating experiment. An acknowledged limitation and our ability to solve it are also separate claims.

Link directly to the supporting original text or official resource, retaining section/table/figure locations. Abstract-only access permits an abstract-level summary, not detailed mechanistic or negative conclusions. Keep inaccessible sources unverified; never invent authors, dates, table numbers, values, or citations.

## 4. Baseline Fairness

Distinguish the main runnable baseline, strongest related method, and cheapest alternative. Record:

- Data sources, training coverage, splits, labels/expert intervention, and information available at evaluation.
- Models and pretrained weights, training/inference budgets, model calls, and tuning/selection budgets.
- Environment/task versions, termination conditions, metric definitions, and treatment of failed or missing results.
- Reproduction sources, executed scope, deviations from the paper's configuration, and their implications.

Control confounds from added data, computation, model size, and tuning. If the proposal requires more resources, report the benefit–cost relationship rather than silently giving baselines smaller budgets. Test mechanistic contributions against simple alternatives using the same extra data or compute.

Report official protocols separately from new research settings. Changing task limits, inputs, success criteria, or training coverage changes the meaning of a score. Distinguish zero-shot evaluation, few-shot adaptation, and benchmark fine-tuning. Split by leakage units such as objects, subjects, task families, source trajectories/branches, or initial conditions, rather than randomly splitting frames alone.

If code for the strongest method is unavailable, a fair reconstruction is possible with implementation differences disclosed. Comparing only with weak methods cannot establish superiority over all related work. For theoretical candidates, align assumptions, problem classes, complexity, and existing bounds.

## 5. Novelty Comparison

For the few closest works, build:

| Closest work and version | Inputs, outputs, and available information | Training target, supervision, and mechanism | Covered problem and evidence | Proposed difference and decisive test |
| --- | --- | --- | --- | --- |

Search again using the mechanism description without invented names. Check synonyms, author follow-ups, references/citations, and adjacent fields. Compare problems, assumptions/supervision, mechanisms, and conclusions rather than module names alone.

Coverage judgments may be "core already covered," "meaningful boundary remains untested," or "insufficient evidence." If the core mechanism has a precedent, stop claiming its first introduction as the contribution. Application and reproduction goals can still have value. Recheck revised boundaries and explain whether they reveal a different failure mechanism, evaluation gap, or meaningful performance boundary.

A defensible statement is: "As of the search date, these queries and reviewed neighbors did not reveal work directly covering this core claim; the following sources or areas remain unchecked." This is not proof of global novelty.

## 6. Resource Verification

For key dependencies, list source/version, license or usage conditions, resource status, budget basis, and alternatives. Separate:

1. **Publicly listed:** An official release or repository exists; weights/data may still be unavailable.
2. **Accessible to the user:** The current user can obtain the files or authorization. Reading a model card does not establish weight access.
3. **Verified by execution:** Commands, environment, logs, and actual results exist. State whether these cover an interface, short run, or target scale.

For feasibility estimates:

- Use actual devices and available GPU memory; do not infer capacity from a GPU model name. Perform read-only hardware checks when authorized.
- Assess inference, LoRA/partial training, and full fine-tuning separately. Weight size alone omits activations, optimizers, caches, extra models, and environment overhead.
- Identify data scale, annotation sources, access barriers, disk/RAM, software compatibility, and runtime. Separate literature measurements, current measurements, and estimates.
- A few samples, updates, or a successful load establish only that scope, not full training or cross-task performance.
- Retain a proposal conditionally when key resources are unknown. Reject it for resources only after confirming that dependencies are unavailable and suitable alternatives do not exist. Do not hide paid or permissioned dependencies behind assumed free access.

## 7. Check Research Grounds Against the Goal

| Criterion | Supporting evidence | Reason to defer or reject |
| --- | --- | --- |
| Problem is real | Specific failures, theoretical limitations, or supported observations to test, with meaningful consequences | Vague slogans, invented pain points, or no explanation of the problem |
| Baselines are comparable | Clear improvement opportunity, runnable/reconstructable references, fair settings | Weak controls, mismatched settings, or no meaningful comparison |
| Foundations support execution | Methods, theory, data, and platforms form an implementation path | A title list or unrelated components |
| Resources are feasible | Necessary dependencies are available and target scale fits the user's budget | Defer unknown dependencies; reject unavailable dependencies without alternatives |
| Contribution fits the goal | A substantive methodological difference, or clear application/reproduction value, with search boundaries disclosed | Method claim already covered, or no practical benefit for an application goal |
| Hypothesis is testable | Experiments/analysis distinguish the mechanism from alternatives and define success/failure | No attribution possible, or every result is called a success |

Record evidence, gaps, and status for each criterion. Do not use a weighted score to cancel critical gaps. Retain high-risk research conditionally when its value, unknowns, and affordable pilot cost are explicit. A missing methodological difference affects a paper's contribution claim; an existing method may still satisfy application or reproduction goals.
