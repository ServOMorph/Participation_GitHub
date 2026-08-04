# Contexte — participation_github

## Objectif (immuable sauf décision explicite)
Créer un agent qui participera à des projets GitHub open source.

## Stack / contraintes techniques (stable, rarement modifié)
À définir (préciser ultérieurement).

## État actuel (réécrit intégralement à chaque /close)
/analyse-prs exécuté le 2026-08-04 sur les 4 repos prioritaires : classement des issues produit.
Meilleure cible : rustdesk/rustdesk #3762 (audio ASIO, 6/10), en attente d'approbation utilisateur.
sst/opencode : aucune issue "good first issue" ni "help wanted" ouverte. Aucune PR lancée pour l'instant.

## Décisions structurantes (append only — 10 entrées max, 5 lignes max/entrée, archiver au-delà)
- 2026-08-04 : Initialisation du protocole vibecoding.
- 2026-08-04 : Projets prioritaires retenus pour la participation : Ollama, RustDesk, Tesseract-OCR, OpenCode.
- 2026-08-04 : Suppression du fork GitHub ServOMorph/opencode (obsolète).
- 2026-08-04 : Structure OpenCode mise en place : `.opencode/commands` (pluriel, copie de `.claude/commands`), dossier `participations/` pour les clones par projet.
