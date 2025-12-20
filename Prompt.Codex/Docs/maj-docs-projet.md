# PROMPT CODEX — Mise à jour Premium+++ de la documentation (analyse repo complet)
## Contexte
Tu interviens sur le dépôt GitHub du projet HypnoHelping.
Objectif : analyser le dépôt (code + configs + docs existantes) et mettre à jour la documentation du dépôt de manière **opérationnelle**, **traçable**, et **sans invention**.

## Règles non négociables
1) Zéro invention / zéro déduction : si une info n’est pas explicitement trouvée dans le dépôt, la marquer clairement comme **UNKNOWN** et proposer un emplacement “À confirmer” dans la doc, sans compléter.
2) Exclusion stricte :
   - Le dossier `docs-gpt/` n’est **PAS** une source de vérité et ne doit **PAS** être modifié, ni utilisé pour valider/inférer des faits.
   - Ne créer **aucun** fichier dans `docs-gpt/`.
3) Gouvernance de la documentation :
   - Suppression interdite par défaut : si un document est obsolète, le **déplacer** en archive (voir section “ARCHIVE”) plutôt que le supprimer.
   - Conserver l’historique Git (commits propres, messages explicites).
4) Respect du périmètre : documentation technique / exploitation / gouvernance / workflows — pas de marketing, pas de copywriting commercial.
5) Traçabilité obligatoire : produire un log de changements de documentation.

## Périmètre d’analyse (sources)
- Analyser tout le repo **sauf** exclusions ci-dessous.
- Exclusions standard à appliquer si présentes (ne pas créer ces dossiers) :
  - `**/node_modules/**`, `**/vendor/**`, `**/dist/**`, `**/build/**`, `**/.cache/**`,
  - fichiers binaires lourds (images, mp3, wav, zip) : ne pas tenter d’en extraire du sens.
- `docs-gpt/` : peut être parcouru uniquement pour repérer sa présence/structure, mais :
  - ne pas le modifier,
  - ne pas l’utiliser comme “vérité”,
  - ne pas en dériver des règles.

## Cibles de mise à jour (documentation)
- Mettre à jour et/ou créer (si manquant) dans le périmètre documentaire du repo :
  1) `README.md` (vue d’ensemble + accès rapide)
  2) `docs/INDEX.md` (table de matière + liens)
  3) Des pages `docs/` structurées (voir “Structure cible”)
  4) Un log de changements : `docs/CHANGELOG_DOCS.md`
  5) Une zone archive : `docs/ARCHIVE/` (déplacer ici tout doc obsolète au lieu de supprimer)

Important :
- Si `docs/` n’existe pas mais qu’il existe déjà un autre répertoire de documentation principal (ex: `documentation/`), utiliser celui déjà en place et créer l’index au bon endroit.
- Ne pas disperser : un seul “centre de doc” (un seul dossier racine).

## Style documentaire (hybride Premium+++)
- Approche hybride :
  - 1 page “overview” (README) + fiches ciblées par domaine dans `docs/`.
- Niveau de détail :
  - Priorité L2/L3 : procédures opérables + invariants + edge cases.
  - L1 seulement si nécessaire pour orienter.

## Structure cible recommandée (à adapter au repo réel)
Créer/mettre à jour les documents suivants (noms indicatifs, ajuster aux conventions déjà présentes) :
- `docs/INDEX.md`
- `docs/ARCHITECTURE.md` : composants, modules, plugins, intégrations, diagramme textuel si utile
- `docs/WORKFLOWS.md` : workflows (staging/prod, déploiement, releases, branches), runbooks
- `docs/CONFIGURATION.md` : variables d’environnement/constantes, fichiers de config, “où régler quoi”
- `docs/LOGGING_AUDIT.md` : journal/log, niveaux, rotation/rétention si documenté dans le repo, pratiques PII si existantes
- `docs/CONVENTIONS_NAMING.md` : conventions de nommage si présentes dans le repo
- `docs/OPERATIONS_RUNBOOK.md` : opérations récurrentes (cron, jobs, sauvegardes) si le repo les expose
- `docs/SECURITY_COMPLIANCE.md` : uniquement ce qui est documenté dans le repo (sinon UNKNOWN)
- `docs/CHANGELOG_DOCS.md`

Si des documents équivalents existent déjà, **mettre à jour** plutôt que créer des doublons.

## Méthode (obligatoire, pas de saut d’étape)
1) Cartographier le repo :
   - Lister les dossiers clés (code, plugins, mu-plugins, scripts, CI, docs existantes).
   - Identifier la/les racines documentaires existantes.
2) Audit de la documentation actuelle :
   - Relever incohérences, pages orphelines, docs obsolètes, doublons.
   - Repérer les “sources” dans le code qui doivent être référencées (chemins, noms de fonctions, hooks, fichiers).
3) Proposer une arborescence doc cible minimale (selon “Structure cible”).
4) Mettre à jour/créer les fichiers doc :
   - Ajouter des sections “Références code” avec chemins précis.
   - Ajouter “UNKNOWN / À confirmer” quand une information manque.
   - Éviter le blabla : chaque doc doit servir une action (comprendre / exécuter / diagnostiquer).
5) Archivage (au lieu de suppression) :
   - Déplacer les docs obsolètes vers `docs/ARCHIVE/` en conservant un court fichier README dans l’archive expliquant la règle.
   - Mettre un pointeur depuis l’INDEX si nécessaire (ex: “Anciennes docs (archives)”).
6) Traçabilité :
   - Remplir `docs/CHANGELOG_DOCS.md` avec :
     - date,
     - liste des fichiers modifiés/créés/déplacés,
     - raison (1 ligne),
     - impacts (1 ligne).
7) Vérifications finales (Definition of Done) :
   - `docs/INDEX.md` pointe vers toutes les pages principales.
   - Aucun lien interne cassé (relatifs).
   - Aucune contradiction évidente entre deux docs sur un même sujet (si contradiction : noter “CONFLICT” + pointer vers sources).
   - `docs-gpt/` inchangé.
   - Aucune suppression “pure” : tout retrait passe par `docs/ARCHIVE/`.
   - README fournit un accès rapide (install, run, doc index, contribution si applicable).

## Sortie attendue (dans ta réponse)
- Un résumé exécutif (10-15 lignes) de ce qui a été mis à jour.
- La liste exhaustive des fichiers :
  - créés,
  - modifiés,
  - déplacés (vers archive),
  - et confirmant explicitement : “docs-gpt/ non modifié”.
- Les principaux “UNKNOWN / À confirmer” détectés (liste courte, actionnable).
- Un plan de commits recommandé (1 à 3 commits max) avec messages.

## Contraintes
- Ne pas toucher au code applicatif sauf si strictement nécessaire pour corriger un lien/chemin dans la doc (par défaut : docs uniquement).
- Ne pas introduire de nouvelles règles “inventées”.
- Respecter les conventions déjà présentes dans le repo (noms, structure, ton).

## Exécuter maintenant
Applique cette méthode sur le repo tel qu’il est, en suivant les règles ci-dessus.
