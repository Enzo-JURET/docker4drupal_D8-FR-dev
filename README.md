# Pile Drupal à base de dockers

[![Build Status](https://travis-ci.org/wodby/docker4drupal.svg?branch=master)](https://travis-ci.org/wodby/docker4drupal)

## Introduction

Docker4Drupal est un ensemble d'images de docker optimisé pour Drupal. Utilisez le fichier `docker-compose.yml` de la [dernière version stable](https://github.com/wodby/docker4drupal/releases) pour faire tourner l'environnement local sous Linux, Mac OS X et Windows. Cette projet existe déjà dans sa version complète [ici](https://github.com/Enzo-JURET/docker4drupal_D8-FR)

* Lire la documentation sur [**comment utiliser**](https://wodby.com/docs/stacks/drupal/local#usage)
* Rejoignez notre communauté sur [Spectrum](https://spectrum.chat/wodby/drupal) et posez des questions sur le canal `#Drupal`.
* Suivez [@wodbycloud](https://twitter.com/wodbycloud) pour les annonces à venir

## Version du Projet
version : 1.1.0

## Stack

La pile (stack) Drupal se compose des conteneurs par défaut suivants :

| Container       | Versions               | Service name    | Image                              | Default |
| --------------  | ---------------------- | --------------- | ---------------------------------- | ------- |
| [Nginx]         | 1.17	               | `nginx`         | [wodby/nginx]                      | ✓       |
| [Drupal]        | 8, 7                   | `php`           | [wodby/drupal]                     | ✓       |
| [PHP]           | 7.3					   | `php`           | [wodby/drupal-php]                 | ✓       |
| [MariaDB]       | 10.4				   | `mariadb`       | [wodby/mariadb]                    | ✓       |
| Traefik         | latest                 | `traefik`       | [_/traefik]                        | ✓       |

Versions Drupal supportées : 8

## Documentation

La documentation complète est disponible à l'adresse https://wodby.com/docs/stacks/drupal/local

## Images' tags

Le format des balises d'images est `[VERSION]-[STABILITY_TAG]` où :

`[VERSION]` est la _version d'une application_ (sans version patch) s'exécutant dans un conteneur, par exemple `wodby/nginx:1.1.15-x.x.x.x' où la version Nginx est `1.15' et `x.x.x' est un tag de stabilité. Pour certaines images, nous incluons des versions majeures et mineures comme PHP `7.2`, pour d'autres nous incluons seulement des versions majeures comme Redis `5`. 

'[STABILITY_TAG]` est la _version d'une image_ qui correspond à une balise git du référentiel d'images, par exemple `wodby/mariadb:10.2-3.3.3.8` a MariaDB `10.2` et la balise de stabilité[`3.3.8`](https://github.com/wodby/mariadb/releases/tag/3.3.8). Les nouvelles balises de stabilité incluent des mises à jour de patchs pour les applications et les corrections/améliorations d'images (nouvelles env vars, corrections d'actions d'orchestration, etc). Les changements d'étiquette de stabilité sont décrits dans la description correspondante de l'étiquette git. Les étiquettes de stabilité suivent[versionnement sémantique](https://semver.org/).
Nous vous encourageons fortement à n'utiliser des images qu'avec des étiquettes de stabilité.
Traduit avec www.DeepL.com/Translator (version gratuite)

## Maintenance

Nous mettons régulièrement à jour les images utilisées dans cette pile et les publions ensemble, voir [page des versions](https://github.com/wodby/docker4drupal/releases) pour le journal complet des modifications et les instructions de mise à jour. La plupart des mises à jour de routine pour les images et ce projet ont été effectuées par [Le bot](https://github.com/wodbot) via des scripts situés sur [wodby/images](https://github.com/wodby/images).

## Au-delà de l'environnement local

Docker4Drupal est un projet conçu pour vous aider à créer un environnement local avec docker-compose. Si vous voulez déployer une pile cohérente avec orchestrations sur votre propre serveur, allez voir [Drupal stack](https://wodby.com/stacks/drupal) sur Wodby ![](https://www.google.com/s2/favicons?domain=wodby.com).

## Etapes de mise en place

* Télécharger / Cloner le projet dans un répertoire
* Modifier le fichier des variables d'environnement (.env)
* Modifier le fichier de configuration .yml (docker-compose.yml)
* Adapter les volumes selon l'emplacement de votre Drupal
* Démarer le serveur Docker avec la commande (docker-compose up -d)
* Accéder à votre site cette structure d'URL : PROJECT_BASE_URL:PORT_TRAEFIK


## Autres projets Docker4x

* [docker4php](https://github.com/wodby/docker4php)
* [docker4wordpress](https://github.com/wodby/docker4wordpress)
* [docker4ruby](https://github.com/wodby/docker4ruby)
* [docker4python](https://github.com/wodby/docker4python)

## Licence d'utilisation

Ce projet est licencié sous la licence open source du MIT.

[Drupal]: https://wodby.com/docs/stacks/drupal/containers#php
[MariaDB]: https://wodby.com/docs/stacks/drupal/containers#mariadb
[Nginx]: https://wodby.com/docs/stacks/drupal/containers#nginx
[PHP]: https://wodby.com/docs/stacks/drupal/containers#php
[_/traefik]: https://hub.docker.com/_/traefik
[wodby/drupal-php]: https://github.com/wodby/drupal-php
[wodby/mariadb]: https://github.com/wodby/mariadb
[wodby/nginx]: https://github.com/wodby/nginx
