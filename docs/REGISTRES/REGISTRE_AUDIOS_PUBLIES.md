# Registre des audios publiés (template figé)

## Rôle du document
Consigner chaque audio publié, ses métadonnées, son positionnement éditorial et son statut de version. Ce registre est la référence figée Premium+++ pour toute diffusion et tout suivi qualité.

## Règle fondamentale
1 audio publié = 1 entrée unique. Toute évolution nécessite une nouvelle version (aucune suppression d’entrée).

## Vue synthétique (tableau du registre)
Copier-coller le modèle ci-dessous (code Markdown) pour maintenir une vue consolidée.

```
| ID | Titre | Thème | Mode | Durée | Effets | Statut | Version | Qualité (%) | Maturité | Rôle |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| HH-AUD-001 | Titre de référence | Sommeil | Voix seule | 20:00 | Léger | Publié | v1.0.0 | 92 | Stabilisée | Pilier |
```

## Fiche détaillée (gabarit par audio)
- **ID / Titre / Thème / Mode / Durée / Effets** : champs d’identification obligatoires.
- **Statut** : publié / retiré / archivé (jamais supprimé).
- **Version** : format sémantique (vX.Y.Z), chaque entrée est figée par version.
- **Indice de qualité global : XX %** — évalue cohérence hypnotique, confort d’écoute, stabilité émotionnelle.
- **Maturité éditoriale : initiale / stabilisée / aboutie**.
- **Rôle dans le catalogue : pilier / complément / expérimental / transition**.
- **Pistes d’amélioration (si nouvelle version)** : ≤ 3 puces, optionnelles.

## Versions et statuts
- Toute nouvelle version crée une nouvelle ligne et une nouvelle fiche détaillée.
- Un statut « retiré » ou « archivé » conserve l’entrée, sans suppression.
- Le score de qualité est figé pour la version concernée (pas de recalcul hors nouvelle version).

## Règles de gouvernance
1. 1 audio publié = 1 entrée unique (pas de fusion).
2. Pas de suppression : utiliser les statuts « retiré » ou « archivé ».
3. Score figé par version, recalcul uniquement lors d’une nouvelle version.
4. Remarques / pistes d’amélioration bornées à 3, et optionnelles.
5. Un audio publié est considéré terminé ; les remarques servent aux itérations futures.

## TODO (hors V1)
- Ajouter des exemples de statuts historiques si besoin.
- Décrire un flux de validation QA détaillé (post-V1).
