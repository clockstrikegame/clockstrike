# 🎮 CLOCKSTRIKE — Precision Timing Game

> Stop the clock hand in the golden zone. Simple. Addictive. Impossible to put down.

---

## 🚀 DEPLOY TO GITHUB PAGES — STEP BY STEP

### STEP 1 — Create GitHub Account
1. Go to **https://github.com**
2. Click **"Sign up"**
3. Choose a username (example: `clockstrikegame`)
   - Make it short and memorable
   - It will appear in your game URL
4. Enter email and password
5. Verify your email

---

### STEP 2 — Create the Repository
1. After login, click the **"+"** button (top right) → **"New repository"**
2. Repository name: `clockstrike`
3. Set to **Public** (required for free GitHub Pages)
4. Do NOT check "Add README" (files already included)
5. Click **"Create repository"**

Your game URL will be:
```
https://YOUR_USERNAME.github.io/clockstrike/
```

---

### STEP 3 — Upload Your Files
**Method A — Via Browser (easiest, no software needed):**
1. On your new empty repo page, click **"uploading an existing file"**
2. Drag and drop ALL files from the clockstrike folder:
   - `index.html`
   - `manifest.json`
   - `robots.txt`
   - `sitemap.xml`
3. Scroll down → write commit message: `first upload`
4. Click **"Commit changes"**

**Method B — Via Git (from your computer):**
```bash
# Install Git from https://git-scm.com first, then:

cd path/to/clockstrike        # go to your game folder
git init
git add .
git commit -m "launch"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/clockstrike.git
git push -u origin main
```

---

### STEP 4 — Enable GitHub Pages
1. In your repository, click **"Settings"** (top menu)
2. Scroll down to **"Pages"** (left sidebar)
3. Under **"Branch"**: select `main` → folder `/` (root)
4. Click **"Save"**
5. Wait 1-3 minutes
6. Your game is LIVE at: `https://YOUR_USERNAME.github.io/clockstrike/`

---

### STEP 5 — Update SEO with Your Real URL
Open `index.html` and replace all instances of:
```
https://yourusername.github.io/clockstrike/
```
With your actual URL:
```
https://YOUR_REAL_USERNAME.github.io/clockstrike/
```

Also update `robots.txt` and `sitemap.xml` the same way.

---

## 📊 TRACK VISITORS — Google Analytics

### Setup (Free):
1. Go to **https://analytics.google.com**
2. Sign in with Google → **"Start measuring"**
3. Create Account name: `ClockStrike`
4. Create Property name: `clockstrike`
5. Platform: **Web**
6. Enter your GitHub Pages URL
7. Copy your **Measurement ID** (looks like: `G-XXXXXXXXXX`)

### Add to your game:
In `index.html`, find this comment block and uncomment it:
```html
<!-- <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>window.dataLayer=window.dataLayer||[];function gtag(){dataLayer.push(arguments);}gtag('js',new Date());gtag('config','G-XXXXXXXXXX');</script> -->
```
Replace `G-XXXXXXXXXX` with your real ID, then remove the `<!--` and `-->`.

### Where to see stats:
- **Real-time visitors**: Analytics → Reports → Realtime
- **Total visitors**: Reports → Acquisition → Overview
- **Countries**: Reports → User → Demographics
- **Devices**: Reports → Tech → Overview

---

## 💰 ADD GOOGLE ADSENSE (earn money)

1. Go to **https://adsense.google.com**
2. Apply with your GitHub Pages URL
3. Wait for approval (1-14 days)
4. After approval, add their code snippet inside `<head>` in `index.html`

**Best ad placements for games:**
- Between game rounds (interstitial)
- Below the game canvas
- In the game over screen

---

## 🎮 GAME MECHANICS

| Element | Value |
|---------|-------|
| Starting speed | Slow |
| Zone size (Level 1) | ~72° arc |
| Zone size (Level 10) | ~25° arc |
| Lives | 3 |
| Level up every | 5 hits |
| Perfect hit bonus | 100 pts + 12×combo |
| Normal hit | 50 pts + 6×combo |

---

## 🌍 LANGUAGES INCLUDED
- 🇺🇸 English (default)
- 🇫🇷 French
- 🇸🇦 Arabic (RTL support)
- 🇪🇸 Spanish
- 🇨🇳 Chinese
- 🇩🇪 German

Language is **auto-detected** from the visitor's browser/device.

---

## 🔍 SEO TIPS TO RANK FASTER

1. **Share on Reddit**: Post in r/WebGames, r/indiegaming, r/html5games
2. **Post on itch.io**: Free listing, gets organic traffic
3. **Share on Twitter/X**: "I made a free browser game, try to beat my score!"
4. **Submit to game directories**:
   - https://www.crazygames.com (submit your game)
   - https://itch.io
   - https://newgrounds.com
5. **Update sitemap date** when you make changes

---

## 🛠 CUSTOMIZATION

To change difficulty:
- `hSpeed`: starting speed (line ~270 in index.html)
- `zSize`: starting zone size (larger = easier)

To change colors: edit CSS variables at top:
```css
--gold:  #C9A84C;   /* zone & accent color */
--green: #50FFAA;   /* good hit color */
--red:   #FF4C6A;   /* miss color */
```

---

*Built with pure HTML + Canvas + Web Audio API. Zero dependencies. Zero cost.*
