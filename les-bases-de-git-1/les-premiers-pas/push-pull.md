Maintenant que nou avons effectué un commit, nous allons voir comment se synchroniser avec un serveur. C'est-à-dire envoyer votre ou vos commits sur le serveur, mais également pouvoir récupérer des modifications sur le serveur qui ne sont pas encore sur votre poste local. 

Afin de simplifier l'opération, dans un premier temps nous allons supposer que vous êtes seul à travailler sur ce dépôt. Ainsi, il n'est pas possible d'avoir de modifications d'un même fichier sur votre ordinateur, et sur le serveur. Nous verrons comment gérer le travail collaboratif dans la partie 2. 

# Connaître les modifications présentes sur le serveur
La commande que vous devez effectuer très régulièrement, peut-être une des commandes des plus utiles avec le `git status` est la commande `git fetch`. Cette commande va simplement intérroger le serveur, et vous donner sons état.

C'est-à-dire qu'avec cette commande, vous serez capable de savoir le nombre de commits présents sur votre serveur, mais absent de votre poste local. Cela peut-arriver en cas de travail à plusieurs personnes, ou en cas de modifications sur plusieurs ordinateurs distincts. 

Si la commande ne retourne rien, c'est que vous étier à jour sur votre dépôt. Si vous travaillez tout seul, vous serez la plupart du temps dans ce cas. Sinon, vous aurez un résultat ressemblant à celui-ci : 
``` bash
$ git fetch
remote: Counting objects: 454, done.
remote: Total 454 (delta 109), reused 109 (delta 109), pack-reused 345
Réception d'objets: 100% (454/454), 217.46 KiB | 24.16 MiB/s, fait.
Résolution des deltas: 100% (209/209), complété avec 42 objets locaux.
Depuis git@github.com:aroquemaurel/Tutoriel-Git.git
   d2725d44..37c2d0dd  master     -> origin/master
```

La commande signal simplement qu'elle a trouvé de nouveaux commits, et qu'elle à mis à jour la branche « master ». Les branches seront étudiées en détail plus tard.

Après avoir effectué un git fetch, vous pouvez faire un `git status`, et une nouvelle informations va être présente : 

``` bash
$ git status
Sur la branche master
Votre branche est en retard sur 'origin/master' de 2 commits, et peut être mise à jour en avance rapide.
  (utilisez "git pull" pour mettre à jour votre branche locale)

rien à valider, la copie de travail est propre
```

Comme vous le voyez, le git status vous signal que vous êtes en retard de deux commits. Et il a même une proposition de commande afin de pouvoir vous mettre à jour. 


[[information]]
| origin est le nom par défaut de votre serveur. `origin/master` signifie donc la branche master sur le serveur origin. 

``` bash
$ git pull
Mise à jour d2725d44..37c2d0dd
Fast-forward
les-bases-de-git-1/introduction.md    |   2 +-
les-bases-de-git-1/conclusion.md      |   23 +++++--- 
2 files changed, 24 insertions(+), 6 deletions(-)
```

La commande a mis à jour deux fichiers, et nous signale le nombre d'insertions et de suppressions qui ont eu lieu sur le fichier. Maintenant vous êtes à jour. 

[[attention]]
| Le `git pull` est à utiliser uniquement si vous n'avez aucune modifications en locale, commitées ou non. Dans un premier temps, nous utiliserons toujours cette commande.
| Nous verrons dans la partie 2 comment vous mettre à jour en case de modifications sur votre poste local, et sur le serveur.

# Envoyer vos modifications
Dès que vous avez effectués au moins un commit, vous avez la possibilité d'envoyer celui-ci sur le serveur de votre dépôt. Avant-


``` bash
$ git push
Décompte des objets: 8, fait.
Delta compression using up to 12 threads.
Compression des objets: 100% (8/8), fait.
Écriture des objets: 100% (8/8), 2.40 KiB | 2.40 MiB/s, fait.
Total 8 (delta 5), reused 0 (delta 0)
remote: Resolving deltas: 100% (5/5), completed with 5 local objects.
To github.com:aroquemaurel/Tutoriel-Git.git
   09e14ec..c66e4ab  master -> origin/master
```
