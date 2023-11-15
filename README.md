# docker-postgres-fr_fr


[![Docker Pulls](https://img.shields.io/docker/pulls/abesesr/postgres-fr_fr.svg)](https://hub.docker.com/r/abesesr/postgres-fr_fr/) [![build-test-pubtodockerhub](https://github.com/abes-esr/docker-postgres-fr_fr/actions/workflows/build-test-pubtodockerhub.yml/badge.svg)](https://github.com/abes-esr/docker-postgres-fr_fr/actions/workflows/build-test-pubtodockerhub.yml)

Images docker 🐳 pour un postgresql embarquant la locale Française.

Cf préconisation de l'image docker officielle de postgresql :  
https://github.com/docker-library/docs/blob/master/postgres/README.md#locale-customization

## Version alternative

Une image docker d'une vielle version de postgresql est maintenue dans la branche [8.2.23](https://github.com/abes-esr/docker-postgres-fr_fr/tree/8.2.23) de ce dépôt github.
On y retrouver les sources permettant de construir l'image docker ``abesesr/postgres-fr_fr:8.2.23``

Cette vielle version a comme unique usage l'application Prada de l'Abes.

## Générer une version

Cette image suit le cycle de développement de postgres ce qui signifie que pour générer une nouvelle version de cette image il faut :
- vérifier qu'une nouvelle version de postgres est disponible cf https://github.com/docker-library/docs/blob/master/postgres/README.md#supported-tags-and-respective-dockerfile-links  
  par exemple, la version ``14.3``
- modifier le numéro de version dans le Dockerfile [``FROM postgres:14.3``](https://github.com/abes-esr/docker-postgres-fr_FR/blob/main/Dockerfile#L1)
- lancer la github action [``create-release.yml``](https://github.com/abes-esr/docker-postgres-fr_FR/actions/workflows/create-release.yml) et indiquer ``14.3.0`` comme numéro de release (incrémenter le dernier chiffre ``0`` si jamais des nouvelles versions indépendantes de la version de postgres sont à générer)
