# Forecast method (summary)

- Seeded Monte Carlo with 10,000 trials over the last 12 weeks of weekly completed-item counts.
- Scope growth factor sampled from a triangular distribution around the observed growth since baseline.
- Outputs P50, P85 and P95 completion dates; "available to the business" adds the release lag.
- Fewer than 4 weeks of history: no forecast. Fewer than 9: forecast shown with an "insufficient history" warning.
- Calibration records whether completed epics hit the forecasts made 4, 2 and 1 weeks earlier.
