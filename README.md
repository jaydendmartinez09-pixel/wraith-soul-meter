# Wraith Soul Meter (Deadlock HUD mod)

An econ HUD for Wraith, shown next to **SOULS** (bottom-left):

- **You 15,200 / Eternus Wraith 15,715 @15:00**: your net worth (souls + items) vs the average Eternus Wraith at the same match time
- **Soul rank D to SSS**: your souls/min over the last 60 s vs the Eternus Wraith pace
- Unsecured-souls timer, **FARM!** idle alarm, **SPEND** reminder, +souls popups

Eternus Wraith net worth (deadlock-api.com, ranked, Eternus average badge, last 30 days, 6,503 games):

| 3:00 | 6:00 | 9:00 | 12:00 | 15:00 | 20:00 | 25:00 | 30:00 | 40:00 |
|---|---|---|---|---|---|---|---|---|
| 1,867 | 4,184 | 7,486 | 11,389 | 15,715 | 22,912 | 30,502 | 37,751 | 52,449 |

## Install

Paste into PowerShell:

```powershell
irm https://raw.githubusercontent.com/jaydendmartinez09-pixel/wraith-soul-meter/main/install.ps1 | iex
```

It finds Deadlock through Steam, downloads `WraithSoulMeter_v12.zip` from this repo, checks its SHA-256, and copies the
mod into `game\citadel\addons` as a free `pakNN_dir.vpk`. Restart Deadlock afterwards. Mods must be enabled
(Deadlock Mod Manager does that). To uninstall, delete the `pakNN_dir.vpk` the installer printed.

Manual install: unzip `WraithSoulMeter_v12.zip` and copy `Wraith Soul Meter.vpk` to
`Deadlock\game\citadel\addons\pak88_dir.vpk` (any free number).

Notes: the rank/idle/spend sounds come from a companion Shiv mod, so on its own the meter is silent. The meter loads
through the game's match-start layout, so a big Deadlock HUD patch may need an updated build.
