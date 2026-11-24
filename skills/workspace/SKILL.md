---
name: workspace
description: "Set up a new workspace root and organize research projects according to the user's habits, keeping papers, code, isolated environments, models, data, experiments, weekly reports, and blog drafts inside it. Use for workspace creation or reorganization and connected research workflows; do not reorganize files merely to answer an ordinary question."
---

# Research Workspace

Treat the workspace as a complete, understandable working unit. Start a requested new workspace with an explicit root directory; keep its work inside that root. Help the user move from sources to hypotheses, experiments, and writing without losing evidence or changing their intent.

## User Preferences to Preserve

These defaults come from the user's explicit preferences. Current instructions and the target project's conventions take precedence.

- When creating a new workspace, establish a new workspace root at the chosen location first. Keep projects, papers, environments, weights, data, caches, runs, reports, and blog materials beneath it. Do not choose `~/.local/share/`, `~/.cache/`, or another external directory as the default home for research resources.
- Do not silently treat the agent's current directory as the intended root. Confirm the target through the request and existing files; ask for a root path only if it is required and cannot be inferred. A root may contain multiple projects; follow the user's chosen grouping.
- Inspect before reorganizing. Preserve original files, names, writing habits, and existing useful structure. Do not move an older external runtime into the workspace merely because this skill is loaded.
- Use the current request's language for deliverables, normally Chinese for this user. English skill documentation does not require English research notes. Preserve mixed-language notes unless asked to translate.
- Distinguish sourced facts, hypotheses, plans, interface probes, and measured results. Prefer small, falsifiable mechanisms and fair experiments to module accumulation.
- Keep ordinary work in chat and the workspace. Use Notion only when the current request explicitly asks to use Notion. Do not automatically read it, fetch its skills, save decisions there, or synchronize workspace changes.
- Respect explicit protection boundaries. Where present, retained ESTR assets, personal-site files, and useful no-sleep infrastructure are outside unrelated cleanup. Do not recreate retired research harnesses, revive their timers, or modify another user's files.
- Creating a draft does not authorize publishing, sending a report, deploying a website, or scheduling recurring jobs.

## Establish the Workspace

Inspect applicable `AGENTS.md` files, the current directory, project READMEs, Git status/remotes, and relevant indexes. Check whether the user requested a new workspace or continuation of an existing one. Do not use an obsolete README section as evidence that a retired environment is active.

For new workspaces, choose the root from the user's path or an unambiguous requested name/location, create it, and record it in the root README. For existing work, identify the actual root and preserve its conventions. Do not automatically create a new root for every small follow-up.

Read [layout-and-environments.md](references/layout-and-environments.md) when creating directories, isolating dependencies, or reorganizing files. The sample tree is a fallback design, not a requirement to rebuild existing workspaces.

Maintain a short root README with project entry points, paper indexes, experiment locations, environment/run commands, report/blog links, and important protection boundaries. Add durable operational rules to a local `AGENTS.md` only when setting up or maintaining the workspace is within the request. Keep transient progress in run notes rather than growing the instruction file.

## Choose the Right Skill

Use the smallest set of available skills needed for the task. Read a skill's entry point before applying it, then only the relevant supporting references. Availability of a skill does not authorize using its service.

| Task | Preferred route |
| --- | --- |
| Workspace roots, directory organization, isolated environments, run records | This skill |
| Research questions, closest work, baselines, hypotheses, experiment design, research decisions | `$research-idea-scout`, if installed |
| Papers or web articles added to the local library | [papers-and-articles.md](references/papers-and-articles.md); use an available archival skill if applicable |
| Technical blog posts, paper explainers, equations, figures, meeting notes | `$technical-blog-writing`, if installed |
| Weekly research updates | [weekly-and-blog.md](references/weekly-and-blog.md), based on actual records |
| PDF, DOCX, spreadsheet, slide, or HTML deliverables | The available skill for that artifact type, only when the requested output needs it |
| Explicit Notion or cloud-document work | The relevant connected-service skill, within the current authorization |

If a named skill is unavailable, say so when it affects the work and follow the relevant guidance here. Do not claim it ran or install additional skills silently. When using multiple skills, keep one deliverable and evidence trail rather than producing duplicate plans.

## Add Papers and Articles

Read [papers-and-articles.md](references/papers-and-articles.md). Identify the source and version, deduplicate, save into the current library structure, validate the artifact, and update its index. Distinguish a downloaded source, reading notes, a full translation, and an authored article.

Preserve an existing thematic library. Apply dated folders only when required by that library; do not revive an archived date-based workflow in a new workspace. Prefer links for cross-topic discovery over duplicate PDFs.

## Run Experiments

Use `$research-idea-scout` for scientific design when available. Read [experiments.md](references/experiments.md) for workspace execution and evidence handling.

Before expensive execution, establish the claim, comparable baseline, budget, environment, smallest decisive test, and stop criteria. Use an isolated environment and a unique run directory under the workspace. Capture commands, versions, configs, seeds, inputs, logs, outputs, costs, and failure/termination reasons.

Diagnose protocol and resource problems before changing the hypothesis. A loaded model, successful backward pass, or short control loop establishes only that scope. Preserve negative runs and distinguish replay videos from live capture.

## Write Weekly Reports and Blog Posts

Read [weekly-and-blog.md](references/weekly-and-blog.md). Derive weekly updates from the actual period's source additions, commits, run records, results, and decisions. Mark missing evidence and separate measured findings from next-week plans.

Use `$technical-blog-writing` for authored posts when available. Keep prose, figures, and source notes linked inside the workspace; verify equations with the actual renderer. Save a draft at the requested destination. Publication or delivery to other people requires the corresponding authorization.

## Maintain and Verify

For file reorganization, record old and new paths, check content hashes, preserve permissions and Git staging, and repair local links. Before deleting anything substantial, honor named protection boundaries and verify an authorized archive can be restored. Use existing authorized archive destinations; this skill does not authorize a cloud upload or destructive cleanup.

Finish with the actual root and changed entry points, relevant verification results, and material gaps. Verify relative links, environment locations, artifact references, and claimed experimental results. Report an inaccessible resource or unfinished render as unverified rather than completed.
