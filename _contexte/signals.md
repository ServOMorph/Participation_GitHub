# Signals — participation_github   (MAJ 2026-08-04)

## Actions ouvertes
- [P1|ouvert] Lancer /analyse-prs sur les projets prioritaires pour choisir une première PR
  fait quand: un tableau de classement des issues est produit et une PR est choisie
  réf: .claude/commands/analyse-prs.md, _DOCS/projets_candidats.md

## Dernière session (2026-08-04)
<!-- Écrasé intégralement par /close. Synthèse < 25 lignes. -->
# Session du 2026-08-04

## Décisions prises
- Repo GitHub ServOMorph/opencode supprimé (fork obsolète)
- Projets prioritaires retenus : Ollama, RustDesk, Tesseract-OCR, OpenCode
- Nom "commands" (pluriel) confirmé pour .opencode/commands, malgré la convention "command" du repo OpenCode cloné
- Nom "participations" retenu pour le dossier racine regroupant les clones par projet

## Livrables produits ou modifiés
- .claude/commands/analyse-prs.md : créé
- .opencode/commands/ : créé (copie de .claude/commands)
- _DOCS/projets_candidats.md : créé, section priorités ajoutée
- _contexte/contexte.md : décisions de session ajoutées
- participations/OpenCode/ : déplacé depuis la racine, .git imbriqué supprimé au préalable

## Hypothèses validées / invalidées
- VALIDE : structure .opencode/commands (pluriel) confirmée par l'utilisateur
- EN ATTENTE : exécution de /analyse-prs sur les 4 projets prioritaires

## Prochaine étape exacte
Lancer /analyse-prs pour obtenir le classement des issues candidates sur Ollama, RustDesk,
Tesseract-OCR, OpenCode, puis choisir la première contribution.

## Question bloquante pour la session suivante
Aucune
