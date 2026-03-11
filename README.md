# 🏋️ NK's Fit Journal

> A personal calorie tracking & weight loss journal — built for Nikhil, usable by anyone.

**Live URL:** `https://NikhilKadari38.github.io/nks-fit-journal`

---

## 📁 File Structure

```
nks-fit-journal/
├── index.html          ← Landing page (constellation animation)
├── dashboard.html      ← Daily summary, water, workout toggle
├── foodlog.html        ← Add food entries freely throughout the day
├── database.html       ← Browse & add custom foods
├── progress.html       ← Charts: weight, calories, macros, streak
├── profile.html        ← Personal stats & settings
├── css/
│   ├── main.css        ← Global styles, CSS variables, light/dark themes
│   └── components.css  ← Navbar, buttons, cards, all UI components
├── js/
│   ├── firebase-config.js  ← Storage layer (localStorage now, Firebase later)
│   ├── app.js              ← Theme toggle, navbar, toast, modal, utilities
│   ├── animations.js       ← 6 unique canvas background animations
│   ├── fooddata.js         ← 75+ food database + FoodDB utility functions
│   ├── dashboard.js        ← Dashboard logic
│   ├── foodlog.js          ← Food log logic
│   ├── database.js         ← Database page logic
│   ├── progress.js         ← Chart.js charts logic
│   └── profile.js          ← Profile save/load logic
└── README.md
```

---

## 🚀 How to Deploy to GitHub Pages

### Step 1 — Create GitHub Repository
1. Go to [github.com](https://github.com) → Sign in
2. Click **"New repository"** (green button)
3. Name it exactly: `nks-fit-journal`
4. Set to **Public**
5. Click **"Create repository"**

### Step 2 — Upload Your Files
**Option A: Upload via browser (easiest)**
1. Open your new repo
2. Click **"uploading an existing file"**
3. Drag and drop ALL files and folders
4. Click **"Commit changes"**

**Option B: Git command line**
```bash
git init
git add .
git commit -m "Initial commit — NK's Fit Journal"
git branch -M main
git remote add origin https://github.com/NikhilKadari38/nks-fit-journal.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings** tab
2. Scroll to **Pages** in the left sidebar
3. Under **Source** → select **"Deploy from a branch"**
4. Branch: **main** | Folder: **/ (root)**
5. Click **Save**
6. Wait 2–3 minutes → your site is live at:
   **`https://NikhilKadari38.github.io/nks-fit-journal`**

---

## 🔥 Connect Firebase (for cloud data sync)

Right now the app uses your browser's localStorage — data is saved locally on your device.
To sync data across devices, connect Firebase:

### Step 1 — Create Firebase Project
1. Go to [firebase.google.com](https://firebase.google.com)
2. Click **"Get Started"** → **"Add project"**
3. Name: `nks-fit-journal` → Continue
4. Disable Google Analytics (not needed) → **Create project**

### Step 2 — Add Web App
1. Click the **Web icon** (`</>`)
2. App nickname: `nks-fit-journal`
3. Click **"Register app"**
4. Copy the `firebaseConfig` object

### Step 3 — Enable Firestore
1. Left sidebar → **Build → Firestore Database**
2. Click **"Create database"**
3. Choose **"Start in test mode"** → Next → Done

### Step 4 — Update Your Code
Open `js/firebase-config.js` and:
1. Replace all `"YOUR_..."` values with your real Firebase config
2. Change `const USE_FIREBASE = false;` to `const USE_FIREBASE = true;`
3. Push to GitHub

---

## 🎨 Features

| Feature | Details |
|---|---|
| 🌙 Dark / Light mode | VSCode dark ↔ Netflix warm white |
| 🎬 Unique animations | 6 different canvas animations per page |
| 🍽️ Food Log | Free-add any time, auto macro calc from grams |
| 🗄️ Food Database | 75+ foods (veg + non-veg), add custom foods |
| 📊 Charts | Weight line, calorie bar, macro donut, streak calendar |
| 💧 Water tracker | Animated filling glass, add 250ml / 500ml |
| 🎯 Goal progress | Live progress bar from 76kg → 65kg |
| 🏋️ Workout toggle | Switches calorie goal: 1,462 ↔ 2,034 kcal |
| 📱 Responsive | Works on mobile, tablet, desktop |

---

## 👤 Default Profile (Nikhil Kadari)

| Stat | Value |
|---|---|
| Age | 26 years |
| Weight | 76 kg |
| Height | 5'3" (160 cm) |
| Goal Weight | 65 kg |
| BMR | 1,635 kcal |
| Rest Day Target | 1,462 kcal |
| Workout Day Target | 2,034 kcal |
| Water Goal | 3,000 ml/day |

---

## 📝 Notes

- Data is stored in your **browser's localStorage** until Firebase is connected
- Clearing browser data will erase logs — connect Firebase for permanent storage
- The app works fully offline for reading; adding data requires the page to be open
- All macro data is per 100g/100ml based on standard nutritional databases

---

*Built with ❤️ for Nikhil's fitness journey — 76kg → 65kg 💪*
