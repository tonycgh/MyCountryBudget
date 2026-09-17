# My Country Budget roadmap

Updated: 17 September 2026

## Direction

Ship a credible, mobile-first multi-country budget simulator that a new visitor can complete in under five minutes. Keep the approved country-comparison layout and the finite **10 decisions. That's it.** overview. No sign-in is needed to play.

This is a deployed prototype. Deployment of the interface does not mean that the fiscal model, AI challenge or community features are finished.

## What is already delivered

- Public website at https://mycountrybudget.com with HTTPS.
- Eleven playable countries: United Kingdom, Canada, United States, Mexico, Germany, France, India, UAE, Saudi Arabia, Italy and Spain.
- Ten-decision overview, open in any order, save and revisit.
- Existing UK pound-based model plus versioned 2025 IMF baselines for new country scenarios, with annual deficit/surplus and per-person results.
- Non-UK controls are explicit revenue/spending targets in % GDP; per-person results use Intl $ PPP. They are not local tax-rate forecasts.
- Country links and separate per-country drafts survive refresh in the current browser tab.
- Optional short explanations and copyable budget summary.
- Both return-to-ten controls and versioned frontend assets.
- Three redundant UK landing callouts removed.
- Public methodology and data definitions; application CI tests.

## Ordered delivery plan

| Priority | Milestone | Work | Completion evidence |
| --- | --- | --- | --- |
| 1 — running | Reliable prototype operations | Dedicated operator runner, automatic tested releases, exact-revision checks, independent backups and phone/desktop browser gates are active. Continue recovery rehearsals. | Successful production workflow, verified backup copy and all-country browser checks; isolated restore/rollback tests pass. |
| 2 | Credible UK model | Replace prototype sensitivities with sourced, versioned assumptions; record reference periods, units and accounting definitions; document uncertainty, timing and excluded effects. Audit international comparisons and their source records. | Each lever has a reviewable source/assumption record, fiscal cross-checks pass, and every saved result identifies its baseline/model version. |
| 3 | Complete anonymous experience | Test phone and keyboard journeys; improve slow/failed calculation handling; extend current tab-local drafts where needed; verify completion and copying/sharing. | A first-time visitor can complete all ten decisions on a phone in under five minutes and recover from refresh/network errors. |
| 4 | AI challenge | Give AI the same baseline, ten controls and constraints; validate its choices and calculate both budgets with the same engine; explain differences. | Human and AI outcomes can be reproduced from their inputs. AI never judges its own answer, and there is no single political winner score. |
| 5 | Community | Add login only at save/publish/vote/fork; persist versioned proposals; support voting on explanations and forks; add reporting/moderation. | Publishing, attribution, voting, forking and moderation work end to end; there are no reply threads. |
| 6 | People's Budget and expansion | Aggregate completed budgets with distributions and participation counts. Expand beyond the eleven playable scenarios; deepen country-specific tax/pension modelling separately. | Aggregates do not award extra weight for popularity. Each new country passes its own data/model and browser checks. |

Priorities describe delivery order, not promised dates. Reliability checks continue throughout.

## Canada — retained for later

Canada is playable as a national GDP-share scenario. A province/territory layer remains deferred: distinguish federal and provincial responsibilities before introducing it.

## Operations activation — 17 September 2026

The first operations milestone now has merged implementation: deployment of a tested revision, a separate Python environment per release, verified pre-deploy database backups, guarded application rollback, nightly backups plus an independent operator copy, and phone/desktop browser release checks.

CI passed the complete ten-decision journey, results/copy/revisit/reset, PostgreSQL restoration and corruption rejection, guarded rollback, and fresh-install failure cleanup.

The dedicated MyCountryBudget runner is active on `sr-operator`. Production release `54b2141` passed deployment, independent backup copy, exact-revision verification and hosted mobile/desktop journeys. The operator backup timer is enabled. Country expansion release `98ad930a` passed the expanded production gate: all eleven countries on mobile and desktop, including ten saves, known fiscal changes, copying, separate drafts, cancellation and reset.

Real-host disaster recovery remains a continuing rehearsal task; passing isolated CI recovery tests is not proof of every disaster scenario.

## Remaining release checks

- [x] Automated deployment independent of the laptop's forwarded SSH agent.
- [x] Deployed revision visible in health/release evidence.
- [x] Repeatable mobile browser check of both return controls, save/revisit, all ten decisions, results and reset.
- [ ] Backup retention, restore verification and rollback procedure.
- [ ] Sourced UK sensitivity model and bias/trade-off review.
- [ ] Anonymous completion/share experiment.

## Scope rules

- Preserve the approved layout while completing functionality.
- Keep observed facts, derived figures and modelled outcomes distinct.
- Annual deficit/surplus per person is not debt per person.
- International PPP gross-debt comparisons are not the UK simulator's ONS public-sector baseline.
- Leave comparison fields blank when definitions cannot yet be normalized.
- Keep the prototype label until model-validation requirements are met.
- AI challenge, account saving, public publishing, votes and forks are future work; their current preview text is not evidence of implementation.

The private production launch checklist tracks operational evidence. This public roadmap records product direction; update both when a milestone changes.
