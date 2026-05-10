# UDSM Drift Scoring — Releases

Signed `.ksm` builds of the **UDSM Drift Scoring** mod for *CarX Drift Racing Online*.

UDSM is a tournament-grade drift judging mod: depth-zone line scoring, per-zone angle ranges, automatic deduction tracking (wall taps, missed clipping points, off-course, overshoot, excessive braking), live tandem-battle countdown via the lamp post, lobby-synced scoreboard, and a host-controlled qualifying / battle workflow.

---

## Install

1. Make sure you have **[KSL (Kino Script Loader)](https://github.com/Kinomod/KSL)** installed and working.
2. Download `UDSMDriftScoring.ksm` from this repository (or from the **Releases** page).
3. Copy it into:
   ```
   <CarX install>\kino\mods\
   ```
   The default Steam path is:
   ```
   C:\Program Files (x86)\Steam\steamapps\common\CarX Drift Racing Online\kino\mods\
   ```
4. Launch CarX. The UDSM tile will appear in the KSL launcher (look for the U/D/S/M logo).

---

## Track authoring

To author tracks compatible with UDSM you'll need the SDK components. Grab them from:

➡ **[udsm_drift_scoring_sdk](https://github.com/StuartLTL/udsm_drift_scoring_sdk)**

Drop the `UDSM_SDK/` folder into your Unity track project under `Assets/`, then mark zones, walls, off-track meshes, the start lights, etc. via **Add Component → UDSM/...**

---

## Compatibility

- KSL 1.0.10+
- CarX Drift Racing Online — current Steam build at the time of release

---

## Reporting issues

Open an issue in this repository with:
- KSL version
- CarX game version
- The relevant slice of `kino\output.log` (the file `output.log` next to the mods folder, lines beginning `[UDSM ...]`)

---

## License

The `.ksm` package is distributed as-is. Source code lives in a private repository.
