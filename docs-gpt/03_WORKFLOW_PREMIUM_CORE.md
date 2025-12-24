# Workflow premium core (miroir canon /docs/audio/PLAN_REFERENCE_USINE_AUDIO_PREMIUM+++.md)

## Chaîne de production canonique
- Pipeline unique pour tous les audios : cadrage → script clean/studio → VOICE_DRAFT → VOICE_LOCKED → SEGMENTATION_LOCKED → SOUND_DESIGN_ALLOWED → MIX_ITERATING → PREVIEW_APPROVED → FINAL_RENDERED → RELEASE_LOCKED.
- Aucun saut d’étape : VOICE_LOCKED est obligatoire avant toute musique/binaural/spatialité ou sound design.
- Deux modes seulement (STANDARD Premium+++, SIGNATURE) suivent exactement les mêmes étapes ; SIGNATURE ajoute une validation renforcée.
- Toute modification de script crée une nouvelle version audio (lien explicite script_version ↔ audio_version).

## Exigences de production
- Scripts hébergés dans chaque projet GitHub : `script_clean.md` (texte hypnotique pur) et `script_studio.md` (intentions vocales, silences, respiration).
- Découpage par blocs hypnotiques : découpage fonctionnel long, chaque bloc = unité de travail ; segmentation figée avant tout sound design.
- Gestion des créations partielles : voix seule intégrable ; audio complet existant = recréation contrôlée (jamais patchée).
- Réutilisation de blocs audio non active en V1 (bibliothèque prévue plus tard).

## Validation et contrôle
- HH-AutoMix Engine v1 déterministe, déclenché uniquement si AUTOMIX_AUTORISE après pré-check bloquant.
- Aucune ré-exécution silencieuse : toute nouvelle itération nécessite une autorisation humaine explicite et tracée.
- Validation post-mix : écoute humaine ≤ 60 s puis décision souveraine (Go / ajustement minimal / No-Go) avant publication.
- Journal perceptif humain court par bloc hypnotique ; jamais automatisé.

## Gouvernance et traçabilité
- Décisions versionnées et réversibles ; exceptions consignées dans docs-gpt/14_DECISIONS_TODO_LOG.md.
- Statut voix global dérivé : jamais saisi manuellement ; repose sur l’état des segments et du pipeline.
- Hashs consignés dans registres/logs QA, jamais dans le nommage fichier.
