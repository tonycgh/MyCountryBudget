# Country data schema

This document defines the minimum provenance expected for country facts and model parameters.

## Baseline record

Each country baseline should contain:

- `country_code`
- `country_name`
- `baseline_id`
- `status` (`provisional`, `final`, `historical`, etc.)
- factual starting values
- source metadata

Each value should retain:

- numeric value
- unit
- reference/effective period
- classification (`observed`, `derived`, `modelled`, `scenario`)
- optional geography/level of government
- notes describing definitions or limitations

## Policy lever definition

Each editable lever should eventually specify:

- stable lever ID
- public label
- country-specific starting value
- display unit
- safe UI range
- source for starting value
- direct fiscal model version
- second-order model version, if any
- effective date / phase-in rules
- confidence / limitation note

## Published user proposal

A proposal should be immutable once published except for moderation metadata. It references a baseline ID and model version so that later revisions to official statistics do not rewrite history.

Suggested fields:

- proposal ID
- anonymous/user ID
- country code
- baseline ID
- model version
- created timestamp
- lever values
- calculated outcome snapshot
- optional overall justification
- optional per-lever justifications
- fork parent proposal ID

## Votes

Votes are attached to a justification or proposal and are not inputs to the fiscal calculation. One authenticated account should have at most one active vote per target.

## Aggregation

Aggregate public views should be computed from completed proposals, not from justification vote totals. Distribution data should be retained so the public can see disagreement rather than only one summary value.
