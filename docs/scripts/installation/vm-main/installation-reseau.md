# Script

## creation-reseaux

Localisation : `Wiki-SAES4/scripts/creation-reseaux`

``` sh
$ ./creation-reseaux 
```

Ce script n'a pas besoin d'être dans un répertoire spécifique pour être executé.
**Mais il créé 3 fichiers *.xml dans l'endroit où il est exécuté.**

Le programme boucle sur une liste de noms de réseaux virtuels : "server", "admin", et "user".

Dans chaque itération de la boucle, le nom du réseau virtuel est stocké dans la variable "reseau", en concaténant la chaîne de caractères "vlan" avec le nom du réseau. Un fichier de configuration XML est créé pour chaque réseau (sous la forme vlan[nom].xml). Le contenu du fichier XML contient toute la configuration du réseau. Il n'est pas supprimé à la fin de l'exécution.

Ensuite, le script utilise le fichier précédemment créé pour créer le réseau, activer la fonctionnalité "autostart", puis démarrer le réseau.

Enfin, le programme affiche tous les réseaux de virsh pour pouvoir avoir une idée de la bonne exécution ou non du programme.


!!! info "Sortie"
    Créé 3 fichiers xml à l'endroit où il est exécuté.

??? abstract "Code"
    ```sh title="Wiki-SAES4/scripts/check-scripts" linenums="1"
    
    --8<-- "scripts/creation-reseaux"
    ```

## creation-interfaces

Localisation : `Wiki-SAES4/scripts/creation-interfaces`

``` sh
$ ./creation-interfaces
```

Le script n'a pas besoin d'être dans un répertoire spécifique pour être exécuté.

Ce script créé 5 interfaces (sous la forme de tapX où X prend un nombre) pour chaque utilisateur dans le groupe admin (pour voir les groupes et les personnes dans un groupe, tapez `cat /etc/group`).

Sur ces interfaces, aucune adresse IP n'est attribuée, c'est-à-dire que toutes les adresses IP sont acceptables sur ces interfaces.

Cependant, ces interfaces sont liées à l'interface virbr1 d'adresse IP 192.168.0.1 de la machine principale.

??? abstract "Code"
    ```sh title="Wiki-SAES4/scripts/check-scripts" linenums="1"
    
    --8<-- "scripts/creation-interfaces"
    ```