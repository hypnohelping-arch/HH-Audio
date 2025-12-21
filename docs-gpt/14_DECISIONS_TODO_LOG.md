# Décisions & TODO log
Rôle : centraliser les décisions, dérogations et tâches ouvertes du corpus audio.

## Règles clés
- Enregistrer chaque décision avec date, auteur, impact et action.
- Lier les tâches ouvertes aux segments ou fichiers concernés.
- Clore une tâche seulement après validation QA ou gouvernance.
- Mentionner les risques identifiés et les mesures de mitigation.
- Conserver l'historique ; ne pas supprimer les entrées closes.

## Entrées
- Date : 2025-12-20 | Décision : Taxonomie statuts segments (DRAFT, RECORDED, QA, LOCKED, ARCHIVE) | Impact : alignement des statuts et transitions | Fichiers concernés : docs-gpt/13_GOUVERNANCE_STATUTS_SEGMENTS.md, docs-gpt/04_FORMAT_SCRIPT_FRACTIONNE_V1.md | Statut : VALIDÉ
- Date : 2025-12-20 | Décision : Suppression du statut obsolète | Impact : retrait du statut des conventions | Fichiers concernés : docs-gpt/12_NOMMAGE_FICHIERS_CONVENTIONS.md | Statut : VALIDÉ
- Date : 2025-12-20 | Décision : Gating absolu voix → son | Impact : interdiction d’ajouts musique/binaural/spatialité avant voix LOCKED | Fichiers concernés : docs-gpt/07_MUSIQUE_CHARTE.md, docs-gpt/08_BINAURAL_FREQUENCES_CHARTE.md, docs-gpt/09_SPATIALITE_CHARTE.md | Statut : VALIDÉ
- Date : 2025-12-20 | Décision : Seuils QA audio chiffrés | Impact : seuils LUFS/dBTP obligatoires en QA | Fichiers concernés : docs-gpt/11_QA_CHECKLIST_AUDIO.md | Statut : VALIDÉ
- Date : 2025-12-20 | Décision : Traçabilité par hash hors nommage | Impact : hash consigné en registre/log QA, pas dans le nom de fichier | Fichiers concernés : docs-gpt/03_WORKFLOW_PREMIUM_CORE.md, docs-gpt/12_NOMMAGE_FICHIERS_CONVENTIONS.md | Statut : VALIDÉ
- Date : 2025-12-20 | Décision : Mise en place du mécanisme de dette documentaire (signalement A / B / C) | Impact : gouvernance documentaire transverse | Fichiers concernés : docs-gpt/00_INSTRUCTIONS_GPT.md, docs-gpt/03_WORKFLOW_PREMIUM_CORE.md, docs-gpt/13_GOUVERNANCE_STATUTS_SEGMENTS.md, docs-gpt/14_DECISIONS_TODO_LOG.md | Statut : VALIDÉ
- Date : 2025-12-20 | Décision : Hiérarchie documentaire (GitHub canon, docs-gpt miroir) + obligation clause DOCUMENTATION dans les prompts Codex | Impact : gouvernance documentaire systématique (suggestions GPT + MAJ docs par Codex) | Fichiers concernés : docs-gpt/00_INSTRUCTIONS_GPT.md, docs-gpt/03_WORKFLOW_PREMIUM_CORE.md, docs-gpt/14_DECISIONS_TODO_LOG.md, docs/STRATEGIE_DOCUMENTAIRE.md | Statut : VALIDÉ
- Date : 2025-12-21 | Décision : Init LABO-INTUITION-01 (VOIX_EXISTANTE) + voix déclarée LOCKED (décision humaine) | Impact : traçabilité complète, aucun binaire audio dans Git | Fichiers concernés : production/audio/LABO/LABO-INTUITION-01/*, docs-gpt/14_DECISIONS_TODO_LOG.md | Statut : VALIDÉ
- Date : 2025-12-21 | Décision : Validation QA documentaire LABO-INTUITION-01 | Impact : script fractionné V1 validé (structure, intégrité, confort vocal), gouvernance conforme, audio prêt à être archivé ou utilisé comme base V2 | Fichiers concernés : production/audio/LABO/LABO-INTUITION-01/*, docs-gpt/14_DECISIONS_TODO_LOG.md | Statut : VALIDÉ
