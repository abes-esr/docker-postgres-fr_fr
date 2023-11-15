# postgres en version 8.2.23 et en locale FR

[![Docker Pulls](https://img.shields.io/docker/pulls/abesesr/postgres-fr_fr.svg)](https://hub.docker.com/r/abesesr/postgres-fr_fr/)

Ce dépôt contient les sources de l'image docker ``abesesr/postgres-fr_fr:8.2.23``  
Pour la récupérer :

```shell
docker pull abesesr/postgres-fr_fr:8.2.23
```

Cette image embarque postgresql en version ``8.2.23``

A noter que cette version n'est pas disponible dans les [images officielles de postgresql sur dockerhub](https://hub.docker.com/_/postgres) probablement car elle est trop vielle.

La version officielle la plus vielle disponible sur le [dockerhub officiel de postgresql](https://hub.docker.com/_/postgres) est la version ``8.4.22``

## Pourquoi cette image si vielle ?

Car une application Abes (Prada) a besoin de cette base de données dans cette version bien précise car le code source (également très vieux) en est dépendant. 
