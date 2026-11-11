# Project instructions

Before any repository work, read and follow [the shared workflow](.agent-workflow/AGENTS.md).
Read that file explicitly; a Markdown link does not automatically load instructions.
Resolve its project paths from this repository root, not from the submodule.
If the file is missing, stop and ask for submodule initialization.

## Project-specific settings

- Setup confirmed: yes
- Repository: `mongilyov/skills`
- Reviewers: `mongilyov`
- Integration branch: `master`
- Agent branch prefix: `codex` (branches use `codex/`)
- Setup command: `git submodule update --init --recursive` (human initialization
  for new clones; agents follow the shared workflow's bot-only synchronization rules).
  The bot helper requires Python 3.9+, OpenSSL, and Git.
- Build command: not applicable; the current repository contains documentation only.
- Focused test command: not applicable until executable skill resources are added;
  define their relevant test commands in the same change.
- Full test command: not applicable; no project executable code or test suite yet.
- Other required checks: `git diff --check`, verify local Markdown link targets,
  verify the recorded submodule pin, and review the final diff. For skill changes,
  verify YAML frontmatter has a matching `name` and a discriminating `description`,
  referenced resources exist, and any executable helpers pass relevant tests.
- UI verification: not applicable; no executable UI is delivered.
- Architecture and conventions: follow [PROJECT_SPEC.md](PROJECT_SPEC.md) and
  [WORK_PLAN.md](WORK_PLAN.md). Each skill has its own lowercase, hyphenated root
  directory containing `SKILL.md` with YAML `name` and `description`. Add supporting
  resources only when needed. Keep language-specific rules scoped to that skill;
  shared repository workflow stays in the read-only submodule.
- Workflow submodule: `.agent-workflow`
- GitHub bot helper: `.agent-workflow/github_bot/github_bot.py`
- GitHub bot README: `.agent-workflow/github_bot/README.md`
- GitHub App ID: `5557899`
- GitHub installation ID: `177288016`
- Private-key path environment variable: `GITHUB_APP_PRIVATE_KEY_PATH` (optional
  override; otherwise the helper reads the ignored `.github-bot-key-path` in the
  project root). Never commit the key or its local path.
