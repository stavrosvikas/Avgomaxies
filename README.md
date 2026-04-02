# 🥚 Egg Battle

Παιχνίδι αυγομαχίας εμπνευσμένο από Tekken 1 — flat 2D με αίσθηση βάθους. 6 χαρακτήρες, 6 μοναδικά maps, single player με endless stages και multiplayer P2P μέσω link.

---

## 🎮 Gameplay

Κυλάς το αυγό σου και προσπαθείς να σπάσεις τον αντίπαλο.  
Η ζημιά εξαρτάται από την **ταχύτητα σύγκρουσης** — όσο πιο γρήγορα χτυπάς, τόσο περισσότερο damage.  
Αν συγκρουστείτε ταυτόχρονα, **και οι δύο** παίκτες χάνουν ζωή ανάλογα με την ένταση.

### Controls

| Κίνηση | PC | Mobile |
|--------|-----|--------|
| Άλμα | ↑ | Αριστερός αντίχειρας ↑ |
| Φόρτιση | Κράτα ↓ | Αριστερός αντίχειρας ↓ |
| **Super Jump Attack** | Άφεσε ↓ | Άφεσε ↓ |
| Αριστερά / Δεξιά | ← → | Δεξιός αντίχειρας ← → |
| Mute ήχου | M | — |
| Πίσω (menus) | ESC | Κουμπί ΠΙΣΩ |

**Charge:** Κράτα ↓ για να φορτίζεις — όσο περισσότερο κρατάς, τόσο πιο δυνατό το Super Jump Attack.  
Η κατεύθυνση της επίθεσης καθορίζεται από το ← → που κρατάς τη στιγμή που αφήνεις.

### Special mechanics
- **Combo ×N** — Αν χτυπάς ξανά μέσα σε 1.2 δευτερόλεπτα: +15% damage ανά επίπεδο
- **PERFECT** — Κέρδισες round χωρίς να δεχτείς καμία ζημιά
- **Wall bounce** — Τα αυγά αναπηδούν από τους τοίχους αν χτυπούν με ταχύτητα
- **Screen shake** — Ανάλογα με την ένταση της σύγκρουσης
- **Countdown 3-2-1** — Πριν κάθε round

---

## 🥚 Χαρακτήρες

Κάθε χαρακτήρας έχει το δικό του **map** — στο single player παίζεις πάντα στο map του αντιπάλου, στο multiplayer στο map του host.

| # | Όνομα | Χρώμα | Map | Στυλ AI |
|---|-------|-------|-----|---------|
| 01 | Sunny | Κίτρινο | Χρυσή Έρημος | Ισορροπημένος |
| 02 | Bruno | Καφέ | Αρχαίο Σπήλαιο | Αργός, τεράστιο charge |
| 03 | Alba | Λευκό | Λευκός Ναός | Γρήγορος, πολλά jumps |
| 04 | Nero | Μαύρο | Κυβερνητικό Κενό | Επιθετικός, αποφεύγει |
| 05 | Azure | Μπλε | Βυθός Ωκεανού | Τεχνικός, ακριβής |
| 06 | Rosso | Κόκκινο | Ηφαιστειακός Κρατήρας | Επιθετικός |

---

## 🕹️ Modes

### Single Player
- Endless stages — κάθε νίκη αυξάνει τη δυσκολία
- Ο αντίπαλος γίνεται πιο γρήγορος, πιο επιθετικός, αποφεύγει καλύτερα
- Μετράει **streak** νικών — αποθηκεύεται τοπικά
- Αν χάσεις: γράφεις nickname και μπαίνεις στο Hall of Fame

### Multiplayer (P2P)
1. **Host:** Πατάς Multiplayer → αντιγράφεις το link → το στέλνεις στον φίλο σου
2. **Guest:** Ανοίγεις το link → αυτόματη σύνδεση
3. Και οι δύο διαλέγετε χαρακτήρα στην ίδια οθόνη (βλέπετε ο ένας τι επιλέγει ο άλλος)
4. Πατάτε READY → ξεκινά ο αγώνας
5. Μετά τον αγώνα: πατάς → επιστρέφεις στο lobby με την ίδια σύνδεση

> **Σημαντικό:** Το multiplayer χρειάζεται **HTTPS** — δηλαδή να παίζεις από GitHub Pages ή άλλο HTTPS URL, όχι από `file://` τοπικά.

---

## 📁 Assets που χρειάζονται

### Sprites — Horizontal sprite sheets, PNG με transparency

Τοποθέτησε στο `assets/characters/characterXX/` (XX = 01 έως 06).  
Κάθε frame είναι **128×128px**. Αν λείπει κάποιο αρχείο, το παιχνίδι χρησιμοποιεί αυτόματα placeholder (χρωματιστά αυγά).

| Αρχείο | Frames | Διαστάσεις sheet |
|--------|--------|-----------------|
| `idle.png` | 4 | 512 × 128 |
| `roll.png` | 6 | 768 × 128 |
| `jump.png` | 4 | 512 × 128 |
| `charge.png` | 4 | 512 × 128 |
| `superjump.png` | 4 | 512 × 128 |
| `hit.png` | 3 | 384 × 128 |
| `dead.png` | 4 | 512 × 128 |

### UI

| Αρχείο | Διαστάσεις | Σημειώσεις |
|--------|------------|------------|
| `assets/favicon.png` | 64 × 64 | Αυγό icon |
| `assets/logo.png` | 600 × 200 | Διαφανές φόντο — εμφανίζεται στο intro |

### Ήχοι

Τοποθέτησε στο `assets/sounds/`. Όλοι προαιρετικοί — χωρίς αυτά παίζουν procedural Web Audio API sounds.

| Αρχείο | Περιγραφή |
|--------|-----------|
| `music_menu.mp3` | BGM κατά τα menus |
| `music_fight.mp3` | BGM κατά τον αγώνα |
| `character01_hit.wav` … `character06_hit.wav` | Ήχος χτυπήματος ανά χαρακτήρα |
| `character01_dead.wav` … `character06_dead.wav` | Ήχος θανάτου ανά χαρακτήρα |

---

## 🚀 Εκτέλεση

```bash
# Απλά άνοιξε το index.html — single player δουλεύει και τοπικά
open index.html

# Για multiplayer χρειάζεται HTTPS — γρήγορο local server:
npx serve .
# ή
python3 -m http.server 8080
```

**GitHub Pages:**
1. Ανέβασε το repo
2. Settings → Pages → Branch: `main`, folder: `/` (root)
3. Το παιχνίδι είναι playable online με πλήρες multiplayer

---

## 🛠️ Tech Stack

| | |
|--|--|
| Engine | Vanilla HTML5 Canvas + JavaScript (zero dependencies) |
| Multiplayer | [PeerJS](https://peerjs.com) P2P — δεν χρειάζεται server |
| Audio | Web Audio API (procedural) + αρχεία MP3/WAV |
| Font | [Bebas Neue](https://fonts.google.com/specimen/Bebas+Neue) via Google Fonts |
| Canvas | 960 × 540px (16:9), scales σε οποιαδήποτε οθόνη |

---

## 📐 Δομή project

```
egg-battle/
├── index.html                        ← όλο το παιχνίδι
├── README.md
├── .gitignore
└── assets/
    ├── favicon.png
    ├── logo.png
    ├── characters/
    │   ├── character01/              ← idle, roll, jump, charge, superjump, hit, dead
    │   ├── character02/
    │   ├── character03/
    │   ├── character04/
    │   ├── character05/
    │   └── character06/
    └── sounds/
        ├── music_menu.mp3
        ├── music_fight.mp3
        ├── character01_hit.wav
        └── ...
```
