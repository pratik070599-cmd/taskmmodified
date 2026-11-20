# TaskFlow — Smart Task Manager

A responsive, local-first task manager built with React, Vite, Tailwind CSS, Lucide React and Recharts.

## Requirements
- Node.js 18+ and npm
- Internet access to install npm dependencies on first setup

## Run locally
```bash
npm install
npm run dev
```
Open the URL shown by Vite (typically http://localhost:5173).

## Build and preview
```bash
npm run build
npm run preview
```

## Automated tests
```bash
npm test
```

## Features
- Create, edit, delete, complete and reopen tasks
- Priorities, categories, descriptions, due dates and completion timestamps
- Search, filters and sorting
- Dashboard metrics, charts, 7-day deadlines
- Interactive month calendar with date selection
- Analytics and productivity metrics
- Light/dark mode and persisted preferences
- LocalStorage persistence, validated JSON import/export
- Responsive desktop and mobile layout

## GitHub
1. Create a new repository on https://github.com/new.
2. Upload **the contents of this folder** (not the ZIP itself). Do not upload `node_modules` or `dist`.
3. Commit changes.

Or via terminal:
```bash
git init
git add .
git commit -m "Initial TaskFlow app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
git push -u origin main
```

## Vercel
1. Visit https://vercel.com/new and import the GitHub repository.
2. Choose **Vite** framework preset (or configure manually).
3. Build command: `npm run build`.
4. Output directory: `dist`.
5. Deploy. No environment variables are required.

## Storage and privacy
Task data is saved to **localStorage in each browser**. It is not synchronized between devices or users. Clearing browser data or switching devices may lose tasks. Export JSON backups regularly. Import **replaces** the existing task list after confirmation.

The `src/services/storage.js` module isolates persistence so a future Supabase integration can replace it.

## Analytics definitions
- Weekly/monthly completion rate = percentage of tasks created in the past 7/30 days that are currently complete.
- Trend = number of tasks marked complete on each day, based on `completedAt`.
- Pending includes all incomplete tasks, including overdue ones.
- Upcoming excludes today and overdue tasks.

## Notes
- This ZIP contains source code, not preinstalled npm packages.
- The app is client-only; no login or email reminders are included.
- Date-only due dates are interpreted in the user's local timezone.
