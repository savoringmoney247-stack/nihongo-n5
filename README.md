# 🇯🇵 Nihongo N5 — Japanese JLPT Trainer PWA

A fully offline-capable Progressive Web App for learning Japanese at JLPT N5 level.

## ✨ Features

- 🃏 **Flashcard Trainer** — 20+ vocab cards with audio, flip animation, spaced-repetition marking
- 漢 **Kanji Grid** — All 103 N5 kanji with on/kun readings, stroke count, and mastery tracking
- 📝 **JLPT-Style Quiz** — Vocabulary, Kanji reading, Grammar, and Listening quiz modes
- 📖 **Grammar Guide** — 10+ grammar patterns with accordion explanations and examples
- あ **Kana Charts** — Full hiragana and katakana with tap-to-hear audio
- ✍️ **Sentence Builder** — Word-order drag/tap exercises
- 📊 **Progress Dashboard** — Streak tracking, per-category progress bars, local persistence
- 📵 **Fully Offline** — Works with no internet after first load
- 📱 **Installable** — Full PWA with install prompt and home screen icon
- 🎯 **Lead Generation** — Email capture form for study pack delivery

## 🚀 Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `nihongo-n5`)
2. Upload all 3 files:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
3. Go to **Settings → Pages**
4. Set source to **main branch / root folder**
5. Your app will be live at `https://yourusername.github.io/nihongo-n5/`

> **Note:** PWA install prompt only works on HTTPS — GitHub Pages provides this automatically.

## 📁 File Structure

```
/
├── index.html         # Main app (all-in-one)
├── manifest.json      # PWA manifest
├── service-worker.js  # Offline caching
└── README.md
```

## 🔧 Customization

### Replace placeholder icons
The manifest uses placeholder images. Replace them with real icons:
1. Create a 512×512 PNG icon with red background and 日 kanji
2. Use [realfavicongenerator.net](https://realfavicongenerator.net) to generate all sizes
3. Update the `icons` array in `manifest.json`

### Connect the lead gen form
In `index.html`, find the `submitLead()` function and replace the `localStorage` logic with your preferred email service:
- **Mailchimp**: Use their embed form API
- **ConvertKit**: Use their subscriber API
- **Formspree**: Simple `fetch` POST to `https://formspree.io/f/YOUR_ID`

### Add more vocabulary
Extend the `VOCAB` array in the `<script>` section of `index.html`.

## 🛠 Tech Stack

- Pure HTML/CSS/JavaScript — zero dependencies
- Web Speech API for audio pronunciation
- localStorage for progress persistence
- Service Worker for offline support
- CSS custom properties for theming
- Google Fonts (Shippori Mincho, DM Sans, JetBrains Mono)

## 📄 License

MIT — free to use, modify, and distribute.
