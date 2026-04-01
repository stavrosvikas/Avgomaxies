# 🥚 Egg Battle

Παιχνίδι αυγομαχίας με 6 μοναδικούς χαρακτήρες, εμπνευσμένο από Tekken 1. Single player με endless stages και multiplayer P2P μέσω link.

## 🎮 Gameplay

- **Κίνηση**: Κυλάς αριστερά/δεξιά
- **Άλμα**: ↑
- **Charge**: Κράτα ↓ → άφεσε = Super Jump Attack (η ένταση εξαρτάται από πόσο κράτησες)
- **Σκοπός**: Σπάσε το αντίπαλο αυγό

Damage βασίζεται στη ταχύτητα σύγκρουσης. Ταυτόχρονη επίθεση = και οι δύο χάνουν ζωή.

## 🕹️ Controls

| PC | Mobile |
|----|--------|
| ↑ Άλμα | Αριστερός αντίχειρας ↑ |
| ↓ Φόρτιση | Αριστερός αντίχειρας ↓ |
| ← → Κίνηση | Δεξιός αντίχειρας ← → |
| M Mute | — |
| ESC Back | Κουμπί ΠΙΣΩ |

## 🥚 Χαρακτήρες & Maps

| # | Όνομα | Χρώμα | Map |
|---|-------|-------|-----|
| 01 | Sunny | Κίτρινο | Χρυσή Έρημος |
| 02 | Bruno | Καφέ | Αρχαίο Σπήλαιο |
| 03 | Alba | Λευκό | Λευκός Ναός |
| 04 | Nero | Μαύρο | Κυβερνητικό Κενό |
| 05 | Azure | Μπλε | Βυθός Ωκεανού |
| 06 | Rosso | Κόκκινο | Ηφαιστειακός Κρατήρας |

## 🌐 Multiplayer

Το multiplayer λειτουργεί P2P μέσω [PeerJS](https://peerjs.com) — δεν χρειάζεται server.

- **Host**: Πάτα Multiplayer → αντίγραψε το link → στείλε στον αντίπαλο
- **Guest**: Άνοιξε το link → αυτόματη σύνδεση
- Το **map** καθορίζεται από τον χαρακτήρα του host

## 📁 Assets που χρειάζονται

### Sprites (PNG με transparency, horizontal sprite sheets)

Κάθε frame **128×128px**. Τοποθέτησε στο `assets/characters/characterXX/`.

| Αρχείο | Frames | Διαστάσεις |
|--------|--------|------------|
| `idle.png` | 4 | 512×128 |
| `roll.png` | 6 | 768×128 |
| `jump.png` | 4 | 512×128 |
| `charge.png` | 4 | 512×128 |
| `superjump.png` | 4 | 512×128 |
| `hit.png` | 3 | 384×128 |
| `dead.png` | 4 | 512×128 |

### UI Assets

| Αρχείο | Διαστάσεις | Σημειώσεις |
|--------|------------|------------|
| `assets/favicon.png` | 64×64 | Αυγό icon |
| `assets/logo.png` | 600×200 | Διαφανές φόντο |
| `assets/backgrounds/stage0X.png` | 960×540 | Προαιρετικό |

### Ήχοι (MP3/WAV)

| Αρχείο | Περιγραφή |
|--------|-----------|
| `assets/sounds/music_menu.mp3` | BGM menu |
| `assets/sounds/music_fight.mp3` | BGM fight |
| `assets/sounds/character0X_hit.wav` | Hit sound per character |
| `assets/sounds/character0X_dead.wav` | Death sound per character |

> Χωρίς αρχεία ήχου το παιχνίδι χρησιμοποιεί procedural Web Audio API sounds.  
> Χωρίς sprites χρησιμοποιεί placeholder αυγά (χρωματιστές ελλείψεις).

## 🚀 Εκτέλεση

Απλά άνοιξε το `index.html` σε browser. Δεν χρειάζεται server για single player.

Για multiplayer από local file: χρειάζεσαι HTTPS ή localhost (π.χ. `npx serve .`).

## 🛠️ Tech Stack

- Vanilla HTML5 Canvas + JavaScript
- [PeerJS](https://peerjs.com) για P2P multiplayer
- [Bebas Neue](https://fonts.google.com/specimen/Bebas+Neue) font (Google Fonts)
- Web Audio API για procedural sounds
