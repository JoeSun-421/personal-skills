# Experiment Design and Improvement

Use for empirical research. For theoretical work, substitute propositions, assumptions, proofs, counterexamples, and differences from the closest theory.

## Claim to Measurement

Record the core hypothesis in one row:

| Claim | Intervention | Mechanism prediction | Competing explanation | Decisive comparison | Refuting result |
| --- | --- | --- | --- | --- | --- |
| Improvement under specified conditions | The one component changed | Observable change predicted | Could more data, compute, information, or better initialization explain the gain? | Control that isolates the factor | Outcome that leaves the mechanism unsupported |

Express improvements as behavior or metrics. Measure fewer generated tokens, fewer model calls, lower runtime, and lower total compute separately. When a local stage score improves, also check full-task outcomes and preservation conditions.

## Baseline Selection

The main baseline is usually the system being modified. Use the strongest relevant method to assess research standing, checking availability and protocol. Use simple alternatives to test whether the complex mechanism is necessary: equal extra data, equal compute, equal information, fixed rules, or more direct regularization.

Explain which alternative explanation each baseline can rule out. Strong methods that cannot be run fairly may remain in related work with the reconstruction or comparison gap disclosed. If reproducing the original system yields a gap, check implementation and protocol first, preserving the conditions of both published and local scores.

Match budget accounting to the claimed advantage:

| Claimed advantage | Comparison |
| --- | --- |
| Higher quality | Compare quality at equal data, model, and resources, recording added costs. |
| Lower inference cost | Compare actual time, total compute, and failed-attempt costs at similar quality. |
| Better sample efficiency | Plot quality against all interactions or data, including filtering, calibration, retries, and teacher costs. |
| Stronger generalization | Freeze training and tuning, then test independent tasks, objects, initial states, or other target units. |
| Greater robustness | Test controlled perturbations and normal conditions, including recovery, original-goal completion, and preserved constraints. |

If budgets cannot all be matched, show resource–quality curves and explain the accounting. One operating point cannot establish every advantage.

## Experimental Protocol

Before running, record necessary details in the existing task document:

- Subjects, versions, primary metrics, and their relation to the actual objective.
- Main factor and controls, changing only that factor between adjacent groups where possible. Add ablations when data, models, supervision, and compute change together.
- Training, development, and test splits by potential leakage units. Keep derivatives of the same source trajectory or prefix in one split.
- Definitions of success, failure, timeout, truncation, filtering, retry, and infrastructure error. Preserve all valid attempts and raw judgments.
- Checkpoint selection and tuning rules, with comparable search budgets. Reserve the test set for final assessment.
- Randomness, independent sample units, and uncertainty estimation. Analyze paired or clustered data at the corresponding unit.
- Criteria for continuing, stopping, or scaling, with supported numeric thresholds. If budgets are unknown, measure variance and unit cost first.

Every mechanism must admit at least one interpretation of results that refutes it. Necessary ablations ask whether the claim survives without a component and whether a simpler method at equal cost works equally well. Avoid experiments that merely enlarge a table without distinguishing explanations.

## Resource Probe

Choose the cheapest effective check for the key risk. As needed, check access, loading, real inputs/outputs, a backward pass and update, a short closed loop, or target scale.

Record input scope, versions, peak resources, time, and raw results each time. Assess inference, partial training, and full fine-tuning separately. Disclose deviations such as quantization, substitute inputs, privileged information, shorter tasks, and random modules.

If the request is only resource verification, deliver after covering the relevant risks. If a complete target experiment is requested, continue beyond probes to that experiment. A probe's conclusion always remains limited to what was tested.

## Result-Driven Improvement

Interpret results and choose the next action:

1. **Baseline is invalid.** Check versions, success judgments, data, initialization, and budgets. Fix them before evaluating the intervention.
2. **Metrics change without the mechanism prediction.** Check proxy/goal misalignment and confounds from data, compute, or information.
3. **The mechanism prediction appears without target-metric improvement.** Check whether the factor is the real bottleneck, whether errors propagate, or whether other costs offset gains.
4. **The average improves but particular conditions regress.** Locate boundaries by task or failure type, report uncertainty, and avoid selecting only favorable subsets.
5. **The minimal experiment supports the mechanism.** Expand validation with independent data, formal budgets, and comparable baselines.

For each revision, record evidence, the specific change, expected effect, and next decisive comparison. Identify failure causes before adding modules so complexity does not hide an unsupported hypothesis.

## Decision and Evidence

Retain positive, negative, and uncertain results. State when a small sample supports further validation without claiming universal effectiveness. Tie each improvement to a specific comparison and interval or error range.

Conclusions may concern a mechanism's benefit, application value, reproduction findings, or informative negative results. Identify gaps when current conditions cannot support a claim. Continue requested execution while authorized work remains feasible.
