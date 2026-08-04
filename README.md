# Participation GitHub

## Objectif
Créer un agent qui participera à des projets GitHub open source.

## Stack
À définir (préciser ultérieurement).

## Structure
- `.claude/commands/` : commandes Claude Code (`/start`, `/close`, `/analyse-prs`)
- `.opencode/commands/` : miroir des commandes pour OpenCode
- `participations/` : un sous-dossier par projet ciblé (clone local)
- `_DOCS/` : documentation de zone (but du projet, projets candidats)
- `_contexte/` : protocole vibecoding (`contexte.md`, `signals.md`)

## État actuel
Structure du projet en place : `.claude/commands/analyse-prs.md` (classement des PR candidates),
`.opencode/commands/` (miroir pour OpenCode), `participations/` (clones par projet, contient
OpenCode). Projets prioritaires définis : Ollama, RustDesk, Tesseract-OCR, OpenCode. Commande
`/analyse-prs` créée mais pas encore exécutée.
