# Workflow premium core (miroir canon /docs/audio/PLAN_REFERENCE_USINE_AUDIO_PREMIUM+++.md)

## Chaîne de production canonique
- Pipeline unique pour tous les audios : cadrage → script clean/studio → VOICE_DRAFT → VOICE_LOCKED → SEGMENTATION_LOCKED → SOUND_DESIGN_ALLOWED → MIX_ITERATING → PREVIEW_APPROVED → FINAL_RENDERED → RELEASE_LOCKED.
- Aucun saut d’étape : VOICE_LOCKED est obligatoire avant toute musique/binaural/spatialité ou sound design.
- Deux modes seulement (STANDARD Premium+++, SIGNATURE) suivent exactement les mêmes étapes ; SIGNATURE ajoute une validation renforcée.
- Toute modification de script crée une nouvelle version audio (lien explicite script_version ↔ audio_version).

### Séquence détaillée (Premium+++)
1. **Étape 1 — Cadrage** : cadrage du projet audio et périmètre.
2. **Étape 2 — Autorisation d’écriture** : validation humaine du droit d’écrire.
3. **Étape 2.5 — Documentation GPT** : cadrer GPT avant toute rédaction.
   - **Objectif** : fournir à GPT un cadre canon minimal avant écriture.
   - **Entrées requises** : FICHE AUDIO V0 (V1) validée ; chartes langage + sécurité voix ; structure canon du script clean.
   - **Sortie** : PACK DE DOCUMENTATION GPT (interface uniquement).
   - **Garde-fous** : lecture seule ; aucune invention ; aucune création de fichier ; aucune inclusion d’éléments sonores.
   - **Statut pipeline** : SCRIPT_CLEAN interdit tant que l’ÉTAPE 2.5 n’est pas exécutée.
4. **Étape 3 — Script clean** : rédaction du texte hypnotique pur.
5. **Étape 4 — Script studio** : ajout des intentions vocales et respirations.
6. **Étape 5 — VOICE_DRAFT** : enregistrement ou import voix V0.
7. **Étape 6 — VOICE_LOCKED** : validation voix verrouillée.
8. **Étape 7 — SEGMENTATION_LOCKED** : découpage final figé.
9. **Étape 8 — SOUND_DESIGN_ALLOWED** : autorisation sound design (pas avant VOICE_LOCKED).
10. **Étape 9 — MIX_ITERATING** : itérations de mixage contrôlées.
11. **Étape 10 — PREVIEW_APPROVED** : validation écoute humaine (≤ 60 s).
12. **Étape 11 — FINAL_RENDERED** : rendu final.
13. **Étape 12 — RELEASE_LOCKED** : verrouillage publication.

### PACK DE DOCUMENTATION GPT (pré-Étape 3)
- **Rôle** : transmettre à GPT un kit d’information minimal, sécurisé et aligné avant la rédaction du script clean.
- **Usage** : copier-coller intégralement le pack dans le prompt GPT **avant** l’Étape 3 (Script clean).
- **Structure canon (sections 1 → 10)** : (1) Métadonnées audio ; (2) Objectif hypnotique ; (3) Public/contre-indications ; (4) Chartes langage & voix ; (5) Structure canon du script clean ; (6) Blocage musique/binaural/spatialité ; (7) Zones interdites ; (8) Tonalité & rythme ; (9) Journal perceptif attendu ; (10) Validation attendue.
- **Cadres relationnels** : posture relationnelle calme, accompagnante, non démonstrative ; densité métaphorique simple, universelle, parcimonieuse.
- **Statut** : obligatoire, non versionné, généré à la demande ; ne contient que de l’interface (aucun asset ni binaire).

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
