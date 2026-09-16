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

The interface will continuously show the change from the real starting deficit/surplus and other resulting fiscal indicators.

## Public and private repositories

This repository is the public home for methodology, source data definitions, provenance records and eventually reusable/open-source calculation components.

The production web application, operational configuration and deployment tooling live in a separate private repository.

## Status

Early prototype. Data and model outputs must not be treated as official forecasts unless explicitly identified as such.
