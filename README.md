# Solstice — Easy Time Zone Converter

> A zero-dependency, single-file time zone converter. No build step. No frameworks. Just open `index.html`.

---

## Features

- **Live clock** — ticks every second across all your selected time zones
- **Custom time mode** — pick any date & time to see what it is around the world simultaneously
- **53 cities across 6 regions** — UTC, Americas, Europe, Africa, Asia, and Pacific
- **Add / remove zones** — curated dropdown prevents duplicates; cards animate in and out smoothly
- **Copy Schedule** — one-click copy of the current time across all active zones
- **12 / 24-hour toggle** — switch time format globally from the settings panel
- **Light / Dark / System theme** — respects your OS preference by default
- **Persistent settings** — your zones, theme, and time format preferences are saved and restored on every visit
- **Works on all devices** — fully responsive layout that adapts seamlessly from mobile to desktop

---

## Getting Started

No installation. No dependencies. Zero config.

```bash
# Repository link will be added later
open index.html   # or just double-click it
```

That's it. Everything — HTML, CSS, and JavaScript — lives in a single file.

---

## Zone Catalogue

53 hand-picked cities organised by region:

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

1. **Add a zone** — select a city from the *+ Add time zone* dropdown in the toolbar.
2. **Remove a zone** — hover over a card and click the X that appears.
3. **Switch to Custom mode** — click **Custom** in the toolbar, then pick any date and time.
4. **Change time format or theme** — click the gear icon (top-right) to open the settings panel.
5. **Copy schedule** — click **Copy Schedule** to copy all current zone times to your clipboard.
6. **Clear all** — click **Clear All** to reset to the default 5 zones.

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

Stored in `localStorage` and restored on every visit.

---

## Browser Compatibility

| Browser | Minimum Version |
|---------|-----------------|
| Chrome  | 95+             |
| Firefox | 97+             |
| Safari  | 15.4+           |

Requires `Intl.DateTimeFormat` with `timeZoneName: 'longOffset'` support. A graceful fallback is in place for older environments.

---

## Built With

- **Vanilla HTML / CSS / JavaScript** — no frameworks, no libraries
- **`Intl.DateTimeFormat`** — for all time formatting and UTC offset calculations
- **`localStorage`** — for persisting zones and settings across sessions
