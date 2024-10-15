# ESGI test FYC project

## Overview

Projet en microservice, où l'on construit une application avec un front, un back, un service d'authentification, et un serveur nginx comme seul point d'entré qui bloque les requêtes non autentifiés. On y vois aussi comment le setup pour faire du kubernetes en local avec du live reload comme docker-compose.

* Auth : Express JS, très simple sans bdd
* Frontend : Vuejs + axios + lint, injection de l'URL au Nginx
* Backend : Django + linter ruff + une vue qui renvoi l'heure
* Nginx : Routage aux autres services + Authentification

chacun des services a un Dockerfile et un fichier de deploiement kubernetes, pour fonctionner sous tilt et docker-compose 

## Lancer le projet

lancable avec docker-compose ou bien avec tilt.

Pour tilt vous devez l'installer, installer kind pour avoir un kube en local et ctlptl pour créer un cluster kind avec un registre d'images local, plus globalement il y a besoin de kubectl pour intéragir avec kind


