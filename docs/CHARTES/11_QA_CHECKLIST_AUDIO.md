# QA — Checklist audio

---
Statut: CANON (opérationnel)
Version: V1 (CORE figé)
Date: 2025-12-24
Source: publication depuis docs-gpt (miroir)
Gouvernance: voir docs-gpt/14_DECISIONS_TODO_LOG.md
---


## Sources canoniques
- Validation post-mix : écoute humaine ≤ 60 s avant publication (docs/audio/PLAN_REFERENCE_USINE_AUDIO_PREMIUM+++.md).
- TODO_SYSTEME_QUALITE_AUDIO.md : structuration en cours de l’indice qualité et des seuils éditoriaux.

## Checklist minimale (canon + rappel opérations)
- Pré-check bloquant avant HH-AutoMix Engine v1, puis déclenchement uniquement si `AUTOMIX_AUTORISE`.
- Aucune ré-exécution silencieuse : toute nouvelle itération nécessite une autorisation humaine explicite et tracée.
- Écoute humaine courte (≤ 60 s) pour décider : Go / ajustement minimal / No-Go.

## Dette documentaire
- Seuils LUFS/dBTP et grille QA détaillée non formalisés dans /docs : interdiction de les inventer ; attendre la formalisation IQv1 et registres qualité.
