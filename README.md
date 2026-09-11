# Collection journal

A single-file web app. No build step, no dependencies, no server required.

Three sections: **Add** a quote, browse your **Library** (grouped by source, plus a Books reading tracker), and **Random** for a swipe-through of quotes filtered by source.

## Run it in VSCode

1. Open this folder in VSCode.
2. Install the **Live Server** extension (by Ritwick Dey) if you don't have it — Extensions panel, search "Live Server".
3. Right-click `index.html` → **Open with Live Server**.
4. It opens in your browser at `http://127.0.0.1:5500` (or similar).

That's it — no `npm install`, no build process. It's plain HTML/CSS/JS in one file.

## Using it on your phone

This app stores data in the browser's `localStorage`, which is tied to **one browser on one device**. To actually use it day-to-day on your phone:

1. Get the app hosted somewhere your phone can reach it. Easiest free options:
   - **GitHub Pages** — push this folder to a GitHub repo, enable Pages in repo settings, get a public URL.
   - **Netlify / Vercel** — drag-and-drop the folder onto their web dashboard, get a URL instantly, no account setup beyond signup.
2. Open that URL in your phone's browser.
3. iPhone (Safari): tap Share → **Add to Home Screen**. Android (Chrome): menu → **Add to Home Screen** / **Install app**.
4. It now opens like a normal app icon, full-screen, no browser chrome.

## Backing up your data — do this regularly

Your data lives only in that one browser's local storage. This means:

- **Clearing your phone browser's site data/cache will delete your entire library**, with no recovery.
- **Switching browsers** (e.g. Safari to Chrome) or **reinstalling the browser** starts you with an empty library.
- There is **no cloud backup or sync** built in — this only works because you use it on one device.

On the Library page:

- **Export** — downloads your whole library as a timestamped JSON file. On a real phone (not the desktop Live Server preview), this opens your phone's native share sheet, so you can send it straight to Mail, AirDrop, Google Drive, etc. — get it off the device, not just into Downloads.
- **Import** — pick a previously exported JSON file to restore from. It merges with what's already there and skips anything already present (matched by ID or by matching quote text), so it's safe to import into a library that isn't empty.

**Export regularly.** The backup only protects you if you actually have a recent one saved somewhere off your phone.

## Books tracker

Inside the Library tab, toggle to **Books** to track what you're reading separately from your quotes — title, author, and a status (On the list / In progress / Completed / Dropped). Not linked to your saved quotes; a fully separate list.

## Files

- `index.html` — the entire app: markup, styles, and logic in one file.

