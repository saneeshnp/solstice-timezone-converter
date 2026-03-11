# 🌍 Solstice — Easy Time Zone Converter

> Compare times across the world instantly. No install. No sign-up. No nonsense.

**[▶ Try it live →](https://saneeshnp.github.io/solstice-timezone-converter/)**

---

## What is it?

Solstice is a beautifully minimal, fully static time zone converter that runs entirely in your browser. It's a single HTML file — no build step, no frameworks, no dependencies. Clone it, open it, done.

Whether you're scheduling a call with a colleague in Tokyo, figuring out if your São Paulo contact is awake yet, or planning a meeting across four continents — Solstice gives you the answer at a glance.

---

## Features

- **Live clock** — ticks every second across all your selected time zones
- **Plan a time** — pick any date & time to see what it looks like around the world simultaneously
- **Schedule mode** — set a start time and duration; see the meeting window on every card, with conflict warnings for unsociable hours
- **Find Meeting Overlap** — automatically surfaces the best time slots where everyone is in business hours
- **Download Calendar Invite** — generate and download a `.ics` file to share with attendees
- **59 cities across 6 regions** — UTC, Americas, Europe, Africa, Asia, and Pacific
- **Day / Night indicators** — ☀️ 🌅 🌙 at a glance for every zone
- **12 / 24-hour toggle** — switch time format globally from the settings panel
- **Light / Dark / System theme** — respects your OS preference by default
- **Drag to reorder** — arrange cards in any order you like
- **Copy Schedule** — one-click copy of all current zone times to your clipboard
- **Persistent settings** — your zones, theme, and preferences are saved and restored on every visit
- **Fully responsive** — works seamlessly from mobile to desktop

---

## Getting Started

```bash
git clone https://github.com/saneeshnp/solstice-timezone-converter.git
cd solstice-timezone-converter
open index.html   # or just double-click it
```

No `npm install`. No config files. Everything — HTML, CSS, and JavaScript — lives in a single file.

Or just **[run it in your browser right now](https://saneeshnp.github.io/solstice-timezone-converter/)**.

---

## Zone Catalogue

59 hand-picked cities organised by region:

| Region   | Sample Cities                                      |
|----------|----------------------------------------------------|
| UTC      | UTC                                                |
| Americas | Honolulu, Vancouver, New York, São Paulo           |
| Europe   | London, Paris, Berlin, Moscow, Istanbul            |
| Africa   | Cairo, Lagos, Nairobi, Johannesburg                |
| Asia     | Dubai, Mumbai, Bangkok, Singapore, Tokyo           |
| Pacific  | Perth, Sydney, Melbourne, Auckland, Fiji           |

---

## How to Use

1. **Add a zone** — select a city from the *+ Add time zone* dropdown in the toolbar
2. **Remove a zone** — hover over a card and click the ✕ that appears
3. **Plan a time** — click **Plan a time** in the toolbar, then pick any date and time
4. **Schedule a meeting** — click **Schedule**, set a start time and duration; conflict cards highlight automatically
5. **Find the best slot** — click **Find Overlap** to see tiered suggestions ranked by convenience
6. **Download an invite** — in Schedule mode, click **Download Invite** to export a `.ics` calendar file
7. **Change format or theme** — click the ⚙️ icon (top-right) to open the settings panel

---

## Architecture

| Concern         | Approach                                                        |
|-----------------|-----------------------------------------------------------------|
| Time formatting | `Intl.DateTimeFormat` — no external date libraries             |
| Theming         | CSS custom properties + `data-theme` attribute                 |
| State           | Plain JS variables; persisted to `localStorage`                |
| Animations      | CSS transitions triggered via double `requestAnimationFrame`   |
| Structure       | Single file (`index.html`); no build step, no bundler          |

### Default time zones (on first load)

```
UTC · America/New_York · Europe/London · Asia/Kolkata · Asia/Tokyo
```

Your local zone is auto-detected and placed first. Stored in `localStorage` and restored on every visit.

---

## Browser Compatibility

| Browser | Minimum Version |
|---------|-----------------|
| Chrome  | 95+             |
| Firefox | 97+             |
| Safari  | 15.4+           |

Requires `Intl.DateTimeFormat` with `timeZoneName: 'longOffset'` support. A graceful fallback is in place for older environments.

---

## Contributing

Found a bug? Have a city you'd love to see added? PRs and issues are welcome over at the [GitHub repository](https://github.com/saneeshnp/solstice-timezone-converter).

---

## Built With

- **Vanilla HTML / CSS / JavaScript** — no frameworks, no libraries
- **`Intl.DateTimeFormat`** — for all time formatting and UTC offset calculations
- **`localStorage`** — for persisting zones and settings across sessions
