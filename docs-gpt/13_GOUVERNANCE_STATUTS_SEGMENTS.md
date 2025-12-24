# Gouvernance — Statuts des segments (miroir canon /docs/audio/PLAN_REFERENCE_USINE_AUDIO_PREMIUM+++.md)

## Statuts séquentiels canoniques
1. PROJECT_INIT
2. VOICE_DRAFT
3. VOICE_LOCKED
4. SEGMENTATION_LOCKED
5. SOUND_DESIGN_ALLOWED
6. MIX_ITERATING
7. PREVIEW_APPROVED
8. FINAL_RENDERED
9. RELEASE_LOCKED

## Règles clés
- Aucun saut d’étape ; VOICE_LOCKED et SEGMENTATION_LOCKED conditionnent tout ajout sonore (musique/binaural/spatialité).
- Toute décision est traçable et réversible ; exceptions consignées dans docs-gpt/14_DECISIONS_TODO_LOG.md.
- Statut voix global dérivé des statuts segments/pipeline ; jamais saisi manuellement.

## Transitions
- Respecter l’ordre strict ci-dessus ; toute régression ou dérogation nécessite décision documentée.
