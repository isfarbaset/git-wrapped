# GitHub Insights

Generate your own GitHub stats card. Enter a username, get a downloadable PNG you can share on LinkedIn, add to your portfolio, or post anywhere.

**Live:** [isfarbaset.github.io/github-insights](https://isfarbaset.github.io/github-insights/)

![Preview](preview.png)

## Features

- Lifetime stats: repos, stars, followers, forks, commits, PRs, issues
- Longest and current daily streaks
- Developer personality badge and peak coding time
- Top repositories bar chart
- Monthly, day-of-week, and time-of-day activity breakdowns
- Top languages with color-coded bar
- Fun facts
- Download as high-res PNG
- One-click LinkedIn sharing

## Rate Limits

GitHub allows 60 API requests per hour without a token. If you hit the limit, click "Add GitHub token" on the page and paste a personal access token to get 5,000 requests per hour.

You can create a token here: [github.com/settings/tokens](https://github.com/settings/tokens/new?scopes=public_repo,read:user&description=GitHub+Insights)

Your token is stored in your browser's local storage only. It is never sent anywhere other than GitHub's API.

## Run Locally

```bash
git clone https://github.com/isfarbaset/github-insights.git
cd github-insights
python3 -m http.server 8090
# Open http://localhost:8090
```

## Deploy

Served from the `docs/` folder via GitHub Pages. After making changes:

```bash
cp index.html card.css card.js docs/
git add -A && git commit -m "Update site" && git push
```

## License

MIT
