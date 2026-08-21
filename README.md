# Lucie & Yo Training App

App de suivi pour le programme Renfo de Lucie et Yo. Elle utilise la **même base de données Supabase** que les apps de Jox, Loan, Fifi et Manon — pas besoin de recréer un compte ou un projet.

## Particularité par rapport aux autres apps

Lucie et Yo partagent le même programme et la même app (un seul déploiement, une seule URL). Après avoir entré le code d'accès, un écran demande "Qui es-tu ?" — chacun choisit son prénom, et son suivi (charges, Hooper, historique) reste totalement séparé de l'autre dans la base de données, grâce à la colonne `athlete`. Un bouton "Changer" dans l'en-tête permet de revenir à cet écran (par exemple si les deux s'entraînent sur le même téléphone/ordinateur).

## 1. Base de données

✅ Déjà faite — cette app utilise le même projet Supabase que les autres, avec la colonne `athlete` qui sépare les données de chacun (ici "Lucie" et "Yo").

## 2. Configurer l'appli

✅ Déjà fait — `index.html` contient l'URL et la clé Supabase (les mêmes que pour les autres), et un code d'accès unique partagé (`2469` par défaut, modifiable en cherchant `APP_PIN` dans le fichier).

## 3. Déployer sur Vercel (gratuit) — sans rien installer

Même procédure que pour les autres athlètes :

1. Crée un nouveau repo GitHub (ex: `lucie-yo-training-app`).
2. Upload les 2 fichiers (`index.html`, `README.md`) via "uploading an existing file" sur la page du repo.
3. Va sur [vercel.com/new](https://vercel.com/new), importe ce nouveau repo, déploie avec les réglages par défaut.
4. Récupère l'URL propre du projet (ex: `https://lucie-yo-training-app.vercel.app`, pas l'URL avec un hash aléatoire) dans la section "Domains" du projet.

## 4. Utilisation

Envoie l'URL + le code `2469` à Lucie et à Yo. Chacun choisit son prénom au premier lancement (mémorisé ensuite sur son propre téléphone). Toi, tu ouvres la même URL sur ton ordinateur avec le même code, tu choisis un profil pour consulter son suivi, et tu peux "Changer" pour voir l'autre.
