# PM Manipulation Watch — 2026-11-23

**Window:** past 3 days · **Scanned:** 9 markets (union of top-30 by 24h and 7d volume on Polymarket, filtered to geopolitics/election/regulatory) · **Suspicious (≥3):** 3 · **High-confidence (≥4):** 0

## Methodology
3-day price/volume/comment scan + multilingual press sweep. Each candidate scored 0–5 across 6 anomaly classes (see `skills/pm-manipulation/SKILL.md`). Platform: Polymarket (no `memory/topics/prediction-markets.md` override; defaults used).

Implementation notes and limits (read these before trusting the scores):
- `data-api.polymarket.com/trades` (v1) now returns **HTTP 410 (retired)**. Used `data-api.polymarket.com/v2/trades?condition_id=...&limit=500` instead. The 500-trade cap truncates the window on busy markets (e.g. Jensen Huang Dec-31 covers only ~11h of the 72h), so whale share and peak/median volume are **sample-limited** and peak/median is inflated by sparse hourly buckets.
- Top-3 wallet share cannot distinguish market makers from directional whales.
- `concentrated-move` was counted only when |3d net move| ≥ 5pp; with smaller net moves the "% of net in one 6h block" ratio exceeds 100% as a noise artefact.
- Comments endpoint returned nothing for the US-Iran and Israel-Iran ceasefire events.
- Hourly price history carries no volume; volume stats come from the trades sample only.

## Suspicious Markets (score 3 — none corroborated by press asymmetry)

### 1. Will Gadi Eizenkot be the next Prime Minister of Israel? — score 3/5
- **Slug:** `who-will-be-the-next-prime-minister-of-israel-after-the-next-election` (market `will-gadi-eizenkot-be-the-next-prime-minister-of-israel`)
- **3d action:** 62.4¢ → 61.3¢ (−1.1pp net) but swung 67.0¢ high → 57.2¢ low (~10pp) inside the window; whale share (top-3 wallets) 48% of sampled 31h notional (~$137k); peak/median hourly volume 28x.
- **Flags triggered:** `reversal`, `volume-spike`, `whale-concentrated`
- **Comments:** 14 comments in 72h; no bot-burst, no duplicate text. Hebrew-language comments are ordinary political argument.
- **Local press:**
  - he: Ynet — Netanyahu accuses Eizenkot of using the Ra'am-activist detention affair to block a unity government ([ynet](https://www.ynet.co.il/news/article/b1pzzq00rml)).
  - he: Ynet — Eizenkot: "Netanyahu's conduct is a threat to democracy" (`התנהלות נתניהו היא איום על הדמוקרטיה`) ([ynet](https://www.ynet.co.il/news/article/b1nqlkdamx)).
  - he: Ynet — Netanyahu "does not rule out a rotation with Eizenkot" (`לא שולל רוטציה עם איזנקוט`) ([ynet](https://www.ynet.co.il/news/article/yokra14945206)).
  - he: Ynet poll-of-polls / government-formation scenarios — Channel 12 poll gives Eizenkot's bloc 55 seats vs 51 ([ynet](https://www.ynet.co.il/news/elections2026/article/hkj8dy8nfe)).
- **English press:** not separately checked for this market; the story is major domestic political news with live polling, not a local-only scoop.
- **Asymmetry:** n/a
- **Take:** Price swings are consistent with a news-dense week (rotation talk, polls, detention affair). Flags are mechanical; no evidence of a coverage gap that a local-information trader could exploit. Keep on the list, low priority.

### 2. Israel x Iran ceasefire continues through December 31? — score 3/5
- **Slug:** `israel-x-iran-ceasefire-continues-throughptptpt-20260716224448963` (market `israel-x-iran-ceasefire-continues-through-december-31-415`)
- **3d action:** 65.5¢ → 69.5¢ (+4.0pp net); dipped to 59.5¢ then rose to 70.5¢ (~11pp range); top-3 wallets 48% of sampled notional (~$88k over 66h); peak/median 33x.
- **Flags triggered:** `reversal`, `volume-spike`, `whale-concentrated`
- **Comments:** endpoint returned no comments.
- **Local press:**
  - he: Ynet — ceasefire extended "until Sunday" per US update to Israel (`הפסקת האש באיראן הוארכה עד יום ראשון`) ([ynet](https://www.ynet.co.il/news/article/sk3cefltwg)).
  - he: Ynet — government announced ceasefire, Iran fired again; chief of staff: "we will strike with force" ([ynet](https://www.ynet.co.il/news/article/rk8pbpdegg)).
  - he: Ynet — nightly fire and mutual accusations, yet "the ceasefire holds" (`הפסקת האש שנשמרת`) ([ynet](https://www.ynet.co.il/news/article/s1h1abafgl)).
  - ar: Al Jazeera — Iran accuses US and Israel of breaching the ceasefire (2026-06-01; older context, not within the window) ([aljazeera.net](https://www.aljazeera.net/news/2026/6/1/%D8%A5%D9%8A%D8%B1%D8%A7%D9%86-%D8%AA%D8%AA%D9%87%D9%85-%D8%A3%D9%85%D8%B1%D9%8A%D9%83%D8%A7-%D9%88%D8%A5%D8%B3%D8%B1%D8%A7%D8%A6%D9%8A%D9%84-%D8%A8%D9%86%D9%82%D8%B6-%D9%88%D9%82%D9%81)).
- **English press:** ceasefire status is mainstream international news.
- **Asymmetry:** n/a
- **Take:** Dips line up with recurring violation/strike headlines; the sibling "through November 30" market (below) moves in the same pattern, so this looks like shared news-driven volatility rather than one actor.

### 3. Israel x Iran ceasefire continues through November 30? — score 3/5
- **Slug:** same event as #2 (market `israel-x-iran-ceasefire-continues-through-november-30`)
- **3d action:** 86.5¢ → 92.5¢ (+6.0pp); low 78.5¢ → high 93.5¢ (a 15pp rebound); 83% of the 3d move in the single largest 6h block; top-3 wallets only 29%; peak/median 9.8x (marginal).
- **Flags triggered:** `concentrated-move`, `reversal`, `volume-spike` (marginal)
- **Comments:** none returned.
- **Local press / English press / Asymmetry:** as #2 — violations and extensions reported in Hebrew press during the window; no language gap found.
- **Take:** Typical headline-driven repricing after a scare. Whale share is low, which weighs against a single-actor push.

## Watchlist (score 2)
- **Will Jensen Huang rejoin NVIDIA by Dec 31, 2026?** — 5.6¢ → 10.7¢ (+5.2pp), 75% of the move in one 6h block (late in window), top-3 wallets 58% of the *last ~11h only* (sample-limited). English press is dense and explains the interest: board is reportedly not considering a return ([QZ](https://qz.com/nvidia-board-jensen-huang-return-investigation-111626), [CNBC](https://www.cnbc.com/2026/11/16/nvidia-ceo-jensen-huang.html)), while Huang says he is open to returning ([CNBC](https://www.cnbc.com/2026/11/17/nvidia-jensen-huang-statement.html)) amid a petition with 180k+ signatures. Comments: 22 in 72h, one user (`Manumvv`) 4×, no duplicates. A price that rises while the reported board stance is negative is worth a look, but the press does not show a gap. Asymmetry: english-contradicts (board stance) vs. English-confirms (public pressure) — mixed, not scored.
- **Will Benjamin Netanyahu be the next PM of Israel?** — 20.5¢ → 28.4¢ (+7.9pp, spread across the window, 52% in the biggest block), top-3 wallets 48%, peak/median 15.5x. Same event and same news flow as the Eizenkot market; rotation reporting ([ynet](https://www.ynet.co.il/news/article/yokra14945206)) plausibly explains the drift.
- **Will the U.S. invade Iran before 2027?** — 6.5¢ → 5.5¢ (−1.0pp); top-3 wallets 56%, peak/median 203x. Price move is immaterial; flags come from thin trade buckets. No comments available.
- **French 2027 presidential (event `next-french-presidential-election`), de Villepin market** — price flat (2.5¢ → 2.4¢). The event comment thread shows a bot-burst signature (8 accounts matching `imanedepumpfunN`) and a duplicated French spam post ("signalez tous ses messages… les 25k de son portefeuille seront redistribués"), consistent with spam/scam activity rather than price manipulation. Worth noting for the comment-spam pattern only.

## Clean
| Market | 3d change | Why scanned / note |
|---|---|---|
| Taipei mayor — Puma Shen (YES) | 37.4¢ → 29.7¢ (−7.8pp) | Non-US election, 7d vol >$1.1M. Peak/median 15.6x, top-3 40%. Local press explains the drift: six final pre-blackout polls split 3–3 (Shen led in Trust in Democracy Assoc., Fengcan Media, Taiwan Inspiration Assoc.; Chiang led in China Times, ETtoday, TVBS) ([Yahoo TW](https://tw.news.yahoo.com/%E5%8F%B0%E5%8C%97%E5%85%A9%E5%A4%A9%E5%85%AD%E4%BB%BD%E5%B0%81%E9%97%9C%E6%B0%91%E8%AA%BF-%E4%B8%89%E4%BB%BD%E6%B2%88%E4%BC%AF%E6%B4%8B%E9%A0%98%E5%85%88-%E4%B8%89%E4%BB%BD%E8%94%A3%E8%90%AC%E5%AE%89%E9%A0%98%E5%85%88-%E6%9C%80%E5%BE%8C%E6%95%B8%E5%AD%97%E5%90%84%E8%AA%AA%E5%90%84%E8%A9%B1-045638609.html), [China Times](https://www.chinatimes.com/realtimenews/20261116004555-260407)); English press covers the same split ([Taipei Times](https://www.taipeitimes.com/News/front/archives/2026/11/17/2003867865)). Note: Liberty Times (`ltn.com.tw`) results skew toward Shen-leading polls, which a single-outlet read would have mistaken for contradiction. Same on the Chiang Wan-an mirror market (+8pp, 62.5¢ → 70.5¢, spread out, 25% concentration, top-3 38%). No asymmetry; comments show no coordination. |

## Notes for next run
- Taipei mayor election is imminent (polls just went into blackout); Taiwanese markets may see more volatility into election day.
- Skill doc still references the retired v1 trades endpoint; v2 `condition_id=` works and should replace it.
