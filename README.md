# GitHub Insights

Generate your own GitHub stats card to showcase anywhere — LinkedIn, Instagram, your portfolio & more. No tokens, no sign-ups. Just enter a username and download a beautiful PNG.

**Live:** [isfarbaset.github.io/github-insights](https://isfarbaset.github.io/github-insights/)

## Features

- **Lifetime Stats** — Repos, stars, followers, forks, commits, PRs, issues (via GitHub REST + Search APIs)
- **Streak Tracking** — Longest & current daily streaks (via contribution calendar)
- **Developer Personality** — Fun badge based on your activity patterns
- **Peak Coding Time** — Night owl? Early bird? We'll tell you
- **Top Repositories** — Bar chart of your most active repos
- **Monthly Activity** — See which months you were most productive
- **Heatmaps** — Day-of-week and time-of-day activity breakdowns
- **Language Breakdown** — Your top programming languages with color-coded bar
- **Fun Facts** — Bugs squashed, lines of code, cups of coffee
- **Download PNG** — High-res 2× retina card screenshot
- **Share on LinkedIn** — One-click share with auto-generated post text + image

## How It Works

Everything runs **client-side** in the browser — no backend, no API tokens needed.

| Data | Source |
|------|--------|
| Profile, repos, stars, forks | GitHub REST API |
| Lifetime PRs & issues | GitHub Search API |
| Lifetime commits per repo | GitHub Contributors Stats API |
| Daily contribution streaks | [github-contributions-api.jogruber.de](https://github-contributions-api.jogruber.de) |
| Activity patterns (charts) | GitHub Events API (recent ~300 events) |

## Tech Stack

- **HTML / CSS / JS** — No frameworks, no build step
- **html2canvas** — PNG screenshot generation
- **Web Share API** — Native sharing on supported devices
- **GitHub Pages** — Static hosting

## Run Locally

```bash
git clone https://github.com/isfarbaset/github-insights.git
cd github-insights
python3 -m http.server 8090
# Open http://localhost:8090
```

## Deploy

The site is served from the `docs/` folder via GitHub Pages.

To update the deployed version after making changes:

```bash
cp index.html card.css card.js docs/
git add -A && git commit -m "Update site" && git push
```

## API Rate Limits

Without authentication, GitHub allows **60 requests/hour** per IP. For users with many repos, you may occasionally hit limits — just wait a minute and try again.

## Privacy

This project only accesses **public** GitHub data. Nothing is stored, tracked, or sent to any server. Everything runs in your browser.

## License

MIT — feel free to use, modify, and share!
