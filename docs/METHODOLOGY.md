# Methodology

## Purpose

My Country Budget is a public simulation and comparison tool. It should help participants understand the consequences of major fiscal choices without endorsing a political outcome.

## Data classes

Every numeric value exposed by the product must be tagged as one of:

- **Observed** — an official or otherwise directly measured value.
- **Derived** — arithmetic transformation of observed/modelled inputs, such as per-capita spending.
- **Modelled** — an estimated consequence of a policy change.
- **Scenario** — an explicit hypothetical or stress-test assumption.

Each record should retain source URL, publisher, source date, effective/reference period, unit, geography, methodology version and notes about revisions or limitations.

## Starting fiscal position

A country run begins from a locked factual baseline. The participant cannot edit the starting deficit/surplus or starting debt. Those figures are sourced and dated.

The participant changes policy levers. The end deficit/surplus and other results are derived/modelled from those changes.

Because public-finance statistics are revised, the production system must retain historical baseline versions rather than silently rewriting an already published user proposal.

## Ten-lever constraint

The public experience should expose approximately ten major controls. Detailed tax bands and programme-level spending may exist behind the model, but the first interaction should remain simple enough to understand on a phone.

Initial UK candidates:

1. Personal income tax
2. VAT / consumption tax
3. Corporation tax
4. Effective tariff rate
5. Healthcare spending
6. Education spending
7. Defence spending
8. Government pension level
9. State pension / retirement age
10. Other major spending / public investment

## International comparison

Rates and spending should only be compared when definitions are genuinely comparable. The product must distinguish national, federal, provincial/state and local taxation where relevant.

Per-capita, percentage-of-GDP and purchasing-power measures may be used alongside headline rates where they improve comparability. None should be presented as interchangeable when they are not.

## Policy effects

A change may have:

- a direct fiscal effect;
- a behavioural response;
- a macroeconomic response;
- delayed effects;
- uncertainty.

The interface should reveal which effects are included. A simple model must not imply that second-order effects were calculated when they were not.

## Tariffs

Tariff changes must not be represented solely as revenue changes once the model advances beyond the first prototype. Production modelling should account, where evidence permits, for import substitution, reduced import volumes, consumer/business price effects and possible retaliation. Unmodelled effects should be labelled explicitly.

## Pensions and retirement age

Government pension level and statutory/state-pension age should be separate controls where a country system permits it. Country-specific eligibility rules, contribution requirements and transition schedules should be retained in the underlying data rather than flattened into a misleading single global rule.

## User proposals and justifications

A published proposal may include a short justification for the full proposal and/or individual levers.

Other participants may:

- up-vote or down-vote a justification;
- fork a single setting;
- fork the complete proposal;
- report abuse.

There are no conversational reply threads in the initial design. Votes surface reasoning but do not change the fiscal model.

## People's Budget

The People's Budget must not simply be the most-upvoted user proposal. It should be an aggregate derived from completed participant budgets and show distributions as well as summary statistics.

Popularity of a justification, number of followers, or virality must not give one participant extra weight in the aggregate.

## AI challenge

AI receives the same starting facts, available levers and constraints as a human participant. The AI does not score itself or the human.

The engine publishes comparable factual outcomes across both proposals. If a game layer later presents a challenge result, any scoring dimensions and weights must be visible and must not be presented as an objective political ranking.

## Events and stress tests

Historical and future event modules may later introduce disasters or economic shocks. Historical mode should reveal only information that would have been knowable at the simulated point in time. Probabilistic hazards should be described as probabilities or return intervals, not as deterministic predictions that an event is 'due'.
