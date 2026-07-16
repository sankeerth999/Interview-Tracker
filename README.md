# Interview Tracker

A lightweight, zero-dependency browser app for tracking graduate school (or any) interview invitations. Runs entirely in Safari on iPhone and laptop — no server, no install, no account required.

---

## Features

- **Tiles** for each school — name, interview date, optional notes
- **Rank ordering** — drag tiles or use arrow buttons to set your preference ranking
- **Sort modes** — toggle between "By Rank" and "By Date" at any time
- **Unscheduled badge** — schools without a date are clearly marked
- **Past interview** indicator — completed interviews are visually distinguished
- **Add / Edit / Delete** schools via a modal form
- **Export / Import JSON** — back up your data or transfer between devices
- **localStorage persistence** — data is saved automatically in your browser

---

## Getting Started

### Open locally

```bash
open index.html   # macOS
```

Or just double-click `index.html` in Finder — it opens in your default browser.

### iPhone (Safari)

1. AirDrop `index.html` to your iPhone
2. Tap **Open in Safari**
3. Tap the Share icon → **Add to Home Screen** for an app-like shortcut

---

## Data Storage

All data is stored in **browser localStorage**. Nothing is sent to a server.

| Scenario | Behavior |
|----------|----------|
| Normal browsing | Data persists automatically across sessions |
| Clear browser history / site data | Data is wiped — export a backup first |
| Private / Incognito mode | Data is lost when the tab closes |
| Moving to a new device | Export on old device, import on new |

### Backup & Restore

- Click **Export** in the header to download `interview-tracker.json`
- Click **Import** and select a previously exported file to restore

---

## Project Structure

```
interview-tracker/
  index.html      # The entire app — HTML, CSS, and JS in one file
  README.md       # This file
  .gitignore      # Git ignore rules
```

The app is intentionally a single file. No build tools, no `node_modules`, no framework. The only external dependency is [SortableJS](https://sortablejs.github.io/Sortable/) loaded from a CDN for drag-and-drop support.

---

## Usage

### Adding a school

1. Tap **+ Add**
2. Enter the school name (required)
3. Optionally set an interview date and notes
4. Tap **Save**

New schools are added at the bottom of the rank list.

### Reordering / changing rank

- **Drag** the `⋮⋮` handle on the left of any tile (works with touch on iPhone)
- Or use the **▲ ▼ arrow buttons** on the right of each tile

Rank numbers update automatically. Reordering is only available in "By Rank" sort mode.

### Sorting by date

Click **By Date** in the header. Schools with no date appear at the bottom. This is a view-only sort — it does not change your saved ranks.

---

## Browser Compatibility

| Browser | Support |
|---------|---------|
| Safari (iPhone, iPad) | Full |
| Safari (macOS) | Full |
| Chrome / Firefox / Edge | Full |

---

## License

MIT — do whatever you want with it.
