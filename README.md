# 🐾 Taupe-O-Matic

> Un jeu de type *Whack-a-Mole* rétro et pixelisé, jouable directement dans le navigateur — sans installation, sans dépendances.

---

## 🎮 Présentation

**Taupe-O-Matic** est un jeu d'arcade inspiré des bornes des années 80-90. Des taupes surgissent de leurs trous dans un jardin pixelisé, et ton seul objectif est de les frapper avant qu'elles ne replongent sous terre. Plus tu en frappes, plus les points s'accumulent — mais les taupes deviennent de plus en plus rapides et nombreuses au fil du temps.

Le curseur de la souris se transforme en **tapette à mouche pixel art**, les sons sont générés en temps réel via le **Web Audio API**, et tout l'affichage adopte une esthétique **rétro pixelisée** fidèle aux vieux jeux de téléphone.

---

## 🕹️ Comment jouer

1. Clique sur **▶ JOUER** pour démarrer une partie.
2. Surveille les trous — une taupe peut surgir à n'importe quel moment.
3. **Clique sur la taupe** pour la frapper avant qu'elle rentre dans son trou.
4. Enchaîne les frappes sans rater pour monter ton **combo** et multiplier tes points.
5. Tu as **60 secondes** — fais le meilleur score possible !

### Contrôles

| Action | Contrôle |
|---|---|
| Frapper une taupe | Clic gauche / Tap (mobile) |
| Pause / Reprise | Bouton ⏸ PAUSE |
| Arrêter la partie | Bouton ⏹ ARRÊTER |
| Rejouer | Bouton 🔄 REJOUER |

---

## ⚙️ Mécaniques de jeu

### Système de score
- Chaque taupe frappée rapporte **10 points × le multiplicateur de combo**.
- Le combo augmente à chaque frappe consécutive (jusqu'à **×8**).
- Rater une taupe ou cliquer dans le vide **réinitialise le combo à ×1**.

### Niveaux
La partie dure 60 secondes, divisée en **4 niveaux** de 15 secondes chacun :

| Niveau | Temps écoulé | Effet |
|---|---|---|
| 1 | 0 – 15s | Tempo normal |
| 2 | 15 – 30s | Taupes plus rapides |
| 3 | 30 – 45s | Plusieurs taupes simultanées |
| 4 | 45 – 60s | Vitesse maximale, chaos total |

### Taupes simultanées
Le nombre de taupes pouvant être visibles en même temps augmente avec le niveau (jusqu'à **4 taupes en même temps**).

---

## 🔊 Sons

Tous les sons sont **générés procéduralement** via le Web Audio API — aucun fichier audio externe.

| Événement | Son |
|---|---|
| Taupe qui sort | Pop aigu |
| Taupe qui rentre | Plop grave |
| Frappe réussie | Crack de fouet |
| Frappe ratée | Boing descendant |
| Level up | Fanfare ascendante |
| Game over | Mélodie descendante |

---

## 🛠️ Stack technique

| Composant | Technologie |
|---|---|
| Structure | HTML5 |
| Style | CSS3 (variables, animations, media queries) |
| Logique | JavaScript vanilla (ES6+) |
| Audio | Web Audio API (synthèse procédurale) |
| Graphismes | SVG inline + CSS pixel art |
| Police | [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) (Google Fonts) |

**Aucun framework. Aucune dépendance npm. Un seul fichier HTML.**

---

## 📁 Structure du projet

```
taupe-o-matic/
└── whack-a-mole.html   # Tout le jeu en un seul fichier
```

---

## 🚀 Lancer le jeu

Aucune installation requise. Il suffit d'ouvrir le fichier dans un navigateur moderne :

```bash
# Option 1 — Double-clic sur le fichier
whack-a-mole.html

# Option 2 — Via un serveur local (recommandé pour éviter les restrictions CORS)
npx serve .
# ou
python -m http.server 8080
```

> ✅ Compatible Chrome, Firefox, Edge, Safari (desktop & mobile).

---

## 📱 Support mobile

Le jeu est **responsive** et jouable sur téléphone :
- Le curseur tapette est masqué sur les appareils tactiles.
- Les taps remplacent les clics.
- La grille et les trous s'adaptent aux petits écrans.

---

## 🎨 Direction artistique

L'esthétique vise les **jeux des anciens téléphones Nokia / Game Boy** :
- Rendu pixelisé (`image-rendering: pixelated`)
- Police bitmap Press Start 2P
- Palette de couleurs limitée et contrastée
- Animations par étapes (`steps()`) pour simuler le rendu frame-by-frame
- Nuages et ciel animés en CSS pur
- Taupes dessinées entièrement en SVG pixel art

---

## 📄 Licence

Projet libre — fais-en ce que tu veux. Aucune restriction.
