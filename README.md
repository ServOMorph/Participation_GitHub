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
Projets prioritaires définis : Ollama, RustDesk, Tesseract-OCR, OpenCode. `/analyse-prs` exécuté
le 2026-08-04 : classement des issues candidates produit sur les 4 repos. Meilleure cible retenue :
rustdesk/rustdesk #3762 (audio ASIO). Aucune PR lancée, en attente d'approbation utilisateur.
