# Changelog

## v1.0.0 — 2026-03-18

- Initial release
- Timezone converter with 59 cities across 6 regions (Americas, Europe, Africa, Asia, Pacific, UTC)
- Auto-detects local timezone on first load and places it first in the list
- Three modes: **Now** (live clock), **Plan a time** (compare any moment), **Schedule** (pick a start time and meeting duration)
- Quick time presets: Now, Next hour, In 30 min, Tomorrow 9 AM
- Day/night period indicator (☀️ day, 🌅 twilight, 🌙 night) per card, with matching background tints
- Working hours status label per card (Business hours / Early morning / Evening / Late night)
- Schedule mode: meeting end time shown on each card, with +1 day badge on midnight crossovers
- Schedule conflict highlighting (amber border) when start or end falls outside business hours
- Find Meeting Overlap: tiered algorithm scores 48 half-hour slots and suggests the least disruptive times
- 24-hour availability grid in the overlap modal showing all active zones side by side
- Clicking an overlap suggestion populates the time selects and switches to Schedule mode
- Copy Schedule: copies all active zone times (or ranges in Schedule mode) to clipboard
- Per-tile copy button copies that card's time to clipboard
- Download Invite: generates a `.ics` calendar file with RFC 5545-compliant line folding
- Drag-and-drop tile reordering with custom ghost and placeholder
- 12h / 24h time format toggle, persisted across sessions
- Light / dark / system theme with CSS custom properties
- UTC offset display toggle (show/hide)
- Configurable default mode (Now / Plan a time / Schedule)
- Mobile-responsive layout with sticky copy bar at the bottom
- Single static HTML file — no build step, no external dependencies
