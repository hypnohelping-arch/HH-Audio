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

---

## 6. Scripts audio

### 6.1 Emplacement
Les scripts vivent **dans le projet audio**, sur GitHub.

### 6.2 Deux versions obligatoires
- `script_clean.md` : texte hypnotique pur
- `script_studio.md` : intentions vocales, silences, respiration

### 6.3 Règle absolue
Aucune indication musicale, sonore ou technique n’est autorisée dans le texte hypnotique.

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
