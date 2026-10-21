# Changelog — fork history (ours + upstream)

This fork of [Mte90/opencode-auto-resume](https://github.com/Mte90/opencode-auto-resume) carries local changes that are not (yet) in upstream.

**Attribution key: [US] = authored by the fork owner (famewolf); [UPSTREAM] = authored by the upstream project (Daniele Scasciafratte / Mte90).**

This file is kept current automatically: the fork owner's daily upstream-sync job regenerates it from each branch's `git log upstream/master..<branch>` (our changes) plus the recent upstream `master` history, so it stays accurate even after a rebase or sync from upstream.

## Our changes — not yet in upstream [US]

| Branch | Head | Date | Change | Submitted as | Status (2026-10-21) |
|---|---|---|---|---|---|
| `pr20-v2port` | [`1bc7652`](https://github.com/famewolf/opencode-auto-resume/commit/1bc7652) | 2026-10-19 | OpenCode v2 port (155 commits ahead of upstream/master — newest 30 listed below; the v1 loop-fix #36 was merged upstream separately and is no longer carried here). The port lives in a self-contained v2 module. Owner-side fixes landed 2026-10-14 (`75ea298`, `4b633ea`), 2026-10-15 (6 commits incl. `1667832` = merge of upstream master + `b27cda5` test fix) and 2026-10-16..10-19 (6 more: `f98eb28`, `6419444`, `a0b51d9` + its revert `7394c79`, `cf1a395`, `1bc7652`). | [Mte90/opencode-auto-resume#37](https://github.com/Mte90/opencode-auto-resume/pull/37) | **OPEN, mergeable=CLEAN (2026-10-21)** — head `1bc7652` (pushed 10-20: the PR head and gitea `pr20-v2port` are both `1bc7652`), 155 ahead; base `29cfd3d` = current master; 11 comments, last = our 10-15 19:05 test-fix follow-up — no new maintainer reply. NEW third-party PR #47 (San4es, 2026-10-21) 'Support OpenCode 2 plugin API (dual-shape default export)' — a thin compat shim (`src/v2.ts` + synthesized `@opencode/client`) against our full `src/v2/index.ts` port; ours is the deeper implementation, no action taken. Mte90 issue #45 (2026-10-13): fold the guardrail into #37 + bump to 1.2 — satisfied (bump `5d7560c` pushed, reply posted 2026-10-13); he merges + releases 1.2 when #37 merges. Mte90 filed issue #46 2026-10-14 (provider rate-limit misclassified as OOC — our `75ea298` fixes the class; cross-ref draft pending approval). Earlier: 2026-10-02 Mte90 "we can proceed" (issue #33); valentimarco closed his own PR #20 unmerged 2026-09-29 (credit stays with #37). |
| `local/v1-revert-watch` | [`939d232`](https://github.com/famewolf/opencode-auto-resume/commit/939d232) | 2026-10-01 | v1: drop a session's watch state when a revert arrives — v1 has no revert-named event; a rewind arrives as `session.updated` with `properties.info.revert` (verified live on v1.18.34: 79 events, zero revert-named). Single commit on upstream `0c9bc06`. | [Mte90/opencode-auto-resume#39](https://github.com/Mte90/opencode-auto-resume/issues/39) (issue, full patch inlined) | **Mte90 replied 2026-10-02 08:47: "I need a PR :-)" — PR draft ready (title+body, UNSSENT, awaiting approval)** |

Commits on `pr20-v2port` (newest first):

| Commit | Date | Change |
|---|---|---|
| `1bc7652` | 2026-10-19 | v2: consume a stall rung only when the continue prompt is delivered |
| `cf1a395` | 2026-10-18 | auto-resume: do not skip stall detection when subagent parentID is undiscoverable |
| `7394c79` | 2026-10-17 | Revert "feat(v2): efficiency pass + bounded stall-ladder restarts" |
| `a0b51d9` | 2026-10-17 | feat(v2): efficiency pass + bounded stall-ladder restarts |
| `6419444` | 2026-10-17 | fix(v2): broaden STOP_STATEMENT_PATTERNS with completion/blocked vocabulary from Aider, OpenHands, Cline, SWE-agent |
| `f98eb28` | 2026-10-16 | fix(v2): add waiting-for-user-input stop states to STOP_STATEMENT_PATTERNS |
| `618ca42` | 2026-10-15 | docs: confirmed todo pairing is upstream opencode-todolist (fork retired) |
| `b27cda5` | 2026-10-15 | test(v2): derace the silent-tool re-arm test |
| `1667832` | 2026-10-15 | merge upstream master (stopPatterns #43, revert-watch #40, package 1.1.21) into PR37 |
| `66b7ffe` | 2026-10-15 | docs: compat floor, updating, uninstall (no release bundle yet) |
| `5b349b0` | 2026-10-15 | feat(v2): standby/ready completion stops + done-claim consolidation + TASK COMPLETE case discipline |
| `bc7d71f` | 2026-10-15 | docs: harden AGENTS snippet completion rule (exact bytes, v2 note, why) |
| `4b633ea` | 2026-10-14 | feat(v2): lifetime cap on stall continues (lifetimeMaxContinues, default 9) |
| `75ea298` | 2026-10-14 | fix(v2): throttle phrasing never latches OOC (upstream issue #46) |
| `f3b8ae9` | 2026-10-13 | docs: move Installation to top of README |
| `5d7560c` | 2026-10-13 | chore: bump to 1.2.0 for v2-port release (Mte90 #45) |
| `b099abf` | 2026-10-13 | fix(v2): strip trailing @N@ boundary markers before completion tests |
| `7746cc0` | 2026-10-13 | fix(v2): token flow resets the stall clock only when usage grows |
| `07cc2c8` | 2026-10-13 | docs: ship a bare-bones AGENTS snippet with the plugin |
| `1d0f7b5` | 2026-10-13 | docs: accuracy pass — version marks, v2 architecture, completion docs |
| `bf7b341` | 2026-10-13 | fix(v2): celebration latch is last-line only, not anywhere-in-tail |
| `001c642` | 2026-10-12 | fix(v2): celebration emoji latches anywhere in the tail, not just trailing |
| `8e42951` | 2026-10-12 | docs: add Todo list nudges section (upstream todolist link, nudge example) |
| `99a8ab4` | 2026-10-12 | fix(v2): migrate watches adopted from older builds; never throw on missing map |
| `d63440c` | 2026-10-12 | feat(v2): retry count restarts on genuine turns, ladder untouched |
| `4fca944` | 2026-10-12 | fix(v2): retry number counts recoveries, not progress restarts |
| `313fa36` | 2026-10-12 | fix(v2): user-takeover park uses >= so same-sweep messages count |
| `184607b` | 2026-10-12 | feat(v2): stall text carries the episode retry number |
| `2637ff2` | 2026-10-12 | fix(v2): clamp genuine-user timestamps to the present at ingestion |
| `5193461` | 2026-10-12 | fix(v2): park a scheduled recovery when the user speaks mid-backoff |
| *(…119 more earlier commits on `pr20-v2port` — full list: `git log upstream/master..origin/pr20-v2port` in the fork)* | | |
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
| `29cfd3d` | Daniele Scasciafratte | 2026-10-08 | Update package.json |
| `5d5bcf2` | Daniele Scasciafratte | 2026-10-08 | feat: stopPatterns option — explicit stop lines count as awaiting the user |
| `939d232` | famewolf | 2026-10-01 | Drop watch state on a revert: v1 has no revert-named event |
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
- 2026-10-13: rebase stance REVOKED — the v2 port is a self-contained module on base `0c9bc06`; mergeable=dirty vs upstream `29cfd3d` is cosmetic, no rebase planned. Mte90 issue #45 (fold guardrail into #37 + bump to 1.2) answered the same day (bump `5d7560c` pushed, reply posted); awaiting his merge + 1.2 release. PR #37 head `f3b8ae9`.
- 2026-10-14: two owner-side commits on `pr20-v2port`: `75ea298` fix(v2) throttle phrasing never latches OOC (upstream issue #46) and `4b633ea` feat(v2) lifetime cap on stall continues (`lifetimeMaxContinues`, default 9) — head `4b633ea`. Mte90 filed issue #46 10-14 11:06 (provider rate-limit text misclassified as context overflow, recovery permanently halted; our `75ea298` fixes the class — cross-ref draft pending approval). openchamber PR #4582 (inline-chat visibility) merged 2026-10-13.
- 2026-10-15 (9am sync): upstream master `29cfd3d` UNMOVED. PR #37 OPEN/dirty, head `4b633ea`, 10 comments. Issues #45 (open, awaiting merge+release) and #46 (open, 0 comments) unchanged. No new SelfRef Reverts/removals. Full own-commit table regenerated (136 own commits).
- 2026-10-16 (9am sync): upstream master `29cfd3d` UNMOVED. PR #37 now **mergeable=CLEAN** — 2026-10-15 pushed 6 own commits to `pr20-v2port` (incl. `1667832` = MERGE of upstream master, branch now on current master `29cfd3d`, 149 ahead; `b27cda5` deraced the failing test; head `618ca42`); 11 comments (last = our 10-15 19:05 test-fix follow-up); CI ran 10-15. Awaiting Mte90 merge + 1.2.0 release. Full own-commit table regenerated (149 ahead).
- 2026-10-20 (9am sync): upstream master `29cfd3d` UNMOVED (0 new; 2026-10-08). PR #37 OPEN CLEAN, head `618ca42`, 11 comments, 0 new; 149 ahead. 0 to port. Fork master `7385f35` UNMOVED. **DRIFT (fail-loud):** local `refs/heads/pr20-v2port` = `1bc7652` (10-19, unpushed WIP from another dev session — NOT part of PR #37; gitea `pr20-v2port` = `a0b51d9`, origin/gitea `pr37-merge-upstream` = `cf1a395`). No push this run; changelog data UNMOVED (no fork commit).
- 2026-10-01: upstream master 49957b2→0c9bc06 (package.json bump prep, no functional change; latest release still 1.1.20). Mte90 answered issue #33 (2026-10-01): single-PR scope — full v2+v1 compat, all options supported. PR #37 still open, mergeable, 0 new PR comments.
- 2026-10-02: `pr20-v2port` head 4855d18→805aca4 (rebased onto upstream `0c9bc06`, force-pushed; PR body rewritten, mergeable=clean). Mte90 2026-10-02 08:47 on #33: "I think that we can proceed" — scope resolved in our favor. New branch `local/v1-revert-watch` @939d232 → issue #39; Mte90: "I need a PR :-)" (draft awaiting approval). Upstream master unchanged at `0c9bc06` (no v1 porting work in the 10-01→10-02 window).
- 2026-10-03: `pr20-v2port` head 805aca4→a355db3 (3 new commits pushed: `a83e158` fix(v2) read todos from session message log; `801e22e` docs; `a355db3` docs). PR #37 still OPEN, not merged. Upstream master unchanged at `0c9bc06`.
- 2026-10-21 (9am sync): upstream master `29cfd3d` UNMOVED (0 new -> 0 v1 ports). PR #37 OPEN, mergeable=CLEAN, head `1bc7652` (pushed 10-20), 155 ahead, base `29cfd3d` = current master, 11 comments, last = our 10-15 19:05 test-fix follow-up — no new maintainer reply. NEW third-party PR #47 (San4es, 2026-10-21) 'Support OpenCode 2 plugin API (dual-shape default export)' — thin compat shim (`src/v2.ts` + synthesized `@opencode/client`), same intent as our full `src/v2/index.ts` port, mergeable_state = unstable; no action taken. Fork master `7385f35` UNMOVED until this changelog commit. Changelog regenerated in-run (section (a) head + 6 new own commits + status; sections (b)/(c) data unchanged — upstream master did not move).
- A canonical copy of this changelog is kept by the fork owner (`memory/fork-changelogs/famewolf__opencode-auto-resume.md`) so the record survives a destructive fork reset; the sync job restores it if a sync removes it from the fork.
