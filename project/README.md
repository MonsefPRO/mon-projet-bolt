# Ellipsys - Site Web

Site web professionnel pour Ellipsys, spécialiste du nettoyage par drone.

## Déploiement rapide

### Option 1 : Netlify (Recommandé)

1. Créez un compte sur [Netlify](https://netlify.com)
2. Connectez votre repository GitHub
3. Configuration automatique détectée
4. Ajoutez les variables d'environnement dans Netlify :
   - Allez dans Site settings > Environment variables
   - Ajoutez `VITE_SUPABASE_URL` et `VITE_SUPABASE_ANON_KEY`
   - Utilisez les valeurs de votre fichier `.env` local
5. Le site sera en ligne automatiquement

### Option 2 : GitHub + Netlify

1. Créez un repository sur GitHub
2. Uploadez tous les fichiers du projet
3. Sur Netlify, cliquez sur "Import from Git"
4. Sélectionnez votre repository
5. Déployez automatiquement

### Option 3 : Upload manuel sur Netlify

1. Exécutez `npm run build` dans le projet
2. Sur Netlify, glissez-déposez le dossier `dist`
3. Votre site est en ligne

## Structure du projet

```
ellipsys-site/
├── public/              # Images et ressources
├── src/                 # Code source
│   ├── components/      # Composants réutilisables
│   ├── contexts/        # Contextes React
│   ├── pages/           # Pages du site
│   ├── translations/    # Traductions FR/EN
│   └── utils/           # Utilitaires
├── dist/                # Build de production (généré)
├── .env                 # Variables d'environnement
├── index.html           # Point d'entrée HTML
└── package.json         # Dépendances
```

## Technologies utilisées

- React + TypeScript
- TailwindCSS
- Vite
- React Router
- Supabase (base de données)

## Commandes utiles

```bash
npm install          # Installer les dépendances
npm run dev         # Lancer en développement
npm run build       # Créer le build de production
npm run preview     # Prévisualiser le build
```

## Fonctionnalités

- Site multilingue (FR/EN)
- Design responsive
- Formulaire de contact
- Pages de services détaillées
- Optimisé pour le SEO
- Animations fluides

## Support

Pour toute question : contact@ellipsys.fr
