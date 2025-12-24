# Plan de Référence — Usine de Production Audio HypnoHelping (Premium+++)

**Statut : RÉFÉRENCE OFFICIELLE — VERROUILLÉE (V1)**  
**Date : 2025-12-21**  
**Note : référence officielle.**

## 0. Statut du document
**Statut : RÉFÉRENCE OFFICIELLE — VERROUILLÉE (V1)**  
Ce document constitue la base stratégique et opérationnelle de l’usine de production d’audios d’hypnose HypnoHelping. Toute évolution future devra faire l’objet d’une décision explicite et versionnée.

---

## 1. Objectif stratégique
Mettre en place une **usine audio Premium+++**, permettant :
- une **automatisation maximale** des tâches répétitives et techniques,
- une **qualité hypnotique irréprochable**,
- une **sécurité émotionnelle absolue**,
- une **scalabilité industrielle**,
- sans jamais dégrader la voix, le langage ou l’expérience de l’auditeur.

---

## 2. Principes non négociables
1. **La voix est l’axe de référence absolu.**
2. Le **texte hypnotique est souverain** ; l’audio en est toujours une conséquence.
3. Aucune musique, effet, binaural ou spatialité ne doit détourner l’attention de la voix.
4. L’automatisation ne remplace jamais la validation humaine sur les points sensibles.
5. Toute décision doit être **traçable et réversible**.

---

## 3. Architecture des rôles et responsabilités

### 3.1 ChatGPT
- Architecte du système
- Spécification des règles, structures et workflows
- Validation conceptuelle et qualitative

### 3.2 Codex
- Exécutant automatisé
- Création de structures, ingestion, mesures, rendus
- Application stricte des règles définies
- Aucune initiative créative ou structurelle

### 3.3 GitHub (canon texte)
- Scripts audio (clean + studio)
- Découpage par blocs hypnotiques
- Manifests de projets
- Registres d’assets (musique / SFX)
- QA, journaux perceptifs, décisions

### 3.4 pCloud (canon binaire)
- Voix WAV, musiques, SFX
- Bounces, previews, masters, exports
- Accès strictement limité à un dossier racine partagé via compte service

---

## 4. Pipeline de production

### 4.1 Pipeline unique
Un **pipeline unique** est utilisé pour tous les audios.

### 4.2 Deux modes de production
- **STANDARD Premium+++** : automatisation maximale, garde-fous stricts
- **SIGNATURE** : mêmes étapes, libertés sonores contrôlées, validation renforcée

Aucun mode ne peut bypasser une étape critique.

### 4.3 Étapes séquencées (mise à jour Premium+++)
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
10. **Étape 9 — PREVIEW_APPROVED (PRÊTE)** : validation écoute humaine (≤ 60 s) en condition réelle avant rendu final.
    - **Accès** : uniquement après **MIX_ITERATING** validé et preview prêt.
    - **Cadre** : charte **VALIDÉE / FROZEN (Premium+++), PRÊTE** — validation de l’expérience (pas de perfection technique), écoute intégrale aux volumes normal et bas, écoute en condition d’usage réel, non-correction cosmétique si validé, continuité d’engagement et engagement éditorial explicite.
    - **Décision** : droit au refus intuitif ou au report ; validation différée recommandée ; critères de validation/refus formalisés ; interdiction de modifier le preview après validation.
    - **Ouverture** : PREVIEW_APPROVED ouvre **FINAL_RENDERED** sous dépendance stricte.
11. **Étape 10 — FINAL_RENDERED** : rendu définitif publiable, accessible uniquement après PREVIEW_APPROVED ; charte dédiée à définir ultérieurement.
12. **Étape 11 — RELEASE_LOCKED** : verrouillage publication.

### 4.4 PACK DE DOCUMENTATION GPT (pré-Étape 3)
- **Rôle** : transmettre à GPT un kit d’information minimal, sécurisé et aligné avant la rédaction du script clean.
- **Usage** : copier-coller intégralement le pack dans le prompt GPT **avant** l’Étape 3 (Script clean).
- **Structure canon (sections 1 → 10)** : (1) Métadonnées audio ; (2) Objectif hypnotique ; (3) Public/contre-indications ; (4) Chartes langage & voix ; (5) Structure canon du script clean ; (6) Blocage musique/binaural/spatialité ; (7) Zones interdites ; (8) Tonalité & rythme ; (9) Journal perceptif attendu ; (10) Validation attendue.
- **Cadres relationnels** : posture relationnelle calme, accompagnante, non démonstrative ; densité métaphorique simple, universelle, parcimonieuse.
- **Statut** : obligatoire, non versionné, généré à la demande ; ne contient que de l’interface (aucun asset ni binaire).

---

## 5. Gouvernance par statuts

Statuts séquentiels obligatoires :
1. PROJECT_INIT
2. VOICE_DRAFT
3. VOICE_LOCKED
4. SEGMENTATION_LOCKED
5. SOUND_DESIGN_ALLOWED
6. MIX_ITERATING
7. PREVIEW_APPROVED
8. FINAL_RENDERED
9. RELEASE_LOCKED

Aucune étape ne peut être sautée.

Statuts script bloquants complémentaires :
- SCRIPT_CLEAN_VALIDÉ : requis pour déclencher l’ÉTAPE 4.
- SCRIPT_STUDIO_VALIDÉ : requis avant toute capture VOICE_DRAFT et toute validation VOICE_LOCKED.

---

## 6. Scripts audio

### 6.1 Emplacement
Les scripts vivent **dans le projet audio**, sur GitHub.

### 6.2 Deux versions obligatoires
- `script_clean.md` : texte hypnotique pur
- `script_studio.md` : intentions vocales, silences, respiration

### 6.3 Règle absolue
Aucune indication musicale, sonore ou technique n’est autorisée dans le texte hypnotique.

### 6.4 Charte ÉTAPE 4 — SCRIPT STUDIO
- Le SCRIPT STUDIO applique la charte ÉTAPE 4 (transformation non destructive, annotations légères et visuellement distinctes).
- SCRIPT_STUDIO_VALIDÉ est le passage obligé avant toute VOICE_DRAFT ; aucun enregistrement n’est autorisé sans cette validation.
- La structure reste identique au SCRIPT CLEAN ; toute modification de sens doit passer par une nouvelle version du SCRIPT CLEAN.

---

## 7. Découpage par blocs hypnotiques
- Découpage long et fonctionnel
- Chaque bloc correspond à une fonction hypnotique claire
- Les blocs sont l’unité de travail audio et musical
- La segmentation est figée avant tout sound design

---

## 8. Gestion des créations partielles
- **Voix seule existante** : intégration directe dans le pipeline
- **Audio complet existant** : recréation contrôlée (jamais patch)
- **Script seul** : création standard

---

## 9. Versioning
- Toute modification de script crée automatiquement une **nouvelle version audio**
- Lien explicite entre :
  - `script_version`
  - `audio_version`
- Variantes possibles par mode (STANDARD / SIGNATURE)

---

## 10. Journal perceptif
- Un journal perceptif court par bloc hypnotique
- Rédigé par l’humain
- Jamais automatisé
- Sert de mémoire qualitative long terme

---

## 11. Réutilisation (non active en V1)
- Aucune réutilisation de blocs audio en V1
- Bibliothèque de blocs audio validés prévue en évolution future

---

## 12. Autorité de validation
- Une seule autorité humaine (phase actuelle)
- Pas de traçage d’identité
- Évolution possible ultérieurement

---

## 13. TODO stratégiques (mémoire active)
- TODO-01 : gestion multi-validateurs
- TODO-02 : bibliothèque de blocs audio validés
- TODO-03 : scripts comme entités indépendantes (Option B)
- TODO-04 : formalisation de plages de tolérance par type de bloc

---

## 14. Conclusion
Ce plan définit une **usine audio Premium+++**, sécurisée, automatisable et évolutive, respectant pleinement les principes de l’hypnose ericksonienne moderne et les exigences de qualité HypnoHelping.

Toute implémentation doit se conformer strictement à ce document.
