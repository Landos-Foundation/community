# Provisional Governance (Pre-Activation)

Landos's real governance — the bicameral Token Holder Assembly + Community Hub Assembly, with quadratic voting and a 2/3 supermajority — only makes sense once there's a real token distribution and real Community Hubs. Until the chain exists, this is how members participate in decisions and how those decisions get recorded.

This process is deliberately temporary. It ends the moment on-chain governance activates (see design doc Section 18.2). Nothing here should be assumed to carry forward in its current form — see [Open Questions #11](../OPEN-QUESTIONS.md) for what's still unresolved about it.

New to this or not technical? Read [instructions.md](instructions.md) instead — plain-language, step by step.

## Who can vote

Anyone listed in [MEMBERS.md](MEMBERS.md). A person becomes a member when Brock adds their GitHub handle to that file. This is a provisional stand-in for real membership criteria, which is still an open question — does registering a Governance DID alone qualify later on, or does it require something more (a registered parcel, a direct invite)?

## How a decision gets made

1. **Propose.** Any member opens a GitHub Issue in this repo using the [proposal template](templates/PROPOSAL.md), labeled `proposal`.
2. **Notice period — 7 days.** Discussion happens in the issue thread. No vote yet. This mirrors the 7-day stage duration used elsewhere in the design — slowness as a feature, not a bug.
3. **Vote record opens.** After the notice period, a new file is created at `governance/votes/PROP-<number>.md` from the [vote record template](templates/VOTE_RECORD.md), with the final proposal text and a voting window (7 days).
4. **Vote.** Each member casts their vote by opening a pull request that adds exactly one row to that file: GitHub handle, vote (For / Against / Abstain), and an optional short comment. Opening the PR is the vote — it's timestamped and tied to that member's authenticated GitHub account. This stands in for the signed Governance DID vote the real system will use later. It's not cryptographic signing — that's an honest limit of this interim process, not a design decision to carry forward.
5. **Tally.** When the voting window closes, all vote PRs are merged into the vote record. Simple majority decides for now — whether it should be a higher bar even at this scale is still open.
6. **Ratify or override.** Brock can override any outcome — he holds the admin keys during this period, and that doesn't change here. If he does, the override and its reason are recorded directly in the vote record file, not left out. The default is to follow what the group decided.

## Why record it this way

No live chain exists yet to write signed votes to. Git history is the interim substitute: it's public, timestamped, and hard to quietly rewrite. When the chain exists, this same shape — proposal, notice, signed vote, recorded outcome — moves onto it, with an actual Governance DID doing the signing instead of a GitHub login.
