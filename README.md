# GitHub Insights 2025

A year-in-review insights report for your GitHub activity. See your stats, streaks, top repositories, and discover who you've been as a developer this past year.

**Live Demo:** https://isfarbaset.github.io/github-insights/

## Quick Start

```bash
# 1. Clone and enter the repo
git clone https://github.com/isfarbaset/github-insights.git
cd github-insights

# 2. Install dependencies
pip install requests

# 3. Edit index.qmd and change GITHUB_USERNAME to your username

# 4. Render with your GitHub token
GITHUB_TOKEN="your_token_here" quarto render

# 5. Your report is in docs/index.html - open it or deploy to GitHub Pages
```

## Features

- **Stats Overview**: Total commits, PRs, issues, and repositories contributed to
- **Streak Tracking**: See your longest and current coding streaks
- **Developer Personality**: Fun personality badge based on your activity
- **Top Repositories**: Bar chart of your most active repos with medals
- **Monthly Contributions**: See which month you were most productive
- **Activity Heatmaps**: When do you code? Day of week and time of day analysis
- **Language Breakdown**: What programming languages did you use?
- **Fun Facts**: Entertaining stats about your coding year

## Setup

### Prerequisites

- Python 3.8+
- [Quarto CLI](https://quarto.org/docs/get-started/)
  ```bash
  # macOS
  brew install quarto
  
  # Or download from https://quarto.org/docs/get-started/
  ```
- GitHub Personal Access Token

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/isfarbaset/github-insights.git
   cd github-insights
   ```

2. Install Python dependencies:
   ```bash
   pip install requests
   ```

3. Create a GitHub Personal Access Token:
   - Go to GitHub → Settings → Developer Settings → Personal Access Tokens → [Tokens (classic)](https://github.com/settings/tokens)
   - Click "Generate new token (classic)"
   - Select scopes: `public_repo` and `read:user`
   - Copy the token

4. Edit `index.qmd` and change the `GITHUB_USERNAME` variable (line 21) to your GitHub username:
   ```python
   GITHUB_USERNAME = "your_username_here"
   ```

### Render

To generate your GitHub Insights report:

```bash
GITHUB_TOKEN="your_token_here" quarto render
```

The output will be in the `docs/` folder, ready for GitHub Pages.

### Deploy to GitHub Pages

1. Push the `docs/` folder to your repository
2. Go to your repo Settings > Pages
3. Set source to "Deploy from a branch" and select `main` branch, `/docs` folder
4. Your GitHub Insights will be live at `https://yourusername.github.io/github-insights/`

## Customization

### Change the Year

Edit the `YEAR` variable in `index.qmd`:
```python
YEAR = 2025
```

### Styling

Modify `styles.css` to customize colors, fonts, and layout. The main GitHub color variables:

```css
:root {
  --gh-dark: #0d1117;
  --gh-green: #238636;
  --gh-blue: #58a6ff;
  --gh-purple: #a371f7;
  --gh-orange: #d29922;
}
```

## API Rate Limits

Without authentication, GitHub API allows 60 requests per hour. With a personal access token, you get 5,000 requests per hour. The GraphQL API (used for accurate contribution data) requires authentication.

## Privacy

This project only accesses public GitHub data. Your personal access token is only stored locally and never transmitted to any third party.

## License

MIT License - feel free to use, modify, and share!
