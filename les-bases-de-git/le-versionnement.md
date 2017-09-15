Avant d'apprendre à utiliser Git, il faut savoir de quoi nous parlons. La problématique de sauvegarde ou de travail collaboratif n'est pas quelque chose de nouveau, et il existe plusieurs logiciel, plus ou moins anciens, permettant d'effectuer du contrôle de version. Nous allons voir ce qu'apporte Git par rapport à d'autres alternatives. 

# Vous avez-dit gestion de version ? 
Bien que le versionnement peut s'appliquer pour n'importe quel type de projet texte, tel qu'un livre ou un tutoriel, celui-ci a
d'abord été pensé pour le génie logiciel. En effet, un logiciel peut être assez conséquent, et être développé par un grand nombre de
personne. 

Le premier intérêt de la gestion de version, comme le nom l'indique, c'est qu'il faut pouvoir revenir à une version ultérieure
facilement et rapidement. Dans le cadre d'un logiciel, il peut arriver que d'anciennes fonctionnalités ne fonctionne plus. Il est
alors indispensable de revenir à la version précédente afin de corriger le problème. 

Mais l'autre facette va être toute la getion collaborative du projet. Ainsi, il est possible d'être plusieurs personnes à travailler
simultanément sur le projet. C'est alors le logiciel qui se chargera de la fusion des travaux des différents membres de l'équipe.

Enfin, un projet peut-être ancien. Et il peut arriver d'avoir besoin de parcourir son histoire : qui a rédigé cette fonctionnalité
? À quelle date ? À-t-elle été modifiée depuis ? 

TODO : schéma contenant un historique simple à comprendre

# Deux approches différentes du contrôle de version
Dans la famille de la gestion de version, il existe deux approches très différentes de celle-ci : les systèmes centralisés, et les
systèmes distribués. 

## Un système centralisé
Lorsque plusieurs personnes travaillent à plusieurs, un *serveur* est nécessaire. Ce serveur est le *centre* de tout échange entre les
différents membres de l'équipe. Chaque membre de l'équipe est ensuite un *client*.

C'est-à-dire qu'à chaque fois qu'une personne souhaite effectuer une action sur le contrôle de version, une communication réseau
avec le serveur central est nécessaire. Ces actions peuvent-être par exemple : 

- Afficher l'historique
- Envoyer du nouveau code
- Obtenir le code d'un autre membre de l'équipe
- Revenir à une version ultérieure

Le serveur central est donc le cœur du système, et son intégrité physque doit être conservé au maximum. En effet, hors backup, toute l'histoire
du projet est sur celui-ci ! 

TODO : schéma contenant un serveur + N clients

Les systèmes centraliés sont historiquement les premiers à être apparus, ce sont souvent des logiciels un peu plus
anciens qui utilisent ceux-ci. 

Ils ont l'avantage d'être assez simple à apréhender et à mettre en place. En revanche, si le serveur n'est pas accessible (en cas de
		problème réseau, ou si le serveur ne fontionne plus par exemple) toute l'équipe ne peut plus effectuer d'actions de versionnement. Pour cette même raison, il est compliqué de travailler dans un endroit sans connexion internet, tel que le train.

## Un système distribué
Les systèmes distribués quant-à-eux sont plus complexe à apréhender. Chaque membre de l'équipe peut-être vu à la fois comme un
client et comme un serveur. Bien que ce soit systématiquementh le cas, un serveur central n'est donc pas nécessaire. 

TODO : schéma contenant interconnexion de clients

La conséquence principale de ce sytème, c'est que chaque développeur à accès à toutes les informations de versionnement directement
sur son ordinateur. Ainsi, hors connexion, ou sans accès au serveur, il est possible d'effectuer toutes les tâches présentées
précédemment. Cela veut dire également que chaque membre de l'équipe possède l'histoire du projet depuis ses prémices. 

À noter que le schéma présenté précédemment est volontairement biaisé. En effet, afin de synchroniser facilement tous les membres de
l'équipe, un serveur Git est mis en place. Celui-ci est au centre des communications, mais contrairement à un système centralisé, la
plupart des actions serons effectué sur le poste de l'utilisateur, lorsque celui-ci le souhaitera, il sera possible de se
synchroniser avec le serveur afin d'être à jour.

Git est un système distribué.

TODO : schéma contenant Serveur + clients avec lien dans deux sens, et flèches locales

# Git, face à la concurrence
Maintenant que vous savez comment fonctionne un logiciel de versionnement classique, il va être plus facile de comparer les
différents outils. Nous allons juste vous présenter certains outils, afin que vous connaissiez les différentes possibilités.

| Nom			| Type
|	SVN			|
|	Mercurial	|
|  Bazaar		|
| CVS			|
| Git			|

## Et Git dans tout ça ? 
Git est un logiciel libre, sous license GNU, qui a été créé par Linus Torvalds, le créateur de Linux, en 2003 (TODO : check date).

Celui-ci présente l'avantage d'être utilisé par un grand nombre de projets, et notamment des projets libres tel que zestedesavoir.
Il est possible de facilement posséder un serveur Git en utilisant des sites web collaboratifs tel que Github : celui-ci
fournit un espace gratuit à condition que le code source soit ouvert, d'où sa popularité dans le logiciel libre. Si vous souhaitez
participer à des projets open source, c'est une excellente plateforme.

