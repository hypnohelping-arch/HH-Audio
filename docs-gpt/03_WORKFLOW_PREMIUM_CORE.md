# Workflow premium core
Rôle : décrire la chaîne de production standardisée pour les séances premium.

## Règles clés
- Segmenter en phases : cadrage, script, voix, son, QA, verrouillage.
- Chaque phase requiert une validation formelle avant de passer à la suivante.
- La dette documentaire est un mécanisme transversal, non bloquant par défaut, immédiat ou différé, et ne freine pas l’avancement dès lors qu’elle est tracée.
- DOC UPDATE (obligatoire) : toute évolution de règle/flux/convention/statut/QA doit déclencher une mise à jour des docs GitHub ou une dette documentaire A/B/C consignée.
- Les artefacts doivent rester traçables (versions datées, hash consignés en registre ou log QA).
- Aucun hash n'est requis dans le nom de fichier.
- Les exceptions doivent être journalisées dans 14_DECISIONS_TODO_LOG.md.
- Livrer uniquement après double contrôle croisé (voix + QA audio).

## Automatisation Premium+++ (clarification workflow)
Objectif : expliciter ce qui est automatisable, semi-automatisable et humain obligatoire, sans changer les principes CORE.

### Profils HH-AutoMix (V1)
Profils déterministes, non créatifs, compatibles HH-AutoMix Engine v1.

- **HH-AutoMix Standard** — motivation, concentration, mémoire, confiance en soi, développement personnel, créativité, arrêter de fumer (par défaut).
- **HH-AutoMix Apaisement** — stress, anxiété, douleur, relaxation profonde, méditation, relaxation & éveil.
- **HH-AutoMix Sommeil / Nuit** — sommeil, endormissement, relaxation nocturne.
- **HH-AutoMix Immersion Mémoire** — intuition, revivre un souvenir, éveil des sens (si intention immersive), visualisation narrative douce.

Règle obligatoire : si aucun profil existant ne couvre à 100 % l’intention, la catégorie et les contraintes du projet, la création d’un nouveau profil doit être demandée dès la **PHASE DE CADRAGE**, avant toute génération musicale ou mix. La décision de créer le nouveau profil reste humaine.

### Script voix
- Automatisable : génération de script V0.
- Semi-automatisable : préparation du script fractionné V1 (segments enregistrables), sous validation humaine.
- Humain obligatoire : validation vocale humaine avant toute suite.

### Musique
- Automatisable : génération musicale.
- Semi-automatisable : ajustements techniques (niveau constant, fondus synchronisés), sous règles de la charte.
- Humain obligatoire : sélection humaine des pistes et validation QA avant mix final.

### Mix
- Automatisable : mix technique.
- Semi-automatisable : itérations de mix après voix LOCKED, la voix restant la référence (gating voix → son non négociable).
- Humain obligatoire : validation humaine du mix.

### QA
- Automatisable : QA chiffrée (LUFS / dBTP).
- Semi-automatisable : vérification de correspondance balises script ↔ timeline audio.
- Humain obligatoire : écoute humaine obligatoire.

#### Checklist d’écoute humaine post-mix (≤ 60 s)
- La voix est-elle confortable et naturelle partout ?
- La musique attire-t-elle l’attention à un moment ?
- Y a-t-il un masquage voix / musique ?
- Les silences sont-ils respectés ?
- Ressenti global : « j’oublie le son et j’écoute la voix ».

Si toutes les réponses sont positives : publication possible. Sinon : ajustement humain minimal avant livraison.

### Assistant de pré-alertes vocales
Objectif : signaler les risques sans correction automatique ni blocage de production.

- Détection de segments longs.
- Détection de densité verbale élevée.
- Détection de débit rapide.
- Détection de respiration insuffisante.

### Gouvernance
- Automatisable : consignation des versions datées et des hash en registre ou log QA.
- Semi-automatisable : pré-structuration des journaux d’exceptions et de dette documentaire.
- Humain obligatoire : décision finale toujours humaine.

## Gestion des audios en cours (méthode Premium+++)

### Principe de traçabilité
- 1 audio = 1 dossier dédié (terrain de production), jamais écrasé, jamais implicite.
- La vérité officielle de gouvernance reste dans les documents :
  - décisions / dérogations / travaux en cours : `docs-gpt/14_DECISIONS_TODO_LOG.md`
  - audios publiés uniquement : `docs-gpt/15_REGISTRE_AUDIOS_PUBLIES.md`
- Le dossier audio documente l’exécution et l’état réel (fichiers, versions, notes), mais ne remplace pas la gouvernance.

### Structure minimale recommandée d’un dossier audio
Exemple (indicatif, à adapter au besoin sans complexifier) :

- `voix/` : source voix (jamais écrasée)
- `son/` : mixes et itérations (v1, v2, …), notes son
- `notes/` : journal d’évolution daté
- `README.md` : état actuel (1 page max)

### Deux parcours de production selon l’état de la voix

#### PARCOURS A — VOIX_EXISTANTE (voix déjà enregistrée / quasi figée)
Usage : audio labo ou expérimental lorsque la voix n’est pas réenregistrée.

Règles :
- La voix peut être considérée LOCKED par décision humaine si explicitement acté.
- Toute dérogation au gating voix → son doit être consignée dans `docs-gpt/14_DECISIONS_TODO_LOG.md`.
- L’optimisation sonore reste prudente : la voix demeure la référence et ne doit pas être masquée.
- Le score cible et le plafond réaliste doivent être définis avant itérations.

#### PARCOURS B — CREATION_FROM_SCRATCH (co-création native)
Usage : production Premium+++ native.

Règles :
- Script fractionné V1 dès le départ (segments enregistrables).
- Voix enregistrée par segments, puis QA, puis LOCKED.
- Aucun ajout musique/binaural/spatialité avant voix LOCKED (règle standard).

### Champs Premium+++ (obligatoires en mode LABO)
Pour tout audio en mode LABO (et recommandé au-delà), documenter dans le `README.md` du dossier audio :

- `MODE_DE_PRODUCTION :` VOIX_EXISTANTE | CREATION_FROM_SCRATCH
- `INTENTION_DE_TEST :` (obligatoire en LABO) ce que l’on cherche à apprendre/mesurer
- `CRITERE_D_ARRET :` (obligatoire en LABO) seuil de fin d’itération (ex. score cible atteint ou gain marginal faible)
- `GAIN_ESTIME :` (recommandé) estimation simple avant / après (ex. voix seule vs après design sonore)

Note :
- Ces champs améliorent la gouvernance et évitent les tests implicites.
- Ils n’ajoutent pas de complexité technique ; ils rendent l’expérimentation traçable et exploitable.

### Capitalisation terrain (TODO)
- Après 10 à 15 audios produits via HH-AutoMix Engine v1, compiler les cas où le mix auto passe en Go direct et ceux nécessitant un ajustement humain.
- Objectif : proposer des itérations v1.1 / v1.2 fondées sur les données réelles.

### Audios personnels / signature — décision stratégique
- Certains audios existants constituent une base personnelle / signature.
- Ils ne sont pas encore analysés selon le workflow Premium+++ et sont exclus du périmètre usine actuel.
- Leur analyse et amélioration sont prévues ultérieurement, une fois l’usine stabilisée et productive (TODO stratégique, sans lancement immédiat).

## TODO
- Ajouter les diagrammes détaillés du flux lorsque prêts.
