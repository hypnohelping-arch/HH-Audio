# Nommage fichiers — Conventions
Rôle : garantir un schéma de nommage cohérent et traçable pour tous les fichiers audio et scripts.

## Règles clés
- Structure recommandée : <mode>__<segment>__<version>__<statut>.<ext>.
- <statut> peut être : DRAFT / RECORDED / QA / LOCKED / ARCHIVE.
- Utiliser des dates au format ISO si nécessaire : YYYYMMDD.
- Bannir les espaces ; privilégier l'underscore double pour séparer les blocs.
- Conserver un changelog des renommages dans 14_DECISIONS_TODO_LOG.md.
- Le hash est consigné dans un registre ou log QA, jamais dans le nom de fichier.

## TODO
- Ajouter les exemples complets par type de fichier.
