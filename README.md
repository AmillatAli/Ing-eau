# INGÉEAU — Site vitrine

Page web statique (un seul fichier `index.html`, sans dépendance externe) pour la formation en hydrologie, hydraulique urbaine et hydroinformatique.

## Contenu du dossier

```
ingeeau-site/
├── index.html   → la page complète (HTML + CSS + JS)
├── images/      → desalination.jpg, hydrologie.jpg, Hydraulique.png, Hydroinformatique.png
├── README.md    → ce fichier
└── .gitignore
```

Garde le dossier `images/` au même niveau que `index.html` : les chemins sont relatifs (`images/desalination.jpg`, etc.), donc si tu déplaces ou renommes une image, mets aussi à jour le `background-image` correspondant dans le `<style>`.

## Héberger sur GitHub Pages (gratuit)

1. Crée un nouveau dépôt sur GitHub, par exemple `ingeeau-site` (public, sans README ni licence auto-générés).
2. Depuis ce dossier, en local :
   ```bash
   git init
   git add .
   git commit -m "Site INGÉEAU"
   git branch -M main
   git remote add origin https://github.com/<ton-utilisateur>/ingeeau-site.git
   git push -u origin main
   ```
3. Sur GitHub : **Settings → Pages**.
4. Sous « Build and deployment », choisis **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
5. Après 1–2 minutes, le site est en ligne à l'adresse :
   `https://<ton-utilisateur>.github.io/ingeeau-site/`

### Nom de domaine personnalisé (optionnel)
Dans **Settings → Pages → Custom domain**, ajoute ton domaine (ex. `ingeeau.com`) puis configure chez ton registrar un enregistrement `CNAME` pointant vers `<ton-utilisateur>.github.io`.

## Modifier le contenu

Tout est dans `index.html` :
- **Textes** : cherche directement la phrase à modifier (ex. `PARCOURS HYDROLOGIE`, les horaires `60 h`, etc.).
- **Couleurs** : modifie les variables en haut du `<style>` (`--blue-dark`, `--cyan`, `--green`, `--purple`).
- **Contact** : section `#contact`, liens `mailto:` et `wa.me`.

## Ce qui a été corrigé/amélioré par rapport à la version initiale

- Les 4 images (bandeau + 3 cartes de parcours) sont bien branchées et incluses dans `images/`.
- Ajout d'un menu mobile (bouton hamburger) : la navigation était masquée sous 900 px sans aucun moyen de l'ouvrir.
- Favicon ajouté (icône vague, cohérente avec le logo).
- Balises Open Graph et `theme-color` pour un meilleur rendu au partage et sur mobile.
- Lien d'évitement (« Aller au contenu ») et styles de focus visibles au clavier, pour l'accessibilité.
- `rel="noopener noreferrer"` sur le lien WhatsApp qui s'ouvre dans un nouvel onglet.
- Année du copyright mise à jour automatiquement.
