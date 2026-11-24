# Layout and Environment Isolation

## Choose and Record the Root

On a request to create a new workspace, first establish its new root at the user's chosen location. All research materials belong below it. The directory name may be `workspace` or another name explicitly chosen by the user. Do not hardcode a particular home directory or host.

A root can hold several projects. Keep the user's chosen grouping; do not force one new root per project. Continue in an existing workspace when that is what the user requested.

This is a suggested layout only when no structure exists. Create the directories needed by the current work, not an empty scaffold of every possible workflow:

```text
<workspace-root>/
  README.md
  AGENTS.md
  projects/
    <project>/
      README.md
      research-ideas/
      related_works/
        README.md
        <topic>/
        logs/
      experiments/
        <experiment>/
          README.md
          configs/
          src/
      .runtime/
        envs/
        weights/
        data/
        cache/
        runs/
      reports/
        weekly/
      blog/
        drafts/
        assets/
        sources/
```

A single-project workspace can omit `projects/<project>/`. If the user already has `related_work/`, `src/`, `.venv/`, `long-task-records/`, or other established paths, use those rather than renaming for consistency. Shared resources, if actually needed, can live in a clearly documented directory under the same root; projects must not overwrite one another's dependencies.

Keep source code, small configs, indexes, and authored Markdown in version control where appropriate. Ignore environments, weights, datasets, caches, raw logs, and large media. Preserve any existing exceptions for curated result tables. Git ignore rules do not remove already tracked content; inspect before changing tracked artifacts.

## Isolate Execution

Use the project's existing environment manager. Create a separate environment per incompatible dependency stack, under the chosen workspace root. A project-local `.venv/` or `.runtime/envs/<stack>/` is sufficient for many Python projects. Use containers when required by the project's native dependencies, simulator, or established runtime; do not introduce them for every task.

Before installation or execution, inspect the effective interpreter, package manager, versions, available GPU memory, disk, active jobs, and relevant ports. Use explicit environment interpreter paths in reproducible commands rather than relying on shell activation.

Keep caches and downloads under the root too. Configure the relevant tools for the subprocess or project, for example `HF_HOME`, `XDG_CACHE_HOME`, `PIP_CACHE_DIR`, or `UV_CACHE_DIR`. Set only variables relevant to the actual tools; avoid broad global shell changes. Do not repurpose `HOME` or `CODEX_HOME` to redirect caches.

Pin source commits, package locks or version manifests, model/data revisions, and relevant CUDA/runtime versions. Separate inference and simulator environments when their requirements conflict. A venv isolates Python packages; verify compatibility with system drivers, native libraries, and the actual GPU separately.

Keep upstream checkouts unmodified when the project requires it. Put adapters, patches, launchers, and local experiments in the project's own code, or record a patch against a pinned upstream version. Preserve an existing runtime rather than upgrading it to satisfy an unrelated experiment.

Container bind mounts and output paths should point inside the workspace. Use the host user's UID/GID where the runtime supports it so outputs remain accessible. Never run a workload as root merely to bypass a permission problem.

Credentials stay in the user's existing credential mechanism. Do not copy secrets into workspace documentation, commit them, or include them in run manifests. This rule concerns research files and runtimes; it does not require relocating normal system services or the agent's own global installation/configuration.

## Run Lifecycle

Assign each run a unique output directory beneath the workspace. Record the command, working directory, environment, source revision, output path, start time/timezone, budget, and any PID/job/container identifier. Do not start a duplicate because the first run is slow.

Use a small resource/interface probe for the identified risk before committing the full budget. Reuse a known-good environment when compatible rather than reinstalling for every run. Preserve optional dependency differences and quantify their implications.

If a long-running job is authorized, record how to inspect and stop it. Respect current pause/cancel instructions. Do not create persistent services, background timers, or recurring downloads merely to keep the workspace organized.

## Reorganization and Existing External Assets

Existing files outside the desired root do not move automatically. If migration is requested, inventory paths, sizes, owners, active users/jobs, links, and environment references first. Document a reversible source-to-destination plan. Do not copy multi-GB models just to make a directory tree look tidy.

For moves, record old/new paths and hashes, preserve file permissions, update scripts and links, and verify behavior before retiring a source. Environments may contain absolute interpreter paths; recreate from a recorded specification when necessary rather than assuming a moved venv still works.

Preserve unrelated edits and staging. Use branches or Git worktrees inside the chosen workspace when isolation is needed; do not force a new worktree for a small documentation edit. Check the actual repository boundary, since the workspace root may contain independent repositories.
