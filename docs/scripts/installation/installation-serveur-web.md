# Scripts pour l'installation et la configuration du serveur web et de la base de données

Le script suivant permet d'installer et de configurer le serveur web et la base de données.
Le serveur web utilise Apache et la base de données postgresql

## `script-serv-web-sql`

Localisation : `Wiki-SAE4/scripts/setup-apache-psql/`

Le script installe apache et le configure pour que la page par défaut d'apache soit accessible.
Le script installe postgresql et créé une base de données de test avec des valeurs et un utilisateur.
Après installation, apache est disponible sur le port 80 et postgresql sur le port 5432

``` sh
$ ./script-serv-web-sql
```

!!! info "Sortie"
    Il faut que la personne executant le script saisisse un mot de passe pour le compte `usertest`de la base de données au moment ou le shell lui demande. 

??? abstract "Code"
    ```sh title="Wiki-SAES4/scripts/setup-apache-psql/script-serv-web-sql" linenums="1"
    
    --8<-- "scripts/setup-apache-psql/script-serv-web-sql"
    ```