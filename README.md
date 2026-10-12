# Targil · תרגיל

Aide aux devoirs de maths pour les olim hadashim. L'élève photographie un exercice ou une leçon en hébreu ; Claude traduit l'énoncé dans sa langue et guide la résolution pas à pas, avec la phrase de réponse à écrire en hébreu dans le cahier.

## Installer sur un téléphone Android

1. Ouvrir l'adresse GitHub Pages du dépôt dans Chrome.
2. Menu ⋮ → « Installer l'application » (ou « Ajouter à l'écran d'accueil »), ou le bouton « Installer Targil » sur l'accueil.
3. Dans Targil : Réglages → « Clé API Claude (pour les parents) » → coller la clé → « Enregistrer et tester ».

## Clé API

- Créée sur https://platform.claude.com (facturation à l'usage, séparée de l'abonnement Claude).
- Saisie sur l'appareil, stockée dans le navigateur du téléphone, envoyée uniquement à `api.anthropic.com`.
- Jamais dans ce dépôt. Prévoir une clé dédiée et une limite de dépense mensuelle dans la Console.

## Fichiers

- `index.html` : toute l'application (interface, textes en 5 langues, appels à l'API Claude).
- `manifest.webmanifest`, `icons/` : installation sur l'écran d'accueil.
- `sw.js` : démarrage hors ligne de l'interface (les appels à Claude nécessitent Internet).

Modèles utilisés : `claude-sonnet-5-5` (lecture des photos, résolution), `claude-haiku-5-5` (réexplications courtes, correction des réponses).
