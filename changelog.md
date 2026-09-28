# Changelog — fork history (ours + upstream)

This fork of [Mte90/opencode-auto-resume](https://github.com/Mte90/opencode-auto-resume) carries local changes that are not (yet) in upstream.

**Attribution key: [US] = authored by the fork owner (famewolf); [UPSTREAM] = authored by the upstream project (Daniele Scasciafratte / Mte90).**

This file is kept current automatically: the fork owner's daily upstream-sync job regenerates it from each branch's `git log upstream/master..<branch>` (our changes) plus the recent upstream `master` history, so it stays accurate even after a rebase or sync from upstream.

## Our changes — not yet in upstream [US]

| Branch | Head | Date | Change | Submitted as | Status (2026-09-28) |
|---|---|---|---|---|---|
| `pr20-v2port` | [`875d7e4`](https://github.com/famewolf/opencode-auto-resume/commit/875d7e4) | 2026-09-28 | OpenCode v2 port (11 commits — listed below; the v1 loop-fix #36 was merged upstream separately and is no longer carried here). Head is a **strict superset of upstream PR #20** (`b5fd8aa` is a direct ancestor). | [Mte90/opencode-auto-resume#37](https://github.com/Mte90/opencode-auto-resume/pull/37) | OPEN — 0 maintainer replies (2 doc comments on #37, 1 reply on #20) |

Commits on `pr20-v2port` (newest first):

| Commit | Date | Change |
|---|---|---|
| `875d7e4` | 2026-09-28 | fix(v2): stop self-inflicted "Step interrupted" and synthetic-continue bursts — routes all three v2 recovery paths through a single `injectOnce()` choke point (rate limit + busy check), stops the plugin reacting to its own abort events, adds liveness handlers, and makes `src/v2/index.ts` buildable |
| `3c1d88c` | 2026-09-27 | v2 back-port: `shouldStandDownForUser` guard (v1 parity) — stand down on a pending tool_use/question or recent user activity; + `activeUserWindowMs` option (default 15min) |
| `0dd0403` | 2026-09-27 | fix(v2): never nudge a turn that hands off to the user |
| `9a44699` | 2026-09-27 | v2: never interrupt compaction or live busy sessions |
| `0a0a961` | 2026-09-26 | OOC lock (parity with v1 loop-fix) |
| `5491286` | 2026-09-24 | Merge `upstream/master` into `pr20-v2port` |
| `b5fd8aa` | 2026-09-17 | docs(v2): document `@opencode/plugin` resolution requirement (upstream: valentimarco) |
| `aa89252` | 2026-09-17 | docs(v2): add install guide and stable migration notes (upstream: valentimarco) |
| `ad92b39` | 2026-09-17 | feat(v2): target stable `@opencode/plugin` 2.0.5 API (upstream: valentimarco) |
| `5e04ade` | 2026-08-26 | feat(plugin): show visible notification when recovering from stall/failure (upstream: valentimarco) |
| `7511aea` | 2026-08-25 | feat(plugin): add opencode v2 port with event-driven architecture (upstream: valentimarco) |

## Our changes — merged into upstream [US]

| PR | Merged upstream as | Date | Change |
|---|---|---|---|
| [Mte90/opencode-auto-resume#29](https://github.com/Mte90/opencode-auto-resume/pull/29) | `88bbd87` | 2026-09-17 | block-site invisible tool result fix (open-todos) — in release 1.1.17 |
| [Mte90/opencode-auto-resume#30](https://github.com/Mte90/opencode-auto-resume/pull/30) | `3c8767f` (head `60075d9`) | 2026-09-18 | task-complete repeat-guard — in release 1.1.18 |
| [Mte90/opencode-auto-resume#31](https://github.com/Mte90/opencode-auto-resume/pull/31) | `a546b75` (head `a26a62b`) | 2026-09-21 | block-nudge input gate — in release 1.1.18 |
| [Mte90/opencode-auto-resume#34](https://github.com/Mte90/opencode-auto-resume/pull/34) | `6f4a5af` (head `e0d6a27`) | 2026-09-23 | stop the infinite "continue" loop when the model server is down — in release 1.1.19 |
| [Mte90/opencode-auto-resume#36](https://github.com/Mte90/opencode-auto-resume/pull/36) | `48d4541` (head `9af63fb`) | 2026-09-28 | stop the recovery-continue infinite loop (counter reset + `gaveUp` choke-point guard) — in release 1.1.20 |

## Upstream activity — recent `master` history [UPSTREAM]

| Commit | Author | Date | Change |
|---|---|---|---|
| `8ef7053` | Daniele Scasciafratte | 2026-09-28 | perf(tests): cut toolext runtime from 104s to 23s |
| `48d4541` | Daniele Scasciafratte | 2026-09-28 | Merge pull request #36 from famewolf/fix/recovery-counter-reset — *our contribution* |
| `9af63fb` | famewolf | 2026-09-26 | Stop the recovery-continue infinite loop — *our contribution* |
| `02b2e01` | Daniele Scasciafratte | 2026-09-23 | fix(esc): and other stuff |
| `6f4a5af` | Daniele Scasciafratte | 2026-09-23 | Merge PR #34 from famewolf/fix/recovery-continue-loop — *our contribution* |
| `e0d6a27` | famewolf | 2026-09-22 | fix(recovery): stop the infinite "continue" loop when the model server is down — *our contribution* |
| `442f0df` | Daniele Scasciafratte | 2026-09-21 | fix(abort): #32 |
| `f47b5b6` | Daniele Scasciafratte | 2026-09-21 | Fix open-todos reminder not firing when w.todos is empty |
| `a546b75` | Daniele Scasciafratte | 2026-09-21 | Merge PR #31 from famewolf/block-nudge-input-gate — *our contribution* |
| `a26a62b` | famewolf | 2026-09-17 | Gate block-site visible nudge on pending user input — *our contribution* |
| `9a57af8` | Daniele Scasciafratte | 2026-09-18 | feat(tool): on unknown tool suggest the right one |
| `3c8767f` | Daniele Scasciafratte | 2026-09-18 | Merge PR #30 from famewolf/fix/task-complete-repeat-guard — *our contribution* |

*Rows marked "our contribution" were authored by famewolf and merged into upstream; all other rows are upstream authors' work — not fork changes.*

## Notes

- Default branch `master` is functionally in sync with upstream `master` (its local commits were merged upstream as PRs #29/#30/#31/#34/#36; hash-level ahead/behind may show small deltas because of merge style).
- A canonical copy of this changelog is kept by the fork owner (`memory/fork-changelogs/famewolf__opencode-auto-resume.md`) so the record survives a destructive fork reset; the sync job restores it if a sync removes it from the fork.
