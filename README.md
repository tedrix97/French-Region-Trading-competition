# Weltrade Africa — Affiliate Competition Leaderboard

Static leaderboard for GitHub Pages. No build step, no backend.

| File | Who uses it | Upload to GitHub? |
|---|---|---|
| `index.html` | Partners. The public leaderboard page. | Yes |
| `data.js` | Holds all the figures. The only file you edit each day. | Yes |
| `admin.html` | You. CSV preview and the daily data generator. | **No.** Keep it on your computer, in the same folder as `data.js`. |
| `README.md` | These instructions. | Yes |

GitHub Pages sites are public. Anything you upload can be opened by anyone with the link, so leave `admin.html` out of the repository.

## Scoring

| KPI | Weight |
|---|---|
| Net deposit (deposits minus withdrawals, USD) | 35% |
| FTDs (first-time deposits in the window) | 35% |
| Active clients (clients who traded in the window) | 15% |
| SpreadPay (spread-based payout, USD) | 15% |

KPI points = (affiliate's result ÷ best result among all affiliates) × weight.
Score = the four KPI points added together, out of 100. A negative net deposit scores 0 for that KPI.
At close, the top 3 scores are selected. Ties go to more FTDs, then higher net deposit.

Open to every Weltrade affiliate.

Scoring window: 25 Nov 2026 00:00 to 31 Dec 2026 23:59, Kigali time (UTC+2). The countdown on the page switches to "Day X of 37" automatically at launch.

## First publication

1. Sign in at github.com and click **New repository**. Name it, for example, `affiliate-leaderboard`. Set it to **Public**.
2. On the empty repository, click **uploading an existing file**.
3. Drag in `index.html`, `data.js` and `README.md`. Put them in the root, not in a folder.
4. Commit with a message such as `initial leaderboard`.
5. Go to **Settings → Pages**. Under Source choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
6. Wait two or three minutes and refresh. The live link appears at the top: `https://<username>.github.io/<repository>/`
7. Open the link on a phone before sharing it with partners.

## Launch state

- `data.js` ships **empty**. Until the first upload, the page shows the countdown, the scoring rules, and a "Standings open soon" message in the table.
- The competition opens on **25 November 2026**. The **first upload is on 26 November**, with the figures from 25 November.
- No other setting needs changing at launch.

## Daily update (about 5 minutes)

1. Export each affiliate's totals for the window so far: net deposit, FTDs, active clients, SpreadPay.
2. Open `admin.html` on your computer (double-click it). Go to **Daily update**.
3. Paste the figures as CSV, one affiliate per line:
   `affiliate_id,net_deposit,ftd,active,spreadpay`
4. Press **Preview standings** and check the Leaderboard tab.
5. Press **Copy new data.js**. It builds the complete file with today's date and adds today's top 3 to the history.
6. On GitHub, open `data.js`, click the pencil icon, select everything, paste, and **Commit changes**.
7. The live page updates within a few minutes. Save the new `data.js` on your computer as well, so `admin.html` starts from the latest figures next time.

## Checks before sharing the link

- The affiliate count matches your official list.
- Every affiliate ID in `data.js` is spelled the way partners know it.
- The page looks right on a phone, with no sideways scrolling.
