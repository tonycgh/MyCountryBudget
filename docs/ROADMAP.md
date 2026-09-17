# My Country Budget roadmap

Updated: 17 September 2026

## Direction

Ship a credible, mobile-first multi-country budget simulator that a new visitor can complete in under five minutes. Keep the approved country-comparison layout and the finite **10 decisions. That's it.** overview. No account is needed to play, save, share, fork, vote or report.

This is a deployed prototype. Community publishing, voting and forking are implemented. The fiscal sensitivity models and AI challenge remain separate unfinished milestones.

## What is already delivered

- Public website at https://mycountrybudget.com with HTTPS.
- Generated [XML sitemap](https://mycountrybudget.com/sitemap.xml), robots.txt discovery and matching canonical URLs for public country builders, reference pages and community information.
- Eleven playable countries: United Kingdom, Canada, United States, Mexico, Germany, France, India, UAE, Saudi Arabia, Italy and Spain.
- Ten-decision overview, open in any order, save and revisit.
- Existing UK pound-based model plus versioned 2025 IMF baselines for new country scenarios, with annual deficit/surplus and per-person results.
- Non-UK controls are explicit revenue/spending targets in % GDP; per-person results use Intl $ PPP. They are not local tax-rate forecasts.
- Country links and separate per-country drafts survive refresh in the current browser tab.
- Optional short explanations and copyable budget summary.
- Account-free saving with share links; immutable published budgets; attributed forks; browser-based up/down votes on budgets and justifications.
- Banknote favicon, same-browser saved lists and contribution removal; separate legacy-account and moderator access.
- Landing tabs for comparisons, latest/top budgets by country, top positively rated justifications, and election/budget references.
- Personal published-budget lists, public or link-only visibility, withdrawal, reporting and moderator tools.
- Sourced income/corporation tax headlines for all eleven countries, with jurisdiction and period notes.
- Dated election references that distinguish government budgets, presidential requests, opposition proposals and historical manifestos. Coverage gaps remain explicit.
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
| Delivered; maintain | Community | Account-free saving, fixed snapshots, share links, browser-based voting, attributed forks, country feeds, withdrawal and moderation. Existing accounts and operator-approved moderators have separate access. | Real PostgreSQL tests and mobile/desktop account-free save/share/vote/fork checks pass. There are no reply threads. |
| 6 | People's Budget and expansion | Aggregate completed budgets with distributions and participation counts. Expand beyond the eleven playable scenarios; deepen country-specific tax/pension modelling separately. | Aggregates do not award extra weight for popularity. Each new country passes its own data/model and browser checks. |

Priorities describe delivery order, not promised dates. Reliability checks continue throughout.

## Canada — retained for later

Canada is playable as a national GDP-share scenario. A province/territory layer remains deferred: distinguish federal and provincial responsibilities before introducing it.

## Operations activation — 17 September 2026

The first operations milestone now has merged implementation: deployment of a tested revision, a separate Python environment per release, verified pre-deploy database backups, guarded application rollback, nightly backups plus an independent operator copy, and phone/desktop browser release checks.

CI passed the complete ten-decision journey, results/copy/revisit/reset, PostgreSQL restoration and corruption rejection, guarded rollback, and fresh-install failure cleanup.

The dedicated MyCountryBudget runner is active on `sr-operator`. Production release `54b2141` passed deployment, independent backup copy, exact-revision verification and hosted mobile/desktop journeys. The operator backup timer is enabled. Country expansion release `98ad930a` passed the expanded production gate: all eleven countries on mobile and desktop, including ten saves, known fiscal changes, copying, separate drafts, cancellation and reset.

Community release `ef1ae931b778deb48be9ee070b88d0e26e7b2049` implements accounts, immutable publication, voting, attributed forks, country feeds and sourced tax/election references. [CI passed](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35236104512) with 70 model, API, database, security and reference tests. [Production verification passed](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35236717474): exact revision, independent backup copy, all eleven countries on mobile and desktop, and real publishing, voting and forking journeys. Temporary accounts were removed and no public seed activity was created. Rollback was not needed.

The follow-up table-wrapping fix is live in `9b1466bb86b22c02d9eb7d772b588c5f54961ac5`. Its [CI](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35236983442) and [complete production verification](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35237644319) also passed, including the community journeys and cleanup.

Search discovery shipped in `bbab5b3d7362e6637a7f5132932a666ef2c15b2e`: 23 public canonical URLs generated from the country catalog, with user proposals/account/API URLs excluded and no artificial modification dates. [CI](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35243990524) passed all 73 tests; [production verification](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35244538281) passed XML coverage, the robots.txt sitemap link, HEAD support and the existing mobile/desktop/community journeys. The public sitemap and robots.txt both returned HTTP 200. Cloudflare settings were not changed.

Account-free participation shipped in `26a0a9c3ae4a2e1ec2ffb8d27cc0a9baab374230`: no login needed to save, share, fork, vote or report. Saved budgets are fixed snapshots; changes are attributed forks. A private browser cookie remembers saved budgets and supports withdrawal/removal, with an explicit keep-your-link reminder. A banknote favicon is served in ICO and PNG sizes. [CI](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35248968932) passed all 77 tests. [Production verification](https://github.com/tonycgh/MCB-Project-Build/actions/runs/35249549368) passed exact-revision health, independent backup copy, all-country phone/desktop journeys, favicon delivery and real account-free save/share/vote/fork checks. Test contributions stayed unlisted and their browser identities were removed. Rollback was not needed.

Real-host disaster recovery remains a continuing rehearsal task; passing isolated CI recovery tests is not proof of every disaster scenario.

## Remaining release checks

- [x] Automated deployment independent of the laptop's forwarded SSH agent.
- [x] Deployed revision visible in health/release evidence.
- [x] Repeatable mobile browser check of both return controls, save/revisit, all ten decisions, results and reset.
- [x] Backup retention tooling, isolated restore verification and guarded rollback procedure.
- [ ] Continue real-host disaster-recovery rehearsals and retention audits.
- [ ] Sourced UK sensitivity model and bias/trade-off review.
- [ ] Anonymous completion/share experiment.

## Scope rules

- Preserve the approved layout while completing functionality.
- Keep observed facts, derived figures and modelled outcomes distinct.
- Annual deficit/surplus per person is not debt per person.
- International PPP gross-debt comparisons are not the UK simulator's ONS public-sector baseline.
- Label missing comparison data explicitly. A missing rate must not imply no tax.
- Expand verified pension schedules and current government/opposition document coverage; review source dates around elections.
- References are manually reviewed, not an automatic political-news feed.
- Keep the prototype label until model-validation requirements are met.
- The AI challenge remains a labelled preview. Community saving/voting/forking require no account. Published originals cannot be edited; changes are attributed forks. Private account-synced editable drafts and social sign-in are outside the current direction.
- Keep public community feeds free of synthetic seed votes or test budgets. Release checks use unlisted proposals and remove their temporary browser identities.
- Anonymous vote counts are community reactions, not verified people or representative polls. Keep share links: clearing cookies or switching devices loses the saved list and withdrawal access, while published links persist.

The private production launch checklist tracks operational evidence. This public roadmap records product direction; update both when a milestone changes.
