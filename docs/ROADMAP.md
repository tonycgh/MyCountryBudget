# My Country Budget roadmap

Updated: 16 September 2026

## Direction

Ship a credible, mobile-first UK budget simulator that a new visitor can complete in under five minutes. Keep the approved country-comparison layout and the finite **10 decisions. That's it.** overview. No sign-in is needed to play.

This is a deployed prototype. Deployment of the interface does not mean that the fiscal model, AI challenge or community features are finished.

## What is already delivered

- Public website at https://mycountrybudget.com with HTTPS.
- Six-country comparison table; United Kingdom is playable.
- Ten-decision overview, open in any order, save and revisit.
- Locked UK starting baseline, annual deficit/surplus and per-person results.
- Optional short explanations and copyable budget summary.
- Both return-to-ten controls and versioned frontend assets.
- Three redundant UK landing callouts hidden in the deployed stylesheet.
- Public methodology and data definitions; application CI tests.

## Ordered delivery plan

| Priority | Milestone | Work | Completion evidence |
| --- | --- | --- | --- |
| 1 — next | Reliable prototype operations | Connect the dedicated deployment runner; verify the deployed revision; add automatic browser checks; establish database backups and a tested restore/rollback procedure. | A release can be deployed and checked without a laptop command, and recovery has been demonstrated. |
| 2 | Credible UK model | Replace prototype sensitivities with sourced, versioned assumptions; record reference periods, units and accounting definitions; document uncertainty, timing and excluded effects. Audit international comparisons and their source records. | Each lever has a reviewable source/assumption record, fiscal cross-checks pass, and every saved result identifies its baseline/model version. |
| 3 | Complete anonymous experience | Test phone and keyboard journeys; improve slow/failed calculation handling; preserve an unfinished budget across refresh; verify completion and copying/sharing. | A first-time visitor can complete all ten decisions on a phone in under five minutes and recover from refresh/network errors. |
| 4 | AI challenge | Give AI the same baseline, ten controls and constraints; validate its choices and calculate both budgets with the same engine; explain differences. | Human and AI outcomes can be reproduced from their inputs. AI never judges its own answer, and there is no single political winner score. |
| 5 | Community | Add login only at save/publish/vote/fork; persist versioned proposals; support voting on explanations and forks; add reporting/moderation. | Publishing, attribution, voting, forking and moderation work end to end; there are no reply threads. |
| 6 | People's Budget and expansion | Aggregate completed budgets with distributions and participation counts. Add further playable countries only after their baselines and policy responsibilities are modelled. | Aggregates do not award extra weight for popularity. Each new country passes its own data/model and browser checks. |

Priorities describe delivery order, not promised dates. Reliability checks continue throughout.

## Canada — retained for later

Keep one Canada row in the country comparison. When Canada becomes playable, add a province/territory choice and clearly distinguish federal and provincial responsibilities and tax effects. Do not expand the current UK build into provincial simulation work.

## Remaining release checks

- [ ] Automated deployment independent of the laptop's forwarded SSH agent.
- [ ] Deployed revision visible in health/release evidence.
- [ ] Repeatable mobile browser check of both return controls, save/revisit, all ten decisions, results and reset.
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
