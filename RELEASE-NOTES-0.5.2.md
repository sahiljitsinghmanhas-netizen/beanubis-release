Beanubis 0.5.2 - fixes from a full audit of 0.5.1 (143 confirmed findings), dead code removed.

**Install:** download `beanubis-0.5.2.zip`, check it against `beanubis-0.5.2.zip.sha256`
(`sha256sum -c`), and extract it into `tools/beanubis/` of the IIQ repository (no wrapper
folder). Then follow `INSTALL.md`; `HANDOFF.md` has the context, decisions and what to verify.

**Upgrading from 0.5.x:** copy `templates/.github/workflows/beanubis.yml` again (it now checks
out the pull request head commit). Delete `files.changed_only`, `scoring.profile` and
`ai.handoff_dir` from `.beanubis.yml` (still accepted, with a warning).

**Main fixes** (full list in CHANGELOG.md inside the zip):

- Pull requests: line numbers and anchors come from the head commit, not GitHub's merge
  commit. "Fixed in" is replied only when the code was really re-checked. A re-review posts
  findings the latest push caused on untouched lines. Code text is HTML-escaped in comments.
- Change collection: one base (the merge-base) for every mode. A new branch's pre-push base
  is the nearest of `targets.base_branches`, not `origin/main`. Personal git diff settings,
  renames, `review .`, windows-1252 base versions and running from a subfolder all work.
- Parsing: a bad `\u` escape is `IIQ-SYNTAX` (it crashed the run), and `IIQ-SYNTAX` cannot be
  suppressed. IQService native rules are not parsed as BeanShell. Objects inside
  `<ImportAction>` are found.
- Rules: QUALITY-014 corrected (Correlation rules return a Map). False positives and false
  negatives were fixed in about 25 checks, including LOG-007, QUALITY-012/017, the PERF
  checks, SEC-001/002, STYLE-002/003/005, XML-003 tabs and NAME-001 suggestions.
- The release `.sha256` and text files use LF line endings.

Tested: unit suite (Ubuntu and Windows, Python 3.10 and 3.12), a metamorphic bug hunt over 48
seed files, and 14 live pull-request scenarios on a synthetic IIQ repository.
