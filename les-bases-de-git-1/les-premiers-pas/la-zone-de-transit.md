Un des concepts  essentiel de Git, est la zone de transit, ou *staging area*. Cette zone a pour but de savoir quelles modifications vont être commitées. Cette zone peut être simplement vue comme un une zone d'embarquement permettant de savoir quels changement vont être « envoyés ».  

# L'état de la zone de transit 
Une modification peut être dans l'un des états suivants : 

- **Modifications qui seront validées** : les modifications qui sont prêtes à être commitées.
- **Modifications qui ne seront pas validées** : des modifications sur des fichiers connus par Git, mais qui pour le moment ne seront pas commitées
- **Fichiers non suivis** : des fichiers qui ne sont pas connus par Git, donc des fichiers encore jamais ajoutés au dépôt.

Il est possible de connaître l'état de la zone de transit via la commande `git status`. C'est certainement une des commandes que vous allait employer le plus : celle-ci devrait systématiquement
être utilisée avant de commiter un changement. 

``` Bash
$ git status
Sur la branche master
Modifications qui seront validées :
(utilisez "git reset HEAD <fichier>..." pour désindexer)
modifié :         la-zone-de-transit.md

Modifications qui ne seront pas validées :
(utilisez "git add <fichier>..." pour mettre à jour ce qui sera validé)
(utilisez "git checkout -- <fichier>..." pour annuler les modifications dans la copie de travail)
modifié :         le-commit.md

Fichiers non suivis:
(utilisez "git add <fichier>..." pour inclure dans ce qui sera validé)
schema-staging.jpg
```
Ci dessus un exemple de `git status`, tiré du dépôt de ce tutoriel, comme vous pouvez le voir, cette commande donne un certain nombre d'informations sur l'état de votre dépot local : 

- La première ligne indique la branche sur laquelle vous êtes situé : nous verrons le fonctionnement des branches plus tard, pour le moment vous pouvez simplement retenir que « master » est la branche principale du dépot. 
- Le fichier `la-zone-de-transit.md` a été modifié, et sera commité
- Le fichier `le-commit.md` a été modifié, mais ne sera pas commité
- Le fichier `schema-staging.jpg` est un nouveau fichier qui n'est pas connu par Git.

La commande `status` présente également l'avantage de proposer des solutions pour faire passer un fichier d'un état à un autre :

- La commande `git add fichier…` permet de faire passer un fichier ou un dossier dans la zone de fichiers indexés. Cela peut-etre un fichier qui était non suivi, ou un fichier modifié qui était dans la parti des modifications qui ne seront pas commités.
- La commande `git reset fichier…` permet de faire passer un fichier de la partie des fichiers indexés, vers la partie des fichiers qui ne seront pas commités.

% TODO schéma avec genre les états différents d'un fichier (unstaged, staged, …)

# Commiter des modifications
Une fois que l'ont a compris le fonctionnement de la zone de transit, le fonctionnement du commit coule de source. Un commit peut se faire via plusieurs syntaxe différentes, mais le fonctionnement reste toujours le même : spécifier quels seront les modifications à commiter. 

- `git commit` : va commiter toutes les modifications qui sont dans la zone de modifications qui seront validées. Pour utiliser cette commande directement, il faut avoir effectuer des `git add` au préalable.
- `git commit fichier1 fichier2 …` : les seuls fichiers qui seront commités seront les fichiers en argument. Cela permet d'aller plus vite et d'effectuer le commit en une seule étape. Les fichiers en arguments doivent être suivis sous git, c'est-à-dire ne pas être dans la 3e section de la zone de transit. Dans le cadre d'un nouveau fichier, il faudra avoir utilisé `git add` au préalable.
- `git commit -a` : commit tous les fichiers modifiés, les seuls fichiers qui ne seront pas commités sont les fichiers non suivis. Ce commande n'est pas toujours recommandée, car en allant vite on risque de perdre le contrôle et de commiter des fichiers par erreur. À utiliser avec vigilence.

Lors de l'appel à la commande `commit`, un éditeur de texte va s'ouvrir. L'éditeur dépends de votre système, sous linux cela peut être *nano* par défaut. Dans cet éditeur, il faut renseigner la description du commit, donc des modifications. Une fois le message renseigné, un simple enregistrement suffit à valider le commit.

[[information]]
| Il est possible de renseigner un message de commit sur plusieurs lignes, 
| néanmoins dans les conventions de Git, la première ligne doit correspondre 
| à une description succinte de la modification, et les lignes suivantes à une 
| description plus approfondie. À l'instar d'un titre ou objet et de son contenu.
|
| À noter qu'en l'absence de message de commit, le commit sera annulé.

Si juste avant de faire un commit, vous souhaitez connaitre le détail des modifications effectuées sur vos fichiers, afin de savoir précisemment ce que votre commit va contenir, vous pouvez utiliser la commande `git diff [fichier]`, qui affichera les différences, soit du ou des fichiers donnés en paramètres, soit de tous les fichiers modifiés. 


% TODO : je pense que je vais transformer ça en un exo : un petit énnoncé tout bte, et une solution cachée avec les résultats.

# ## Exemple d'utilisation
% TODO : créer une organisation github pour mettre les exos. Ici, on pourrait récupérer un dépôt très basique avec quelques fichiers


[[information]]
| Afin de reproduire cet exemple, vous pouvez récupérer le dépôt sur Github.

Notre dépôt contient actuellement 3 fichiers : 
```
FichierA
dossier1/FichierB
FichierC
```

Lorsque vous clonez un dépôt, celui-ci est « propre », ainsi la zone de transit sera vide : 

```
$ git status
Sur la branche master
rien à valider, la copie de travail est propre
```

Nous allons maintenant modifier le `fichierA` et le fichier `dossier1/FichierB`, il suffit de l'ouvrir et rajouter une ligne de texte à la fin, on sauvegarde, on quitte.
