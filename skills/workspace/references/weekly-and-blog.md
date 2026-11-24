# Weekly Reports and Blog Posts

Use an existing user template or prior accepted example first. The structures below are suggested defaults when no format has been established; they are not claims about the user's historical templates.

## Weekly Evidence Collection

State the exact reporting interval and timezone. Use the user's dates; otherwise identify the intended week from the request and existing report names, asking only if ambiguity matters. Use Asia/Hong_Kong for new date labels unless overridden. Do not silently include future days or old results as this week's work.

Collect evidence from the project README, paper index, version-control changes, research notes, experiment plans, run manifests, raw summaries, and previous reports. Link to original evidence and distinguish when work happened from when it was written up.

Keep status explicit:

- **Completed:** A concrete artifact or action with verifiable evidence.
- **Measured:** Actual results with configuration, sample size, costs, uncertainty, and limitations.
- **Proposed/in progress:** A design, expected outcome, or running job.
- **Blocked/unverified:** A missing resource, failed check, inaccessible source, or incomplete validation.

Reading a paper, implementing an adapter, running a probe, training a model, and improving full-task performance are different accomplishments. Report only what happened; include negative results and plan changes.

## Suggested Weekly Report

Save under the existing reports location, or `reports/weekly/YYYY-MM-DD.md` inside the project when no convention exists. Use the period-end date and state the interval in the document. Update a report index if one exists or is needed for navigation.

A concise report can follow this structure:

1. **Question and conclusion:** The research question, what changed this week, and what current evidence supports.
2. **Completed work:** Papers read/added, designs or code changed, and verifiable deliverables, with links.
3. **Experiments and findings:** Condition, baseline, sample count, quality, cost, uncertainty, and interpretation. Separate probes from task results.
4. **Failures and open questions:** Negative results, regressions, blockers, and their implications.
5. **Next week:** The few next decisive actions, evidence of success/failure, and required resources. These are plans.
6. **Decisions needed:** Only choices actually requiring the user's input.

Omit empty sections and tables. Do not invent results, owners, deadlines, effort estimates, or decisions. When logs are missing, report that limitation and summarize only the evidence available.

Drafting or saving a report does not authorize emailing it, posting it to a team service, writing to Notion, or creating a weekly automation.

## Blog from Verified Research

Use `$technical-blog-writing` when installed. A blog is an explanation with an argument, not a pasted weekly report or chronological agent work log.

Choose one concrete question and organize the post around the difficulty, mechanism, necessary derivation, evidence, and limitations. For a proposal-only post, label it as a proposal and keep predicted gains conditional.

Keep the draft, source notes, and assets inside the workspace, using existing paths or `blog/drafts/`, `blog/sources/`, and `blog/assets/<slug>/`. Use stable relative paths and neutral title/date/description/tags metadata only when the project needs it.

Cite paper versions and exact method sections, equations, or figures for implementation claims. Distinguish original results, local measurements, teaching examples, and new proposals. Reuse the experiment's recorded sample counts and costs rather than reconstructing attractive numbers from selected runs.

Preserve the user's wording and reasoning when editing existing notes. Make technical corrections explicitly and support them with sources. Do not impose a formal paper voice on informal notes.

## Verify and Deliver

Check local links, source locations, image loading, captions/provenance, numerical examples, and equation semantics. Use the actual KaTeX/MathJax pipeline and browser inspection for mathematical display; a delimiter checker alone is insufficient.

Keep source PDFs unchanged; retain figure labels, axes, legends, version, page/figure identifiers, and applicable licensing information when extracting figures. Do not present a generative redraw as an original figure.

If rendering or source access cannot be verified, report the actual gap. Deliver the saved draft and relevant checks. Publishing, site modifications, and external distribution remain separate actions requiring the corresponding request.
