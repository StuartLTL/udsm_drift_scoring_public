# CHAPPiE — Releases

Signed `.ksm` builds of **CHAPPiE**, a tournament-grade drift judging mod for *CarX Drift Racing Online*.

**📖 Full documentation: [chappie.online](https://chappie.online)**

Depth-zone line scoring, per-zone angle ranges, automatic deduction tracking (wall taps, missed clipping points, off-course, overshoot, excessive braking), live countdown on the start lights, lobby-synced scoreboard, judge review, CSV results, and a host-controlled qualifying workflow.

> Formerly published as **UDSM Drift Scoring**. Same mod, same repository — the
> download keeps the filename `UDSMDriftScoring.ksm` so existing installs and
> links continue to work.

---

## Install

1. Make sure you have **[KSL (Kino Script Loader)](https://github.com/Kinomod/KSL)** installed and working.
2. Download `UDSMDriftScoring.ksm` from this repository, or from [chappie.online](https://chappie.online), which always serves the current build with its size and SHA-256.
3. Copy it into:
   ```
   <CarX install>\kino\mods\
   ```
   The default Steam path is:
   ```
   C:\Program Files (x86)\Steam\steamapps\common\CarX Drift Racing Online\kino\mods\
   ```
   If the game is on another drive, look for the `SteamLibrary` folder there instead.
4. Launch CarX. The **CHAPPiE** tile appears in the KSL launcher.

Everyone in a session should run the **same build**. Mixed versions silently break lobby features such as the shared scoreboard and the start-box lock.

---

## Documentation

| | |
|---|---|
| [Getting started](https://chappie.online/getting-started) | Install, roles, running a session |
| [Track authoring](https://chappie.online/tutorials/) | Maya/Blender → Unity → Kino, end to end |
| [Naming contract](https://chappie.online/reference/naming-contract) | The GameObject names the mod reads |
| [Scoring model](https://chappie.online/reference/scoring-model) | How a run becomes a number |
| [DQ and deduction rules](https://chappie.online/reference/dq-rules) | Thresholds, with config keys |

---

## Track authoring

To author tracks compatible with CHAPPiE you'll need the SDK components:

➡ **[udsm_drift_scoring_sdk](https://github.com/StuartLTL/udsm_drift_scoring_sdk)** — or download the SDK zip from [chappie.online](https://chappie.online)

Drop the `UDSM_SDK/` folder into your Unity track project under `Assets/`, then mark zones, off-track meshes, the start lights and the run lines via **Add Component → UDSM/...**

Full walkthrough: [chappie.online/tutorials](https://chappie.online/tutorials/)

---

## Compatibility

- KSL 1.0.10+
- CarX Drift Racing Online — current Steam build at the time of release

---

## Reporting issues

Open an issue in this repository with:

- KSL version and CarX game version
- **`debug.log`**, found next to the mod's own data at:
  ```
  <CarX install>\kino\mods\CHAPPiE\debug.log
  ```

That file is the first place to look for anything. It records the zone and
special-line scan on every scene load, role changes with their reason, every
score received, and **every DQ with the values that triggered it** — which is
usually enough to explain a result on its own.

---

## License

The `.ksm` package is distributed as-is. Source code lives in a private repository.
