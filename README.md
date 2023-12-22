# Get_next_line

42 project:

Il y a 2 versions de ce projet: Avec et sans les bonus.

Je vous conseil de compiler celle avec _bonus pour avoir tout les fonctionnalite de mon gnl.

 Le but du projet est d'écrire une fonction C qui permet de lire une ligne (jusqu'à un retour à la ligne) depuis un descripteur de fichier, et de la renvoyer à chaque appel de la fonction.

Voici une brève description du projet et de ses exigences :
Objectif du Projet :

Le principal objectif de get_next_line est de permettre la lecture d'une ligne terminée par un caractère de fin de ligne ('\n') depuis un fichier descripteur donné (par exemple, un fichier, un flux d'entrée, ou même l'entrée standard).
Contraintes et Exigences :

    Utilisation des Fonctions Système : Les étudiants doivent utiliser uniquement les fonctions système standard autorisées par l'énoncé, telles que read, malloc, et free.

    Gestion de la Mémoire : La gestion de la mémoire est cruciale. Les étudiants doivent allouer et libérer la mémoire correctement pour éviter les fuites de mémoire.

    Réentrance : La fonction get_next_line doit être capable de traiter plusieurs descripteurs de fichiers simultanément sans perdre l'état entre les appels.

    Fonctionnalités Avancées (Bonus) : Des fonctionnalités avancées peuvent être ajoutées en bonus, comme la gestion de plusieurs descripteurs de fichiers simultanément, la gestion d'autres caractères de fin de ligne, etc.

    Norme 42 : Le code doit respecter la norme de codage spécifique à l'école 42.

Utilisation Typique :

```c

#include "get_next_line.h"

int main() {
    int fd;
    char *line;

    fd = open("exemple.txt", O_RDONLY);
    while (get_next_line(fd, &line) > 0) {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return (0);
}
```

Points Clés :

    La fonction get_next_line doit être capable de gérer la lecture progressive d'un fichier jusqu'à la fin du fichier.
    Elle doit pouvoir gérer la lecture de plusieurs fichiers simultanément sans conflits.

La réalisation réussie de ce projet nécessite une compréhension approfondie des opérations d'entrée/sortie en C, de la gestion de la mémoire et de la manipulation des fichiers.
