# Changelog — fork history (ours + upstream)

This fork of [Mte90/opencode-auto-resume](https://github.com/Mte90/opencode-auto-resume) carries local changes that are not (yet) in upstream.

**Attribution key: [US] = authored by the fork owner (famewolf); [UPSTREAM] = authored by the upstream project (Daniele Scasciafratte / Mte90).**

This file is kept current automatically: the fork owner's daily upstream-sync job regenerates it from each branch's `git log upstream/master..<branch>` (our changes) plus the recent upstream `master` history, so it stays accurate even after a rebase or sync from upstream.

## Our changes — not yet in upstream [US]

| Branch | Head | Date | Change | Submitted as | Status (2026-10-04) |
|---|---|---|---|---|---|
| `pr20-v2port` | [`f773ea6`](https://github.com/famewolf/opencode-auto-resume/commit/f773ea6) | 2026-10-03 | OpenCode v2 port (21 own commits — listed below; the v1 loop-fix #36 was merged upstream separately and is no longer carried here). Rebased onto upstream `0c9bc06` 2026-10-01 (`d890f6c`); the port lives in a self-contained v2 module. | [Mte90/opencode-auto-resume#37](https://github.com/Mte90/opencode-auto-resume/pull/37) | OPEN, mergeable=clean at f773ea6 — **Mte90 replied 2026-10-02 08:47 (issue #33): "I think that we can proceed" — scope decision resolved in our favor (v2 port as-is; v1 untouched on master)**. PR body rewritten 2026-10-02, STALE vs f773ea6 (refresh draft at `/tmp/opencode/drafts/pr37_body_numbers_refresh.md` — review-before-send). Awaiting maintainer review/merge — 0 new Mte90 reviews as of 2026-10-04. Earlier: 2026-10-01 single-PR scope ask; valentimarco closed his own PR #20 unmerged 2026-09-29 (credit stays with #37) |
| `local/v1-revert-watch` | [`939d232`](https://github.com/famewolf/opencode-auto-resume/commit/939d232) | 2026-10-01 | v1: drop a session's watch state when a revert arrives — v1 has no revert-named event; a rewind arrives as `session.updated` with `properties.info.revert` (verified live on v1.18.34: 79 events, zero revert-named). Single commit on upstream `0c9bc06`. | [Mte90/opencode-auto-resume#39](https://github.com/Mte90/opencode-auto-resume/issues/39) (issue, full patch inlined) → [Mte90/opencode-auto-resume#40](https://github.com/Mte90/opencode-auto-resume/pull/40) (PR) | **Mte90 replied 2026-10-02 08:47: "I need a PR :-)" → PR #40 OPENED 2026-10-02 (head 939d232, base master; 0 comments as of 2026-10-04). Awaiting review/merge.** |

Commits on `pr20-v2port` (newest first):

| Commit | Date | Change |
|---|---|---|
| `f773ea6` | 2026-10-03 | docs: recommend opencode-todo-fork as the confirmed todo plugin |
| `ef25e39` | 2026-10-03 | test: gate back-to-back idles on observed nudge, not 10ms hope |
| `5f3fb0a` | 2026-10-03 | docs: sync todo storage section to namespaced reality, 780 count |
| `a355db3` | 2026-10-03 | docs: say why the todo parser is a copy and not an import |
| `801e22e` | 2026-10-03 | docs: correct why the storage fallback cannot be promoted |
| `a83e158` | 2026-10-03 | fix(v2): read todos from the session message log, not the dead storage key |
| `805aca4` | 2026-10-01 | Drop the session.reverted case: v1 never emitted it |
| `263a8e8` | 2026-10-01 | docs(v2): the install guide was describing a plugin this is not |
| `d890f6c` | 2026-10-01 | Merge `upstream/master` into the v2 port (base `0c9bc06`) |
| `537b2d3` | 2026-10-01 | feat(v2): judge a finished turn once its text has settled, not the instant it ends |
| `3c15386` | 2026-10-01 | feat(v2): recover a parent left waiting on a subagent that will not answer |
| `516c40f` | 2026-10-01 | feat(v2): name a replacement when a model calls a tool that does not exist |
| `7d7c8c3` | 2026-10-01 | feat(v2): offer the model an explicit way to say it is finished |
| `16fdc92` | 2026-10-01 | feat(v2): read the todo list, and stop trusting the emoji on its own |
| `887ae94` | 2026-10-01 | feat(v2): ask for the tool call when the model writes one in its reasoning |
| `d301bd2` | 2026-10-01 | feat(v2): catch the stream that finished without saying anything |
| `f93dfa1` | 2026-10-01 | feat(v2): read the token window and route saturated sessions like v1 does |
| `e61dfec` | 2026-10-01 | feat(v2): catch the premature stop, and make activeUserWindowMs real |
| `c871c29` | 2026-10-01 | feat(v2): sweep sessions on startup, and give the plugin a log file at all |
| `7135c46` | 2026-10-01 | feat(v2): read every v1 option, warn on unknown keys, and complete busyStallStrategy |
| `0c9bc06` | 2026-10-01 | UPSTREAM — fix(bump): ready (rebase base; package.json bump prep, no functional change) |
| `49957b2` | 2026-09-30 | UPSTREAM — Raise default chunk timeout to 180s (implements our issue #38, now closed upstream) |
| `e1b8374` | 2026-09-29 | UPSTREAM — Fix todoNudgeAttempts burning retries on failed sends |
| `8ef7053` | 2026-09-28 | UPSTREAM — perf(tests): cut toolext runtime from 104s to 23s |
| `48d4541` | 2026-09-28 | UPSTREAM — Merge PR #36 from famewolf/fix/recovery-counter-reset — *our contribution* |
| `9af63fb` | 2026-09-26 | UPSTREAM — Stop the recovery-continue infinite loop — *our contribution* |

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
| `abfb2e2` | Daniele Scasciafratte | 2026-10-05 | Merge pull request #40 from famewolf/local/v1-revert-watch — *our contribution* |
| `0c9bc06` | Daniele Scasciafratte | 2026-10-01 | fix(bump): ready — package.json version-bump prep (no functional change; latest release still 1.1.20) |
| `49957b2` | Daniele Scasciafratte | 2026-09-30 | Raise default chunk timeout 45s→180s — implements our issue #38 (now closed upstream) |
| `e1b8374` | Daniele Scasciafratte | 2026-09-29 | Fix todoNudgeAttempts burning retries on failed sends |
| `8ef7053` | Daniele Scasciafratte | 2026-09-28 | perf(tests): cut toolext runtime from 104s to 23s |
| `48d4541` | Daniele Scasciafratte | 2026-09-28 | Merge pull request #36 from famewolf/fix/recovery-counter-reset — *our contribution* |
| `9af63fb` | famewolf | 2026-09-26 | Stop the recovery-continue infinite loop — *our contribution* |
| `02b2e01` | Daniele Scasciafratte | 2026-09-23 | fix(esc): and other stuff |
| `6f4a5af` | Daniele Scasciafratte | 2026-09-23 | Merge PR #34 from famewolf/fix/recovery-continue-loop — *our contribution* |
| `e0d6a27` | famewolf | 2026-09-22 | fix(recovery): stop the infinite "continue" loop when the model server is down — *our contribution* |
| `442f0df` | Daniele Scasciafratte | 2026-09-21 | fix(abort): #32 |
| `f47b5b6` | Daniele Scasciafratte | 2026-09-21 | Fix open-todos reminder not firing when w.todos is empty |
| `a546b75` | Daniele Scasciafratte | 2026-09-21 | Merge PR #31 from famewolf/block-nudge-input-gate — *our contribution* |

*Rows marked "our contribution" were authored by famewolf and merged into upstream; all other rows are upstream authors' work — not fork changes.*

## Notes

- Default branch `master` is functionally in sync with upstream `master` (its local commits were merged upstream as PRs #29/#30/#31/#34/#36; hash-level ahead/behind may show small deltas because of merge style).
- 2026-09-30: upstream implemented our issue #38 directly (`49957b2` — 180s default chunk timeout; #38 closed, no PR needed). valentimarco closed his own PR #20 unmerged (credit stays with #37).
- 2026-10-01: upstream master 49957b2→0c9bc06 (package.json bump prep, no functional change; latest release still 1.1.20). Mte90 answered issue #33 (2026-10-01): single-PR scope — full v2+v1 compat, all options supported. PR #37 still open, mergeable, 0 new PR comments.
- 2026-10-02: `pr20-v2port` head 4855d18→805aca4 (rebased onto upstream `0c9bc06`, force-pushed; PR body rewritten, mergeable=clean). Mte90 2026-10-02 08:47 on #33: "I think that we can proceed" — scope resolved in our favor. New branch `local/v1-revert-watch` @939d232 → issue #39; Mte90: "I need a PR :-)" (PR #40 opened 2026-10-02 after approval). Upstream master unchanged at `0c9bc06` (no v1 porting work in the 10-01→10-02 window).
- 2026-10-03: `pr20-v2port` head 805aca4→a355db3 (3 new commits pushed: `a83e158` fix(v2) read todos from session message log; `801e22e` docs; `a355db3` docs). PR #37 still OPEN, not merged. Upstream master unchanged at `0c9bc06`.
- 2026-10-04: `pr20-v2port` head a355db3→f773ea6 (3 commits pushed 2026-10-03 after the 9am run: `5f3fb0a` docs, `ef25e39` flake-test, `f773ea6` docs; gitea in sync at f773ea6). PR #37 OPEN, mergeable=clean, 0 new Mte90 reviews; PR #40 OPEN, 0 comments. Upstream master unchanged at `0c9bc06` (no v1 porting work). Latest release still 1.1.20.
- 2026-10-05: **PR #40 (v1 revert-watch fix, head 939d232) MERGED into master by Mte90 10-05T07:43** (merge abfb2e2, 0 review comments); issue #39 closed. **Mte90 closed third-party PR #41 (scienceguy v2 entry) in favor of our PR #37** — "we are focusing on #37" (positive momentum). `pr20-v2port` head unchanged at f773ea6 (0 new Mte90 reviews).
- A canonical copy of this changelog is kept by the fork owner (`memory/fork-changelogs/famewolf__opencode-auto-resume.md`) so the record survives a destructive fork reset; the sync job restores it if a sync removes it from the fork.
