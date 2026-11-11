# Work plan: Skills

## Increment 01: Adopt the shared workflow

Selected by the user for this bootstrap. One focused setup PR will contain the
submodule, root settings, and collection documentation. The user approved a
bootstrap-only setup-gate bypass and the proposed project settings.

- [x] 01.1 Pin the shared workflow as `.agent-workflow` and reference it explicitly
  from root instructions. Verify: submodule HEAD matches the staged gitlink and
  its configured URL points to `mongilyov/agents.md`.
- [x] 01.2 Configure repository settings and protect the local bot key-path file.
  Depends on 01.1. Verify: settings have no placeholders; path file is ignored
  and untracked, and the key remains outside this repository.
- [x] 01.3 Document the collection structure and contribution workflow.
  Depends on 01.1. Verify: local Markdown links resolve and `git diff --check` passes.
- [ ] 01.4 Verify bot access and deliver the setup PR for review by `mongilyov`.
  Depends on 01.1–01.3. Verify: fetch succeeds, PR is ready, reviewer is requested,
  and available CI results are inspected.

### Verification and delivery

Pinned the merged upstream workflow commit
`c31451e4729b316301125da652dd6e8894678c91` (previous bootstrap candidate:
`50366279dcd683d2a030cb31efbcec462da4727b`). Their file trees are identical;
the new pin records the accepted upstream merge, including project-local ignored
bot key-path support already configured here.

Bot authentication and required permissions are verified. Both repositories were
fetched through the trusted helper. Local Markdown links, submodule URL and pin,
ignored/untracked key-path handling, and whitespace checks pass.

The remote repository initially had no branches. Delivery requires an initial
base branch before the setup PR can be opened; publishing that initial commit
requires an explicit bootstrap exception to the integration-branch push rule.

## Later increments

Choose the first skill and agree on its scope before adding it.
