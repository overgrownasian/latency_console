# Latency Console

**Client-side network diagnostics dashboard for schools, enterprises, and home labs.**Latency Console is a lightweight HTML/JS tool that continuously probes defined endpoints, measures latency, and visualizes the results with sparklines, averages, jitter, and CSV exports — all directly in your browser. No server component is required.

---

## Features

- 🌐 **Client-side only** — runs fully in the browser, no backend needed.
- 📊 **Live latency monitoring** — last, min, max, average, and jitter per service.
- 📉 **Sparklines** — quick glance at performance trends, with zoomable charts.
- 🎨 **Dark/Light mode** — toggle theme with a single click.
- ⚡ **Configurable thresholds** — set “Good” and “Warn” latency levels.
- 📝 **CSV export** — export per-service or all results with timestamps.
- 🔄 **Dynamic targets** — auto-reloads a JSON file of endpoints so your test list stays fresh.

---

## Getting Started

### 1. Clone or Download

```bash
git clone https://github.com/yourusername/latency-console.git
cd latency-console
```

### 2. Serve the Files

Because browsers restrict local file access, you should serve the project with a simple webserver:

```bash
# Python 3
python -m http.server 8080
```

Then open [http://localhost:8080/index.html](http://localhost:8080/index.html) in your browser.

---

## Configuration

Targets are defined in [`targets.json`](targets.json):

```json
[
  { "name": "Google", "url": "https://8.8.8.8" },
  { "name": "Microsoft", "url": "http://www.msftconnecttest.com/" },
  { "name": "Clever", "url": "https://status.clever.com" },
  { "name": "Youtube", "url": "https://youtube.com" },
  { "name": "Google Docs", "url": "https://docs.google.com" },
  { "name": "Google Drive", "url": "https://drive.google.com" },
  { "name": "Google Classroom", "url": "https://classroom.google.com" },
  { "name": "Google Meet", "url": "https://meet.google.com" },
  { "name": "Google Calendar", "url": "https://calendar.google.com" },
  { "name": "Google Sites", "url": "https://sites.google.com" },
  { "name": "Google Slides", "url": "https://slides.google.com" },
  { "name": "Google Sheets", "url": "https://sheets.google.com" },
  { "name": "Google Forms", "url": "https://forms.google.com" },
  { "name": "Google Keep", "url": "https://keep.google.com" },
  { "name": "Google Jamboard", "url": "https://jamboard.google.com" },
  { "name": "Kahoot", "url": "https://kahoot.it" },
  { "name": "Quizlet", "url": "https://quizlet.com" },
  { "name": "Edpuzzle", "url": "https://edpuzzle.com" },
  { "name": "Padlet", "url": "https://padlet.com" },
  { "name": "Nearpod", "url": "https://nearpod.com" },
  { "name": "Flipgrid", "url": "https://flipgrid.com" },
  { "name": "ClassDojo", "url": "https://www.classdojo.com" },
  { "name": "Remind", "url": "https://www.remind.com" },
  { "name": "Microsoft Teams", "url": "https://teams.microsoft.com" },
  { "name": "Zoom", "url": "https://zoom.us" }]
```

- **name**: Display name in the dashboard
- **url**: Probe target (HTTP(S) or IP)

You can update this file at runtime — the dashboard reloads it automatically every 60 seconds.

---

## Usage

1. Monitoring begins at page load.
2. Adjust thresholds for "Good" and "Warn" latency.
3. Click sparklines to open a larger chart with tooltip details.
4. Export results for analysis or archiving.
5. Keep the page visible while testing — background tabs may pause timers.


## License

MIT License — feel free to use, modify, and share.
