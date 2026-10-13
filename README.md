# Targil · תרגיל

Aide aux devoirs de maths pour les olim hadashim. L'élève photographie un exercice ou une leçon en hébreu ; Claude traduit l'énoncé dans sa langue et guide la résolution pas à pas, avec la phrase de réponse à écrire en hébreu dans le cahier.

## Fonctions

- Exercices : photo → texte hébreu lu (corrigeable) → traduction → aide en mode « indices d'abord » → solution pas à pas.
- Vérifier ma copie : photo du cahier de l'élève, Claude trouve la première erreur sans donner la réponse.
- Leçon : idées clés, traduction ligne à ligne, exemple résolu.
- Lexique : mots hébreux de chaque page, avec audio.
- Calculs exacts : Claude utilise une calculatrice intégrée (fractions exactes) pour chaque nombre écrit.
- Pays d'origine : les explications signalent les conventions israéliennes qui diffèrent (point décimal, etc.).
- Espace parent protégé par un code à 4 chiffres : clé API, mode d'aide (libre ou indices d'abord), retours « explication utile / signalée ».
- Les photos restent sur le téléphone (IndexedDB) ; elles ne sont envoyées qu'à l'API Claude.

## Installer sur un téléphone Android

1. Ouvrir l'adresse GitHub Pages du dépôt dans Chrome.
2. Menu ⋮ → « Installer l'application » (ou « Ajouter à l'écran d'accueil »), ou le bouton « Installer Targil » sur l'accueil.
3. Dans Targil : « Première étape » → créer le code parent → coller la clé API → « Enregistrer et tester ».

## Clé API

- Créée sur https://platform.claude.com (facturation à l'usage, séparée de l'abonnement Claude).
- Saisie sur l'appareil, stockée dans le navigateur du téléphone, envoyée uniquement à `api.anthropic.com`.
- Jamais dans ce dépôt. Prévoir une clé dédiée et une limite de dépense mensuelle dans la Console.

## Fichiers

- `index.html` : toute l'application (interface, textes en 5 langues, appels à l'API Claude).
- `manifest.webmanifest`, `icons/` : installation sur l'écran d'accueil.
- `sw.js` : démarrage hors ligne de l'interface (les appels à Claude nécessitent Internet).

Modèles utilisés (réglage « Coût et qualité » de l'espace parent) :

- Économique (par défaut) : `claude-sonnet-5-5` lit les photos (exercices, leçons) et les copies, et refait une explication signalée ; `claude-haiku-5-5` fait tout le reste (résolution avec la calculatrice, indices, réexplications, retraduction, correction, exercices similaires).
- Qualité maximale : `claude-sonnet-5-5` pour tout.
- Pour la résolution, la photo n'est renvoyée que si l'exercice a une figure, si l'énoncé n'a pas été lu, ou si l'élève a signalé un énoncé mal lu.
