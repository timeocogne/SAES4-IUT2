# Scripts utilitaires pour la production

Les scripts suivants aident au développement et au test de nos divers scripts.
Ces scripts ne sont pas utiles à l'installation de l'architecture.

## `check-scripts`


Localisation : `Wiki-SAES4/scripts/check-scripts`  

Ce script est à exécuter dans le répertoire `Wiki-SAES4/scripts/`.

Parcourt le répertoire `Wiki-SAES4/scripts/` et ses sous répertoires récursivement,
et passe chaque script exécutable au logiciel shellcheck.

``` sh
$ ./check-scripts [SEVERITY]
```

!!! question "Options"
    ``` { .txt .no-copy title="SEVERITY"}
    La gravité des erreurs à rechercher.

    style (default)     recherche toutes les erreurs par défaut
    info
    warning
    error               ne recherche que les erreurs les plus graves
    ```

!!! info "Sortie"
    Pour chaque script (exécutable) rencontré, affiche s'il passe le spellcheck ou non, 
    et les erreurs éventuellement rencontrées (selon la gravité demandée).

??? abstract "Code"
    ```sh title="Wiki-SAES4/scripts/check-scripts" linenums="1"
    
    --8<-- "scripts/check-scripts"
    ```

## `create-administrateurs-sae`

Localisation : `Wiki-SAES4/scripts/create-administrateurs-sae.`


Ce script créer des utilisateurs sur la machine où il est exécuté.
Ces utilisateurs ne sont utiles que dans le cadre de la SAE.

``` sh
$ ./create-aministrateurs-sae
```

??? abstract "Code"
    ```sh title="Wiki-SAES4/scripts/create-administrateurs-sae" linenums="1"
    
    --8<-- "scripts/create-administrateurs-sae"
    ```
