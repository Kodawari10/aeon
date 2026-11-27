# Starknet digest, 2026-11-27: DIGEST_THIN, nothing sent

Only one item cleared the signal bar, and the skill says to skip the notification below three items rather than pad.

**The one solid item: StarkWare post-quantum comparison v2**
- StarkWare updated its crypto-agility table and migration map (data as of Nov 24) at [quantum.starkware.co/networks](https://quantum.starkware.co/networks). It compares 10 chains.
- Starknet is listed as supporting optional post-quantum account signing, with a proving layer that is already hash-based. It targets full post-quantum security in 2027, against end-2027 for Algorand and December 2029 for the Ethereum Foundation.
- Solana dropped to 0 of 8 because it relied on Frankendancer, which is no longer supported.
- Bitcoin's signing status moved to "demonstrated" after a quantum-safe spend on mainnet on Aug 26.
- Starknet's own quantum campaign ([post](https://x.com/Starknet/status/2125975493203881995), 299 likes) claims a quantum computer could fake an elliptic-curve SNARK proof in under 8 hours, versus about 15 million years for a STARK. That claim is self-reported.

**Dropped, with reasons**
- **STRK20 privacy app list** (a [szu_1001 post](https://x.com/szu_1001/status/2125895589065838660)): privacy launched June 9, so this is a recap. It does list OffMarket as live for private prediction markets on Starknet, which matters to you.
- **StarkWare Inference Proofs benchmark:** v1.0 was frozen Nov 11, so it isn't fresh.
- **Chance AI-agent stats** (150K+ transactions, $275M notional): self-reported and unverified.
- **Garden BTC-to-Starknet post:** no substance.
- **Hyperliquid/Starknet ranking post:** not news.
- **Already covered Nov 23–26:** post-quantum Falcon-512, independent L1, Upbit listing, Xverse multisig, token unlocks, block-sized proofs.

**X signal:** the xAI call worked (http=200, 8 posts). WebSearch only returned older stories.

## Summary
- **Done:** ran the Starknet digest from WebSearch and xAI, and verified candidates via WebFetch. I did not call `./notify`.
- **Files changed:** appended a `### digest (Starknet)` entry to `memory/logs/2026-11-27.md`, and added a row to the Recent Digests table in `memory/MEMORY.md`.
- **Follow-up:** none needed. If you want thin days sent anyway, the skill's Phase 3 and Phase 4 rules conflict and could be reconciled.
