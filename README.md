# OlaPurse

**A personal finance dashboard that turns raw income and spending into clear, actionable insight — built from scratch with vanilla JavaScript, HTML, and CSS. No frameworks, no build step, installable as a Progressive Web App.**

🔗 **Live demo:** https://olapurse.netlify.app

---

## Why I built it

I work in analytics (Python · R · SQL), and I wanted a project that paired that data mindset with hands-on frontend engineering — something that wasn't just a chart on a page, but a small product: real data modelling, derived metrics, offline behaviour, and thoughtful UX. OlaPurse started as a simple budget calculator and grew into a full personal-finance dashboard that computes the kind of metrics I'd normally reach for a notebook to produce — savings rate, month-over-month trends, forecasts — and surfaces them live in the browser.

## Analytics & data highlights

The features I'm proudest of are the ones that show data thinking, not just UI:

- **Derived financial metrics** — savings rate, month-over-month spending change, and average daily spend, all recomputed reactively as the underlying data changes.
- **Per-month data model** — income and expenses are stored per month rather than as single global values, so trends and history are truthful rather than a flat line projected backwards.
- **Spending forecast** — projects month-end spend from the current run-rate, honestly labelled as an estimate.
- **Category breakdowns** — donut and trend visualisations rendered on HTML canvas (no charting library), plus budget-limit alerts per category.
- **Net worth tracking** — assets vs. liabilities rolled into a single figure.
- **Live currency data** — 10+ currencies via a primary API with a fallback API and offline caching, so the converter degrades gracefully when a source is unavailable.
- **CSV import/export** — get data in and out for analysis elsewhere.

## Full feature set

- Income tracking (hourly or monthly) with optional recurring carry-forward
- Expense tracking with categories, budgets, and recurring expenses
- Editable transactions and month/year history
- Savings goals with progress tracking
- Net worth tracker
- Insights: savings rate, month-over-month spend, average daily spend
- Shareable monthly summary (generated image + copyable text)
- Currency converter with caching and fallback
- Multiple local profiles (e.g. Personal / Business) with optional **Sign in with Google**
- Built-in assistant that reads your figures on-device to answer spending questions
- Light/dark mode, fully responsive, installable PWA with offline support
- Backup & restore (export/import all data as JSON)

## Architecture & engineering decisions

- **Zero-dependency, single-file core.** The entire app is one `index.html` (inline CSS + JS). No framework, no bundler — a deliberate constraint to keep it fast, portable, and easy to reason about.
- **Client-side persistence.** Data is stored in `localStorage`, namespaced per profile, with migration logic so older saves upgrade cleanly to newer data models.
- **Offline-first PWA.** A service worker uses a **network-first strategy for the page** (so updates reach users immediately when online) while falling back to cache offline — avoiding the classic "stale until hard-refresh" PWA trap.
- **Graceful degradation.** Google sign-in and the live-AI assistant are both optional layers: if they aren't configured, the app quietly falls back to local profiles and an on-device assistant. Nothing breaks.

## Tech stack

`Vanilla JavaScript` · `HTML5` · `CSS3` · `Canvas API` · `Service Workers` · `localStorage` · `Web App Manifest (PWA)`

## Honest scope

This is a personal/portfolio project. Data lives in the browser on each device — profiles and Google sign-in personalise the experience but **do not** sync across devices or act as secure authentication, since the app runs without a backend database. Cloud sync and real accounts would be the natural next step.

## Author

Built by **Olasunkanmi Oladele** — Data Analyst & ML Practitioner (Python · R · SQL), open to analytics and data roles.

- LinkedIn: www.linkedin.com/in/analystolasunkanmi
- Portfolio / contact: olasunkanmi.analytics@gmail.com
