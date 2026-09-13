# Paper Testnet (Pre-Chain)

There's no real Landos network yet — no chain, no nodes, no LOS. But the rules that will govern real land claims are already written down in the design doc (Sections 11–13). This is a way to actually run those rules by hand, on GitHub, before any code exists.

This process is deliberately temporary and deliberately not real. A claim filed here has no legal weight and doesn't automatically become anything on the real chain once it launches — see "What this isn't," below. The point isn't the record. The point is finding out whether the rules as written actually work when real people try to follow them.

New to this or not technical? Read [instructions.md](instructions.md) instead — plain language, step by step.

## What this isn't

- **Not a real land registry.** A test parcel is a fictional or clearly-labeled placeholder — never a real address or real GPS coordinates of actual property. Don't file a claim on land you or anyone else actually owns.
- **Not guaranteed to carry forward.** Whether any of this data migrates to the real testnet later is an open question, not a promise. Treat every claim here as a dry run.
- **Not a complete simulation.** Some mechanisms can't be done on paper — see "What this doesn't simulate," below.

## Who can participate

Anyone in [PARTICIPANTS.md](PARTICIPANTS.md) — a separate list from governance's [MEMBERS.md](../governance/MEMBERS.md), since attesting or witnessing a test claim isn't a governance vote. Ask in the [Discord](https://discord.gg/DBNpwm7MjW) or reach out to Brock directly to be added.

**Note on group size:** with only a few participants so far, most claims can get through the Notice Period solo, but Neighbor Quorum and Land Witness Review both require independent people who aren't the claimant. Until the group grows, expect claims to stall at Stage 3 — that's expected, not a bug, and it's part of why recruiting more people matters right now.

## How a test claim moves through the stages

This mirrors the real staged entry model (Section 13.1) as closely as paper allows.

**Stage 1 — Claim filed.** The claimant opens a GitHub Issue labeled `test-claim` for discussion, and creates a claim file at `testnet/claims/TEST-XXXX.md` from the [claim template](templates/PARCEL_CLAIM.md). The parcel description must be clearly fictional or placeholder — see "What this isn't." Status: **Claimed**.

**Stage 2 — Notice Period (7 days).** The claim sits visible to the whole community. No vote yet. Anyone can raise an objection using the contest section of the [claim template](templates/PARCEL_CLAIM.md#contest-log). This mirrors the real Notice Period exactly — slowness on purpose.

**Stage 3 — Neighbor Quorum, or the Land Witness fallback (7 days).**
- Normal path: 3-of-5 other participants each add a row to the claim file's Attestations table by opening a PR — this stands in for the real Neighbor Quorum (Section 11.2). Opening the PR is the attestation, timestamped and tied to a GitHub account, the same trust model the provisional governance process uses for votes.
- Independent Claimant Path (Section 11.6): if fewer than 3 attestors are available — likely, given the group's current size — 2 independent Land Witnesses substitute instead, folding straight into Stage 5.
- Interested Party Exclusion (Section 12.2) applies exactly as written: no one who is the claimant, or has any stake in the claim, can attest or witness it.

**Stage 4 — Habitation log (7 days minimum).** The real mechanism verifies this with GPS and accelerometer data over time — not possible on paper. Stand-in: the claimant posts at least two or three short dated updates over the week describing ongoing engagement with the test claim, in the claim file's Habitation Log section. This is explicitly symbolic, not a working substitute for the real proof.

**Stage 5 — Land Witness Review (7 days).** One or two neutral participants (depending on which Stage 3 path was used) certify the claim using the [Land Witness section](templates/PARCEL_CLAIM.md#land-witness-certification) of the claim file. They cannot be the claimant or an attestor on the same claim.

**Outcome.** No open contest and all required stages complete → status updated to **Confirmed** in the claim file. A contest raised at any point → status **Contested**, resolved by discussion among participants before the claim can continue.

## What this doesn't simulate

- **Dispute Bond (Section 12.5)** — requires a real LOS token to hold in escrow. Not simulated here; contests are resolved by discussion instead.
- **Personal Validation Score (Section 12.3)** — not formally tracked. Participation here is good practice, not an enforced reputation score.
- **AR Boundary Walking, real GPS habitation data** — not possible without a phone and real land. The Habitation Log stage is a written stand-in, nothing more.

## Why do this at all

Two reasons. It gives someone joining right now something real to do, not just documents to read. And it's the cheapest possible way to find out where the design doc's rules break down in practice — before any of it is locked into code.

## Questions

Ask in the [Discord](https://discord.gg/DBNpwm7MjW), or reach out to Brock directly.
