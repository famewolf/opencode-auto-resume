# Changelog — fork history (ours + upstream)

This fork of [Mte90/opencode-auto-resume](https://github.com/Mte90/opencode-auto-resume) carries local changes that are not (yet) in upstream.

**Attribution key: [US] = authored by the fork owner (famewolf); [UPSTREAM] = authored by the upstream project (Daniele Scasciafratte / Mte90).**

This file is kept current automatically: the fork owner's daily upstream-sync job regenerates it from each branch's `git log upstream/master..<branch>` (our changes) plus the recent upstream `master` history, so it stays accurate even after a rebase or sync from upstream.

> **Last sync 2026-10-13:** PR #37 head `5d7560c` (1.2.0 bump pushed; +76 commits since c480fa5, all owner-side). Upstream `master` UNMOVED at `29cfd3d` (no new v1 — no ports). Rebase N/A for #37 (separate v2 module; the 5 post-base commits: 2 ours + stopPatterns ALREADY-COVERED + merge + package.json bump).

## Our changes — not yet in upstream [US]

| Branch | Head | Date | Change | Submitted as | Status (2026-10-13) | Retire-when |
|---|---|---|---|---|---|---|
| `pr20-v2port` | [`5d7560c`](https://github.com/famewolf/opencode-auto-resume/commit/5d7560c) | 2026-10-13 | OpenCode v2 port (self-contained `src/v2/` module + docs; base `0c9bc06`). Rebased onto upstream `0c9bc06` 2026-10-01; 1.2.0 version bump for release (Mte90 #45). | [Mte90/opencode-auto-resume#37](https://github.com/Mte90/opencode-auto-resume/pull/37) | OPEN, mergeable=dirty (cosmetic — separate module, rebase N/A). Mte90 #45 ask satisfied (guardrail already in branch; bump pushed) — awaiting merge | Merged upstream → repoint config to upstream release + archive fork, remove row |

Commits on `pr20-v2port` since `upstream/master` (newest first):

| Commit | Date | Change |
|---|---|---|
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
| `17135a8` | 2026-10-11 | chore(v2): log session.idle event data keys (turn-identity probe) |
| `604b26f` | 2026-10-11 | test(v2): give the quota-drop poll room under full-suite load |
| `82354a9` | 2026-10-11 | fix(v2): shells get their own stall-path young TTL (10 min) |
| `f255fbd` | 2026-10-11 | revert(v2): remove stall→stuck delegation that false-positives on live long calls |
| `0ec74ef` | 2026-10-11 | fix(v2): scope the stop-statement connective guard to the final clause |
| `a08b674` | 2026-10-11 | stall: send the stuck prompt when a stall parks on a wedged tool |
| `7866b7d` | 2026-10-11 | fix(v2): latch completion claims before activity stand-down; clear latch only on genuine new wo |
| `000e567` | 2026-10-11 | fix(v2): stall ladder defers on unfinished work in history, not just events |
| `3484d16` | 2026-10-11 | test(v2): annotate guardrail-wire test callback (fixes tsc implicit-any) |
| `1d0b214` | 2026-10-11 | fix(v2): every synthetic continue carries the no-destructive / no-new-work guardrail |
| `50f5001` | 2026-10-11 | test(v2): behavioural coverage for the stall watchdog's shell guard |
| `3b8cecc` | 2026-10-11 | fix(v2): orphan watch yields to a fresh user message; one dead child, one abort |
| `ce6f7e1` | 2026-10-11 | fix(v2): watchdog re-checks stuck tools; stop vocabulary covers real phrasings |
| `cab79d6` | 2026-10-11 | feat(v2): busy stall defers while young tools run; compress never interrupted |
| `408ffec` | 2026-10-11 | feat(v2): one instant nudge for turns that end with nothing delivered |
| `bdb6f58` | 2026-10-11 | fix(v2): a stale server listing must defer the dead-stream recovery, not bury it |
| `f4fdc3a` | 2026-10-11 | fix(v2): stop the process-global registry from silencing other instances |
| `8730116` | 2026-10-11 | test: size poll budgets for the parallel suite, not for isolation |
| `4c664b9` | 2026-10-11 | test: bound each fuse rung against its own nominal, not the previous gap |
| `21eaa07` | 2026-10-10 | test: replace fixed sleeps with condition polls in two more flaky tests |
| `a142c00` | 2026-10-10 | test: fix the two load-flaky tests at their root causes |
| `eda3522` | 2026-10-10 | v2: clear gaveUp only on observable new episodes, never in markBusy |
| `c6ceb0f` | 2026-10-10 | v2: extract shared serveQuotaRung for quota cooldown serving |
| `0d8c098` | 2026-10-10 | test: fix the two causes of suite flakiness under parallel load |
| `b059ad9` | 2026-10-10 | v2: persist the quota ladder to storage, not the log file |
| `e9b257c` | 2026-10-10 | v2: read history roles through shared accessors (prod sends role, not type) |
| `10e589d` | 2026-10-10 | v2: visible quota notices (arm + exhausted), resume:false |
| `ea48be6` | 2026-10-10 | v2: pull 503 slot-busy ladder; 503s are generic failures (SelfRef #5) |
| `d61ca62` | 2026-10-10 | v2: log every ladder reset (kill silent branches) |
| `3e32862` | 2026-10-10 | v2: read flat-text history shapes (prod transcripts carry text, not parts) |
| `bf1a491` | 2026-10-10 | v2: back off refire fuse across one episode (endless 1/3 fix) |
| `3d9282c` | 2026-10-10 | v2: offer hand-off on busy path; scoped stall text; local timestamps |
| `9861ef8` | 2026-10-10 | v2: cover prod-shaped (role) history in latch and recheck tests |
| `964a5cd` | 2026-10-10 | v2: latch bare TASK COMPLETE; recheck idle stand-down at window expiry |
| `5527471` | 2026-10-09 | v2: share watch state across setups behind shareWatchState flag |
| `af99fde` | 2026-10-09 | v2: latch bare TASK COMPLETE like a stop statement |
| `4c2fbf0` | 2026-10-09 | v2: nudge reasoning-only turns that produced nothing |
| `ba6207d` | 2026-10-09 | v2: stall ladder restarts on silence+success progress; 503 slot-busy takes cooldown ladder |
| `532c351` | 2026-10-09 | v2: ladder resets only on observable new episodes, never on transitions |
| `5cf5aed` | 2026-10-09 | v2: failure loops stand down instead of cycling forever |
| `b94b5d6` | 2026-10-09 | v2: failure stalls carry no idle field |
| `b7c4f03` | 2026-10-09 | v2: quietCorrections option; silence order rides in the text |
| `24e85dc` | 2026-10-09 | v2: state each stall fact once in the continue text |
| `b74137a` | 2026-10-09 | v2: watchdog reads server truth when the active surface is missing |
| `aa6a947` | 2026-10-09 | v2: never retry policy-blocked tool calls |
| `4ddac7c` | 2026-10-09 | v2: unknown-tool suggestion goes synthetic, not visible |
| `f84c052` | 2026-10-09 | v2: retry trailing tool errors; ladder resets on text only |
| `c92a9ad` | 2026-10-09 | v2: stuck-tool age gate 60s, not the stall window |
| `6062ee2` | 2026-10-09 | v2: nudge turns parked on a tool result that never arrives |
| `203b178` | 2026-10-09 | v2: centralize lock guards; fix review findings |
| `7463d09` | 2026-10-09 | v2: the stall ladder never climbed, and the stall text had no time |
| `f79af79` | 2026-10-09 | v2: provider.unknown is indeterminate, not permanent |
| `7f1e672` | 2026-10-08 | v2: indeterminate failures get one retry, not a first-occurrence gate |
| `8a8c224` | 2026-10-08 | v2: drop the shell-alias annotation — it changed nothing |
| `24f77fc` | 2026-10-08 | fix: shell alias dedupe must be process-wide, not module-scope |
| `e8e3df8` | 2026-10-08 | fix: the shell alias hint grew by one copy per reload |
| `985702d` | 2026-10-08 | fix: two mod= stamps were not stamping anything |
| `c353d5d` | 2026-10-08 | test: attempt-reset writes to its own log file |
| `cb57a4a` | 2026-10-08 | v2: reload forensics, and the closest available bash->shell fix |
| `aefec42` | 2026-10-08 | v2: enforce the locks at the injection choke point, not two of five paths |
| `cdf9bee` | 2026-10-08 | v2: gate the whole permanent-failure class from opencode's own taxonomy |
| `7bf1329` | 2026-10-08 | v2: permanent-failure latch stops continues into a dead model |
| `c480fa5` | 2026-10-07 | v2: model progress between stalls restarts the attempt ladder |
| `a1ab24c` | 2026-10-07 | v2: silent tool completions defeat the exact-duplicate skip |
| `a6281b2` | 2026-10-07 | v2: bound recovery sends so wedged transports cannot stack twins |
| `a929581` | 2026-10-07 | v2: explicit stop statements latch completion; stall respects the latch |
| `4eeaed8` | 2026-10-07 | v2: genuine user message re-arms after user interrupt (timestamp-gated) |
| `22d8f28` | 2026-10-06 | v2: dead instances send nothing (liveness checks on every send path) |
| `511d64d` | 2026-10-06 | test: parent-wait CONTROL drops the child link entirely |
| `5f85adb` | 2026-10-06 | v2: quiet subagents wait inside a patience window; orphan aborts terminate |
| `0c07d32` | 2026-10-06 | v2: verify delivery before fallback sends (no twin prods) |
| `43246e6` | 2026-10-06 | v2: subagent protection without ctx.client + cancel stall timers on dispose |
| `3c7ce7f` | 2026-10-05 | v2: busy-stall stands down while a turn waits on the user |
| `7cc0714` | 2026-10-05 | v2: inert configProbe option — proves plugins[].options delivery without touching a live knob |
| `27add46` | 2026-10-05 | docs: refresh v2 suite figures and feature list in migration.md |
| `e89bd0b` | 2026-10-05 | docs: v1 backport research (rich text, dup guard, startup log, silent stub) |
| `963a9fd` | 2026-10-05 | docs: dead-stream tool-call exception, plugins-vs-plugin delivery |
| `a9f2425` | 2026-10-05 | test: keep test sessions out of the LIVE auto-resume log |
| `0497165` | 2026-10-05 | test: stand-down CONTROL follows visible-default channel |
| `3df2339` | 2026-10-05 | v2: visibleContinue defaults true (config options dropped by parser) |
| `90113a7` | 2026-10-05 | v2: AUTO_RESUME_VISIBLE_CONTINUE env fallback + startup line reports channel |
| `67437d8` | 2026-10-05 | v2: visible stall continue + rich prod text + duplicate anti-repeat |
| `a38d681` | 2026-10-05 | test: drop the module-scope assertion superseded by the globalThis registry |
| `c36c560` | 2026-10-05 | v2: skip busy-stall recovery while a parent waits on live subagents |
| `05838f7` | 2026-10-05 | v2: re-arm keeps examined parts — stale errors never re-suggest |
| `0fef903` | 2026-10-05 | v2: own-prompt re-arm exclusion survives null-body projections via inject recency |
| `333a4e1` | 2026-10-05 | v2: quota failures stand down on a gate ladder instead of retrying into the ban |
| `7fdc472` | 2026-10-05 | v2: own prompts don't re-arm budgets; bash->shell alias before fuzzy match |
| `8a34aa5` | 2026-10-05 | v2: thinking/tool-call turns are alive — dead-stream detector no longer fires into active work |
| `4ccbf80` | 2026-10-05 | v2: put the singleton on globalThis — module scope cannot see re-evaluations |
| `7fb1b9f` | 2026-10-05 | v2: one live instance per process, and a per-session inject mutex |
| `2052c07` | 2026-10-05 | v2: cross-instance duplicate check via session log |
| `f773ea6` | 2026-10-03 | docs: recommend opencode-todo-fork as the confirmed todo plugin |
| `ef25e39` | 2026-10-03 | test: gate back-to-back idles on observed nudge, not 10ms hope |
| `5f3fb0a` | 2026-10-03 | docs: sync todo storage section to namespaced reality, 780 count |
| `a355db3` | 2026-10-03 | docs: say why the todo parser is a copy and not an import |
| `801e22e` | 2026-10-03 | docs: correct why the storage fallback cannot be promoted |
| `a83e158` | 2026-10-03 | fix(v2): read todos from the session message log, not the dead storage key |
| `805aca4` | 2026-10-01 | Drop the session.reverted case: v1 never emitted it |
| `263a8e8` | 2026-10-01 | docs(v2): the install guide was describing a plugin this is not |
| `d890f6c` | 2026-10-01 | Merge upstream/master into the v2 port |
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
| `4855d18` | 2026-09-29 | fix(v2): handle the session.revert.* family so a rewind drops watch state |
| `67c34ff` | 2026-09-29 | fix(v2): stand down when a question or permission is awaiting the user |
| `875d7e4` | 2026-09-28 | fix(v2): stop self-inflicted "Step interrupted" and synthetic-continue bursts |
| `3c1d88c` | 2026-09-27 | v2 back-port: shouldStandDownForUser guard (v1 parity) - stand down on a pending tool_use/quest |
| `0dd0403` | 2026-09-27 | fix(v2): never nudge a turn that hands off to the user |
| `9a44699` | 2026-09-27 | v2: never interrupt compaction or live busy sessions |
| `0a0a961` | 2026-09-26 | OOC lock (parity with v1 loop-fix) |
| `5491286` | 2026-09-24 | Merge remote-tracking branch 'upstream/master' into pr20-v2port |
| `b5fd8aa` | 2026-09-17 | docs(v2): document @opencode/plugin resolution requirement |
| `aa89252` | 2026-09-17 | docs(v2): add install guide and stable migration notes |
| `ad92b39` | 2026-09-17 | feat(v2): target stable @opencode/plugin 2.0.5 API |
| `5e04ade` | 2026-08-26 | feat(plugin): show visible notification when recovering from stall/failure |
| `7511aea` | 2026-08-25 | feat(plugin): add opencode v2 port with event-driven architecture |

## Our changes — merged into upstream [US]

| PR | Merged upstream as | Date | Change |
|---|---|---|---|
| [Mte90/opencode-auto-resume#29](https://github.com/Mte90/opencode-auto-resume/pull/29) | `88bbd87` | 2026-09-17 | block-site invisible tool result fix (open-todos) — in release 1.1.17 |
| [Mte90/opencode-auto-resume#30](https://github.com/Mte90/opencode-auto-resume/pull/30) | `3c8767f` (head `60075d9`) | 2026-09-18 | task-complete repeat-guard — in release 1.1.18 |
| [Mte90/opencode-auto-resume#31](https://github.com/Mte90/opencode-auto-resume/pull/31) | `a546b75` (head `a26a62b`) | 2026-09-21 | block-nudge input gate — in release 1.1.18 |
| [Mte90/opencode-auto-resume#34](https://github.com/Mte90/opencode-auto-resume/pull/34) | `6f4a5af` (head `e0d6a27`) | 2026-09-23 | stop the infinite "continue" loop when the model server is down — in release 1.1.19 |
| [Mte90/opencode-auto-resume#36](https://github.com/Mte90/opencode-auto-resume/pull/36) | `48d4541` (head `9af63fb`) | 2026-09-28 | stop the recovery-continue infinite loop (counter reset + `gaveUp` choke-point guard) — in release 1.1.20 |
| [Mte90/opencode-auto-resume#40](https://github.com/Mte90/opencode-auto-resume/pull/40) | `abfb2e2` (head `939d232`) | 2026-10-05 | drop watch state on a revert (v1) — merged by Mte90 10-05T07:43 (0 review comments); issue #39 closed |

## Upstream activity — recent `master` history [UPSTREAM]

| Commit | Author | Date | Change |
|---|---|---|---|
| `29cfd3d` | Daniele | Scasciafratte | 2026-10-08 Update package.json |
| `8ac6a83` | Daniele | Scasciafratte | 2026-10-08 Merge pull request #43 from ChakraFusion/feat/stop-patterns |
| `5d5bcf2` | ChakraFusion | 2026-10-08 | feat: stopPatterns option — explicit stop lines count as awaiting the user |
| `abfb2e2` | Daniele | Scasciafratte | 2026-10-05 Merge pull request #40 from famewolf/local/v1-revert-watch — *our contribution* |
| `939d232` | famewolf | 2026-10-01 | Drop watch state on a revert: v1 has no revert-named event — *our contribution* |
| `0c9bc06` | Daniele | Scasciafratte | 2026-10-01 fix(bump): ready ♬ Parov Stelar - Clap Your Hands |
| `49957b2` | Daniele | Scasciafratte | 2026-09-30 Raise default chunk timeout to 180s so healthy slow generations are not interrupted |
| `e1b8374` | Daniele | Scasciafratte | 2026-09-29 Fix todoNudgeAttempts burning retries on failed sends |
| `8ef7053` | Daniele | Scasciafratte | 2026-09-28 perf(tests): cut toolext runtime from 104s to 23s |
| `48d4541` | Daniele | Scasciafratte | 2026-09-28 Merge pull request #36 from famewolf/fix/recovery-counter-reset — *our contribution* |
| `9af63fb` | famewolf | 2026-09-26 | Stop the recovery-continue infinite loop — *our contribution* |
| `02b2e01` | Daniele | Scasciafratte | 2026-09-23 fix(esc): and other stuff |

*Rows marked "our contribution" were authored by famewolf and merged into upstream; all other rows are upstream authors' work — not fork changes.*

## Notes

- Default branch `master` is functionally in sync with upstream `master` (its local commits were merged upstream as PRs #29/#30/#31/#34/#36; hash-level ahead/behind may show small deltas because of merge style).
- 2026-09-30: upstream implemented our issue #38 directly (`49957b2` — 180s default chunk timeout; #38 closed, no PR needed). valentimarco closed his own PR #20 unmerged (credit stays with #37).
- 2026-10-01: upstream master 49957b2→0c9bc06 (package.json bump prep, no functional change; latest release still 1.1.20). Mte90 answered issue #33 (2026-10-01): single-PR scope — full v2+v1 compat, all options supported. PR #37 still open, mergeable, 0 new PR comments.
- 2026-10-02: `pr20-v2port` head 4855d18→805aca4 (rebased onto upstream `0c9bc06`, force-pushed; PR body rewritten, mergeable=clean). Mte90 2026-10-02 08:47 on #33: "I think that we can proceed" — scope resolved in our favor. New branch `local/v1-revert-watch` @939d232 → issue #39; Mte90: "I need a PR :-)" (PR #40 opened 2026-10-02 after approval). Upstream master unchanged at `0c9bc06` (no v1 porting work in the 10-01→10-02 window).
- 2026-10-03: `pr20-v2port` head 805aca4→a355db3 (3 new commits pushed: `a83e158` fix(v2) read todos from session message log; `801e22e` docs; `a355db3` docs). PR #37 still OPEN, not merged. Upstream master unchanged at `0c9bc06`.
- 2026-10-04: `pr20-v2port` head a355db3→f773ea6 (3 commits pushed 2026-10-03 after the 9am run: `5f3fb0a` docs, `ef25e39` flake-test, `f773ea6` docs; gitea in sync at f773ea6). PR #37 OPEN, mergeable=clean, 0 new Mte90 reviews; PR #40 OPEN, 0 comments. Upstream master unchanged at `0c9bc06` (no v1 porting work). Latest release still 1.1.20.
- 2026-10-05: **PR #40 (v1 revert-watch fix, head 939d232) MERGED into master by Mte90 10-05T07:43** (merge abfb2e2, 0 review comments); issue #39 closed. **Mte90 closed third-party PR #41 (scienceguy v2 entry) in favor of our PR #37** — "we are focusing on #37" (positive momentum). `pr20-v2port` head unchanged at f773ea6 (0 new Mte90 reviews).
- 2026-10-07: `pr20-v2port` head 3c7ce7f→4eeaed8 (6 commits pushed to PR #37 — verified PR head 4eeaed8; github+gitea in sync; stray `auto-resume-pr20-v2port` branch on origin deleted. `43246e6` subagent protection w/o ctx.client + cancel stall timers on dispose; `0c07d32` verify delivery before fallback (no twin prods); `5f85adb` quiet-subagent patience window, orphan aborts terminate; `511d64d` test parent-wait CONTROL; `22d8f28` dead instances send nothing (liveness on every send path); `4eeaed8` genuine user message re-arms after interrupt (timestamp-gated); +1053/-25, src/v2 only). Verified: 31/31 pass across the 6 touched test files (delivery-once, user-rearm, subagent-patience, child-guard, parent-wait, orphan) + `tsc --noEmit` clean. NOTE: full `bun test` exceeds 300s in this checkout (per-file runs fine) — recorded, not yet root-caused.
- A canonical copy of this changelog is kept by the fork owner (`memory/fork-changelogs/famewolf__opencode-auto-resume.md`) so the record survives a destructive fork reset; the sync job restores it if a sync removes it from the fork.
- 2026-10-13: `pr20-v2port` head 1d0f7b5→b099abf→5d7560c (owner-side: AGENTS-snippet doc, stall-clock token-flow fix, boundary-marker strip, 1.2.0 bump — all pushed, PR head live). Upstream master UNMOVED `29cfd3d`. Rebase stance revoked (separate module). Mte90 #45: guardrail already in branch, bump pushed; reply drafted, unposted.
