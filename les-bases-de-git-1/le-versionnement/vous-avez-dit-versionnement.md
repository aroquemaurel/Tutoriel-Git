> Avez-vous déjà:
>
> - Effectué un changement de code, réalisé que c'était une erreur, et voulu revenir en arrière ?
> - Perdu du code ou avoir une sauvegarde trop ancienne ? 
> - Du maintenir plusieurs version d'un produit ?
> - Voulu voir la différence entre 2 (ou plus) version de votre code ?
> - Voulu montrer qu'un changement particulier à cassé ou réparé un bout de code ?
> - Voulu revoir l'historique d'un morceau de code ?
> - Voulu envoyer un changement de code à quelqu'un d'autre ?
> - Voulu partage votre code, ou laisser d'autres personnes travailler sur votre code ?
> - Voulu voir quelle quantité de travail a été faite, où, quand et par qui ?
> - Voulu essayer une nouvelle fonctionnalité sans interférer avec du code fonctionnel ? 
>
> Dans ces cas là, et sans doute dans d'autres, un système de contrôle devrait vous simplifier la vie.
>
> Pour mal citer un ami : un outil civilisé pour un age civilisé.
> Source: Traduction d'un [message StackOverflow](https://stackoverflow.com/questions/1408450/why-should-i-use-version-control#1408464)

Ce message trouvé sur Stack Overflow, résume parfaitement les besoins d'un logiciel de versions. 

Le premier intérêt de la gestion de version, comme son nom l'indique, c'est de revenir à version antérieure facilement et rapidement. Dans le cadre d'un logiciel, certaines fonctionnalités cessent de fonctionner. Il est alors indispensable de revenir à la version précédente afin de corriger le problème. 

Mais il existe une autre facette : la gestion collaborative du projet. Il est possible d'être plusieurs personnes à travailler
simultanément sur un même projet. La gestion de version permet d'éviter de s'envoyer du code par e-mail ou par clef USB rendant les tâches de fusions et de suivi des modifications trop complexe.  C'est donc le logiciel de versionnement qui se chargera de la fusion des travaux des différents membres de l'équipe. 

Enfin, un projet peut-être ancien. On peut avoir besoin de parcourir son histoire : qui a rédigé cette fonctionnalité
? À quelle date ? À-t-elle été modifiée depuis ? Chaque modification du code source comporte un message du développeur, son nom ainsi que la date à laquelle la modification à eu lieue. Il est alors aisé de connaître l'histoire d'un projet.

Si je regarde le projet [Zeste de Savoir](https://github.com/zestedesavoir/zds-site/commits/dev), l'historique peut-ressembler à l'image ci-dessous. Comme on peut le voir, on à un petit descriptif de la modification, la date à laquelle elle a été faite, et l'auteur de la modification.

![Exemple d'historique d'un projet](img/historique.png)

