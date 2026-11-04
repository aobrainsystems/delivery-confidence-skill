---
name: delivery-forecast
description: Forecast when a Jira epic or initiative will ship (P50/P85/P95), explain how much to trust the forecast with an itemised 0-100 data-trust score, list open decisions grouped by owner role, and explain why a forecast moved. Use for any question about delivery dates, confidence, readiness gaps or delivery briefs.
license: MIT
allowed-tools: get-forecast get-trust-score get-brief list-decisions explain-forecast
---

# Delivery forecast skill

Use these tools to answer delivery questions about a Jira epic or initiative. Always pass the issue key the user mentions (for example `CHK-12`).

## When to call which tool

| Question | Tool |
|---|---|
| When will it ship? | `get-forecast` |
| How sure are we? Can we commit to this date? | `get-trust-score` |
| What is blocking? Who has to decide what? | `list-decisions` |
| Why did the date move? | `explain-forecast` |
| Summarise for stakeholders | `get-brief` |

## Reading results

- Every tool returns a `status`. `ok` means the numbers are current. `not_computed` means the app has not processed this epic yet; say so and suggest retrying later. `insufficient_history` means fewer than 9 weeks of completed work exist; present the date only with that caveat.
- Present forecasts as a percentile and range: "85% likely by <p85> (50%: <p50>)".
- Trust bands: 80-100 trustworthy, 60-79 use with caution, below 60 do not commit externally.
- Cite the `issueKeys` listed under each deduction or decision.

## Errors

- If a tool errors, tell the user the app could not read the forecast and to open the Delivery Confidence panel on the epic.

See `references/` for the scoring rules and the forecasting method.
