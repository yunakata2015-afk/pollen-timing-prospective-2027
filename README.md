# Pollen Timing Prospective Validation 2027

Prospective validation of probabilistic forecasts of spring pollen dispersal
timing (onset and full-dispersal onset) for the 2027 season in Japan.

This repository is the public, timestamped archive for the validation:

- `protocol/` — the study protocol (in Japanese). The current version is the
  freeze candidate (revised 2026-11-19); the frozen version will be committed
  and tagged at the December 2026 freeze, before the season starts. The frozen
  Platt calibration parameters are in `protocol/calibration_maps.json`.
- `predictions/` — daily probabilistic forecasts (probability that onset /
  full onset occurs within 7 days / 3 days, for two models), pushed daily
  from 2027-01-01 to 2027-04-30. Append-only.

Design in brief: two simple models — climatology and a probabilized
cumulative-temperature rule — with pooled deviation distributions
(Pacific-pool design as the primary structure, block-pool as a pre-specified
comparator), Platt-calibrated on 2007–2021 training data and retrospectively
tested on 2024–2026. A branch variant (threshold shifted by the December–
January temperature anomaly) is pre-registered as a secondary model, and the
Otsu site (Durham method, Shiga University of Medical Science) is tracked in
a separate frame as a local anchor. The prospective run checks whether the
frozen forecasts keep their calibration in a new season. Results will be
reported regardless of outcome.

Companion work: a machine-learning framework for forecasting spring pollen
dispersal amount and real-world medication demand (manuscript under review).
