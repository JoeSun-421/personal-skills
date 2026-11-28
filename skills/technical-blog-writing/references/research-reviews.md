# Research Reviews and Transfer Essays

## Choose a Small, Distinct Set

Identify the target interface and bottleneck before searching. For an agent, distinguish observations, reasoning decisions, executable outputs, and environment feedback. Similar names or benchmark scores do not establish transferable mechanisms.

Select papers with distinct contributions and traceable recipes. Treat requested publication years and algorithm preferences explicitly: distinguish first release from conference year, and PPO clipping from actor–critic PPO with a learned value function. Do not relabel GRPO, REINFORCE++ or supervised routing to satisfy an algorithm preference. If the closest evidence does not fit the preference, explain the tradeoff instead of silently changing the scope.

Keep screened candidates and reasons in a maintenance note. The article should concentrate on the selected papers rather than reproducing the search log. Remove narrated curation such as why a paper enters the main text, which algorithm was retained, or how the writer plans to explain it. Within each paper, follow its problem, mechanism, evidence and training sequence, keeping implementation qualifications beside the affected claim. Removing a paper from the article does not authorize deleting its archived PDF or notes.


When a review is organized by acceleration mechanism, classify the intervention before choosing representatives: budget or mode allocation before generation, stopping during generation, cross-turn reuse, selective model escalation, or draft/verify execution. Categories can overlap; identify the primary source of savings. Keep training efficiency, deployment compute and wall-clock latency separate.

For a recent-work request, prioritize original release dates and current technical evidence; conference acceptance and optimizer names are secondary unless the user makes them requirements. Select for explicit recipes, matched controls, cost accounting, reproducibility and stated failure boundaries. Do not fill a recent-work list with older preprints solely because their conference year is recent.

## Explain Each Paper as a Recipe

When the user requests paper-by-paper organization, use a consistent progression: the concrete problem, the mechanism and training recipe, then transfer implications. Respect their requested heading language and avoid adding generic tutorials or comparison tables by default. When transfer is requested only at the end, keep each paper section on its reported method, training and experiments, and consolidate all target-domain discussion in that final section.

For RL, make this chain reconstructable:

**Collected trajectories → control/action representation → verifier and reward → advantage and its statistical scope → loss positions → updated parameters → evaluation evidence.**

State what is frozen. A loss mask at selected tokens does not freeze shared parameters or guarantee unchanged continuation probabilities. Distinguish a sampled trajectory from a teacher-forced counterfactual, and distinguish a learned mode preference from a hand-specified utility prior.

Explain original methods before proposing replacements. If adapting GRPO to PPO, mark the new critic, reward placement, advantage estimator and decision granularity as a proposed recipe. Do not attribute the adaptation or its expected gains to the source paper.

Use only equations that clarify a decision, supervision signal or update. Define newly introduced symbols next to the equation, especially the set used for normalization. Separate allocated budgets from measured consumption, reasoning tokens from action tokens, and loss computation from environment sampling cost.

## Reason from Partial Disclosures

For restricted or closed models, separate what a system card reports, what a public interface makes observable, and what a proposed implementation would explain. When a reader asks for inference about training, give at least one concrete candidate with data, control signal and objective, then name an alternative and a discriminating observation. Explain remaining ambiguity and keep the proposal out of attribution to the model provider.

For compute allocation, identify the decision granularity and owner. System routing, per-request effort, continuation or stopping during decode, and cross-turn state retention can all affect observed length. Record hard completion caps, effective tokens, cache behavior, and time separately. Where possible, compare modes at the same observation and model revision, then measure downstream success and total cost.

## Make Transfer Falsifiable

For each paper, identify one mechanism worth transferring, the assumption that changes in the target setting, and a result that would falsify the transfer. Keep original empirical results inside their task and model scope. Source-heavy explanations should not end with unsupported claims that the target system already has the proposed capability.

For efficiency, record the success constraint and the complete cost boundary. Include routers, verification, retries, failed episodes and environment time when they affect the claim. Fewer tokens alone do not establish lower end-to-end latency.

## Let Original Figures Carry Explanations

Prefer a useful combination of an original method figure and original evidence figure. Introduce the relationship to inspect in the surrounding prose. Preserve labels and axes; inspect the crop itself before checking the webpage. Honor clean-figure requests through separate provenance records and paper references rather than visible overlays.

For a minimal research-blog design, use generous spacing, restrained type hierarchy, readable prose measure and figures sized to the requested text column. When matching figure and prose widths is requested, remove full-width or mobile-bleed overrides; preserve aspect ratios and verify actual element bounds. Follow the existing site. Verify an exact font before claiming a match, use available licensed fonts, and describe unverified alternatives as stylistic approximations. Check headings, equations and figures at desktop and mobile widths.
