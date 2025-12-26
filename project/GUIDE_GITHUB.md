# Guide : Upload sur GitHub

## Préparation

Le projet est maintenant nettoyé et prêt pour GitHub. Voici les étapes :

## Méthode 1 : Via l'interface GitHub (Plus simple)

### Étape 1 : Créer le repository

1. Allez sur [github.com](https://github.com)
2. Cliquez sur le bouton vert "New" ou "+"
3. Donnez un nom : `ellipsys-site`
4. Laissez "Public" ou choisissez "Private"
5. **NE COCHEZ PAS** "Add a README" (on en a déjà un)
6. Cliquez sur "Create repository"

### Étape 2 : Upload les fichiers

1. Sur la page de votre nouveau repository
2. Cliquez sur "uploading an existing file"
3. **Glissez-déposez TOUS les fichiers et dossiers** du projet
4. Attendez que l'upload se termine
5. En bas, écrivez "Initial commit"
6. Cliquez sur "Commit changes"

## Méthode 2 : Via Git GUI (Alternative)

### Si l'upload web ne fonctionne pas

1. Ouvrez **Git GUI**
2. Cliquez sur "Clone Existing Repository"
3. Source : `https://github.com/VOTRE_USERNAME/ellipsys-site.git`
4. Target : Choisissez un dossier vide
5. Cliquez sur "Clone"
6. Copiez TOUS les fichiers du projet nettoyé dans ce dossier
7. Dans Git GUI : "Rescan" → "Stage Changed" → "Commit" → "Push"

## Fichiers importants inclus

- `README.md` : Documentation du projet
- `.env.example` : Template des variables d'environnement
- `.gitignore` : Ignore les fichiers sensibles
- `netlify.toml` : Configuration Netlify
- `src/` : Tout le code source
- `public/` : Images et ressources

## Fichiers exclus (automatiquement ignorés)

- `node_modules/` : Trop gros, sera réinstallé automatiquement
- `dist/` : Sera régénéré lors du build
- `.env` : Contient des secrets, ne doit PAS être uploadé

## Après l'upload sur GitHub

1. Allez sur [netlify.com](https://netlify.com)
2. "Import from Git" → Choisissez GitHub
3. Sélectionnez votre repository `ellipsys-site`
4. **IMPORTANT** : Ajoutez les variables d'environnement :
   - Site settings → Environment variables
   - Ajoutez `VITE_SUPABASE_URL` et `VITE_SUPABASE_ANON_KEY`
   - (Copiez les valeurs depuis votre fichier `.env` local)
5. Cliquez sur "Deploy"

Votre site sera en ligne en quelques minutes !

## Besoin d'aide ?

Si vous avez des erreurs "File too large", c'est que certains fichiers n'ont pas été supprimés. Vérifiez que :
- Le dossier `.bolt` n'existe plus
- Le dossier `dist` n'existe plus
- Les fichiers ZIP ont été supprimés
- Les images dupliquées (avec "copy") ont été supprimées
