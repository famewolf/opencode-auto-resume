# Changelog — fork history (ours + upstream)

This fork of [Mte90/opencode-auto-resume](https://github.com/Mte90/opencode-auto-resume) carries local changes that are not (yet) in upstream.

**Attribution key: [US] = authored by the fork owner (famewolf); [UPSTREAM] = authored by the upstream project (Daniele Scasciafratte / Mte90).**

This file is kept current automatically: the fork owner's daily upstream-sync job regenerates it from each branch's `git log upstream/master..<branch>` (our changes) plus the recent upstream `master` history, so it stays accurate even after a rebase or sync from upstream.

## Our changes — not yet in upstream [US]

| Branch | Head | Date | Change | Submitted as | Status (2026-09-27) |
|---|---|---|---|---|---|
| `fix/recovery-counter-reset` | [`9af63fb`](https://github.com/famewolf/opencode-auto-resume/commit/9af63fb) | 2026-09-26 | Stop the recovery-continue infinite loop (failed recovery retries count toward the budget; `gaveUp` choke-point guard) | [Mte90/opencode-auto-resume#36](https://github.com/Mte90/opencode-auto-resume/pull/36) | OPEN |
| `pr20-v2port` | [`0a0a961`](https://github.com/famewolf/opencode-auto-resume/commit/0a0a961) | 2026-09-26 | OpenCode v2 port (7 commits — listed below) | [Mte90/opencode-auto-resume#37](https://github.com/Mte90/opencode-auto-resume/pull/37) | OPEN |

Commits on `pr20-v2port` (all [US], newest first):

| Commit | Date | Change |
|---|---|---|
| `0a0a961` | 2026-09-26 | OOC lock (parity with v1 loop-fix) |
| `5491286` | 2026-09-24 | Merge `upstream/master` into `pr20-v2port` |
| `b5fd8aa` | 2026-09-17 | docs(v2): document `@opencode/plugin` resolution requirement |
| `aa89252` | 2026-09-17 | docs(v2): add install guide and stable migration notes |
| `ad92b39` | 2026-09-17 | feat(v2): target stable `@opencode/plugin` 2.0.5 API |
| `5e04ade` | 2026-08-26 | feat(plugin): show visible notification when recovering from stall/failure |
| `7511aea` | 2026-08-25 | feat(plugin): add opencode v2 port with event-driven architecture |

## Our changes — merged into upstream [US]

| PR | Merged upstream as | Date | Change |
|---|---|---|---|
| [Mte90/opencode-auto-resume#29](https://github.com/Mte90/opencode-auto-resume/pull/29) | `88bbd87` | 2026-09-17 | block-site invisible tool result fix (open-todos) — in release 1.1.17 |
| [Mte90/opencode-auto-resume#30](https://github.com/Mte90/opencode-auto-resume/pull/30) | `3c8767f` (head `60075d9`) | 2026-09-18 | task-complete repeat-guard — in release 1.1.18 |
| [Mte90/opencode-auto-resume#31](https://github.com/Mte90/opencode-auto-resume/pull/31) | `a546b75` (head `a26a62b`) | 2026-09-21 | block-nudge input gate — in release 1.1.18 |
| [Mte90/opencode-auto-resume#34](https://github.com/Mte90/opencode-auto-resume/pull/34) | `6f4a5af` (head `e0d6a27`) | 2026-09-23 | stop the infinite "continue" loop when the model server is down — in release 1.1.19 |

## Upstream activity — recent `master` history [UPSTREAM]

| Commit | Author | Date | Change |
|---|---|---|---|
| `02b2e01` | Daniele Scasciafratte | 2026-09-23 | fix(esc): and other stuff |
| `6f4a5af` | Daniele Scasciafratte | 2026-09-23 | Merge PR #34 from famewolf/fix/recovery-continue-loop — *our contribution* |
| `e0d6a27` | famewolf | 2026-09-22 | fix(recovery): stop the infinite "continue" loop when the model server is down — *our contribution* |
| `442f0df` | Daniele Scasciafratte | 2026-09-21 | fix(abort): #32 |
| `f47b5b6` | Daniele Scasciafratte | 2026-09-21 | Fix open-todos reminder not firing when w.todos is empty |
| `a546b75` | Daniele Scasciafratte | 2026-09-21 | Merge PR #31 from famewolf/block-nudge-input-gate — *our contribution* |
| `a26a62b` | famewolf | 2026-09-17 | Gate block-site visible nudge on pending user input — *our contribution* |
| `9a57af8` | Daniele Scasciafratte | 2026-09-18 | feat(tool): on unknown tool suggest the right one |
| `3c8767f` | Daniele Scasciafratte | 2026-09-18 | Merge PR #30 from famewolf/fix/task-complete-repeat-guard — *our contribution* |
| `60075d9` | famewolf | 2026-09-17 | fix(task_complete): reject repeat completion signals after ack — *our contribution* |
| `94ab3be` | Daniele Scasciafratte | 2026-09-17 | feat(bump): new release |
| `88bbd87` | Daniele Scasciafratte | 2026-09-17 | Merge PR #29 from famewolf/fix/blocksite-open-todos — *our contribution* |

*Rows marked "our contribution" were authored by famewolf and merged into upstream; all other rows are upstream authors' work — not fork changes.*

## Notes

- Default branch `master` is functionally in sync with upstream `master` (its local commits were merged upstream as PRs #29/#30/#31/#34; hash-level ahead/behind may show small deltas because of merge style).
- A canonical copy of this changelog is kept by the fork owner (`memory/fork-changelogs/famewolf__opencode-auto-resume.md`) so the record survives a destructive fork reset; the sync job restores it if a sync removes it from the fork.
