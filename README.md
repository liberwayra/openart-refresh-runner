# openart-refresh-runner — public CI host

Runs the weekly OpenArt catalog refresh (Mondays 09:00 UTC). This repo hosts
ONLY the Actions workflow + heartbeat state — all logic and data live in
private repos (`liberwayra/openart-refresh` for logic,
`liberwayra/openart-scraper` for data), pulled at runtime via the `GH_PAT`
secret. See `liberwayra/openart-refresh` README for the full architecture.

Why public? GitHub Free gives unlimited Actions minutes for public repos,
and the liberwayra account cannot run Actions on private repos
(startup_failure — verified Sep 17 + Sep 22 2026).

Heartbeat: [state/last_refresh.json](state/last_refresh.json)
