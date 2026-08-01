# Dar Tajine | دار الطاجين — Site Web

Site vitrine statique (HTML + Tailwind CSS via CDN) pour le restaurant Dar Tajine à Agadir.
Un seul fichier, aucune installation ni build nécessaire.

## Contenu du dossier

```
.
├── index.html      → le site (page unique)
├── .gitignore
└── README.md
```

Vercel sert automatiquement `index.html` comme page d'accueil, c'est pour cela qu'il faut garder ce nom exact à la racine du projet.

---

## Étape 1 — Mettre le projet sur GitHub

### Option A — Sans ligne de commande (le plus simple)
1. Va sur [github.com](https://github.com) et crée un compte si besoin.
2. Clique sur **New repository** (bouton vert en haut à droite).
3. Nomme-le par exemple `dar-tajine`, laisse-le en **Public**, ne coche aucune case d'initialisation, puis **Create repository**.
4. Sur la page suivante, clique sur **uploading an existing file**.
5. Glisse-dépose `index.html`, `.gitignore` et `README.md`.
6. Clique sur **Commit changes**.

### Option B — Avec Git en ligne de commande
```bash
cd chemin/vers/le/dossier
git init
git add .
git commit -m "Site Dar Tajine"
git branch -M main
git remote add origin https://github.com/TON-NOM-UTILISATEUR/dar-tajine.git
git push -u origin main
```
(Crée d'abord le dépôt vide sur GitHub comme à l'étape A.1–A.3, sans y ajouter de fichiers.)

---

## Étape 2 — Déployer sur Vercel

1. Va sur [vercel.com](https://vercel.com) et connecte-toi **avec ton compte GitHub** (bouton "Continue with GitHub").
2. Clique sur **Add New… → Project**.
3. Sélectionne le dépôt `dar-tajine` dans la liste et clique sur **Import**.
4. Vercel détecte automatiquement un site statique :
   - **Framework Preset** : `Other`
   - **Build Command** : laisser vide
   - **Output Directory** : laisser vide (ou `./`)
5. Clique sur **Deploy**.
6. Après ~30 secondes, Vercel te donne une URL du type `dar-tajine.vercel.app` — le site est en ligne.

---

## Étape 3 — Mises à jour futures

Chaque fois que tu modifies `index.html` et que tu pousses (`git push`) ou ré-uploades le fichier sur GitHub, Vercel redéploie automatiquement le site en quelques secondes. Aucune action supplémentaire n'est nécessaire.

---

## Étape 4 — Nom de domaine personnalisé (optionnel)

Si tu possèdes un nom de domaine (ex. `dartajine.ma`) :
1. Dans le projet Vercel, va dans **Settings → Domains**.
2. Ajoute ton domaine.
3. Vercel te donne les enregistrements DNS (souvent un `A` ou `CNAME`) à ajouter chez ton registrar (OVH, GoDaddy, etc.).
4. Le certificat HTTPS est généré automatiquement, gratuitement.

---

## Bon à savoir

- Le site charge Tailwind CSS, les polices Google et une image depuis des CDN externes : une connexion Internet est nécessaire pour que la mise en page s'affiche correctement (normal pour un site web).
- **Pense à remplacer l'image de fond du hero** (actuellement une photo Unsplash de démonstration) par une vraie photo du restaurant dont tu détiens les droits, pour éviter tout souci de droits d'auteur en production.
- Aucune variable d'environnement, base de données ou clé API n'est nécessaire : c'est un site 100 % statique.
