# 💕 Forever Yours, Donnie - Romantic Love Website

A breathtaking, cinematic single-page romantic website built as a love gift. Features elegant dark romantic aesthetics, smooth Framer Motion animations, floating particles, 5 interactive love minigames, and an emotionally moving experience.

![React](https://img.shields.io/badge/React-19-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.9-blue)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-4-pink)
![Framer Motion](https://img.shields.io/badge/Framer%20Motion-11-purple)

---

## ✨ Features

- 🔒 **Password Protection** — Elegant password gate (default: `0301`)
- 🌹 **Hero Section** — Her name in glowing typography, emotional love message, live countdown timer
- 📝 **Shayari Section** — Beautiful poetic typography with floating petals
- 🎮 **5 Romantic Minigames** with shared Love Meter:
  - 🌸 **Petal Promises** — Collect floating petals, each reveals a romantic affirmation
  - 🏮 **Lantern of Love** — Release glowing lanterns into the night sky
  - 💝 **Heart Weaver** — Connect points to weave a glowing heart
  - 💓 **Echoes of Affection** — Rhythm-based orb tapping with romantic messages
  - ☁️ **Cuddle Cloud** — Drag a cloud to catch falling stars and raindrops
- 👑 **Closing Section** — Grand cinematic finale with golden-rose glow
- 🎵 **Ambient Background Music** — Soft Web Audio API generated tones
- 📱 **Fully Responsive** — Mobile-first, polished on all devices
- 💾 **Progress Saving** — localStorage saves game progress
- ✨ **Smooth Animations** — Framer Motion with 60fps performance

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher)
- npm (comes with Node.js)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/forever-yours-donnie.git
cd forever-yours-donnie

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

The site will be available at `http://localhost:5173`

### Build for Production

```bash
npm run build
```

The output will be in the `dist/` folder as a single `index.html` file.

---

## ⚙️ Customization

### 🔑 Change the Password

Edit `src/components/PasswordScreen.tsx`:

```typescript
// Find this line and change '0301' to your desired password
if (password === '0301') {
```

### 📅 Change the Relationship Start Date

Edit `src/components/HeroSection.tsx`:

```typescript
// Change this to your anniversary year
const RELATIONSHIP_START_YEAR = 2026;
```

The countdown automatically calculates from **January 3rd** of the given year. To change the month/day, modify the `calculateTimeTogether` function:

```typescript
const startDate = new Date(RELATIONSHIP_START_YEAR, 0, 3); // Month is 0-indexed (0 = January)
// Change 0 to your month (0=Jan, 1=Feb, ..., 11=Dec)
// Change 3 to your day
```

### 💕 Change Her Name

Edit `src/components/HeroSection.tsx`:

```typescript
const HER_NAME = 'Donnie'; // Change to her name
```

### 💌 Change the Love Message

Edit `src/components/HeroSection.tsx` and find the love message paragraph in the JSX.

### 🎭 Change the Shayari

Edit `src/components/ShayariSection.tsx` and modify the `lines` array.

### 👑 Change the Closing Message & Signature

Edit `src/components/ClosingSection.tsx`:
- Find `I OWN YOU FOREVER MY DONNIE` to change the main declaration
- Find `by rajje` to change the signature

### 🎮 Customize Game Quotes

Edit `src/data/quotes.ts` to add, remove, or modify the romantic quotes used in all minigames.

### 🎵 Adjust Ambient Music

Edit `src/components/BackgroundMusic.tsx` to change the ambient chord or volume.

---

## 🌐 Deploy to Vercel

### Option 1: Vercel CLI

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Deploy
vercel

# Follow the prompts. For production:
vercel --prod
```

### Option 2: GitHub Integration (Recommended)

1. Push your code to GitHub (see instructions below)
2. Go to [vercel.com](https://vercel.com)
3. Click **"New Project"**
4. Import your GitHub repository
5. Framework Preset: **Vite**
6. Click **Deploy**
7. Your site will be live at `your-project.vercel.app`

---

## 📤 Push to GitHub

### First Time Setup

```bash
# 1. Initialize git (if not already done)
git init

# 2. Add all files
git add .

# 3. Create your first commit
git commit -m "💕 Initial commit - Forever Yours romantic website"

# 4. Create a new repository on GitHub:
#    - Go to https://github.com/new
#    - Name it something like "forever-yours-donnie"
#    - Make it Private if you want (recommended for personal content)
#    - Do NOT initialize with README (we already have one)
#    - Click "Create repository"

# 5. Add your remote origin (replace with your actual URL)
git remote add origin https://github.com/YOUR_USERNAME/forever-yours-donnie.git

# 6. Push to GitHub
git branch -M main
git push -u origin main
```

### Subsequent Updates

```bash
git add .
git commit -m "✨ Your update message"
git push
```

---

## 📁 Project Structure

```
├── index.html                    # Entry HTML with Google Fonts
├── package.json                  # Dependencies & scripts
├── vite.config.ts               # Vite configuration
├── tsconfig.json                # TypeScript configuration
├── README.md                    # This file
└── src/
    ├── main.tsx                  # React entry point
    ├── App.tsx                   # Main app component
    ├── index.css                 # Global styles & Tailwind
    ├── data/
    │   └── quotes.ts            # Romantic quotes for games
    ├── utils/
    │   ├── audio.ts             # Web Audio API sound effects
    │   └── storage.ts           # localStorage progress saving
    └── components/
        ├── PasswordScreen.tsx    # Password protection gate
        ├── HeroSection.tsx       # Hero with name & countdown
        ├── ShayariSection.tsx    # Poetic shayari display
        ├── MinigamesSection.tsx  # Games container with Love Meter
        ├── ClosingSection.tsx    # Grand finale section
        ├── LoveMeter.tsx         # Shared progress bar
        ├── BackgroundMusic.tsx   # Ambient music player
        └── games/
            ├── PetalPromises.tsx        # 🌸 Collect petals
            ├── LanternOfLove.tsx        # 🏮 Release lanterns
            ├── HeartWeaver.tsx          # 💝 Weave a heart
            ├── EchoesOfAffection.tsx    # 💓 Rhythm game
            └── CuddleCloud.tsx          # ☁️ Catch stars
```

---

## 🎨 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Deep Burgundy | `#800020` | Primary accents |
| Rose Gold | `#B76E79` | Glowing effects |
| Soft Blush | `#FFB6C1` | Romantic highlights |
| Warm Cream | `#FFF8E7` | Body text |
| Midnight Black | `#0A0A0F` | Background |
| Gold Accent | `#D4AF37` | Special highlights |

---

## 🛠️ Tech Stack

- **React 19** — UI framework
- **TypeScript** — Type-safe development
- **Vite** — Lightning-fast build tool
- **Tailwind CSS 4** — Utility-first styling
- **Framer Motion** — Smooth animations
- **Web Audio API** — Ambient sound generation

---

## ❤️ Made with Love

This website was crafted with love, care, and attention to every detail. Every animation, every quote, and every interaction was designed to make her feel special.

*Forever yours, always.*
