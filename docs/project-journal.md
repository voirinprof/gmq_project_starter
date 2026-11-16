# Journal du projet

L’étudiant ou l’assistant IA peut rédiger les entrées. L’assistant ne consigne que les travaux réellement réalisés ; il distingue les décisions confirmées des propositions, questions ouvertes et décisions à suivre. Ajoutez les entrées de la plus récente en haut et copiez le modèle en fin de document pour chaque nouvelle entrée.

## 2026-11-16 — Création du modèle de dépôt de projet

**Rédigé par :** Assistant IA

**Personnes impliquées :** À préciser

**Identifiants liés :** Aucun — création du modèle

### Travaux réalisés

- Création de la structure de dépôt pour les données brutes, les données préparées, les résultats, le code, les tests, la documentation et le tableau de bord.
- Ajout de fichiers `.gitkeep` dans les répertoires qui doivent être présents dès le démarrage.
- Ajout du `.gitignore` pour exclure les données et les secrets courants du suivi Git tout en conservant les répertoires avec leurs `.gitkeep`, et consigne à l’agent de bloquer les commits de données ou de secrets.
- Création de modèles Markdown pour la définition du projet, l’analyse des données, la conception de la solution et le présent journal.
- Rédaction du README pour guider le démarrage d’un projet individuel ou en équipe, le travail avec Git et la gestion reproductible des données, puis ajout des consignes de synchronisation avant le travail et de publication par commits structurés.
- Rédaction de `AGENTS.md` pour encadrer l’accompagnement par l’IA, les vérifications géomatiques, les normes de code, les identifiants de suivi et la validation des tests par le développeur.
- Création d’un tableau de bord HTML alimenté par `dashboard-data.json`, avec milestones repliables, sous-étapes et suivi des décisions structurantes. Le modèle comprend des exemples de décisions fictives à remplacer ou supprimer.
- Vérification de la validité du JSON et du chargement du tableau de bord avec un serveur local.

### Décisions prises et raisons

- Aucune décision propre à un projet étudiant n’a été confirmée : ce dépôt est un modèle à adapter.
- Le tableau de bord utilise une page HTML simple qui charge un fichier JSON, afin que les étudiants puissent modifier les données sans dépendance logicielle supplémentaire.

### Difficultés et questions ouvertes

- Les étudiants devront adapter la structure, les sous-étapes et les outils à leur projet et à leurs données.

### Prochaines étapes

- Renseigner la définition du projet, analyser les données disponibles et concevoir une approche adaptée.
- Remplacer les exemples fictifs du tableau de bord par les décisions structurantes réellement confirmées, le cas échéant.

---

## Modèle d’entrée

## [AAAA-MM-JJ] — [Séance ou étape]

**Rédigé par :** [Nom(s) ou assistant IA]

**Personnes impliquées :** [Noms, si projet en équipe]

**Identifiants liés :** [M-01, T-001, D-001 ou « Aucun »]

### Travaux réalisés

- [Travail ou avancement réalisé]

### Décisions prises et raisons

- [D-001 — Décision confirmée et raison, ou « Aucune »]

### Difficultés et questions ouvertes

- [Problème rencontré, question ouverte ou décision à suivre, ou « Aucune »]

### Prochaines étapes

- [Action à réaliser — responsable — échéance, si utile]
