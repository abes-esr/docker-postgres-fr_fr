# docker-postgres-fr_FR

Images docker pour un postgresql embarquant la locale Française.

Cf préconisation de l'image docker officielle de postgresql :  
https://github.com/docker-library/docs/blob/master/postgres/README.md#locale-customization

## Générer une version

Cette image suit le cycle de développement de postgres ce qui signifie que pour générer une nouvelle version de cette image il faut :
- vérifier qu'une nouvelle version de postgres est disponible cf https://github.com/docker-library/docs/blob/master/postgres/README.md#supported-tags-and-respective-dockerfile-links  
  par exemple, la version ``14.3``
- modifier le numéro de version dans le Dockerfile [``FROM postgres:14.3``](https://github.com/abes-esr/docker-postgres-fr_FR/blob/main/Dockerfile#L1)
- lancer la github action ``create-release.yml`` et indiquer ``14.3.0`` comme numéro de release (incrémenter le dernier chiffre ``0`` si jamais des nouvelles versions indépendante de la version de postgres sont à générer)
