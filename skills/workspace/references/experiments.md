# Experiment Execution and Evidence

Use the research-method skill, when available, for the scientific question and design. This reference concerns reproducible execution inside the workspace.

## Before Running

Keep a compact plan with the experiment's code:

- Question, causal hypothesis, and observable prediction.
- Original system, strongest comparable reference, and a simple alternative when they test distinct explanations.
- Main factor, controlled conditions, data splits, seeds, and actual success criteria.
- Primary quality metric, full cost accounting, sample unit, and uncertainty method.
- Source/model/data revisions, environment path, device requirements, and output root.
- Smallest decisive test, permitted budget, and continue/stop criteria.

Use the official benchmark protocol for reproduction. Label altered inputs, quantization, task caps, controllers, success predicates, privileged information, and custom tasks as separate conditions. Changing a prompt alone does not change a simulator's success predicate.

For paired interventions, preserve the same initial state/prefix and seed where appropriate, verify reset/replay equivalence, and split shared source trajectories or branches together to avoid leakage. For an online instruction edit, invalidate queued old actions and re-infer from the current observation when required by the claimed intervention.

For training, make the reward/loss computable from recorded signals and trace it into an actual parameter update. A synthetic backward pass tests an interface; it does not show the policy learned the intended behavior.

## Save a Run

Use a unique directory under the workspace's project runtime or established artifact path, such as `.runtime/runs/<timestamp>-<condition>-seed<N>/`. Never overwrite an earlier run in place to hide a failed attempt.

Retain only the artifacts the experiment needs, for example:

| Record | Necessary content |
| --- | --- |
| Manifest/config | Command, working directory, source revision and dirty diff if relevant, environment versions, model/data revisions, seed, task IDs, budget, timestamps/timezone |
| Raw logs/trajectory | Inputs/outputs or safe references to them, actions, judge responses, retries, filtering, timing, termination causes |
| Metrics/summary | Numerators and denominators, quality metrics, sample units, costs, uncertainty, and links to the underlying runs |
| Media | Task/run identity, capture mode, and links to matching trajectories and judgments |
| Run note | What was tested, deviations, failures, interpretation, and next discriminating action |

Preserve raw records and generate curated summaries from them. Large logs, images, videos, datasets, and checkpoints stay ignored by Git unless explicitly selected for tracking. Keep small code/config/manifest files and useful result indexes versioned according to the project.

Never include credentials or unrestricted environment dumps. Reference the authentication mechanism without recording secret values.

## Interpret Without Inflating Evidence

Keep evidence levels separate: download/access, model load, inference, gradient/update, short closed loop, full task, and multi-task or held-out evaluation.

Count failures, timeouts, truncated runs, retries, and rejected samples according to the protocol. An unfinished trajectory is unfinished, not a success or an unexplained zero. Preserve its usable records and identify whether it enters a denominator.

Check original-goal completion together with new-constraint satisfaction and preservation of unedited constraints for runtime editing experiments. Report subgoal progress separately from complete task success.

Report tokens, model calls, latency, environment steps, training cost, and total compute at the level actually measured. A shorter text trace is not automatically a lower total cost.

Videos should distinguish live capture, action replay, and timed replay. A replay can illustrate a recorded result; it does not establish new policy performance. Preserve the link to the original judgment and any replay-state checks.

## Diagnose and Close

First check protocol validity, baseline reproduction, resource constraints, and confounds. Then decide whether evidence supports the proposed mechanism, an alternative explanation, or neither.

Keep negative findings and changes to the hypothesis. Choose the next smallest experiment that can resolve the uncertainty rather than adding modules without diagnosis.

Update the experiment README or result index with commands, completed scope, linked artifacts, outcomes, and open gaps. If a job remains active, report its identity, output path, consumed budget when known, and how to inspect or stop it. Do not claim completion while required runs remain.
