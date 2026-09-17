# My Country Budget

**Build a budget. See the consequences. Compare with the world.**

My Country Budget is an open civic-budget project. It is designed to let a person choose a country, change a small number of major fiscal and policy levers, see the modelled consequences, explain their choices, and compare the result with other participants and AI-generated proposals.

The project is intentionally neutral about which political choices are preferable. The calculation engine should expose trade-offs, sources, assumptions and uncertainty rather than tell a participant what to support.

## Product principles

1. **Mobile first.** A complete run should be practical on a phone.
2. **Start from reality.** Each country begins from a locked, sourced fiscal baseline.
3. **Ten levers, not a spreadsheet.** The public interface should stay understandable.
4. **Facts and models are different things.** Every displayed value must be labelled as observed, derived or modelled.
5. **Per-capita context where useful.** Large totals should be translated into understandable per-person figures when appropriate.
6. **International comparison.** Comparable measures should use normalised definitions and make federal/sub-national differences explicit.
7. **Explain, do not argue.** Users may publish a short justification for a setting; others may vote it up/down or fork it, but there are no reply threads.
8. **Fork instead of fight.** A user who disagrees with a proposal can copy it, change the numbers and publish an alternative.
9. **AI is a participant, not the judge.** Human and AI proposals use the same deterministic calculation engine.
10. **No single political 'winner' score.** Fiscal and service outcomes are shown as separate dimensions; user preferences are not collapsed into a normative ranking.

## Measurement rules

A core rule is to keep fiscal **flows**, **stocks**, and internationally standardized comparison measures visibly separate:

- **Annual deficit/surplus per person** is one year's fiscal balance divided by population.
- **Debt per person** is the outstanding public-debt stock divided by population.
- **International comparison debt per person** uses a standardized general-government definition and PPP-adjusted international dollars where available so country rows can be compared more consistently.
- **Country simulator baselines** use an explicit official national definition and are versioned. The initial UK prototype uses an ONS public-sector baseline.

These measures are not interchangeable. The interface should identify which one is being shown rather than using a generic label such as “balance per person.”

## Data provenance

Published figures should expose, where applicable:

- source and source URL
- source/effective date
- unit and accounting definition
- observed, derived or modelled classification
- data/model version

If a comparison field has not yet been verified or normalized, label it explicitly as missing. A missing field must not imply that the country has no such tax or pension.

## Playable now — 17 September 2026

Eleven countries are live at [mycountrybudget.com](https://mycountrybudget.com): United Kingdom, Canada, United States, Mexico, Germany, France, India, United Arab Emirates, Saudi Arabia, Italy and Spain.

Every country has ten decisions, save/cancel, reset, copyable results and separate drafts within the current browser tab. The UK retains its pound-based prototype. Other countries use explicit revenue/spending targets in percent of GDP, based on 2025 IMF WEO April 2026 estimates; per-person comparisons use international dollars at purchasing power parity. These targets are not tax rates or forecasts of policy effects. Country-specific tax and pension modelling remains a separate next step.

## Community and references — 17 September 2026

Publish a fixed snapshot of your ten choices, vote on budgets and their justifications, or fork someone else's budget into your own version. The landing page switches between country comparison, community budgets (latest, top-rated and top justifications), and election/budget references. No account is needed to save, share, fork, vote or report. Published originals cannot be edited; changes are new attributed forks. The same browser remembers saved budgets through a private cookie. Keep share links: clearing cookies or switching devices loses the saved list and withdrawal access, while published links remain readable. Browser-based votes are community reactions, not verified counts of people. Existing accounts and operator-approved moderators have separate access.

Income and corporation tax headlines now have source links and jurisdiction/period notes for all eleven countries. Election references label current government documents, budget requests, opposition proposals and historical manifestos separately. This is a dated selected collection with explicit coverage gaps, not an automatic news feed. Some pension schedules and matched current opposition-budget sets still need source review.

## Initial scope

The first playable country is the United Kingdom. Initial controls are expected to cover approximately ten major levers, including:

- personal income tax
- VAT / sales tax
- corporation tax
- tariffs
- healthcare spending
- education spending
- defence spending
- government pension level
- state pension / retirement age
- other major spending / investment

The interface continuously shows the change from the real starting deficit/surplus and other resulting fiscal indicators. The landing page is also intended to provide a one-row-per-country comparison using roughly 10–15 important statistics, with debt per person and VAT/GST/sales-tax differences especially visible.

## Public and private repositories

This repository is the public home for methodology, source data definitions, provenance records and eventually reusable/open-source calculation components.

The production web application, operational configuration and deployment tooling live in a separate private repository.

## Roadmap

See the [ordered roadmap](docs/ROADMAP.md) for delivered functionality, next steps and the requirements for moving beyond the prototype.

## Status

Early prototype. Data and model outputs must not be treated as official forecasts unless explicitly identified as such.
