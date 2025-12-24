# Musique — Charte
Rôle : définir l'usage musical compatible avec l'hypnose premium sécurisée.

## Règles clés
- Utiliser des sources libres de droits ou sous licence explicite.
- Maintenir un niveau sonore constant, jamais supérieur à la voix.
- Éviter les motifs rythmiques intrusifs ou stimulants.
- Synchroniser les fondus avec les points de respiration du script.
- Valider chaque piste via QA avant tout mixage final.
- Aucun ajout musical, binaural ou de spatialité (voix ou musique) n’est autorisé tant que la voix n’est pas marquée LOCKED.

## Automatisation
- Automatisable : génération musicale conforme aux règles de la charte.
- Semi-automatisable : ajustements techniques (niveau, fondus, synchronisation), sous validation humaine.
- Humain obligatoire : sélection des pistes et validation QA avant mix final.

### Déclenchement HH-AutoMix Engine v1 — volet musique
- Le mix automatique n’est jamais déclenché par défaut et n’initie aucune sélection musicale intelligente.
- `STATUT_VOIX_GLOBAL` doit être `LOCKED` avant toute fusion voix/musique.
- Le mode musical doit être explicite : `AVEC_MUSIQUE` ou `VOIX_SEULE_INTENTIONNELLE` (l’absence de musique peut être choisie et reste valide).
- La piste musicale doit être fournie ou validée **avant** le déclenchement ; sinon le pré-check bloque l’exécution.
- `AUTOMIX_AUTORISE` doit être positionné à `OUI` pour une seule itération, puis remis à zéro après exécution ; aucune ré-exécution silencieuse n’est tolérée.

## Profils HH-AutoMix (V1) compatibles
Profils déterministes, non créatifs, compatibles HH-AutoMix Engine v1.

- **HH-AutoMix Standard** — motivation, concentration, mémoire, confiance en soi, développement personnel, créativité, arrêter de fumer (par défaut).
- **HH-AutoMix Apaisement** — stress, anxiété, douleur, relaxation profonde, méditation, relaxation & éveil.
- **HH-AutoMix Sommeil / Nuit** — sommeil, endormissement, relaxation nocturne.
- **HH-AutoMix Immersion Mémoire** — intuition, revivre un souvenir, éveil des sens (si intention immersive), visualisation narrative douce.

Rappel : si aucun profil ne correspond à 100 % à l’intention/catégorie/contraintes, demander la création d’un nouveau profil à la phase de cadrage (décision humaine).

## TODO
- Ajouter les profils sonores recommandés et interdits.
