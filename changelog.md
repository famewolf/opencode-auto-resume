# Changelog — local changes in this fork

This fork of [Mte90/opencode-auto-resume](https://github.com/Mte90/opencode-auto-resume) carries local changes that are not (yet) in upstream. This file is kept current automatically: the fork owner's daily upstream-sync job regenerates it from each branch's `git log upstream/master..<branch>` plus the status of the corresponding upstream submissions, so it stays accurate even after a rebase or sync from upstream.

## Not yet merged upstream (open PRs)

| Branch | Head | Date | Change | Submitted as | Status (2026-09-27) |
|---|---|---|---|---|---|
| `fix/recovery-counter-reset` | [`9af63fb`](https://github.com/famewolf/opencode-auto-resume/commit/9af63fb) | 2026-09-26 | Stop the recovery-continue infinite loop (failed recovery retries count toward the budget; `gaveUp` choke-point guard) | [Mte90/opencode-auto-resume#36](https://github.com/Mte90/opencode-auto-resume/pull/36) | OPEN |
| `pr20-v2port` | [`0a0a961`](https://github.com/famewolf/opencode-auto-resume/commit/0a0a961) | 2026-09-26 | OpenCode v2 port (7 commits — listed below) | [Mte90/opencode-auto-resume#37](https://github.com/Mte90/opencode-auto-resume/pull/37) | OPEN |

Commits on `pr20-v2port` (newest first):

| Commit | Date | Change |
|---|---|---|
| `0a0a961` | 2026-09-26 | OOC lock (parity with v1 loop-fix) |
| `5491286` | 2026-09-24 | Merge `upstream/master` into `pr20-v2port` |
| `b5fd8aa` | 2026-09-17 | docs(v2): document `@opencode/plugin` resolution requirement |
| `aa89252` | 2026-09-17 | docs(v2): add install guide and stable migration notes |
| `ad92b39` | 2026-09-17 | feat(v2): target stable `@opencode/plugin` 2.0.5 API |
| `5e04ade` | 2026-08-26 | feat(plugin): show visible notification when recovering from stall/failure |
| `7511aea` | 2026-08-25 | feat(plugin): add opencode v2 port with event-driven architecture |

## Merged into upstream (no longer local-only)

| Local commit | Change | Merged upstream as |
|---|---|---|
| `6f6d612` | Fix block-site invisible tool result (block-nudge input gate) | PR #31 → `a546b75` (in release 1.1.18) |
| — | recovery-continue infinite-loop fix | PR #34, merged 2026-09-23 (in 1.1.19) |
| — | block-site invisible tool result fix | PR #29 → `3a0de90` (in 1.1.17) |
| — | task-complete repeat-guard | PR #30 (in 1.1.18) |

## Notes

- Default branch `master` is functionally in sync with upstream `master` (its local commits were merged upstream as PRs #29/#30/#31/#34 and land there under different hashes due to merge style).
- A canonical copy of this changelog is kept by the fork owner (`memory/fork-changelogs/famewolf__opencode-auto-resume.md`) so the record survives a destructive fork reset; the sync job restores it if a sync removes it from the fork.
