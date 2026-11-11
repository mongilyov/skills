# Skills

A collection of reusable agent skills for programming languages and other tasks.
No skills have been added yet.

Each skill lives in its own directory with a `SKILL.md` entrypoint. Its YAML
frontmatter declares the skill name and when to use it; the body contains focused
instructions. Supporting scripts, references, and assets belong beside the
entrypoint when needed.

## Contributing

Read [AGENTS.md](AGENTS.md), the pinned
[shared workflow](.agent-workflow/AGENTS.md),
[project specification](PROJECT_SPEC.md), and [work plan](WORK_PLAN.md).
Work proceeds in explicitly selected increments and small reviewed PRs.

For a new clone, initialize the pinned workflow submodule:

```sh
git clone --recurse-submodules https://github.com/mongilyov/skills.git
```

For an existing clone, a human can initialize it with
`git submodule update --init --recursive`. Human pulls use
`git pull --ff-only --recurse-submodules`; agents use the bot helper as described
in the shared workflow. Routine synchronization preserves the recorded pin.
Workflow upgrades are separate reviewed changes.
