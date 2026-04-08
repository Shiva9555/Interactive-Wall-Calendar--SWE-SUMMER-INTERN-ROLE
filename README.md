# 🗓️ Interactive Wall Calendar — Premium React Component

A stunning, interactive Wall Calendar component built with React 18 that faithfully emulates a **physical wall calendar aesthetic**. Features spiral binding, hero imagery with diagonal accent overlays, day range selection, integrated lined notes, dark/light theme toggle, holiday markers, and fully responsive design — all without a build step.

---

## ✨ Features

### Core
- **Wall Calendar Aesthetic** — Spiral binding, paper texture, page curl, and a prominent hero image panel with a blue diagonal accent overlay matching the reference design.
- **Day Range Selector** — Click a start date, then an end date. Visual states include: selected start, selected end, in-range highlight, and hover preview.
- **Integrated Notes Section** — Ruled-line notepad area. Notes are contextual: tied to a specific date, date range, or the general month. Persisted to `localStorage`.
- **Fully Responsive** — Adapts from large desktop (560px card) down to mobile full-bleed layout.

### Creative Extras
- **🌗 Dark / Light Theme Toggle** — One-click toggle with smooth transitions.
- **📅 Holiday Markers** — US holidays with gold indicator dots and hover tooltips.
- **📝 Note Indicators** — Green dots on days that have notes.
- **🔄 Month Flip Animation** — Smooth page-transition effect when navigating months.
- **📌 "Today" Quick Button** — Appears when you navigate away from the current month.
- **🎨 Page Curl Effect** — Subtle corner curl for tactile paper realism.
- **📊 Color Legend** — Clear legend bar explaining all visual indicators.
- **♿ Accessibility** — Keyboard navigation, ARIA labels, focus-visible outlines, and `prefers-reduced-motion` support.

---

## 🚀 How to Run Locally

This project uses **zero build tools**. React 18 + Babel are loaded from CDN.

### Option 1 — VS Code Live Server
1. Open the project folder in VS Code
2. Install the **Live Server** extension
3. Right-click `index.html` → **"Open with Live Server"**

### Option 2 — Python
```bash
cd interactive-calendar
python -m http.server 8000
# Open http://localhost:8000
```

### Option 3 — Node / npx
```bash
cd interactive-calendar
npx serve .
```

### Option 4 — Just open it
Double-click `index.html` in your file browser (Babel may have CORS limitations with `file://` in some browsers).

---

## 📁 Project Structure

```
interactive-calendar/
├── index.html          # Main app — React component + Babel JSX
├── styles.css          # Complete design system (vanilla CSS)
├── calendar_hero.png   # Hero image for the calendar
├── hero.png            # Alternate hero image
└── README.md           # This file
```

---

## 🏗️ Architecture & Design Decisions

| Decision | Rationale |
|---|---|
| **Standalone React (CDN)** | No Node/npm required. Babel Standalone processes JSX in-browser. |
| **Monday-start grid** | Matches the reference image's European-style calendar layout. |
| **Vanilla CSS with Custom Properties** | Full theming support (dark/light) via CSS variables. No framework overhead. |
| **`localStorage` persistence** | Notes survive page reloads. Zero backend needed. |
| **`React.memo` on DayCell** | Performance optimization — prevents unnecessary re-renders of 30+ cells. |
| **CSS Grid layout** | Semantic, accessible 7-column grid for the calendar days. |

---

## 📱 Responsive Breakpoints

| Breakpoint | Layout |
|---|---|
| `≥1200px` | Large card (560px max), 16:10 hero |
| `769–1199px` | Standard card (520px), 4:3 hero |
| `421–768px` | Tablet — full-width card, 16:9 hero |
| `≤420px` | Mobile full-bleed — no border-radius, compact sizing |

---

## 🎨 Design Inspiration

The component draws direct inspiration from the provided wall calendar reference image:
- **Spiral binding** along the top edge
- **Hero image** with blue diagonal accent overlay
- **Month + Year label** positioned on the diagonal
- **Clean date grid** with weekend highlighting in red
- **Integrated notes area** below the calendar grid

---

## 📄 License

MIT — Free for personal and commercial use.
