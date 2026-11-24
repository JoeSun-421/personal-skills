# Personal Skills

Personal agent skills for workspace organization, research, and technical writing.

| Skill | Purpose | Entry point |
| --- | --- | --- |
| workspace | Create and maintain a workspace root containing projects, papers, isolated environments, experiments, weekly reports, and blog drafts. | [SKILL.md](skills/workspace/SKILL.md) |
| research-idea-scout | Check research questions, closest work, and baselines; design falsifiable experiments and refine proposals using evidence. | [SKILL.md](skills/research-idea-scout/SKILL.md) |
| technical-blog-writing | Turn papers, equations, and experiments into clear technical posts and research meeting notes; verify sources, figures, and rendered mathematics. | [SKILL.md](skills/technical-blog-writing/SKILL.md) |

## One-prompt installation for XinAgent

Copy the following prompt into XinAgent, or another agent that supports directory-based `SKILL.md` skills and can download and write local files:

```text
Install all skills from https://github.com/JoeSun-421/personal-skills into this agent's supported user-level skills directory.

1. Determine the correct skills directory from this agent's local documentation or configuration. Use an existing explicit user preference if available. If the destination cannot be determined, ask me for it rather than guessing an agent-specific path.
2. Download or clone the repository's default branch into a temporary staging directory, using existing GitHub authentication if needed. If access is denied, stop and explain how I can authorize access; never request that I paste a password, token, or private key into chat.
3. Inspect README.md and discover each direct subdirectory of skills/ that contains SKILL.md. The current skills are workspace, research-idea-scout, and technical-blog-writing.
4. Install each complete skill directory, including its references/ and agents/ files, directly under the supported skills directory. Do not install the repository root or introduce an extra skills/ nesting level. Preserve the published instructions and relative paths.
5. If a skill already exists, leave identical copies in place. Before replacing a differing copy, preserve it in a timestamped backup outside the discovery directory and report the backup location. Leave unrelated skills unchanged.
6. Verify that every installed skill has valid name and description frontmatter, that its name matches its directory, and that all bundled relative file references resolve. Use the agent's existing skill validator if available.
7. Refresh skill discovery using the agent's documented mechanism if available. Report the installed names, absolute paths, source commit when available, and verification results. Distinguish files installed successfully from skills actually discovered by the agent; explain any reload or restart still required.

Complete the download, installation, and verification within the permissions already available. Do not modify unrelated agent settings or publish anything.
```

This repository currently requires authorized GitHub access. A prompt does not grant access to a private repository. Use the agent's existing GitHub connection, SSH key, or credential manager.

### Manual download

With authorized Git access:

```bash
git clone https://github.com/JoeSun-421/personal-skills.git
```

Install the individual directories under `personal-skills/skills/` into your agent's documented skills directory. For Codex, use `$CODEX_HOME/skills`, or `~/.codex/skills` when `CODEX_HOME` is unset. Other agents may use a different location.

## Structure

Each subdirectory of `skills/` is a self-contained skill. `SKILL.md` is its entry point, `references/` holds material loaded as needed, and `agents/openai.yaml` provides OpenAI-specific display metadata and a default invocation prompt.

The writing skill's [editorial patterns](skills/technical-blog-writing/references/editorial-patterns.md) draw on specific articles by Physical Intelligence, Jianlin Su, Distill, Lilian Weng, Andrej Karpathy, Jay Alammar, Sebastian Raschka, and Simon Willison. Sources with limited access are identified separately. Learn from their organization of information without imitating an author's voice.

## Usage

After installation, invoke `$workspace`, `$research-idea-scout`, or `$technical-blog-writing` in agents that support this syntax. In other agents, use their documented skill invocation mechanism. When maintaining a skill, keep its entry point and relative references in sync and validate the skill structure again.

Example requests:

```text
Use $workspace to create a new workspace root at my chosen location, keeping projects, papers, isolated environments, models, data, runs, weekly reports, and blog drafts inside it.

Use $research-idea-scout to assess this research question against the closest work and design the smallest fair experiment that could refute the hypothesis.

Use $workspace to draft this week's research report from the workspace's actual papers, code changes, and experiment records, separating completed results from plans.

Use $technical-blog-writing to turn these notes and verified results into a clear blog draft with checked sources, figures, and equations.
```

The workspace skill records the user's preference to establish a workspace root first and keep research resources beneath it. It follows existing project layouts, keeps Notion opt-in, and does not move old files or publish drafts automatically. Its sample directory tree and weekly-report structure are defaults for new work, not instructions to rebuild an existing workspace.

This repository contains personally maintained skills. It excludes bundled `.system` skills and plugin caches. Paper PDFs, experiment data, and model weights belong in their research workspaces. Credentials stay in the user's existing credential mechanism and are never committed here.
