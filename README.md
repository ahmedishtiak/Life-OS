# Life OS

A single-file personal dashboard. Your data lives in your browser. Nothing is sent anywhere.

## Deploy to GitHub Pages

The whole app is one HTML file. There is no build step.

### Quickest path (5 minutes)

1. **Create a new repository** on GitHub.
   - You can name it anything. If you name it `<your-username>.github.io`, it deploys at the root of your GitHub Pages domain. Any other name deploys to `<your-username>.github.io/<repo-name>/`.

2. **Upload `index.html`** to the root of the repo.
   - Either via the GitHub web UI (Add file → Upload files), or via git clone + commit.

3. **Enable GitHub Pages**.
   - Repo → **Settings** → **Pages**.
   - Source: **Deploy from a branch**.
   - Branch: `main` (or `master`), folder: `/ (root)`.
   - Save.

4. **Wait 1–2 minutes**, then open the URL GitHub shows you on the same Pages screen.
   - Bookmark it. This is your dashboard.

That's it. The site is now live.

### Optional: make it private

GitHub Pages requires a **public** repository on the free plan. If you want privacy:

- **Option A:** Pay for GitHub Pro ($4/month) to enable Pages on private repos.
- **Option B:** Host elsewhere — Netlify, Vercel, or Cloudflare Pages all support private repos on their free tiers.
- **Option C:** Keep the repo public but understand that **your data is never in the repo** — it lives in your browser's localStorage, not in the HTML. So even with a public repo, your tasks and finances are private to your browser.

For most uses, Option C is sufficient and free.

## How your data works

All data is stored in your browser via **localStorage**, scoped to the exact URL where the app is loaded. This means:

- **Per-browser, per-device.** If you open the same URL in Chrome and Safari, they have separate data. Likewise phone vs laptop.
- **Cleared if you clear browser data.** Always export regularly.
- **Never sent anywhere.** No server, no analytics, no telemetry.

### Backing up

**Settings → Backup → Export JSON** downloads everything as a `.json` file. Do this monthly. Save the file to:

- Proton Drive / your encrypted vault, **or**
- A private git repo, **or**
- Any other backup destination you trust

To restore on a new device or after clearing data: **Settings → Backup → Import JSON**.

### Syncing across devices

This app is intentionally local-only. If you need true sync between phone and laptop, two options:

1. **Use the same browser profile** with sync enabled (Chrome sync, Firefox sync, etc.). localStorage syncs in some configurations — verify first.
2. **Manual export/import** weekly. Tedious but bulletproof.

The deeper truth: for life-management data, *not* syncing is sometimes a feature. Phone capture vs. desktop review can be a discipline rather than a problem.

## Customizing

The file is self-contained HTML + CSS + JS. To change:

- **Your name and city:** Settings page, no code edit needed.
- **Colors and fonts:** edit the `:root` CSS variables near the top of the `<style>` block.
- **Quotes:** edit the `QUOTES` array in the `<script>` block.
- **Default data shape:** edit `DEFAULT_DATA` if you want different starter modules.

## What this app is and isn't

**Is:** a personal command center. Tasks, deadlines, net worth snapshots, Finnish learning, job applications, contacts, knowledge notes, a document vault index.

**Isn't:** a replacement for your bank app, your Excel financial models, your calendar, or your password manager. Those are linked from inside this dashboard but live in their proper homes.

## Two pieces that live together

This dashboard is one part of a three-part system:

1. **`Life_OS_Design.md`** — the architecture document. Read once, refer to during quarterly reviews.
2. **`Life_OS_Finance_Tracker.xlsx`** — the deep finance workbook. Update monthly.
3. **`index.html`** — this dashboard. Daily use.

The HTML is the day-to-day interface. The Excel is the deep audit. The Markdown is the source of truth for *how the system works*.

## Keyboard shortcuts

- `/` — focus the quick-capture input
- `Esc` — close any open modal

## Privacy and licensing

Your data is yours. The code is yours to modify. No warranty — this is a personal tool, not a product.

— Built around the Life OS design document.
