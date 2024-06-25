# Scripts utilitaires pour l'installation

Les scripts suivants aident au déploiement réseau.

## `fetch-image-iso`

Ce script est à exécuter dans le répertoire `Wiki-SAES4/scripts/`.
Ce script télécharge l'image ISO de Debian 11.6.0 dans le dossier `Wiki-SAES4/ressources/images-ISO/`

``` sh
$ ./fetch-image-iso
```

!!! success "Note"
    Prend en compte la validation SHA512SUMS.

!!! info "Sortie"
    Indique si l'image est valide ou non. Si l'image est invalide, elle est supprimée 
    du dossier `images-ISO/`
