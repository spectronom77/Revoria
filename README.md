# Disney Magic — Site Vitrine

Un site vitrine dédié à l'histoire fascinante de Disney, construit en HTML, CSS et JavaScript pur.

## ✨ Aperçu

Ce site propose un voyage à travers l'histoire de Disney, depuis la fondation du studio en 1923 jusqu'aux acquisitions modernes (Pixar, Marvel, Lucasfilm).

## 📂 Structure du projet

```
.
├── index.html          # Page d'accueil avec section hero
├── a-propos.html       # Histoire de Disney avec timeline
├── contact.html        # Formulaire de contact
├── css/
│   └── style.css       # Styles (thème magique & coloré)
├── js/
│   └── main.js         # Interactions (menu, animations, validation)
└── assets/
    └── images/         # Dossier pour les images (à compléter)
```

## 🚀 Lancer le site en local

Aucun build n'est nécessaire. Il suffit d'ouvrir `index.html` dans un navigateur, ou de lancer un petit serveur local :

```bash
# Avec Python
python3 -m http.server 8000

# Avec Node (npx)
npx serve .
```

Puis ouvrir [http://localhost:8000](http://localhost:8000) dans le navigateur.

## 🎨 Personnalisation

Les couleurs principales sont définies en variables CSS dans `css/style.css` (section `:root`) :

- `--color-primary` : violet principal
- `--color-secondary` : rose
- `--color-accent` : doré
- `--gradient-magic` : dégradé signature

## 📦 Déploiement

Le site est compatible **GitHub Pages** sans configuration. Une fois poussé sur GitHub :

1. Ouvrir les **Settings** du dépôt
2. Aller dans **Pages**
3. Sélectionner la branche `main` et le dossier `/ (root)`
4. Le site sera publié à l'adresse `https://<utilisateur>.github.io/<repo>/`

## 📝 Licence

Projet vitrine éducatif — Non affilié à The Walt Disney Company.
