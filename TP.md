## Personne du Groupe

- KOFFI Yahse
- Sacaze Steven
- ASSORHANI Abderrahim

## Description des tâches réalisé

1. Forkerez le projet dans votre propre répository
   
   `Création d'un repository github`

2. Créer un fichier TP.md qui contient les membres de votre groupe, et une description de ce que vous avez fait, les difficulités rencontrées, comment vous y avez remédiées.

   `Le fichier TP.md permet de listé les différentes actions effectués sur le projet. Ainsi que les réussites et les problèmes rencontrer.`

3. Ajouter un Jenkinsfile qui permettra de controler l'intégration continue du projet

   `Jenkins créer sur une VM ubuntu. L'utilisation de celui-ci s'effectue via un conteneur Docker`

   - Ce qu'il faut faire : 

   `Mise en place d'un Credentials pour le projet git`
   `Mise en place d'un pipeline pour le projet`
   `Configurer le Build Triggers sur Scrutation de l'outil de gestion de version avec H/15 * * * * comme paramètre`
   `Configurer le pipeline script from SCM`
   `Création du fichier Jenkinsfile sur le projet git`
   `Mettre un script pour vérifier le pipeline dans le Jenkinsfile`
   `Test du script valider`
   `Modifier le script pour executer les tests unitaires`
   `Erreur de version pour maven et le jdk lors du test du pipeline`
   
5. Exécution de tests unitaires (si le projet en fourni), et de tests statiques

    `Utilisation de de l'editeur intelliJ pour démarer le package maven et run les tests unitaires`

6. Génération d'un package (maven)

    `Pour la génération du package, utiliser la commande 'mvn clean package' et build le projet`

8. packaging du projet sous Docker

    `Utilisation de jenkins sous docker`

## Érreur pour réaliser le tp

![](https://cdn.discordapp.com/attachments/921384665238081626/937819168961618030/unknown.png)

`Les PATH pour maven et le jdk ne son pas trouver par le pipeline`