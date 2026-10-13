Beanubis 0.5.3 - documentation release. Beanubis reports exactly what 0.5.2 reports.

**Start:** give `START-HERE.md` to your AI assistant and say "Pick this up and help me install
Beanubis and create the repo map." It follows `HANDOFF.md` section 3.

- `START-HERE.md`: what to read, the job (repo map, install, test pull requests), the rules,
  the bug report format, how to take a new version.
- `HANDOFF.md` section 3 is the step 1 runbook, phases 0-8: org admin questions, the repo map
  first, install in SahilTest, PR-1, Copilot code review on, PR-2 with three pushes, the
  Copilot Memory check, the AccessCentral baseline and rollout. Section 9 is the roadmap.

**Upgrading from 0.5.2:** replace `tools/beanubis/` with this zip. Nothing else changes.
**From 0.5.0/0.5.1:** see the 0.5.2 notes (copy the workflow template again; delete three
retired keys from `.beanubis.yml`).

**Files:** `beanubis-0.5.3.zip` (extract into `tools/beanubis/`), `beanubis-0.5.3.zip.sha256`,
`START-HERE.md`, `HANDOFF.md`, `INSTALL.md`.
