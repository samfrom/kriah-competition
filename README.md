# Kriah Competition - Hebrew Reading Challenge

A competitive Hebrew reading app for multiple players, featuring weekly parsha readings from the Torah.

## How to Run

Just open `index.html` in any modern browser (Chrome, Edge, Firefox). No installation needed.

For PWA support (Add to Home Screen), serve over HTTPS or localhost.

## Features

- **This Week's Parsha**: Auto-detects the current parsha via Hebcal API and puts a prominent "Play Now" shortcut on the dashboard
- **Parsha Text Display**: Shows the Rishon (first aliyah) of each parsha, pulled live from Sefaria (with localStorage caching for speed)
- **Audio Recording**: Record readings directly in the browser using your microphone
- **File Upload**: Upload pre-recorded audio files as an alternative to live recording
- **Speed Scoring**: Automatic scoring based on reading pace (words per minute)
- **Accuracy Scoring**: Judge-rated scoring for pronunciation, fluency, and confidence
- **Bonus Points**: Earn extra points for perfect reads, speed achievements, and great overall scores
- **Seasons**: Each book of the Torah is a "season" with its own standings
- **Rank Progression**: Players advance through ranks from Talmid to Gaon
- **Leaderboard**: Career stats, season standings, and all-time records
- **Multi-Player**: Supports up to 6 players. Select any 2 to compete each round.
- **Head-to-Head Stats**: Win/loss records between competitors shown on the dashboard
- **Streak Tracking**: Weekly participation streaks with flame indicators
- **Previous Scores**: See past scores on each parsha page before re-competing
- **Data Backup**: Export and import all competition data as JSON
- **Navigation Guard**: Warns before accidentally leaving mid-round
- **PWA Support**: Add to Home Screen for a native app experience (when served over HTTPS)
- **Persistent Data**: All scores saved in your browser's localStorage

## Rank System

| Rank | Hebrew | Points | Description |
|------|--------|--------|-------------|
| Talmid | תלמיד | 0+ | Student |
| Chaver | חבר | 150+ | Scholar |
| Baki | בקי | 400+ | Expert |
| Rav | רב | 800+ | Master |
| Gaon | גאון | 1500+ | Genius |

## How It Works

1. **Set up players**: Add up to 6 competitors
2. **Pick a parsha**: Use the "This Week's Parsha" shortcut or browse by season/book
3. **Select competitors**: Choose which 2 players will compete (auto-selected if only 2 registered)
4. **Read the text**: View the Rishon of the parsha (pulled from Sefaria, cached locally)
5. **Record**: Each player records their reading (live mic or upload a file)
6. **Score**: A judge rates each reading for pronunciation, fluency, and confidence
7. **Results**: See the winner, bonus points, streaks, and career rank progression

## Scoring

- **Speed Score (0-50)**: Automatic, based on words per minute. Sweet spot is 80-120 wpm.
- **Accuracy Score (0-50)**: Judge rates pronunciation (0-20), fluency (0-15), confidence (0-15).
- **Bonuses**: Perfect Read (+15), Speed Demon (+10), Outstanding (+10), Great Job (+5).
- **Max possible per round**: 100 base + 35 bonus = 135 points.

## Data Management

- **Export**: Go to Players page and tap "Export Data" to download a JSON backup
- **Import**: Tap "Import Backup" and select a previously exported JSON file
- **Reset**: Use "Reset all data" at the bottom of the Players page to start fresh

## Tech

- Single HTML file, no build step required
- React 18 (via CDN)
- Tailwind CSS (via CDN)
- Sefaria API for Hebrew Torah text (responses cached in localStorage)
- Hebcal API for this week's parsha detection
- Web MediaRecorder API for audio recording
- localStorage for data persistence
- PWA manifest + service worker for installability
