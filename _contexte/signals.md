# Signals — participation_github   (MAJ 2026-08-17)

## Actions ouvertes
- [P1|ouvert] Suivre et évaluer le repo public argosopentech/argos-translate pour une contribution
  fait quand: le repo est cloné localement et un bug de régression est reproductible en test
  réf: https://github.com/argosopentech/argos-translate, issue GitHub #500
- [P2|ouvert] Reproduire le bug de régression de la version 1.10 sur la commande CLI de traduction
  fait quand: la commande "argos-translate --from en --to it ..." reproduit les warnings "Unsupported language: tl/eo/az/ms"
  réf: issue GitHub #500, README du dépôt, code de validation des langues

## Dernière session (2026-08-17)
# Session du 2026-08-17

## Décisions prises
- CIBLE ACTÉE : suivre argosopentech/argos-translate comme dépôt de contribution principal pour cette session.
- CIBLE ACTÉE : l’issue #500 est la piste de contribution la plus concrète signalée dans le flux de travail actuel.

## Livrables produits ou modifiés
- Analyse du dépôt public Argos Translate : identification du projet comme traduction hors ligne en Python, CLI + API + modèles.
- Vérification locale : aucun clone ni code Argos présent dans ce workspace ; le dépôt est suivi via le repo public.

## Hypothèses validées / invalidées
- VALIDE : le dépôt Argos Translate est bien un projet open source de traduction offline en Python.
- VALIDE : les informations de l’issue #500 sont suffisantes pour établir un bug de régression plausible.
- EN ATTENTE : reproduction locale du bug et validation de la piste de correctif dans le code du repo.

## Prochaine étape exacte
Cloner le dépôt public argosopentech/argos-translate dans `participations/` ou dans un dossier local dédié.
Puis reproduire le cas issue #500 (en -> it) et identifier la validation des langues / le point de ralentissement avant d’ouvrir une PR.

## Question bloquante pour la session suivante
Le bug est-il bien causé par la validation de langue “unsupported language” en 1.10, ou le ralentissement vient d’un autre point du pipeline de traduction ?
