# SPEAK NOW v2.3 — Déploiement gratuit

Architecture prête pour hébergement cloud :
- frontend statique
- API Node.js
- PostgreSQL cloud

## API
Déployer `backend`.
Build : `npm install`
Start : `npm start`

Variables d'environnement :
`DATABASE_URL`, `JWT_SECRET`, `CORS_ORIGIN`

## Base de données
Créer une PostgreSQL cloud compatible et placer sa chaîne `DATABASE_URL` dans les variables de l'API.

## Frontend
Publier `frontend` comme site statique.
Dans SPEAK NOW, utiliser l'URL publique de l'API au lieu de `http://localhost:3000`.

## Vérification
Après déploiement :
`https://TON-API/api/health`

Les offres gratuites peuvent changer. Ne mets jamais une clé secrète directement dans le frontend.
