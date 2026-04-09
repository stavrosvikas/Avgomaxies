# 🥚 Luben Αυγομαχίες

> Τσούγκρισε αυγά, κέρδισε rounds, γίνε ο αυγός της χρονιάς.

Ένα browser-based 2D fighting game εμπνευσμένο από την ελληνική πολιτική σκηνή. Διαλέξε το αυγό σου και βάλσου με τον Luben ή με έναν φίλο σου.

---

## ⚔️ Χαρακτήρες

| # | Χαρακτήρας | Χρώμα |
|---|-----------|-------|
| 01 | ΕΥΑΓΓΕΛΑΤΟΣ | 🟡 Κίτρινο |
| 02 | EGG7000 | 🟢 Πράσινο |
| 03 | MAREEGONA | ⚪ Λευκό |
| 04 | ΑΥΓΥΛΑΣ | ⚫ Μαύρο |
| 05 | ΜΗΤΣΟΦΛΑΚΗΣ | 🔵 Μπλε |
| 06 | ΑΥΓΟΥΜΠΑΣ | 🔴 Κόκκινο |

---

## 🕹️ Controls

| Πλήκτρο | Ενέργεια |
|---------|---------|
| `←` `→` | Κίνηση |
| `↑` | Άλμα |
| `↓` κράτα | Φόρτιση |
| `↓` άφεσε | Super Jump Attack! |

**Mobile:** Εμφανίζονται 4 κουμπιά στην οθόνη κατά τη διάρκεια του fight.

---

## 🌐 Multiplayer

Πάτα **"ΤΣΟΥΓΚΡΙΣΕ ΜΕ ΕΝΑΝ ΦΙΛΟ ΣΟΥ"**, αντέγραψε το link και στείλτο — P2P σύνδεση μέσω PeerJS, χωρίς server.

---

## 📁 Δομή

```
/
├── index.html          # Το παιχνίδι (single file, vanilla JS)
├── manifest.json       # PWA manifest
└── assets/
    ├── logo.png
    ├── favicon*.png / favicon.ico
    ├── sounds/
    │   ├── music_menu.mp3
    │   ├── music_fight.mp3
    │   ├── intro.wav
    │   └── *_hit.wav   (ένα ανά χαρακτήρα)
    └── characters/
        └── character01-06/
            └── idle / roll / jump / charge / superjump / hit / dead .png
```

---

## 🛠️ Tech Stack

- **HTML5 Canvas** — rendering
- **Vanilla JavaScript** — game engine
- **PeerJS 1.5.4** — P2P multiplayer
- **Web Audio API** — ήχοι & μουσική
- **Press Start 2P + JetBrains Mono** — fonts (Google Fonts, Greek subset)
- **PWA** — installable, fullscreen, landscape lock

---

## 📱 PWA Install

**Android:** Chrome → "Add to Home Screen"  
**iOS:** Safari → Share → "Add to Home Screen"

Μετά το install ανοίγει σαν native app σε fullscreen landscape.

---

## 📄 License

For entertainment purposes only. All characters are fictional eggs.
