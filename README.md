# Profil de management par les couleurs

Application Web statique pour GitHub Pages : questionnaire à curseurs, calcul Rouge / Jaune / Vert / Bleu, radar et export PDF.

## Publication sur GitHub Pages

1. Créez un dépôt GitHub vide.
2. Décompressez l’archive et déposez **le contenu** du dossier à la racine du dépôt.
3. Dans **Settings > Pages**, choisissez **Deploy from a branch**.
4. Sélectionnez la branche **main** et le dossier **/(root)**, puis enregistrez.
5. Ouvrez l’adresse GitHub Pages indiquée par GitHub.

## Structure

- `index.html` : structure de la page et chargement des scripts.
- `css/style.css` : présentation responsive et impression.
- `js/app.js` : questionnaire, calcul, radar, sauvegarde locale et PDF.
- `data/questions.json` : questions, couleurs et barème.
- `.nojekyll` : empêche le traitement Jekyll inutile.

## Modifier les questions

Éditez `data/questions.json` sans changer les noms des propriétés. Chaque question comporte une proposition gauche et droite, chacune associée à une couleur.

## Développement local

Le chargement JSON utilise `fetch`. Pour tester localement, servez le dossier avec un serveur HTTP, par exemple :

```bash
python -m http.server 8000
```

Puis ouvrez `http://localhost:8000`.

## Données et confidentialité

Les réponses sont enregistrées uniquement dans le stockage local du navigateur. Elles ne sont envoyées vers aucun serveur par le code fourni.

## Export PDF

L’export PDF utilise jsPDF chargé depuis cdnjs. Une connexion Internet est donc requise au moment de charger la page pour activer ce bouton. L’impression du navigateur reste disponible.

## Avertissement pédagogique

Cet outil est inspiré du modèle DISC / management par les couleurs. Il ne constitue ni un diagnostic psychologique ni un test psychométrique validé.
