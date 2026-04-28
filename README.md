# 📊 Dashboarder

**A free, open-source, self-hosted dashboard builder — no server, no account, no subscription.**

Create beautiful full-screen dashboards for wall-mounted displays, smart TVs, tablets, or any screen. Design your layout in the browser, then export a single `dashboard.html` file that runs anywhere.

> Inspired by DAKboard — but completely free and open source.

![Dashboarder Screenshot](screenshot.png)

---

## ✨ Features

### 16 Widget Types
| Widget | Description |
|---|---|
| 🕐 Clock | Time with timezone, 12/24hr, seconds |
| 📆 Date | Standalone date in multiple formats |
| 🌍 World Clock | Multiple cities side by side |
| ⏳ Countdown | Count down to any date/time |
| 🌤 Weather | Live weather via Open-Meteo (no API key needed) |
| 📰 News/RSS | Any RSS feed with auto-scroll |
| 📈 Stocks | Live prices via Yahoo Finance |
| 💬 Quote | Auto-rotating quotes — inspiring, tech, humor, jokes, or custom |
| 📅 Google Calendar | Embed your Google Calendar (Month/Week/Agenda/Day) |
| ✅ To-Do / Tasks | Manual list or sync with Google Tasks |
| 📷 Slideshow | URLs, uploads, Google Photos, or Unsplash categories |
| 🌐 iFrame / Embed | Embed any webpage |
| 🔤 Text | Custom text with rich formatting |
| 📌 Sticky Note | Colorful sticky notes |
| 🗺 Maps | Location view or turn-by-turn directions with travel time |
| ⚙️ Custom HTML | Write any HTML/CSS/JS |

### Builder
- Drag & drop widgets onto a canvas
- Snap to grid with alignment guides
- Duplicate any widget with one click
- Live preview before exporting
- Auto-save every 60 seconds
- 6 built-in layout presets

### Per-Widget Styling
- Font family (12 Google Fonts), font size, content scale
- Background color, opacity, or gradient
- Glass blur (frosted glass effect)
- Border, corner radius, drop shadow
- Accent color
- Content shift (move content inside the card)
- Crop (clip any edge of the widget content)

### Export
- Single `dashboard.html` file — no server needed
- Fully self-contained, works offline (except live data widgets)
- Adaptive scaling: fills any screen size, responds to browser zoom
- All live data fetches on open (weather, stocks, news, quotes, tasks)

---

## 🚀 Quick Start

1. **Download** [`dashboarder.html`](dashboarder.html)
2. **Open it** in any modern browser
3. **Design** your dashboard by dragging widgets onto the canvas
4. **Configure** each widget by clicking it and editing the right panel
5. **Export** with the ⬇ Export HTML button
6. Open your exported `dashboard.html` on any screen

No installation. No account. No internet connection required to run the builder.

---

## 📺 Setting Up a Wall Display

### Raspberry Pi / Any Linux
```bash
# Install Chromium and launch in kiosk mode
chromium-browser --kiosk --noerrdialogs --disable-infobars /path/to/dashboard.html
```

### Windows
```
chrome.exe --kiosk "C:\path\to\dashboard.html"
```

### macOS
```bash
open -a "Google Chrome" --args --kiosk /path/to/dashboard.html
```

### Fire TV / Android TV
Use a browser app (e.g. Firefox, Silk) and navigate to the file, or host it on a local web server.

---

## 📅 Google Calendar Setup

1. Open [Google Calendar](https://calendar.google.com)
2. Click the ⚙️ gear → **Settings**
3. Select your calendar from the left sidebar
4. Scroll to **Integrate calendar**
5. Copy the **Embed code** — grab just the `src="..."` URL inside the `<iframe>` tag
6. Paste into the Google Calendar widget settings in Dashboarder

> The calendar must be set to **Public** for the embed to work.

**Dark mode:** Toggle dark mode in the widget settings. Uses CSS `invert + hue-rotate` to flip the calendar colors.

---

## ✅ Google Tasks Setup

1. Go to [Google OAuth Playground](https://developers.google.com/oauthplayground)
2. Select **Tasks API v1** → `https://www.googleapis.com/auth/tasks.readonly`
3. Click **Authorize APIs** → sign in
4. Click **Exchange authorization code for tokens**
5. Copy the **Refresh token** (lasts forever — not the access token)
6. Paste into the To-Do widget settings → Refresh Token field
7. Click **Sync Tasks Now**

---

## 🌤 Weather Setup

Weather works automatically with no API key using [Open-Meteo](https://open-meteo.com/) (free, open source).

- Leave location blank to use GPS (asks permission when the dashboard opens)
- Or type a city name like `Tampa, FL`

**Optional: Tomorrow.io widget** — for a richer weather display, sign up free at [tomorrow.io](https://tomorrow.io), get an API key, and enable the Tomorrow.io toggle in weather settings.

---

## 📰 RSS Feeds

The news widget works with any RSS/Atom feed. Some suggestions:

| Category | Feed |
|---|---|
| 🌟 Good News | `https://www.goodnewsnetwork.org/feed/` |
| 💻 Tech | `https://techcrunch.com/feed/` |
| 🌍 World | `https://feeds.bbci.co.uk/news/world/rss.xml` |
| 🔬 Science | `https://www.sciencedaily.com/rss/top/science.xml` |
| 🚀 Space | `https://feeds.feedburner.com/NasaBreakingNews` |

---

## 🏗 Project Structure

```
dashboarder/
├── dashboarder.html     # The entire builder — one file
├── screenshot.png       # Screenshot for README
├── README.md            # This file
├── LICENSE              # MIT License
└── examples/
    └── dashboard.html   # Example exported dashboard
```

The entire project is a **single HTML file** (~140KB). There is no build step, no npm, no dependencies.

---

## 🤝 Contributing

Contributions are welcome! Ideas for V2:

- [ ] More widget types (Spotify Now Playing, Home Assistant, Notion, Trello)
- [ ] Community layout marketplace
- [ ] Portrait mode (1080×1920) for vertically mounted screens
- [ ] Multiple pages / slides
- [ ] Password/PIN lock for kiosk mode
- [ ] Screensaver / sleep mode after inactivity
- [ ] WebDAV / local network sync for layouts
- [ ] PWA support

To contribute:
1. Fork the repository
2. Make your changes to `dashboarder.html`
3. Test in Chrome, Firefox, and Safari
4. Submit a pull request with a clear description

---

## 📄 License

MIT License — free to use, modify, and distribute. See [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgements

- [Open-Meteo](https://open-meteo.com/) — free weather API
- [Quotable.io](https://quotable.io/) — free quotes API
- [JokeAPI](https://v2.jokeapi.dev/) — free jokes API
- [RSS2JSON](https://rss2json.com/) — RSS to JSON proxy
- [Picsum Photos](https://picsum.photos/) — Unsplash-style random images
- [Google Fonts](https://fonts.google.com/) — typography

---

*Built with ❤️ — no servers, no subscriptions, just a single HTML file.*
