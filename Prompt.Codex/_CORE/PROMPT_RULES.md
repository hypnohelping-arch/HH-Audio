## Rôle de ces règles

Ces règles sont supérieures à tout prompt individuel.
Aucun prompt ne peut les contourner, les modifier ou y déroger.

## Règles de périmètre

- Codex agit uniquement dans le périmètre explicitement autorisé.
- Tout ce qui n’est pas explicitement autorisé est interdit.
- Toute action hors périmètre est proscrite.

## Règles d’exécution

- Il est interdit de supposer des informations manquantes.
- Il est interdit d’interpréter une intention implicite.
- L’ordre des étapes définies doit être strictement respecté.

## Règles de sécurité

- Toute action doit éviter les effets de bord.
- Il est interdit de modifier des fichiers non listés.
- Il est interdit de masquer, minimiser ou ignorer une erreur.

## Règles d’idempotence

- Chaque prompt doit être relançable sans effet négatif.
- Il est interdit de dépendre d’un état implicite.

## Règles de modification des fichiers

- Seuls les fichiers explicitement listés peuvent être modifiés.
- Il est interdit de reformater des fichiers non concernés.
- Le contenu existant hors zones explicitement ciblées doit être respecté.

## Règles de commit

- Un prompt équivaut à un seul commit.
- Le message de commit doit être explicite et conforme.
- Les commits partiels ou multiples sont interdits.

## Règles de validation

- Les sorties attendues doivent être vérifiées.
- Toute modification non prévue doit être vérifiée et exclue.

## Règles de refus et d’arrêt

- L’exécution doit être refusée si une règle est violée.
- L’exécution doit s’arrêter si une ambiguïté majeure est détectée.
- Aucune tentative de résolution créative non demandée n’est autorisée.

## Statut des règles

- Ces règles sont déclarées CORE.
- Elles ne peuvent être modifiées que par décision humaine explicite.
