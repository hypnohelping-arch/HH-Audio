# PROMPT CODEX — Synchronisation Premium+++ de docs-gpt depuis le repo (sources de vérité internes)

## Contexte
Tu interviens sur le dépôt GitHub du projet HypnoHelping.

Objectif :
- Scruter l’ensemble du dépôt GitHub afin d’identifier les **sources de vérité effectives** (code, configurations, workflows, chartes, statuts, règles documentées).
- Mettre à jour **exclusivement** les fichiers existants du dossier `docs-gpt/` afin qu’ils reflètent fidèlement l’état réel du projet.
- Aucun autre dossier de documentation n’est modifié dans cette mission.

## Règles absolues (non négociables)

### 1) Zéro invention / zéro supposition
- Toute information intégrée dans `docs-gpt/` doit être **explicitement trouvée** dans le dépôt.
- Si une information attendue n’est pas trouvée ou est ambiguë :
  - la marquer clairement comme **UNKNOWN** ou **À CONFIRMER** dans le fichier concerné,
  - ne jamais compléter par déduction, extrapolation ou “bonne pratique supposée”.

### 2) Gouvernance stricte de docs-gpt
- Le dossier `docs-gpt/` est :
  - un **référentiel structurant**,
  - à **fichiers verrouillés**.
- Interdictions formelles :
  - ❌ créer un nouveau fichier dans `docs-gpt/`,
  - ❌ supprimer un fichier existant,
  - ❌ renommer un fichier,
  - ❌ déplacer un fichier hors de `docs-gpt/`.
- Autorisé :
  - ✅ modifier **le contenu interne** des fichiers existants,
  - ✅ mettre à jour sections, listes, tableaux, statuts, mentions, tant que la structure globale reste cohérente.

### 3) docs-gpt comme cible finale
- Contrairement aux missions précédentes :
  - `docs-gpt/` est **la cible de mise à jour**,
  - mais **pas la seule source**.
- Les sources de vérité sont **le reste du repo** (code, configs, scripts, docs techniques, chartes, workflows).

## Périmètre d’analyse (sources)

Analyser l’intégralité du dépôt **hors contraintes suivantes** :

### Exclusions techniques d’analyse
Ne pas analyser comme source sémantique :
- `**/node_modules/**`
- `**/vendor/**`
- `**/dist/**`, `**/build/**`
- `**/.cache/**`
- fichiers binaires lourds (mp3, wav, png, jpg, zip, pdf)

### Inclus explicitement comme sources de vérité potentielles
- Code applicatif (plugins, mu-plugins, scripts)
- Fichiers de configuration (`wp-config`, constantes, `.env.example`, etc.)
- Workflows CI/CD si présents
- Dossiers `docs/`, `Prompt.Codex/`, chartes, specs, runbooks existants
- Fichiers de logs de gouvernance, checklists, statuts si présents dans le repo

## Méthode obligatoire (séquentielle)

### Étape 1 — Cartographie des sources de vérité
- Identifier :
  - règles explicites,
  - invariants documentés,
  - workflows réels,
  - statuts verrouillés,
  - hiérarchies (ex: voix → musique → effets, validation avant exécution, etc.).
- Lister les fichiers précis d’où proviennent ces règles (chemins exacts).

### Étape 2 — Audit de cohérence docs-gpt
Pour chaque fichier existant dans `docs-gpt/` :
- Identifier :
  - sections obsolètes,
  - informations manquantes,
  - décalages avec la réalité du repo,
  - règles non vérifiables dans les sources.

### Étape 3 — Mise à jour contrôlée de docs-gpt
- Mettre à jour le **contenu interne** de chaque fichier :
  - aligner les règles avec ce qui est effectivement implémenté ou documenté ailleurs,
  - ajouter des références explicites vers les fichiers sources du repo,
  - marquer clairement les zones **UNKNOWN / À CONFIRMER** si nécessaire.
- Ne jamais :
  - changer l’intention du fichier,
  - élargir son périmètre au-delà de ce qu’il couvre déjà.

### Étape 4 — Cohérence transversale
- Vérifier que :
  - deux fichiers `docs-gpt/` ne se contredisent pas,
  - les statuts, règles et verrous sont alignés entre eux.
- En cas de conflit entre deux sources du repo :
  - documenter explicitement le conflit dans `docs-gpt/`,
  - citer les deux sources,
  - ne pas arbitrer sans preuve explicite.

### Étape 5 — Traçabilité
- Ne pas créer de nouveau fichier de log dans `docs-gpt/`.
- Ajouter, dans chaque fichier modifié si pertinent :
  - une courte mention de mise à jour (date + “alignement repo”),
  - sans historique narratif excessif.

## Definition of Done (DoD)

La mission est considérée comme terminée si :
1) Tous les fichiers existants de `docs-gpt/` ont été analysés.
2) Les contenus sont alignés avec les sources réelles du repo.
3) Aucune information non vérifiable n’a été ajoutée.
4) Toutes les zones d’incertitude sont explicitement marquées.
5) Aucun fichier n’a été créé, supprimé, renommé ou déplacé dans `docs-gpt/`.
6) Les références aux sources (chemins, fichiers) sont présentes quand utiles.
7) La cohérence globale de `docs-gpt/` est renforcée, pas diluée.

## Sortie attendue (dans ta réponse Codex)
- Résumé exécutif (10–15 lignes) :
  - ce qui a été aligné,
  - ce qui était obsolète,
  - ce qui reste UNKNOWN.
- Liste exhaustive des fichiers `docs-gpt/` modifiés.
- Pour chaque fichier :
  - principales sections mises à jour,
  - sources utilisées (chemins repo).
- Liste finale des points nécessitant **validation humaine**.

## Exécution
Appliquer strictement cette procédure sur l’état actuel du dépôt.
Ne rien supposer. Ne rien inventer. Ne pas “améliorer” au-delà de l’alignement factuel.
