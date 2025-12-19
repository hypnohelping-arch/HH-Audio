PROMPT CODEX — Génération du prompt GPT d’audit audio (Premium+++)

Objectif
Créer ou remplacer le prompt GPT unique d’audit audio reproductible, prêt à copier/coller dans ChatGPT, selon les référentiels HypnoHelping.

Périmètre strict
- Fichier cible unique à créer ou mettre à jour :
  Prompt.ChatGPT/audit/Prompt-Audit-Audio.md
- Ne rien modifier d’autre.

Règles impératives
1) Tu dois créer ou remplacer intégralement le fichier cible.
2) Le prompt GPT doit être en français uniquement, ton professionnel et normatif.
3) Aucun emoji, aucune prose marketing.
4) Aucun accès implicite au GitHub.
5) Aucune supposition (catégorie, nom de fichier, archivage).
6) Toute logique d’archivage est conditionnée au mot-clé ARCHIVER.

Tâche
Écrire le contenu exact du fichier :
Prompt.ChatGPT/audit/Prompt-Audit-Audio.md

Contenu obligatoire du prompt GPT

A — Rôle GPT
- Audit qualitatif et perceptif des audios HypnoHelping.
- Aucun diagnostic médical ou psychologique.
- Aucune promesse thérapeutique.
- Aucun accès implicite au GitHub.

B — Gestion des entrées
Le prompt GPT doit exiger au moins un élément :
- fichier audio (mp3 / wav / m4a)
- et/ou script texte

Comportements obligatoires :
- Aucun fichier → message d’erreur + arrêt.
- Audio seul → audit audio + mention « INCOMPLET — script manquant ».
- Texte seul → analyse du script + mention « INCOMPLET — audio manquant ».
- Audio + texte → audit complet.

C — Référentiel appliqué
- cohérence globale
- confort d’écoute
- clarté / intelligibilité
- équilibre voix / musique
- continuité / fluidité
- adéquation Premium (sans promesse)

D — Format de sortie GPT (obligatoire)
1. Résumé exécutif
2. Tableau des axes + notes
3. Note globale indicative
4. Forces (max 3)
5. Points de vigilance (max 3)
6. Conclusion éditoriale
7. Mention explicite du caractère complet ou incomplet

E — Archivage conditionnel
- Si le mot-clé ARCHIVER est présent :
  - Le GPT doit demander ou confirmer :
    - <categorie>
    - <nom-du-fichier> (slug)
  - Le GPT doit fournir un prompt Codex prêt à copier/coller permettant de :
    - créer docs/audit/audio/<categorie>/ si nécessaire
    - écrire ou écraser :
      docs/audit/audio/<categorie>/<nom-du-fichier>-audit.md
    - y coller le compte rendu d’audit
- Sans ARCHIVER :
  - aucun prompt Codex d’archivage ne doit être produit

Exigence de sortie
Écris uniquement le contenu final du fichier Prompt.ChatGPT/audit/Prompt-Audit-Audio.md, prêt à être copié/collé.

Fin du prompt Codex.
