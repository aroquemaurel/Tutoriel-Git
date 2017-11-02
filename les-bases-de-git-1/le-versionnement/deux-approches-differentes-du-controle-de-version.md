Dans la famille de la gestion de version, il existe deux approches très différentes de celle-ci : les systèmes centralisés, et les systèmes distribués. 

Bien que dans les deux cas la finalité soit la même, sauvegarder les versions et faciliter le travail collaboratif, le fonctionnement va différer. Ainsi alors qu'un système centralisé nécessite un serveur accessible à tous les contributeurs pour effectuer toute action de versionnement, un système décentralisé va permettre d'effectuer un certain nombre d'actions en local, une synchronisation avec les autres contributeurs aura lieu ensuite.

# Les systèmes centralisés
Lorsque plusieurs personnes travaillent en collaboration, un *serveur* est nécessaire. Ce serveur est le *centre* de tout échange entre les
différents membres de l'équipe. Chaque membre de la dite équipe est ensuite un *client*.

C'est-à-dire qu'à chaque fois qu'une personne souhaite effectuer une action sur le contrôle de version, une communication réseau
avec le serveur central est nécessaire. Ces actions peuvent-être par exemple : 

- Afficher l'historique des modifications
- Envoyer une nouvelle modification
- Obtenir les modifications d'un autre membre de l'équipe
- Revenir à une version ultérieure

Le serveur central est donc le cœur du système, et son intégrité physque doit être conservée au maximum. En effet, si celui-ci est innacessible l'équipe peut être fortement pénalisé, de plus, en dehors de toute sauvegarde, l'ensemble de l'histoire de projet se trouve sur ce serveur.

**TODO AR : schéma contenant un serveur + N clients**

Les systèmes centraliés sont historiquement les premiers à être apparus, ce sont souvent des logiciels un peu plus anciens qui utilisent ce système 

Ils ont l'avantage d'être assez simple à apréhender et à mettre en place. En revanche, si le serveur n'est pas accessible (problème réseau, problème matériel, …) toute l'équipe ne peut plus effectuer d'actions de versionnement. Pour cette même raison, il est compliqué de travailler dans un endroit sans connexion internet, tel que le train.

# Les systèmes distribués
Les systèmes distribués quant-à-eux sont plus complexe à apréhender. Chaque membre de l'équipe peut-être vu à la fois comme un
client et comme un serveur. Bien que par commodité ce soit systèmatiquement le cas, un serveur central n'est pas nécessaire.

**TODO AR : schéma contenant interconnexion de clients**

La conséquence principale de ce sytème, c'est que chaque développeur à accès à toutes les informations de versionnement directement
sur son ordinateur. Hors connexion, ou sans accès au serveur, il est possible d'effectuer toutes les tâches présentées
précédemment. Cela veut dire également que chaque membre de l'équipe possède l'histoire du projet depuis ses prémices. 

À noter que le schéma présenté précédemment est volontairement biaisé. En effet, afin de synchroniser facilement tous les membres de
l'équipe, un serveur est mis en place. Celui-ci est au centre des communications, mais contrairement à un système centralisé, la
plupart des actions serons effectué sur le poste de l'utilisateur, lorsque celui-ci le souhaitera, il sera possible de se
synchroniser avec le serveur afin d'être à jour.

**TODO AR : schéma contenant Serveur + clients avec lien dans deux sens, et flèches locales**