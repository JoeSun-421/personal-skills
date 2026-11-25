# Research Reviews and Transfer Essays

## Choose a Small, Distinct Set

Identify the target interface and bottleneck before searching. For an agent, distinguish observations, reasoning decisions, executable outputs, and environment feedback. Similar names or benchmark scores do not establish transferable mechanisms.

Select papers with distinct contributions and traceable recipes. Treat requested publication years and algorithm preferences explicitly: distinguish first release from conference year, and PPO clipping from actor–critic PPO with a learned value function. Do not relabel GRPO, REINFORCE++ or supervised routing to satisfy an algorithm preference. If the closest evidence does not fit the preference, explain the tradeoff instead of silently changing the scope.

Keep screened candidates and reasons in a maintenance note. The article should concentrate on the selected papers rather than reproducing the search log. Removing a paper from the article does not authorize deleting its archived PDF or notes.

## Explain Each Paper as a Recipe

When the user requests paper-by-paper organization, use a consistent progression: the concrete problem, the mechanism and training recipe, then transfer implications. Respect their requested heading language and avoid adding generic tutorials or comparison tables by default.

For RL, make this chain reconstructable:

**Collected trajectories → control/action representation → verifier and reward → advantage and its statistical scope → loss positions → updated parameters → evaluation evidence.**

State what is frozen. A loss mask at selected tokens does not freeze shared parameters or guarantee unchanged continuation probabilities. Distinguish a sampled trajectory from a teacher-forced counterfactual, and distinguish a learned mode preference from a hand-specified utility prior.

Explain original methods before proposing replacements. If adapting GRPO to PPO, mark the new critic, reward placement, advantage estimator and decision granularity as a proposed recipe. Do not attribute the adaptation or its expected gains to the source paper.

Use only equations that clarify a decision, supervision signal or update. Define newly introduced symbols next to the equation, especially the set used for normalization. Separate allocated budgets from measured consumption, reasoning tokens from action tokens, and loss computation from environment sampling cost.

## Make Transfer Falsifiable

For each paper, identify one mechanism worth transferring, the assumption that changes in the target setting, and a result that would falsify the transfer. Keep original empirical results inside their task and model scope. Source-heavy explanations should not end with unsupported claims that the target system already has the proposed capability.

For efficiency, record the success constraint and the complete cost boundary. Include routers, verification, retries, failed episodes and environment time when they affect the claim. Fewer tokens alone do not establish lower end-to-end latency.

## Let Original Figures Carry Explanations

Prefer a useful combination of an original method figure and original evidence figure. Introduce the relationship to inspect in the surrounding prose. Preserve labels and axes; inspect the crop itself before checking the webpage. Honor clean-figure requests through separate provenance records and paper references rather than visible overlays.

For a minimal research-blog design, use generous spacing, restrained type hierarchy, readable prose measure and wider figures. Follow the existing site. Verify an exact font before claiming a match, use available licensed fonts, and describe unverified alternatives as stylistic approximations. Check headings, equations and figures at desktop and mobile widths.
