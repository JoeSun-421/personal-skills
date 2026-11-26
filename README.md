# Personal Skills

Personal agent skills for workspace organization, research, and technical writing.

| Skill | Purpose | Entry point |
| --- | --- | --- |
| workspace | Create and maintain a workspace root containing projects, papers, isolated environments, experiments, weekly reports, and blog drafts. | [SKILL.md](skills/workspace/SKILL.md) |
| research-idea-scout | Check research questions, closest work, and baselines; design falsifiable experiments and refine proposals using evidence. | [SKILL.md](skills/research-idea-scout/SKILL.md) |
| technical-blog-writing | Turn papers, equations, and experiments into clear technical posts and research meeting notes; verify sources, figures, and rendered mathematics. | [SKILL.md](skills/technical-blog-writing/SKILL.md) |
| research-review-template | Expand a supplied Markdown review into mechanism groups with faithful training recipes, original figures and one final transfer section. | [SKILL.md](skills/research-review-template/SKILL.md) |

## One-prompt installation for Agent

Copy the following prompt into Agent, or another agent that supports directory-based `SKILL.md` skills and can download and write local files:

```text
Install all skills from https://github.com/JoeSun-421/personal-skills into this agent's supported user-level skills directory.

1. Determine the correct skills directory from this agent's local documentation or configuration. Use an existing explicit user preference if available. If the destination cannot be determined, ask me for it rather than guessing an agent-specific path.
2. Download or clone the repository's default branch into a temporary staging directory, using existing GitHub authentication if needed. If access is denied, stop and explain how I can authorize access; never request that I paste a password, token, or private key into chat.
3. Inspect README.md and discover each direct subdirectory of skills/ that contains SKILL.md. The current skills are workspace, research-idea-scout, technical-blog-writing, and research-review-template.
4. Install each complete skill directory, including its references/ and agents/ files, directly under the supported skills directory. Do not install the repository root or introduce an extra skills/ nesting level. Preserve the published instructions and relative paths.
5. If a skill already exists, leave identical copies in place. Before replacing a differing copy, preserve it in a timestamped backup outside the discovery directory and report the backup location. Leave unrelated skills unchanged.
6. Verify that every installed skill has valid name and description frontmatter, that its name matches its directory, and that all bundled relative file references resolve. Use the agent's existing skill validator if available.
7. Refresh skill discovery using the agent's documented mechanism if available. Report the installed names, absolute paths, source commit when available, and verification results. Distinguish files installed successfully from skills actually discovered by the agent; explain any reload or restart still required.

Complete the download, installation, and verification within the permissions already available. Do not modify unrelated agent settings or publish anything.
```

Example requests:

```text
Use $workspace to create a new workspace root at my chosen location, keeping projects, papers, isolated environments, models, data, runs, weekly reports, and blog drafts inside it.

Use $research-idea-scout to assess this research question against the closest work and design the smallest fair experiment that could refute the hypothesis.

Use $workspace to draft this week's research report from the workspace's actual papers, code changes, and experiment records, separating completed results from plans.

Use $technical-blog-writing to turn these notes and verified results into a clear blog draft with checked sources, figures, and equations.
```

```text
Use $research-review-template to expand my annotated Markdown into 6–8 source-checked papers in 3–4 mechanism classes, retaining my required papers and consolidating transfer at the end.
```
