Memory flush for 2026-11-24 is done. I promoted two lessons to `memory/MEMORY.md` and added one priority. Nothing was pruned or archived.

- **Window:** 2026-11-23 to 2026-11-24, so I read only `memory/logs/2026-11-23.md`. Log rotation did nothing because only 4 daily files exist, well under the 45-file threshold.
- **Lessons added:**
  - Polymarket data-api v1 `/trades` is retired and returns HTTP 410; use `/v2/trades?condition_id=`. The `pm-manipulation` SKILL.md still lists v1.
  - xAI search calls often time out on 6h/12h windows; retry with a wider window or a minimal ~5-post query before falling back.
- **Priority added:** watch reply-maker, whose quality averaged 2 over 2 runs in the 2026-11-23 skill-health check.
- **Pruning:** there are no open improvement PRs, so no section to maintain. No Skills Built rows or stale lessons exist yet.
- **Watermark:** the log entry is in `memory/logs/2026-11-24.md`, and I stamped the watermark to 2026-11-24.

I didn't send a notification, since the run found nothing that needs a decision.

## Summary
- Modified `memory/MEMORY.md` and `memory/memory-flush-state.json` (watermark stamped to 2026-11-24).
- Created `memory/logs/2026-11-24.md`.
- Follow-up: the `pm-manipulation` SKILL.md should be updated to the v2 trades endpoint.
