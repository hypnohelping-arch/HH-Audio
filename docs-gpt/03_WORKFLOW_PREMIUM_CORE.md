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
4. **Étape 3 — Script clean (VALIDÉE, OPÉRATIONNELLE, BLOQUANTE)** : rédaction du texte hypnotique pur, obligatoire avant toute étape ultérieure.
   - **Objectif** : production du texte hypnotique lisible à plat (aucune technique, aucune intention vocale).
   - **Entrées requises** : FICHE AUDIO V0 (V1) validée ; PACK DE DOCUMENTATION GPT (ÉTAPE 2.5).
   - **Sortie** : SCRIPT CLEAN validé humainement.
   - **Garde-fous** : aucune technique ; aucune indication vocale ; aucune musique/son/binaural ; aucune promesse ou diagnostic.
   - **Statut pipeline** : SCRIPT_CLEAN_VALIDÉ requis pour passer à l’ÉTAPE 4 (blocage si non validé humainement).
   - **Référence** : AUDIO-REF-01 = script clean de référence Premium+++ (respect CORE, niveau attendu, benchmark QA/GPT).
5. **Étape 4 — Script studio** : ajout des intentions vocales et respirations.
   - **Référence obligatoire** : Charte ÉTAPE 4 — SCRIPT STUDIO (transformation non destructive du SCRIPT CLEAN, sens/structure intouchables).
   - **Statut process** : ÉTAPE 4 déclarée **DONE / opérationnelle** (process Premium+++) avec statut **SCRIPT_STUDIO_VALIDÉ** requis avant VOICE_DRAFT / VOICE_LOCKED ; rappel charte Étape 4.
   - **Production** : annotations rares, visuelles, compatibles multi-voix, respectant la densité (1 annotation pour 2 à 4 phrases en moyenne).
   - **Garde-fous** : aucune réécriture, aucune technique audio ; tout changement de sens renvoie à une nouvelle version du SCRIPT CLEAN.
   - **Validation** : statut SCRIPT_STUDIO_VALIDÉ requis avant VOICE_DRAFT et VOICE_LOCKED (pipeline bloqué sinon).
6. **Étape 5 — VOICE_DRAFT** : enregistrement ou import voix V0 (voix humaine seule, alignée sur SCRIPT_STUDIO_VALIDÉ).
   - **Statut** : VALIDÉE / FROZEN (Premium+++), voir charte ÉTAPE 5 — VOICE_DRAFT.
   - **Entrées requises** : SCRIPT_STUDIO_VALIDÉ obtenu ; autorisation explicite d’exécuter l’étape dans le pipeline Premium+++.
   - **Mode opératoire** : voix capturée ou importée sans traitement ni ajout sonore ; respect intégral du SCRIPT STUDIO (annotations, respirations, intentions).
   - **Écoute** : **écoute partielle structurée** autorisée pour détecter les défauts flagrants ; ne constitue pas une validation finale.
   - **Garde-fous** : aucune musique/binaural/spatialité/sound design/mixage/segmentation finale avant VOICE_LOCKED ; interdiction de publier ou diffuser.
   - **Gating** : VOICE_LOCKED inaccessible sans VOICE_DRAFT conforme.
7. **Étape 6 — VOICE_LOCKED (PRÊTE / verrou final de la voix)** : validation voix verrouillée.
   - **Principe** : **écoute humaine complète obligatoire**, engageant la responsabilité éditoriale ; conditionne toute segmentation et tout sound design.
   - **Charte** : **VALIDÉE / FROZEN (Premium+++)**, voir charte ÉTAPE 6 — VOICE_LOCKED.
   - **Gating** : aucune segmentation finale, aucun sound design, aucune spatialité ou musique avant VOICE_LOCKED ; verrou final de la voix avant toute étape aval.
8. **Étape 7 — SEGMENTATION_LOCKED / SOUND_DESIGN_ALLOWED** : découpage final figé + autorisation sound design.
   - **Dépendance** : uniquement accessible après VOICE_LOCKED validé.
   - **Périmètre** : autorise la segmentation et le sound design.
   - **Mise à jour Premium+++** :
     - **ÉTAPE 7.1 — SEGMENTATION_LOCKED** : **VALIDÉE / FROZEN (Premium+++)** et **PRÊTE**, voir charte canon.
     - **ÉTAPE 7.2 — SOUND_DESIGN_ALLOWED** : **VALIDÉE / FROZEN (Premium+++), PRÊTE** ; prérequis **VOICE_LOCKED + SEGMENTATION_LOCKED**, ordre de priorité **voix > silence > musique > effets**, validation humaine renforcée ; ouvre l’accès à **MIX_ITERATING (ÉTAPE 8)**. Voir charte canon.
   - **Rappels** : dépendance stricte à VOICE_LOCKED ; rôle structurel de la segmentation ; validation humaine obligatoire ; condition d’accès à SOUND_DESIGN_ALLOWED et au mix.
9. **Étape 8 — MIX_ITERATING (PRÊTE)** : itérations de mixage contrôlées (voix prioritaire).
   - **Accès** : uniquement après **SOUND_DESIGN_ALLOWED validée**.
   - **Cadre** : charte **VALIDÉE / FROZEN (Premium+++)** — mix invisible vérifiable, itérations à intention unique, validation à volume bas, droit au rejet intuitif, gestion de la fatigue, irréversibilité avant PREVIEW_APPROVED.
   - **Rappels** : dépendance stricte à SOUND_DESIGN_ALLOWED ; itérations réversibles documentées ; aucun rendu final/mastering à ce stade.
   - **Préparation** : preview humain (≤ 60 s) prêt pour PREVIEW_APPROVED.
10. **Étape 9 — PREVIEW_APPROVED** : validation écoute humaine (≤ 60 s) avant rendu final ; charte dédiée à définir ultérieurement.
11. **Étape 10 — FINAL_RENDERED** : rendu final.
12. **Étape 11 — RELEASE_LOCKED** : verrouillage publication.

### PACK DE DOCUMENTATION GPT (pré-Étape 3)
- **Rôle** : transmettre à GPT un kit d’information minimal, sécurisé et aligné avant la rédaction du script clean.
- **Usage** : copier-coller intégralement le pack dans le prompt GPT **avant** l’Étape 3 (Script clean).
- **Structure canon (sections 1 → 10)** : (1) Métadonnées audio ; (2) Objectif hypnotique ; (3) Public/contre-indications ; (4) Chartes langage & voix ; (5) Structure canon du script clean ; (6) Blocage musique/binaural/spatialité ; (7) Zones interdites ; (8) Tonalité & rythme ; (9) Journal perceptif attendu ; (10) Validation attendue.
- **Cadres relationnels** : posture relationnelle calme, accompagnante, non démonstrative ; densité métaphorique simple, universelle, parcimonieuse.
- **Statut** : obligatoire, non versionné, généré à la demande ; ne contient que de l’interface (aucun asset ni binaire).

## Exigences de production
- Scripts hébergés dans chaque projet GitHub : `script_clean.md` (texte hypnotique pur) et `script_studio.md` (intentions vocales, silences, respiration).
- Charte ÉTAPE 4 — SCRIPT STUDIO obligatoire : transformation non destructive, annotations légères, visuelles et compatibles multi-voix.
- Statut SCRIPT_STUDIO_VALIDÉ requis avant tout VOICE_DRAFT et toute validation VOICE_LOCKED (pipeline bloqué sinon).
- Découpage par blocs hypnotiques : découpage fonctionnel long, chaque bloc = unité de travail ; segmentation figée avant tout sound design.
- Gestion des créations partielles : voix seule intégrable ; audio complet existant = recréation contrôlée (jamais patchée).
- Réutilisation de blocs audio non active en V1 (bibliothèque prévue plus tard).

## Validation et contrôle
- HH-AutoMix Engine v1 déterministe, déclenché uniquement si AUTOMIX_AUTORISE après pré-check bloquant.
- Aucune ré-exécution silencieuse : toute nouvelle itération nécessite une autorisation humaine explicite et tracée.
- Validation post-mix : écoute humaine ≤ 60 s puis décision souveraine (Go / ajustement minimal / No-Go) avant publication.
- Journal perceptif humain court par bloc hypnotique ; jamais automatisé.
- Statuts script bloquants : SCRIPT_CLEAN_VALIDÉ pour démarrer l’ÉTAPE 4, SCRIPT_STUDIO_VALIDÉ avant toute capture VOICE_DRAFT et toute validation VOICE_LOCKED.

## Gouvernance et traçabilité
- Décisions versionnées et réversibles ; exceptions consignées dans docs-gpt/14_DECISIONS_TODO_LOG.md.
- Statut voix global dérivé : jamais saisi manuellement ; repose sur l’état des segments et du pipeline.
- Hashs consignés dans registres/logs QA, jamais dans le nommage fichier.
