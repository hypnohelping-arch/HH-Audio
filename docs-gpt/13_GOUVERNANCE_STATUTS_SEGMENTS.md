# Gouvernance — Statuts des segments
Rôle : définir les statuts de progression et de décision pour chaque segment audio.

## Règles clés
- Statuts autorisés : DRAFT, RECORDED, QA, LOCKED, ARCHIVE.
- Tout changement de statut doit être horodaté et signé (initiales).
- Un segment LOCKED ne peut être modifié sans décision consignée.
- Les segments ARCHIVE restent lisibles mais exclus des livraisons.
- Les blocages doivent être tracés dans 14_DECISIONS_TODO_LOG.md.
- Certaines décisions humaines ou exceptions, sans modifier les statuts segments, peuvent générer une dette documentaire à consigner.

## Transitions autorisées
| Statut source | Statut cible |
| --- | --- |
| DRAFT | RECORDED |
| RECORDED | QA |
| QA | LOCKED |
| LOCKED | ARCHIVE |

## Statut voix global (dérivé, jamais saisi)
- Le **STATUT_VOIX_GLOBAL** est un statut dérivé calculé automatiquement à partir des statuts des segments.
- Il n’est pas un statut opérationnel supplémentaire et ne peut pas être saisi manuellement.
- Règles de calcul :
  - `INCOMPLET` : au moins un segment est différent de QA / LOCKED.
  - `QA_OK` : tous les segments sont au moins en QA, avec au moins un segment non LOCKED.
  - `LOCKED` : tous les segments sont LOCKED.
- Le calcul est effectué par Codex et le résultat est affiché dans le `README.md` du dossier audio.
- Toute modification manuelle du STATUT_VOIX_GLOBAL est interdite.

## Indicateur confort vocal (non bloquant)
- Indicateur optionnel renseigné uniquement lors du QA voix : `CONFORT_VOCAL : OK | À_SURVEILLER`.
- Jamais bloquant, ne modifie pas les statuts des segments et sert uniquement à la capitalisation terrain.

## Droit explicite de refus humain
- Un segment peut être refusé lors du QA voix, même s’il est techniquement conforme, si le confort d’écoute ou la charge émotionnelle est jugée excessive par l’humain.
- Conséquence documentaire : le segment reste ou repasse en RECORDED ou DRAFT, avec une justification courte consignée.

## LOCKED par décision (mode LABO uniquement)
- Marqueur documentaire : `LOCKED_BY_DECISION : OUI | NON`.
- Autorisé uniquement pour les audios en mode LABO et doit référencer une entrée explicite dans `docs-gpt/14_DECISIONS_TODO_LOG.md`.
- Ce marqueur ne remplace pas les statuts des segments ; il documente une dérogation assumée.

## Gel vocal temporaire (non statutaire)
- Marqueur opérationnel : `VOIX_GELEE : TEMPORAIRE`.
- Interdit toute modification de la voix tant qu’actif, sans impliquer ARCHIVE ni LOCKED définitif.
- Peut être levé uniquement par décision humaine explicite et reste non bloquant pour la gouvernance.

## Rappels officiels
- Le statut voix officiel repose exclusivement sur les statuts segments (DRAFT / RECORDED / QA / LOCKED).
- Le registre des audios peut référencer les statuts mais ne constitue jamais une preuve canonique.
- Aucun ajout de musique, binaural ou spatialité n’est autorisé tant que `STATUT_VOIX_GLOBAL` n’est pas `LOCKED`.

## Cadre Premium+++ V1 (figé)
Version officielle Premium+++ V1 : aucun principe CORE modifié, gouvernance voix renforcée et souveraineté humaine maintenue.

- `STATUT_VOIX_GLOBAL` reste un dérivé calculé, jamais saisi, affiché dans les dossiers audio.
- `CONFORT_VOCAL` est un indicateur non bloquant ; il ne change pas les statuts segments et nourrit uniquement la capitalisation.
- Le droit de refus humain est explicite : un segment techniquement conforme peut être refusé et reste/repasse en RECORDED ou DRAFT avec justification courte.
- `LOCKED_BY_DECISION` est autorisé en mode LABO uniquement, avec référence décisionnelle consignée.
- `VOIX_GELEE` est temporaire et non statutaire, levé uniquement par décision humaine explicite.
- Gating voix → son non négociable : aucune musique/binaural/spatialité tant que la voix n’est pas LOCKED (statuts segments).
