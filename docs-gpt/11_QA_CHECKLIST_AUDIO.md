# QA — Checklist audio
Rôle : fournir la liste de contrôle minimale pour valider un livrable audio.

## Règles clés
- Vérifier le niveau RMS et le peak selon la norme interne.
- Confirmer l'absence d'artefacts, clicks ou sibilances excessives.
- Tester l'intelligibilité sur casques, écouteurs et enceintes neutres.
- S'assurer que chaque balise de script correspond à la timeline audio.
- Documenter tout écart et la correction associée.

## Automatisation
- Automatisable : QA chiffrée (LUFS / dBTP) et contrôles techniques de base.
- Semi-automatisable : vérification de correspondance balises script ↔ timeline audio, sous validation humaine.
- Humain obligatoire : écoute humaine obligatoire avant validation QA finale.

## Seuils QA chiffrés (référence interne)
**Voix seule**
- Loudness intégré : –19 LUFS
- True Peak max : –1.0 dBTP

**Mix final (voix + musique/effets)**
- Loudness intégré : –16 LUFS
- True Peak max : –1.0 dBTP

Tout écart bloque le passage en QA validée.
