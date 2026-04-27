# Revoria — Site de réservation

Site vitrine de réservation pour **Revoria**, un logement insolite à 6 pièces thématiques Disney situé à 15 minutes de Disneyland Paris.

## ✨ Aperçu

- **Capacité** : jusqu'à 6 voyageurs
- **Tarif** : 400 € la nuit
- **Localisation** : 15 minutes en voiture de Disneyland Paris
- **6 univers thématiques** : Toy Story, Raiponce, Avengers, Pirates des Caraïbes, Ratatouille, Le Monde de Némo

## 📂 Structure du projet

```
.
├── index.html          # Page d'accueil (hero + aperçu pièces)
├── logement.html       # Détail des 6 pièces thématiques
├── reservation.html    # Calendrier de disponibilités + formulaire
├── contact.html        # Page de contact
├── css/
│   └── style.css       # Styles complets
├── js/
│   └── main.js         # Calendrier, validations, animations
└── assets/
    └── images/         # Photos des pièces (à compléter)
```

## 🚀 Lancer le site en local

Aucun build n'est nécessaire. Ouvre simplement `index.html` dans un navigateur, ou lance un petit serveur local :

```bash
# Avec Python
python3 -m http.server 8000

# Avec Node (npx)
npx serve .
```

Puis ouvre [http://localhost:8000](http://localhost:8000).

## 🔧 Comment modifier les choses importantes

### 1. Bloquer des dates sur le calendrier

Ouvre `js/main.js` et cherche la section **`BOOKED_DATES`** (autour de la ligne 18). Ajoute les dates au format `YYYY-MM-DD` :

```js
const BOOKED_DATES = [
    '2026-05-10',
    '2026-05-11',
    '2026-05-12',
    '2026-08-01',
];
```

Chaque date listée correspond à une nuit déjà occupée. Le calendrier les affichera barrées et grisées automatiquement.

### 2. Changer le tarif

Toujours dans `js/main.js`, en haut du fichier :

```js
const PRICE_PER_NIGHT = 400;  // change la valeur ici
```

Pense aussi à mettre à jour les mentions de "400 €" dans `index.html`, `logement.html` et `reservation.html`.

### 3. Changer l'email de contact

Dans `js/main.js` :

```js
const CONTACT_EMAIL = 'revoria.test@gmail.com';
```

Et dans `contact.html`, cherche `revoria.test@gmail.com` et remplace.

### 4. Ajouter les vraies photos

1. Récupère tes photos depuis Instagram et place-les dans `assets/images/`
2. Dans `logement.html`, chaque pièce a un bloc `<div class="room-image" data-theme="...">` avec un dégradé de couleur en placeholder
3. Remplace le contenu du bloc par une vraie image, par exemple :

```html
<div class="room-image">
    <img src="assets/images/toystory.jpg" alt="Chambre Toy Story" style="width:100%;height:100%;object-fit:cover;border-radius:16px;">
</div>
```

## 📤 Comment fonctionnent les formulaires

Les formulaires (réservation et contact) ouvrent automatiquement le client email du visiteur (Gmail, Outlook, Mail…) avec un message **pré-rempli** vers `revoria.test@gmail.com`. Le visiteur n'a plus qu'à cliquer sur "Envoyer".

> ⚠️ Cette approche `mailto:` est simple et sans backend, mais elle nécessite que le visiteur ait un client mail configuré. Pour une solution plus robuste (envoi automatique sans intervention), il faudra brancher un service comme **Formspree**, **Netlify Forms** ou un petit backend.

## 📦 Déploiement sur GitHub Pages

Une fois poussé sur GitHub :

1. Ouvrir les **Settings** du dépôt
2. Aller dans **Pages**
3. Sélectionner la branche `main` et le dossier `/ (root)` → **Save**
4. Le site sera publié à `https://<utilisateur>.github.io/<repo>/`

## 📷 Réseaux

[Instagram @Revoriatest](https://www.instagram.com/Revoriatest/)

## 📝 Licence

Site privé pour le logement Revoria.
