# CCSS Coverage Map

An interactive map of which K–12 learning platforms teach each **Common Core State Standard** for English Language Arts.

**▶ Live map:** https://peterbates-alpha.github.io/CCSS-Coverage-Map/

## What it answers

- **By standard** — search a code (e.g. `L.7.1`) or text and see which platforms teach it, with full provenance.
- **By platform** — filter to one platform and see everything it covers.
- **Gaps** — filter to *black holes* (uncovered), *inherited* (covered via parent anchor), or *redundant* (2+ platforms).
- **Dashboard** — live coverage % per CCSS strand.

## How coverage is shown — honest by design

Every standard sits in one of three states:

| State | Meaning |
|---|---|
| **direct** | a platform maps to this exact standard code |
| **◐ inherited** | no direct mapping, but the *parent anchor* is covered (the platform teaches at a grain coarser than this sub-standard) |
| **● black hole** | neither — genuinely uncovered |

Each mapping is tagged with a **confidence** level:

- **high** — vendor-published per-lesson standard tags
- **medium** — deterministic domain / category / lesson-name mapping (anchor grain)

Hover any platform chip for its source and assessment type; expand "mapping(s)" for full provenance.

## The spine

`ccss_ela_spine.csv` is the canonical, verified row set: **891 CCSS ELA standards** across all six strands (RL, RI, RF, W, SL, L), K–12, transcribed from the official Common Core document and cross-checked against an authoritative machine-readable standards list (zero set-level discrepancies). It is the fixed denominator the coverage map is built against.

## Regenerating the page

The map is generated from the spine + a private coverage-mappings dataset. `index.html` is fully self-contained (data embedded, no server, no build step needed to view). To rebuild after updating mappings, run the build script (kept in the private working repo) with `--sanitize` to produce this public-safe page.

## Notes

This public page contains only the CCSS standards (public) and platform-level coverage states. Internal deployment details, credentials, and data-acquisition scripts are intentionally excluded.
