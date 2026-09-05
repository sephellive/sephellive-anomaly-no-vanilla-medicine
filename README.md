# Sephellive Anomaly No Vanilla Medicine

Blocks the standard Anomaly medicine set everywhere it is registered.

This module depends on `Sephellive Anomaly Content Policy Core` and uses it to blacklist the vanilla medicine section IDs at runtime. The idea is simple: keep the vanilla item definitions in place, but make them disappear from normal gameplay so your own medical items can take over cleanly.

What it does:

- blocks the vanilla medicine catalog globally;
- leaves quest/story objects protected;
- keeps custom medicine items available if they use new section IDs;
- avoids patching vanilla medical configs directly.

Dependencies

- `Sephellive Anomaly Content Policy Core`

Architecture notes

- `sep_policy_vanilla_medicine.script` is a generated registry of vanilla medicine sections.
- The policy is data-driven, so the actual gameplay behavior stays in the shared core.
- This repo is meant to be the clean baseline for a future custom medicine pack.

Install

1. Install the core package first.
2. Install this package after it.
3. Launch the game once and verify that vanilla medicine no longer appears in normal loot, trader stock, or NPC loadouts.

This repository is part of the Sephellive modular Anomaly setup.
