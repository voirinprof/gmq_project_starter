# [Titre du projet]

> **À personnaliser :** remplacez les éléments entre crochets, adaptez les sections à votre projet et supprimez les consignes qui ne vous sont plus utiles.

## Présentation

Ce projet porte sur **[sujet ou territoire étudié]**. Il vise à **[objectif principal]**, en s’appuyant sur **[principales données ou méthodes]**, afin de **[résultat ou utilité attendue]**.

### Problématique

[Formulez en une ou deux phrases la question à laquelle le projet cherche à répondre.]

### Objectifs

- [Objectif 1]
- [Objectif 2]
- [Objectif 3, si nécessaire]

### Périmètre et limites

- **Territoire et période étudiés :** [à préciser]
- **Résultats attendus :** [cartes, indicateurs, analyse, outil, etc.]
- **Limites connues :** [données manquantes, échelle, hypothèses ou autres limites]

## Équipe

Choisissez la section qui convient et supprimez l’autre.

### Projet individuel

- **Auteur ou autrice :** [nom]
- **Contact :** [facultatif]

### Projet en équipe

| Membre | Rôle ou responsabilités |
| --- | --- |
| [Nom] | [Responsabilités principales] |
| [Nom] | [Responsabilités principales] |

Répartissez le travail et convenez d’un mode de communication. Les responsabilités peuvent évoluer ; gardez cette section à jour.

## Bien démarrer

1. **Clarifiez le projet** dans [la définition du projet](docs/project-definition.md) : besoin, question, objectifs et périmètre.
2. **Inventoriez les données** dans [l’analyse des données](docs/data-assessment.md) : sources, formats, dates, qualité, unités et système de coordonnées de référence (CRS).
3. **Décrivez l’approche** dans [la conception de la solution](docs/solution-design.md) : traitements, résultats attendus et tests.
4. **Préparez l’environnement** : choisissez les outils nécessaires au projet et documentez leur installation ainsi que les commandes pour exécuter le travail.
5. **Avancez par petites étapes** : vérifiez les données et les résultats à chaque étape, puis consignez les décisions et les prochaines actions dans [le journal du projet](docs/project-journal.md).

Ne supposez pas que les données sont compatibles parce qu’elles s’ouvrent : vérifiez notamment leur CRS, leur emprise, leurs unités et leurs limites avant de les analyser.

### Validation des développements

Après chaque exécution de tests, l’assistant IA présente les résultats et demande au développeur de les valider, soit en consultant le rapport, soit en effectuant une vérification manuelle. Une tâche ou une milestone ne passe à `Terminé` qu’après cette confirmation. Si les tests automatisés ne sont pas disponibles, l’assistant propose des étapes de test manuel et attend le retour du développeur.

## Données et reproductibilité

- Le `.gitignore` exclut le contenu de `data/` ; seuls les fichiers `.gitkeep` des répertoires `raw/`, `processed/` et `outputs/` préservent la structure dans Git. Ne forcez pas l’ajout de données au dépôt.
- Ne commitez aucun jeu de données, même s’il est petit. Documentez plutôt sa provenance, sa licence et les étapes permettant de l’obtenir. L’assistant IA doit refuser d’aider à committer des données et peut aider à préparer cette documentation ou un procédé de récupération.
- Ne commitez jamais de secrets : mots de passe, jetons, clés privées ou fichiers de configuration contenant des identifiants. Le `.gitignore` exclut notamment les `.env`, fichiers `credentials.*` et `secrets.*`, ainsi que les clés et certificats privés. Un `.env.example` doit contenir uniquement des valeurs fictives ou vides ; l’assistant IA doit vérifier le contenu des fichiers avant un commit.
- Documentez la provenance, la date, la licence et les limites de chaque source de données.
- Ne versionnez pas de données confidentielles, personnelles ou dont la redistribution n’est pas autorisée.
- Évitez d’ajouter au dépôt de gros fichiers reproductibles ou téléchargeables ; expliquez plutôt où les obtenir et comment les préparer.
- Conservez les données originales sans les modifier. Placez les données préparées et les résultats dans les répertoires correspondants.
- Notez les versions des outils et les étapes nécessaires pour reproduire les résultats.

## Travail avec Git

### Pour tous les projets

- Au début de chaque séance de travail, récupérez les changements du dépôt distant avec `git pull --ff-only`. Si vous avez des modifications locales non enregistrées ou si Git signale un conflit, sauvegardez votre travail et résolvez la situation avant de poursuivre ; ne l’écrasez pas.
- Après validation des changements, publiez-les dans le dépôt distant avec des commits structurés : un changement cohérent par commit et un message concis, par exemple `docs: préciser le démarrage` ou `feat: suivre les décisions`.
- L’assistant IA peut aider à vérifier l’état Git, préparer les messages et exécuter les commandes si le dépôt le permet et si vous l’autorisez.
- Ne remplacez pas le travail d’une autre personne sans en discuter.
- Gardez les décisions sur les données, le CRS, les unités et les méthodes documentées.

### En équipe

- Décidez ensemble de la répartition des tâches et de la façon de signaler les blocages.
- Si vous connaissez les branches Git, utilisez une branche par tâche et faites relire les changements avant de les intégrer à la branche principale.
- Évitez de modifier simultanément les mêmes fichiers ; prévenez l’équipe si un fichier partagé doit changer.
- En cas de conflit, comparez les changements et convenez de la version à conserver au lieu de choisir au hasard.

### En projet individuel

Utilisez aussi des commits comme points de sauvegarde et notez les décisions importantes. Cela facilite le suivi et le retour à une version antérieure.

## Structure du dépôt

Adaptez cette structure si le projet le nécessite.

```text
.
├── data/
│   ├── raw/         # Données sources (non modifiées)
│   ├── processed/   # Données préparées
│   └── outputs/     # Résultats produits
├── docs/            # Cadrage, données, conception et journal
├── src/             # Code source
├── tests/           # Tests
└── dashboard/       # Page HTML et données du tableau de bord
    ├── index.html
    └── dashboard-data.json
```

## Afficher le tableau de bord

La page charge automatiquement `dashboard-data.json`. Pour l’afficher dans un navigateur :

1. Installez l’extension **Live Server** dans VS Code, si nécessaire.
2. Ouvrez `dashboard/index.html`, puis cliquez sur **Go Live** dans la barre d’état ou choisissez **Open with Live Server** dans le menu contextuel.
3. La page s’ouvre dans votre navigateur. Vous pouvez aussi ouvrir l’adresse locale fournie par Live Server dans le navigateur intégré de VS Code, si disponible.

Les milestones qui contiennent des sous-étapes se replient et se déplient en cliquant sur leur titre. Survolez leur nom pour afficher l’indication « Cliquer pour voir les sous-étapes ». Un seul milestone peut être ouvert à la fois.

## Identifiants de suivi

Utilisez des identifiants stables dans le journal et le tableau de bord : `M-01` pour une milestone, `T-001` pour une tâche et `D-001` pour une décision. Attribuez les numéros dans l’ordre, ne les réutilisez pas et conservez-les si le libellé ou le statut change.

Les sous-étapes du cadrage reprennent les rubriques des documents de définition, d’analyse des données et de conception. Les autres milestones contiennent des sous-étapes génériques à adapter. Modifiez `dashboard/dashboard-data.json` pour ajuster chaque statut (`À faire`, `En cours`, `Terminé`), ainsi que la phase et la progression globale.

Les décisions à suivre sont les choix qui ont un impact structurant sur l’architecture de la solution, les formats de données ou le flux de traitement ; les petits choix opérationnels n’ont pas besoin d’être listés. Utilisez le statut `Confirmée`, `En attente`, `Reportée` ou `Suspendue`. Le tableau sépare les décisions confirmées des points à suivre ; les décisions ouvertes ne sont pas présentées comme des choix pris. Le tableau de bord contient quatre décisions marquées `EXEMPLE FICTIF` pour illustrer les statuts : supprimez-les ou remplacez-les avant de l’utiliser pour un projet réel.

```json
{
  "id": "D-001",
  "date": "AAAA-MM-JJ",
  "decision": "[Décision confirmée]",
  "status": "Confirmée",
  "reason": "[Raison de la décision]"
}
```

Ajoutez les décisions confirmées et les points structurants à suivre au journal, en distinguant clairement leur statut. Laissez `decisions` vide si le projet n’a encore aucun de ces éléments.

## Outils et exécution

- **Langage ou environnement :** [à préciser]
- **Bibliothèques et logiciels :** [à préciser, seulement ceux réellement utilisés]
- **Installation :** [ajouter les étapes ou commandes nécessaires]
- **Exécution :** [indiquer les commandes ou étapes pour reproduire le traitement]

## Documentation du projet

- [Définition du projet](docs/project-definition.md)
- [Analyse des données](docs/data-assessment.md)
- [Conception de la solution](docs/solution-design.md)
- [Journal du projet](docs/project-journal.md)

## Références et remerciements

[Ajoutez les sources de données, références méthodologiques, licences et contributions externes pertinentes.]
