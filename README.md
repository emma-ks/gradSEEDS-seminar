# SEEDS Seminar Website

Live site → `https://emma-ks.github.io/seeds-seminar`

## Setup: GitHub Pages (one-time, ~5 minutes)

### 1. Create the repository
1. Go to [github.com/new](https://github.com/new)
2. Name it `seeds-seminar`
3. Set it to **Public**
4. Click **Create repository**

### 2. Upload the file
1. On the new repo page, click **Add file → Upload files**
2. Drag in `index.html`
3. Click **Commit changes**

### 3. Enable GitHub Pages
1. Go to **Settings → Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Click **Save**
5. Wait ~1 minute — your site will be live at `https://emma-ks.github.io/seeds-seminar`

---

## Setup: Live Google Sheets pull (optional but recommended)

This makes the schedule update automatically whenever you edit the spreadsheet.

### 1. Publish the sheet as CSV
1. Open your Google Sheet
2. **File → Share → Publish to web**
3. In the first dropdown, select your sheet tab (e.g. `Sheet1`)
4. In the second dropdown, select **Comma-separated values (.csv)**
5. Click **Publish** → copy the URL

### 2. Paste it into index.html
Open `index.html` and find this line near the top of the `<script>` block:

```js
const SHEET_CSV_URL = 'YOUR_PUBLISHED_CSV_URL_HERE';
```

Replace `YOUR_PUBLISHED_CSV_URL_HERE` with the URL you copied.

### 3. Re-upload and commit
Upload the updated `index.html` to your GitHub repo (same process as step 2 above, or use the pencil ✏️ edit button directly on GitHub).

---

## Updating the schedule

Once the CSV URL is set:
- **Just edit your Google Sheet** — the website updates automatically on each page load. No code changes needed.

Before the CSV URL is set:
- The site shows a static snapshot of the schedule from the screenshot you provided.
- To update manually, edit the `allSessions` array inside `renderStatic()` in `index.html`.

---

## Questions?
The site is a single self-contained `index.html` file — no build tools, no dependencies, no server needed.
