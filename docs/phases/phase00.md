# Phase 00 — Design & Documentation

**Status: in progress.**

Figuring out what Landos actually is before committing any of it to code.

## What this phase covers

- The design document — currently `landos-design-v0.1.10.md` in `spec/design/`, the technical source of truth for every decision made so far.
- The whitepaper — `landos-whitepaper-v0.1.2.md` in `community/whitepaper/`, the same design written for a broader audience.
- The philosophical foundations — the three pillars (People First, Hernando de Soto, Bitcoin) and the principles that shape every other decision.
- The plain-language community docs — everything in `community/docs/` explaining individual concepts (Land Witness, Disputed Territories, and others) to non-technical readers.
- Standards alignment work (LADM, STDM, Fit-For-Purpose, VGGT) — checking the design against how the rest of the world thinks about land administration.

## Why this phase doesn't really end

Even once building starts in later phases, parameters get tuned, gaps get found, and the design doc keeps getting revised. That's still Phase 00 work happening in parallel — not a sign the phase failed to finish. Several parameters in the current design are explicitly marked "TBD at testnet" for exactly this reason: Phase 00 hands off a direction, not a finished number, and later phases feed real data back into it.

## Where to look

- `spec/design/` — the versioned design document. This folder lives outside the `community` repo (a sibling folder locally), so it isn't linked here — ask Brock if you need direct access.
- [`community/whitepaper/`](../../whitepaper/) — the whitepaper
- [`community/OPEN-QUESTIONS.md`](../../OPEN-QUESTIONS.md) — resolved decisions and what's still open
- [`community/CHANGELOG.md`](../../CHANGELOG.md) — version history of the design doc

---

*Part of the [Landos phases roadmap](README.md).*
