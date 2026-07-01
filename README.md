# OlaPurse

A personal finance dashboard to track income, expenses, budgets, savings goals, and net worth — built entirely with vanilla JavaScript, HTML, and CSS (no frameworks, no build step). Installable as a Progressive Web App.

**Live demo:** https://olapurse.netlify.app

## Features
- Income tracking (hourly wage or monthly), stored per month with optional recurring carry-forward
- Expense tracking with categories, budget limits, and recurring expenses
- Savings goals with progress tracking
- Net worth tracker (assets vs. liabilities)
- Insights: savings rate, month-over-month spending, average daily spend
- Shareable monthly summary (image + text)
- Live currency converter (10+ currencies, offline caching, fallback API)
- CSV import/export, month/year history
- Multiple local profiles (e.g. Personal / Business) with optional Google sign-in
- Light/dark mode, fully responsive, installable PWA with offline support
- Built-in assistant for spending insights (optional live-AI backend via Netlify Functions)

## Tech
Vanilla JavaScript, HTML, CSS. Data stored locally in the browser (localStorage) — no backend required. Optional serverless function for AI-powered insights.

## Notes
This is a personal/portfolio project. Data lives in the browser on each device; profiles and Google sign-in personalize the app but do not sync across devices.
