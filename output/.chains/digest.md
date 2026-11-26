ℹ️ Starknet digest

*Starknet — 2026-11-26*

_TL;DR: Quiet day; the signal is builder tooling for STRK20 privacy (wallet registration in starknet.js, an AI app builder in private beta) plus Endur's two-year staking numbers._

1. *starknet.js v11.7 prerelease adds STRK20 wallet registration*
   The prerelease supports Wallet API 0.10.5, letting a supporting wallet register a Cairo account in the STRK20 privacy pool. The register action must be the only action in its request.
   Why it matters: dApps can now onboard users into shielded balances through the wallet flow instead of custom plumbing.
   https://x.com/CairoLang/status/2125560153026257222

2. *Starknet.Build opens a waitlist for its AI app builder*
   Describe an app in plain language and it writes the contracts, builds the frontend, runs tests, and deploys to Starknet. It is in private beta, with no public launch date on the site, and is built on the privacy features (STRK20, shielded transfers).
   Why it matters: a no-Cairo path to shipping privacy apps; join the waitlist if you want early access.
   https://x.com/LoLoCoding/status/2125586043193655552

3. *Endur turns 2: 140M+ STRK and 40+ BTC staked*
   The liquid staking protocol reports five Bitcoin flavours (including strkBTC for private BTC staking) and integrations with Vesu, Ekubo, Troves, and Opus. Figures are self-reported.
   Why it matters: strkBTC is now a live staking asset with DeFi integrations, not only a roadmap item.
   https://x.com/endurfi/status/2125916418327879881

*Also worth a glance:* Cairo 2.21 now rejects const comparisons that would ignore a custom PartialEq impl ([PR #10395](https://github.com/starkware-libs/cairo/pull/10395)) · Quiet news day; Upbit listing, Falcon-512, Xverse multisig and unlock cadence were covered earlier this week and skipped.