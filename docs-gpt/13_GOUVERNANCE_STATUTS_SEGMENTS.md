# Gouvernance — Statuts des segments
Rôle : définir les statuts de progression et de décision pour chaque segment audio.

## Règles clés
- Statuts autorisés : DRAFT, RECORDED, QA, LOCKED, ARCHIVE.
- Tout changement de statut doit être horodaté et signé (initiales).
- Un segment LOCKED ne peut être modifié sans décision consignée.
- Les segments ARCHIVE restent lisibles mais exclus des livraisons.
- Les blocages doivent être tracés dans 14_DECISIONS_TODO_LOG.md.

## Transitions autorisées
| Statut source | Statut cible |
| --- | --- |
| DRAFT | RECORDED |
| RECORDED | QA |
| QA | LOCKED |
| LOCKED | ARCHIVE |
