# Contexte — participation_github

## Objectif (immuable sauf décision explicite)
Créer un agent qui participera à des projets GitHub open source.

## Stack / contraintes techniques (stable, rarement modifié)
À définir (préciser ultérieurement).

## État actuel (réécrit intégralement à chaque /close)
Structure du projet en place : `.claude/commands/analyse-prs.md` (classement des PR candidates),
`.opencode/commands/` (miroir pour OpenCode), `participations/` (clones par projet, contient
OpenCode). Projets prioritaires définis. Commande /analyse-prs créée mais pas encore exécutée.

## Décisions structurantes (append only — 10 entrées max, 5 lignes max/entrée, archiver au-delà)
- 2026-08-04 : Initialisation du protocole vibecoding.
- 2026-08-04 : Projets prioritaires retenus pour la participation : Ollama, RustDesk, Tesseract-OCR, OpenCode.
- 2026-08-04 : Suppression du fork GitHub ServOMorph/opencode (obsolète).
- 2026-08-04 : Structure OpenCode mise en place : `.opencode/commands` (pluriel, copie de `.claude/commands`), dossier `participations/` pour les clones par projet.
