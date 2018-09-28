# Sous Windows
https://git-scm.com/download/win

3 outils en un seul téléchargement :
  * *Git GUI* Une interface graphique pour faire appel aux commandes git et pour voir l'état d'un dépôt ;
  * *Git Bash* Un invite de commande qui sert de CLI pour les commandes git mais qui fournis également des outils qu'on retrouve dans les environnement Linux (e.g. outils ssh, diff unix-like, etc.);
  * *gitk* L'interface CLI pour les commandes git utilisables directement dans la console Windows classique (cmd.exe).

Ces outils sont les outils "officiels" disponibles avec un installation de git simple sous Windows.
Il existe également d'autres outils tiers qui fournissent des interfaces graphiques pour utiliser les outils git et gérer ses dépôts.
Nous ne rentrerons pas dans les détails concernant ces outils vu qu'ils s'appuient sur git et ne constitue donc pas une étape de l'installation.
Cependant, certains de ces outils fournissent des fonctionnalités qui facilitent l'utilisation des commandes git, l'exploration des dépôts (fichiers et hitoriques), la gestion des branches, etc.
D'autres sont spécifiques à une plateforme particulière (GitHub Desktop pour ne nommer que lui) qui fournissent des fonctionnalités supplémentaires relatives à ces plateformes.
Dans tous les cas, ces outils ne vous apporteront pas de facilité d'utilisation significative si vous ne maîtriser pas les concepts de git (donc on continue la lecture :p).

Lien vers les GUI tiers : https://git-scm.com/download/guis/

Si vous vous demandez pourquoi avoir fait une section spéciale installation de git sou Windows, c'est parce que c'est pas si trivial qu'on pourrait penser.
Si en principe une installation d'un logiciels sous Windows consiste à simplement lancer un exécutable, cliquer 3 ou 4 fois sur "Suivant" et enfinc cliquer sur "Terminer", l'installation de Git for Windows demande un peu plus d'attention.
Bon d'accord, dans 87% des cas (nombre totalement arbitraire), les paramètres par défaut vous conviendront. Mais pour en être sûr, il faut savoir à quoi tous ces paramètres correspondent !

Nous allons don ici passer les différentes étapes d'installation en détail :
  1. *La licence.* git est fournis sous licence GPL v2. Si vous ne la connaissez pas, je vous invite à la lire, c'est toujours intéressant de connaître les licences du monde libre ;). Sinon, cliquer simplement sur "Next".
  2. *Les éléments à installer.* Ici rien de novateur non plus. Les paramètres par défaut sous acceptable pour une instalation classique.
     Un petit mot cependant sur Git LFS (Large File Support) qui sera détaillé en annexe. Les fichiers dits *binaires* comme par exemple les images, les sons ou même les documents Office ne peuvent pas être gérer par le système de patch de git.
     Pour garder un historique des évolutions et pouvoir restaurer un tel fichier à une version précédente, git garde une copie de chaque version publiée.
     Bien qu'il existe des moyens d'optimiser l'espace utilisé par un dépôt git, le système de LFS permet de garder des fichiers volumineux sans qu'ils soient stockés directement dans le dépôt.
     De plus, Git LFS est un service founit par Github et ne fait donc pas partie du package git "de base". Il est cependant coché par défaut dans l'installation de Git for Windows.
     Lien vers Git LFS https://git-lfs.github.com/
  3. *Choix de l'éditeur de texte par défaut*
  4. *PATH ou pas PATH ?*
  5. *Client SSH à utiliser*
  6. *HTTPS backend*
  7. *Fin de lignes*
  8. *Terminal pour Got Bash*
  9. *Options supplémentaires*
  10. (pour une mise à jour uniquement) *Fermer les éléments ouverts*
  11. *Installation*
  12. *Fin*



# Sous Linux
