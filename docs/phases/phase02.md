# Phase 02 — Alpha

**Status: not yet started.**

Real code begins.

## What this phase covers

- The Cosmos SDK chain itself — Tendermint BFT base layer, the Proof of Land consensus module.
- The token layer — Parcel Record, Land Record NFT (Deed), and LOS, implemented as actual on-chain primitives instead of design-doc descriptions.
- The genesis block scaffolding, ahead of the real Genesis event in Phase 04.
- Basic node software — full, light/SPV, and relay nodes.
- Implementation of the four ZK circuits (Location, Identity, Attestation, Score) — these are fully designed in Section 19.0 of the design doc, but not yet written as working code. This is its own cryptography/engineering track, separate from the base chain build.
- Early mobile app work. Proof of Habitation and AR Boundary Walking don't work without an app, and no app design exists yet — this is likely where that starts.

## How this runs

A closed, internal alpha — a small group building and breaking things, not a public network. Parameters the design doc marks "TBD at testnet" (the Proof of Land scoring curve, hub activation thresholds, and others) get their first real calibration here, against actual usage instead of guesses.

## Known open items feeding into this phase

- Hub ID geographic narrowing — small rural hubs can narrow down a user's location even with hashed coordinates. The design doc flags this as the highest-priority unresolved item, needing a design answer before the ZK circuits get built for real.
- Coerced registration defense — needs legal consultation before implementation; direction is sketched but not finalized.

---

*Part of the [Landos phases roadmap](README.md).*
