# Beanubis releases

Download page for Beanubis, a linter for SailPoint IdentityIQ XML (the BeanShell code in
`<Source>` and the XML around it) that works with GitHub Copilot code review or on its own.

## Start here

1. Download the files of the [latest release](https://github.com/sahiljitsinghmanhas-netizen/beanubis-release/releases/latest)
   (no login needed).
2. Give `START-HERE.md` to your AI assistant (e.g. Copilot Chat in agent mode) and say:
   *"Pick this up and help me install Beanubis and create the repo map."*
3. It follows `HANDOFF.md` section 3, the step 1 runbook: org admin questions, the repo map,
   the install, the test pull requests and what to screenshot.
4. Problems go back as a bug report (format in `START-HERE.md`); fixes come out as a new
   release here. Take the new zip, replace `tools/beanubis/`, re-run the step that failed.

These links always point to the latest release:

| File | What |
|---|---|
| [START-HERE.md](https://github.com/sahiljitsinghmanhas-netizen/beanubis-release/releases/latest/download/START-HERE.md) | Brief for the AI assistant helping with the install |
| [HANDOFF.md](https://github.com/sahiljitsinghmanhas-netizen/beanubis-release/releases/latest/download/HANDOFF.md) | Context, non-negotiables, the step 1 runbook (section 3), roadmap |
| [INSTALL.md](https://github.com/sahiljitsinghmanhas-netizen/beanubis-release/releases/latest/download/INSTALL.md) | Install and settings in detail |
| `beanubis-<version>.zip` + `.sha256` | On the [release page](https://github.com/sahiljitsinghmanhas-netizen/beanubis-release/releases/latest): extract into `tools/beanubis/` of the IIQ repository (no wrapper folder) |

The zip also contains `docs/` (the same documents plus CONFIG, ARCHITECTURE,
DEVELOPER-GUIDE) and `CHANGELOG.md`.

## Latest: 0.5.3

Documentation release on top of 0.5.2 (audit fixes): the START-HERE brief and the step 1
runbook. Release notes: [RELEASE-NOTES-0.5.3.md](RELEASE-NOTES-0.5.3.md).

Copyright (c) 2026 Sahiljit Manhas. All rights reserved.
