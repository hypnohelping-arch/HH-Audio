# Spatialité — Charte
Rôle : définir le placement sonore et la spatialisation compatibles avec l'hypnose.

## Règles clés
- Prioriser la stabilité centrale de la voix pour éviter la désorientation.
- Limiter les déplacements latéraux aux effets explicitement signalés.
- Éviter les rotations rapides ou imprévisibles dans le panorama.
- Calibrer la réverbération pour préserver la clarté des instructions.
- Documenter tout choix de spatialisation dans les notes de mixage.
- Aucun ajout musical, binaural ou de spatialité (voix ou musique) n’est autorisé tant que la voix n’est pas marquée LOCKED.

## Automatisation
- Automatisable : réglages techniques de spatialité conformes à la charte, après voix LOCKED.
- Semi-automatisable : application des limites de mouvement et de réverbération, sous validation humaine.
- Humain obligatoire : validation humaine du placement final.

## Repères HH-AutoMix
- Voix maintenue au centre comme ancrage principal, y compris pour les profils HH-AutoMix v1.
- Effets d’immersion contrôlés uniquement lorsque l’intention du profil le prévoit (ex. Immersion Mémoire), sans rotation rapide ni déstabilisation.
- La spatialité reste subordonnée à la clarté vocale ; tout déplacement doit préserver l’intelligibilité et le confort.

## Premium+++ V1 — alignement spatialité
- `STATUT_VOIX_GLOBAL = LOCKED` est obligatoire avant tout traitement spatial ou mix automatique.
- HH-AutoMix Engine v1 reste déterministe et non créatif ; aucune spatialisation n’est déclenchée sans autorisation humaine `AUTOMIX_AUTORISE` valide.
- Le mix est conditionnel et traçable : pas de ré-exécution silencieuse, autorisation humaine requise à chaque itération.

## TODO
- Ajouter les presets recommandés pour les principaux DAW.
- Les raffinements ultimes optionnels (`AUDIO_FIGE`, `INTENTION_SONORE`, `DECISION_FINALE : AUCUNE MODIFICATION`) restent en attente de retours terrain et ne sont pas requis pour Premium+++ V1.
