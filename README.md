# Spin the Wheel 🎡

A random name picker. Enter up to 50 names, spin the wheel, and get a random winner. The whole app is one `index.html` file with no build step and no dependencies.

## Features
- Add names one at a time, or paste a list (one per line or comma separated)
- Holds up to 50 names. To change the limit, edit `MAX_NAMES` in `index.html`
- Picks are fair: the winner comes from `crypto.getRandomValues`, and the wheel animation lands on that name
- Tick and fanfare sounds, confetti, and a list of recent winners
- Option to remove each winner from the wheel after they're picked
- Names are saved in the browser, so they're still there after a refresh
- Press **Space** to spin

## Add your company branding
The page is set up for Dominion Leasing Software, using `logo.svg` from domls.com. To change the branding:
1. Put the new logo file in this folder, next to `index.html`. PNG, SVG and JPG all work.
2. Near the top of the `<script>` in `index.html`, edit these two lines:
   ```js
   const COMPANY_NAME = "Dominion Leasing Software";
   const LOGO = "logo.svg";
   ```
The logo and name show in a badge above the title. The logo also shows on the winner popup and becomes the browser-tab icon. If the logo file is missing, the logo is hidden and the name still shows.

## Deploy to GitHub Pages
1. Create a new **public** repository on GitHub, for example `name-picker`.
2. Push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Spin the wheel name picker"
   git branch -M main
   git remote add origin https://github.com/<your-username>/name-picker.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, then pick **main** and **/ (root)** and click **Save**.
4. After a minute or so, the site is live at `https://<your-username>.github.io/name-picker/`.

## Run locally
Open `index.html` in any browser.
