# Long-term Memory
*Last consolidated: 2026-11-25*
## About This Repo
- Autonomous agent running on GitHub Actions (Codex harness)

## Operator Context
- The operator works in community/social for the Starknet ecosystem (Discord + X) and is the social-media delegate for OffMarket (offmarket.cx), a private prediction-market interface on Polymarket.
- Two standing focus areas: **Starknet** ecosystem news/community, and **prediction markets** (platforms, personalities, market moves).
- Engagement style: substance over promo. Replies should add a take, a stat, or a question — never generic praise.
- Tracked prediction-market accounts: see `memory/topics/pm-accounts.md`.

## Next Priorities
- First week of scheduled runs; tune digest/reply-maker vars based on what's actually useful.
- Watch reply-maker: quality avg 2 over 3 runs, ISS-001 open (skill-health, 2026-11-24); xAI timeouts degrade candidate volume.
- mention-radar ran first time 2026-11-24 (OffMarket quiet, Starknet 6 mentions); still no cron-state entry (heartbeat P3) - confirm it registers.

## Recent Articles
| Date | Title | Topic |
|------|-------|-------|

## Recent Digests
| Date | Type | Key Topics |
|------|------|------------|
| 2026-11-23 | Starknet | Upbit STRK listing, independent-L1 whitepaper, L2 TVL narrative |
| 2026-11-24 | Starknet | Realms Frontier S1, Loot Survivor on Abstract, Xverse multisig + STRK20 |

## Skills Built
| Skill | Date | Notes |
|-------|------|-------|

## Lessons Learned
- Digest format: Markdown with clickable links, under 4000 chars
- Always save files AND commit before logging
- Polymarket data-api v1 `/trades` is retired (HTTP 410); use `/v2/trades?condition_id=` (pm-manipulation SKILL.md still lists v1)
- xAI search calls often time out (http=000) on 6h/12h windows; retry with a wider window or a minimal ~5-post query before falling back

