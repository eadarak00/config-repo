# config-repo

## config-repo

Ce dépôt contient tous les fichiers de configuration centralisée des microservices du projet **GL 2025** basé sur une architecture **Spring Cloud**.

## Fonctionnement

Ce dépôt est utilisé par le **Spring Cloud Config Server** (`ms-config-server`) pour fournir à chaque microservice sa configuration via Git.

Le serveur de configuration lit ces fichiers et les expose aux autres microservices en fonction de leur nom d’application (`spring.application.name`).

## Structure des fichiers

Chaque fichier correspond à un microservice :

| Fichier                  | Microservice            | Port par défaut | Base de données | Remarques                    |
|--------------------------|-------------------------|------------------|------------------|------------------------------|
| `application.yml`        | Global commun           | -                | -                | Configuration partagée       |
| `ms-config-server.yml`   | Config Server           | 8888             | -                |                                |
| `ms-register-server.yml` | Eureka Server           | 8761             | -                |                                |
| `ms-gateway.yml`         | API Gateway             | 8080             | -                | Routage vers les services     |
| `ms-classe.yml`          | Microservice Classe     | 9001             | MongoDB          | `classe-db`                   |
| `ms-etudiant.yml`        | Microservice Étudiant   | 9002             | MongoDB          | `etudiant-db`                 |

-------------------------------------
👨‍💻 Auteur : *El Hadji Abdou DRAME* 

📅 Dernière mise à jour : Juin 2025