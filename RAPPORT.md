# Rapport de laboratoire Git - Équipe [Nom]

## 1. Membres de l'équipe
- Membre 1 : [Abdul Rahman Zahid - Chef d'équipe]
- Membre 2 : [Adel Tamani - Développeur]
- Membre 3 : [Diane Devi - Testeur]

## 2. Résumé des parties complétées

### Partie 1 : Configuration initiale
Nous avons initialisé un dépôt Git local, créé le dépôt distant sur GitHub et configuré le `README.md`. Nous avons également réglé notre identité Git (`user.name`, `user.email`) et vérifié l'état du dépôt avec `git status`. Cela nous a permis de comprendre le cycle de base (modifier → ajouter → valider → pousser) et l'importance de messages de commit clairs.

### Partie 2 : Ajout des collaborateurs
Le chef d'équipe a ajouté les collaborateurs via l'onglet Settings → Collaborators du dépôt GitHub. Chaque membre a accepté l'invitation puis a cloné le dépôt en local avec `git clone`. Nous avons ensuite configuré la branche par défaut et testé des pushes pour valider l'accès.

### Partie 3 : Première collaboration
Chaque membre a créé un fichier personnel (`membre1.txt`, `membre2.txt`, `membre3.txt`) décrivant son rôle. Nous avons suivi le flux: création/modification du fichier, `git add`, `git commit` puis `git push` sur la branche principale, en veillant à tirer (`git pull`) avant toute nouvelle modification pour éviter les conflits.

### Partie 4 : Résolution de conflits
Nous avons provoqué un conflit en modifiant la même section du `README.md` sur deux machines. Après un `git pull`, Git a signalé des marqueurs de conflit. Nous avons ouvert le fichier, retenu les changements pertinents, supprimé les marqueurs de conflit, validé la résolution (`git add` puis `git commit`) et poussé la version fusionnée. Nous avons appris à lire les marqueurs `<<<<<<<`, `=======`, `>>>>>>>` et à conserver un historique propre.

### Partie 5 : Collaboration HTML
Nous avons créé la page `index.html` et la feuille de styles `style.css` dans `projet-equipe-AbdulRahmanZahid/`. La structure HTML de base a été mise en place (titre, section), et des styles simples (police, marges, couleur d'arrière-plan, centrage du titre) ont été appliqués. Chaque membre a relu et validé les changements via des commits et pushes successifs.

### Partie 6 : Utilisation des branches
Nous avons créé une branche de fonctionnalité pour modifier la page HTML (`git checkout -b feature/html-update`). Les changements ont été validés sur la branche, puis fusionnés sur `main` via une pull request. Après revue, nous avons résolu d’éventuels conflits, validé la PR et supprimé la branche une fois la fusion terminée.

### Partie 7 : Situations réalistes
Nous avons simulé: (1) un conflit de fusion et sa résolution, (2) un commit erroné annulé par `git revert`, (3) une histoire réécrite localement corrigée par `git pull --rebase`, et (4) un travail parallèle sur branches avec revue de code avant fusion.

## 3. Captures d'écran

### Étape 1.2 - Création du compte GitHub
![Profil GitHub](../travail-a-remettre/screenshots/profil_github.png)

### Étape 1.2 - Nouveau dépôt sur GitHub (création)
![Création du dépôt](../travail-a-remettre/screenshots/capture_depot_git.png)

### Étape 1.3 - Premier push réussi
![Push réussi](../travail-a-remettre/screenshots/git_push_success.png)

### Étape 1.3 - README visible sur GitHub
![README visible](../travail-a-remettre/screenshots/readme_visible.png)

### Étape 2.1 - Invitations des collaborateurs
![Collaborateurs](../travail-a-remettre/screenshots/collaborateurs_invitations.png)

### Étape 3.1 - Commandes Git de base (add/commit/push)
![Commandes Git](../travail-a-remettre/screenshots/git_commands.png)

### Étape 5.1 - Édition du code HTML dans VS Code
![Code HTML](../travail-a-remettre/screenshots/codeHTML.png)

### Étape 5.1 - Fichier index.html visible sur GitHub
![index.html sur GitHub](../travail-a-remettre/screenshots/indexGithub.png)

### Étape 6.1 - Création de branche et push
![Branche et push](../travail-a-remettre/screenshots/creationBrancheEtPush.png)

### Étape 6.2 - Page web avec le nouveau style
![Page stylée](../travail-a-remettre/screenshots/pageWebAvecNouveauStyle.png)

### Partie 7 - Situation 1 : Modifications parallèles sans conflit
![Pull et push réussis](../travail-a-remettre/screenshots/terminalPullEtPush.png)

### Partie 7 - Situation 3 : Annulation de commit
![Annulation commit (1)](../travail-a-remettre/screenshots/terminalAnnulationCommit.png)
![Annulation commit (2)](../travail-a-remettre/screenshots/terminalAnnulationCommit2.png)

### Partie 7 - Situation 4 : Visualisation de l'historique
![Historique git](../travail-a-remettre/screenshots/terminalHistorique.png)

## 4. Difficultés rencontrées

### Difficulté 1
- **Problème** : Conflit lors d’un `git pull` après des modifications concurrentes sur `README.md`.
- **Solution** : Résolution manuelle des marqueurs de conflit, validation (`git add`, `git commit`) puis push de la version fusionnée.

### Difficulté 2
- **Problème** : Push rejeté à cause d’un historique en avance sur le distant.
- **Solution** : `git pull --rebase` pour intégrer les changements distants proprement, puis `git push`.

## 5. Apprentissages

### Ce que nous avons appris sur Git
- L’importance de tirer régulièrement (`git pull`) avant de commencer à travailler.
- La lecture et la résolution de conflits de fusion de manière méthodique.
- L’utilisation des branches pour isoler les fonctionnalités et faciliter la revue de code.

### Ce que nous avons appris sur le travail d'équipe
- La communication fréquente évite les doublons et les conflits inutiles.
- La coordination via des branches, des PR et des messages de commit clairs accélère l’intégration.

## 6. Conclusion
Ce laboratoire nous a permis de pratiquer concrètement le flux Git complet, de la configuration initiale jusqu’à la collaboration via branches et pull requests. Nous avons rencontré des conflits réels et appris à les résoudre proprement en conservant un historique lisible. L’utilisation disciplinée des commandes de base, combinée à une communication d’équipe claire, a rendu le travail plus fluide. La réalisation d’une petite page HTML/CSS a servi de support simple pour expérimenter les contributions parallèles. Enfin, nous repartons avec de meilleures habitudes: tirer souvent, valider tôt avec des messages explicites, et privilégier les branches pour toute évolution.
