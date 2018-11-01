Dans la famille de la gestion de version, il existe deux approches très différentes de celle-ci : les systèmes centralisés, et les systèmes distribués. 

Bien que dans les deux cas la finalité soit la même, sauvegarder les versions et faciliter le travail collaboratif, le fonctionnement va différer. Alors qu'un système centralisé nécessite un serveur accessible à tous les contributeurs pour effectuer toute action de versionnement, un système décentralisé permet d'effectuer un certain nombre d'actions en local, une synchronisation avec les autres contributeurs aura lieu ensuite.

# Les systèmes centralisés
Lorsque plusieurs personnes travaillent en collaboration, un *serveur* est nécessaire. Ce serveur est le *centre* de tout échange entre les différents membres de l'équipe. Chaque membre de la dite équipe est ensuite un *client*.

C'est-à-dire qu'à chaque fois qu'une personne souhaite effectuer une action sur le contrôle de version, une communication réseau avec le serveur central est nécessaire. Ces actions peuvent-être par exemple : 

- Afficher l'historique des modifications
- Envoyer une nouvelle modification
- Obtenir les modifications d'un autre membre de l'équipe
- Revenir à une version ultérieure

Le serveur central est donc le cœur du système, et son intégrité physique doit être conservée au maximum. Si celui-ci est inaccessible, l'équipe peut être fortement pénalisé. De plus, en dehors de toute sauvegarde, l'ensemble de l'histoire du projet se trouve sur ce serveur.

**TODO AR : schéma contenant un serveur + N clients**

Les systèmes centralisé sont historiquement les premiers à être apparus, ce sont souvent des logiciels un peu plus anciens.

Ils ont l'avantage d'être assez simple à appréhender et à mettre en place. L'inconvénient principal étant la nécessité d'une connexion réseau avec le serveur. Il est donc compliqué de travailler dans le train par exemple.

# Les systèmes distribués
Les systèmes distribués quant-à-eux sont un peu plus complexes. Chaque membre de l'équipe peut-être vu à la fois comme un client et comme un serveur. Bien que par commodité ce soit systématiquement le cas, un serveur central n'est pas nécessaire.

Contrairement au système centralisé,  chaque développeur à accès à toutes les informations de versionnement directement sur son ordinateur. Hors connexion, il est possible d'effectuer toutes les tâches présentées
précédemment. Cela veut dire également que chaque membre de l'équipe possède l'histoire du projet depuis ses prémices. 

Afin de synchroniser facilement tous les membres de l'équipe, un serveur central est mis en place. Celui-ci est au centre des communications, mais contrairement à précédemment, la plupart des actions serons effectué sur le poste de l'utilisateur, lorsque celui-ci le souhaitera, il pourra effectuer des actions afin de se mettre à jour vis-à-vis des autres utilisateurs.

**TODO AR : schéma contenant Serveur + clients avec lien dans deux sens, et flèches locales**
