---
description: Analyse les repos des projets prioritaires et propose un classement de PR à faire
argument-hint: [repo]
model: opus
allowed-tools: Bash(gh issue list:*), Bash(gh issue view:*), Bash(gh repo view:*), Bash(gh search:*), Bash(gh pr list:*), WebFetch
---

# /analyse-prs [repo]

## Source des projets

Lire `_DOCS/projets_candidats.md`, section "Projets prioritaires", pour obtenir la liste des
repos GitHub à analyser (format `owner/repo`).

## Procédure

1. Résoudre la cible :
   - Si $ARGUMENTS contient un repo (`owner/repo` ou nom d'application de la liste) : analyser
     uniquement ce repo.
   - Si absent : analyser tous les repos de la section "Projets prioritaires".

2. Pour chaque repo cible, interroger GitHub via `gh` :
   - `gh issue list --repo <owner/repo> --label "good first issue" --state open --limit 30`
   - `gh issue list --repo <owner/repo> --label "help wanted" --state open --limit 30`
   - Fusionner les résultats, dédupliquer par numéro d'issue.
   - Exclure les issues déjà assignées (`assignees` non vide) ou déjà liées à une PR ouverte
     (vérifier via `gh issue view <n> --repo <owner/repo> --json assignees,linkedBranches`).

3. Pour chaque issue candidate restante, lire le détail complet :
   `gh issue view <n> --repo <owner/repo> --json title,body,labels,comments,createdAt,updatedAt,assignees`

4. Noter chaque issue sur 10, à partir de ces critères explicites (poids indicatif, à ajuster
   si un critère est inapplicable — le dire dans ce cas) :
   - **Clarté de la spec (0-3)** : description précise, comportement attendu explicite, pas
     d'ambiguïté sur le périmètre.
   - **Taille estimée (0-2)** : petite tâche ciblée = 2, refonte large ou multi-fichiers = 0.
   - **Fraîcheur (0-2)** : issue active récemment (commentaires ou mise à jour < 60 jours) = 2,
     issue stale (> 6 mois sans activité) = 0.
   - **Absence de concurrence (0-2)** : aucune PR liée ni assignation existante = 2, PR déjà en
     cours par un tiers = 0 (exclure si 0, ne pas noter).
   - **Accessibilité technique (0-1)** : label "good first issue" ou équivalent présent = 1.

   Ne jamais inventer une note sans avoir lu le détail de l'issue à l'étape 3. Si une donnée
   manque pour noter un critère, l'indiquer plutôt que de deviner.

5. Produire un tableau classé par note décroissante :

   ```
   ## <owner/repo>

   | # | Issue | Titre | Note /10 | Justification (1 ligne) |
   |---|-------|-------|----------|--------------------------|
   ```

6. À la fin, désigner une seule meilleure recommandation toutes analyses confondues (ou par
   repo si $ARGUMENTS cible plusieurs repos sans dégager de gagnant clair) avec une
   justification de 2-3 lignes citant les critères de l'étape 4.

7. Ne pas commencer de travail sur la PR recommandée (pas de fork, pas de clone, pas de code).
   Attendre une confirmation explicite de l'utilisateur avant toute action suivante.

<!-- SPECIFICITES PROJET : DEBUT (préservé par /update, ne pas toucher hors de ce bloc) -->
<!-- Convention : toute règle liée à une étape précise de la Procédure ci-dessus doit la
     référencer explicitement par son numéro. -->
<!-- SPECIFICITES PROJET : FIN -->
