# Charte ÉTAPE 8 — MIX_ITERATING (Premium+++)

**Statut : VALIDÉE / FROZEN (Premium+++).**

## Définition canon
- MIX_ITERATING = itérations de mixage contrôlées **après SOUND_DESIGN_ALLOWED validée**, visant à équilibrer voix/musique/effets **sans jamais altérer la primauté de la voix**.
- Périmètre : ajustements de niveaux, dynamiques, égalisation, spatialité discrète et silences, **sans ajout de nouveaux assets**.
- Le mix reste **réversible** : chaque ajout ou réglage doit pouvoir être retiré sans casser la structure ni la hiérarchie voix > silence > musique > effets.

## Rôle et non-rôle
- **Rôle** :
  - Assembler et équilibrer les éléments validés (voix + segmentation figée + sound design autorisé) en itérations successives.
  - Tester la cohérence d’écoute en conditions variées (volume bas, équilibre gauche/droite, compatibilité mono).
  - Préparer un preview humainement validable (≤ 60 s) **sans constituer le rendu final**.
- **Non-rôle** :
  - Aucun rendu final ni mastering (FINAL_RENDERED interdit à ce stade).
  - Aucun ajout de nouvelle musique, SFX, binaural ou spatialité hors périmètre SOUND_DESIGN_ALLOWED.
  - Aucune modification de segmentation ou de structure vocale.

## Objectifs du mix
- **Voix prioritaire** : garantir la lisibilité et la dominance de la voix à tout moment, y compris à volume très bas.
- **Mix invisible et vérifiable** : équilibrer sans artefacts perceptibles (pumping, saturation, masquage) ; toute intervention doit rester discrète et traçable.
- **Itérations contrôlées** : chaque passe répond à une **intention unique** (ex. équilibrage voix/musique, correction d’un SFX) avec versionning clair.
- **Prévention du sur-mix** : limiter la densité sonore, préserver les silences structurants, éviter la fatigue auditive.

## Règles Premium+++ (6 principes)
1. **Mix invisible vérifiable** : aucune signature mix perceptible ; contrôle par écoute A/B, mono et volume bas.
2. **Itérations à intention unique** : une seule intention par passe ; journaliser l’objectif et le résultat attendu.
3. **Gestion de la fatigue d’itération** : pauses obligatoires, écoute différée, interdiction de valider après fatigue déclarée.
4. **Validation à volume bas** : chaque itération est vérifiée à faible volume pour confirmer la dominance vocale.
5. **Droit au rejet intuitif** : tout élément mixé peut être retiré sur simple intuition de gêne ou distraction, sans justification supplémentaire.
6. **Irréversibilité avant PREVIEW_APPROVED** : une fois une itération déclarée conforme et stabilisée, retour arrière interdit hors motif bloquant documenté ; aucun saut direct vers FINAL_RENDERED.

## Validation humaine intermédiaire
- Écoute humaine obligatoire à la fin de chaque itération significative (≥ 1 réglage touchant la balance voix/silence/musique/effets).
- Validation documentée : date, périmètre de l’itération, décisionnaire, éléments rejetés/acceptés, niveau d’écoute (volume bas requis).
- **Aucune progression vers PREVIEW_APPROVED** sans validation humaine consignée et conformité aux 6 principes Premium+++.

## Critères de sortie (pour déclarer ÉTAPE 8 terminée)
- Voix confirmée dominante à volume bas ; absence d’artefacts (pumping, saturation, masquage critique).
- Toutes les itérations sont tracées avec intention unique, résultat et statut (accepté / rejet intuitif / à refaire).
- Mix réversible : chaque ajout peut être désactivé sans casser la structure ; segmentation et voix restent intactes.
- Préparation du **preview ≤ 60 s** prête pour validation humaine.
- Accord explicite que le rendu reste **non final** (FINAL_RENDERED interdit) et que la prochaine étape est **PREVIEW_APPROVED**.

## Lien avec PREVIEW_APPROVED (ÉTAPE 9)
- PREVIEW_APPROVED = validation d’écoute humaine (≤ 60 s) avant tout rendu final.
- MIX_ITERATING **ouvre** PREVIEW_APPROVED uniquement après validation humaine consignée et respect intégral des règles ci-dessus.
- Aucun critère de PREVIEW_APPROVED n’est défini ici : ils seront établis dans une charte dédiée.

## Statut
- Charte **VALIDÉE / FROZEN (Premium+++)**.
- **ÉTAPE 8 — MIX_ITERATING** est déclarée **PRÊTE** et conditionne l’accès à **ÉTAPE 9 — PREVIEW_APPROVED**.
