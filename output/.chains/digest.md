ℹ️ Starknet digest 2026-11-25

*Starknet — 2026-11-25*

_TL;DR: Quiet news day; the substantive threads are post-quantum account tooling maturing, first-accelerator lessons, and a fixed STRK unlock calendar through March._

1. *OpenZeppelin folds Falcon-512 gas work into Starknet PQ accounts*
   An OpenZeppelin repo now ships deployable post-quantum account verifiers (Falcon-512 with three hash variants; one spec-compliant, two cheaper). A spec-compliant Falcon-512 account has already executed a mainnet transfer for roughly $0.06, and OZ docs cover migrating an existing account to Falcon keys at the same address. A contributor on X says the provably.fast challenge ideas fed the gas optimizations.
   Why it matters: gives a concrete cost figure for the post-quantum / independent-L1 debate (calldata-fallback cost was the open question in mentions yesterday). The OZ code is marked experimental and unaudited.
   https://github.com/OpenZeppelin/cairo-pq-verifiers
   https://x.com/Nadai02010/status/2125218942608183788

2. *Proof, Starknet's first accelerator, publishes 7 lessons for 0-to-1 founders*
   Cohort 01 ("Proof of Privacy", STRK20 builders) ran Jul 20 – Sep 14 and demoed 7 teams. The thread is the first public retrospective.
   Why it matters: reusable material for builder-facing community posts; Cohort 01 teams are the natural ones to spotlight.
   https://x.com/jessguessing/status/2125250128546279697

3. *STRK unlock cadence: 127M per month through March 2027*
   Circulating supply is roughly 7.8B per a market-data thread; the Nov 15 batch of up to 127M STRK was the latest, with four monthly batches left (about 6.6% of circulating). Next batch is mid-December, assuming the 15th cadence holds.
   Why it matters: the supply overhang is the main recurring bearish talking point in mentions, so the schedule is worth having at hand for replies.
   https://tokenomist.ai/starknet
   https://x.com/TheAltconomy/status/2125220583013306564

*Also worth a glance:* Eli Ben-Sasson on a privacy / AI / quantum panel at Blockchain Life, Dubai, Dec 2 (https://x.com/LunaPRofficial/status/2125538956456722487) · A self-reported activity stat puts monthly active addresses at 38.1K, about 0.1% L2 share, unverified source (https://x.com/sallubroz/status/2125143633829494905)

_Thin day: only 3 items cleared the bar; Xverse multisig, Upbit listing and Paradex $1B were already covered Nov 23-24 and dropped._