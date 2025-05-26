# Quizzs - Application de Quiz en Direct

Une application de quiz en direct avec intégration Discord, construite avec Next.js.

## Fonctionnalités

- Création et gestion de quiz
- Sessions de jeu en direct
- Intégration avec Discord
- Interface de création de quiz
- Interface de jeu en temps réel

## Prérequis

- Node.js 18+
- PostgreSQL
- Compte Discord Developer

## Installation

1. Cloner le repository
```bash
git clone [votre-repo]
cd quizzs
```

2. Installer les dépendances
```bash
npm install
```

3. Configurer les variables d'environnement
```bash
cp .env.example .env
```
Remplir les variables dans le fichier `.env` :
- `DATABASE_URL` : URL de votre base de données PostgreSQL
- `NEXTAUTH_SECRET` : Clé secrète pour NextAuth
- `DISCORD_CLIENT_ID` : ID client de votre application Discord
- `DISCORD_CLIENT_SECRET` : Secret client de votre application Discord

4. Initialiser la base de données
```bash
npx prisma db push
```

5. Lancer le serveur de développement
```bash
npm run dev
```

## Déploiement sur Vercel

1. Créer un nouveau projet sur Vercel
2. Connecter votre repository GitHub
3. Configurer les variables d'environnement dans Vercel :
   - `DATABASE_URL`
   - `NEXTAUTH_SECRET`
   - `DISCORD_CLIENT_ID`
   - `DISCORD_CLIENT_SECRET`

4. Déployer !

## Configuration Discord

1. Aller sur [Discord Developer Portal](https://discord.com/developers/applications)
2. Créer une nouvelle application
3. Dans la section OAuth2 :
   - Ajouter l'URL de redirection : `https://votre-domaine/api/auth/callback/discord`
   - Copier le Client ID et Client Secret
4. Activer les "Bot" et "OAuth2" dans les paramètres de l'application

## Structure du Projet

```
src/
  ├── app/              # Routes et pages Next.js
  ├── components/       # Composants React réutilisables
  ├── lib/             # Utilitaires et configurations
  ├── hooks/           # Hooks React personnalisés
  └── types/           # Types TypeScript
```

## Technologies Utilisées

- Next.js 14
- TypeScript
- Prisma
- PostgreSQL
- NextAuth.js
- Socket.io
- Tailwind CSS
- Shadcn/ui
