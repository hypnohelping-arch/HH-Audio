# Architecture pCloud — Usine Audio HypnoHelping (Premium+++)

## Statut
**Statut : RÉFÉRENCE OFFICIELLE — VERROUILLÉE (V1)**  
Ce document définit l’architecture canon des binaires audio dans pCloud pour l’usine HypnoHelping.

---

## 1. Objectif
Assurer un stockage cloud :
- **périmétré** (accès restreint à Codex),
- **normé** (arborescence stable),
- **industrializable** (automatisation fiable),
- **audit-able** (logs, statuts, interdits).

---

## 2. Principes non négociables
1. **pCloud = canon binaire**, GitHub = canon texte/gouvernance.
2. Codex ne dispose que d’un **accès restreint à un dossier racine** (compte service recommandé).
3. L’architecture racine est **stable** : Codex ne l’invente pas, il l’exécute.
4. Toute création de structure doit être **idempotente** (si existe → ne rien casser).
5. **Aucune suppression automatique** n’est autorisée par défaut.
6. Les exports finals sont **write-once** (verrouillage humain recommandé).

---

## 3. Dossier racine pCloud
Dossier racine attendu (périmètre partagé à Codex) :

`/HypnoHelping/Cloud Codex/HH-audio/`

> Remarque : si l’emplacement exact diffère, il doit être stabilisé une fois pour toutes et documenté ici. Aucune autre zone pCloud ne doit être accessible à Codex.

---

## 4. Arborescence canon (V1)

### 4.1 Racine
- `00_INBOX_DROP/`  
  Dépôt brut (non validé). Point d’entrée ingestion.
- `01_ASSETS/`  
  Bibliothèque validée (réutilisable).
- `02_PROJECTS/`  
  Production par projet audio (un dossier par audio).
- `03_EXPORTS/`  
  Exports globaux (préviews/finals) si besoin hors projet.
- `99_QUARANTINE/`  
  Zone de quarantaine : éléments douteux/non conformes.

### 4.2 Détails

#### 01_ASSETS/
- `01_ASSETS/MUSIC/`
  - `textures/`
  - `accents/`
- `01_ASSETS/SFX/`
  - `oneshots/`
  - `ambiences/`

Règles :
- Les assets présents ici doivent être **validés**.
- L’ajout doit passer par un workflow d’ingestion/QA (job Codex dédié + validation humaine).

#### 02_PROJECTS/<audio_id>/
- `00_ADMIN/` (optionnel : notes locales, export de logs)
- `VOICE/`
  - `SOURCE/` (voix source, prises, exports)
  - `BLOCKS/` (WAV découpés par blocs hypnotiques)
  - `LEGACY/` (sources “audio complet existant” — jamais patch)
- `MIX/`
  - `TESTS/` (itérations)
  - `BLOCKS/` (bounces par bloc si nécessaire)
- `MASTER/`
- `STEMS/` (optionnel)
- `RENDERS/`
  - `PREVIEW/`
  - `FINAL/`

Règles :
- Aucun sound design “définitif” avant `VOICE_LOCKED` (piloté côté GitHub).
- Les exports `FINAL/` doivent être traités comme **write-once** (verrouillage humain recommandé).

#### 03_EXPORTS/
- `PREVIEW/`
- `FINAL/`

Usage :
- uniquement si l’usine souhaite une “sortie globale” en plus des `RENDERS/` projet.

---

## 5. Droits Codex (périmètre et interdits)
Codex :
- **peut créer** des dossiers manquants dans la racine HH-audio (idempotent),
- **peut écrire** dans :
  - `00_INBOX_DROP/`
  - `02_PROJECTS/<audio_id>/...`
  - `99_QUARANTINE/`
- **ne doit pas supprimer** en automatique,
- **ne doit pas renommer** des dossiers racine,
- **ne doit pas accéder** à d’autres emplacements pCloud.

---

## 6. Journalisation minimale
Toute opération structurelle (création de dossiers) doit produire :
- une liste des dossiers créés,
- une liste des dossiers déjà existants,
- les erreurs éventuelles,
- un horodatage.

Le log peut être :
- écrit dans GitHub (recommandé),
- et/ou exporté dans `02_PROJECTS/<audio_id>/00_ADMIN/` quand applicable.

---

## 7. TODO (évolutions futures)
- TODO : stratégie de verrouillage “write-once” systématique pour `FINAL/`
- TODO : détection de dérive (structure cloud ≠ référence)
- TODO : politique de rétention / archivage (quand la volumétrie augmente)
