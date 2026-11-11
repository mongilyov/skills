# Project specification: Skills

## Purpose and scope

Maintain a collection of reusable agent skills for programming languages and
other tasks. Skills should provide focused conventions and guidance that improve
agent decisions for the task described in their frontmatter.

Each skill is a root-level directory with a `SKILL.md` entrypoint containing YAML
`name` and `description`. Directory names match skill names and use lowercase
letters, digits, and hyphens. Add scripts, references, assets, or agent metadata
only when the skill needs them. Keep references discoverable from the entrypoint.

The repository adopts the shared engineering workflow through a pinned
`.agent-workflow` submodule and project-specific root instructions.

## Acceptance criteria

- Root instructions explicitly load the pinned shared workflow.
- Repository settings identify the project, bot, reviewer, and relevant checks.
- Each future skill has a clear scope, valid frontmatter, and usable references.
- Executable skill resources include verification appropriate to their behavior.
- Credentials and machine-specific key paths remain untracked.

## Open decisions

The first skill and its requirements will be selected separately. This bootstrap
does not import existing installed skills or add an installer or publishing system.
