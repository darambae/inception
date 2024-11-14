
# Inception

![image](https://github.com/user-attachments/assets/c7a1a6ac-ae6f-4dab-a306-0ae480f70b10)

## Table des Matières

- [Introduction](#introduction)
- [Fonctionnalités](#fonctionnalités)
- [Installation](#installation)
- [Conteneurs et Configuration](#conteneurs-et-configuration)
- [Structure du Projet](#structure-du-projet)
- [Référence](#référence)

---

## Introduction

Inception est un projet basé sur Docker où le but est de créer une infrastructure web sécurisée comprenant NGINX, WordPress et MariaDB, chacun fonctionnant dans son propre conteneur. Ce projet, faisant partie du programme de l'École 42, enseigne les concepts fondamentaux de l'administration système, de la conteneurisation et du réseau.

---

## Fonctionnalités

- Configuration multi-conteneurs Docker pour une pile de services web complète.
- Configuration sécurisée de NGINX avec prise en charge SSL.
- Stockage de données persistant à l'aide de volumes Docker pour MariaDB et WordPress.
- Isolation du réseau entre les conteneurs pour une sécurité accrue.

---

## Installation

```bash
git clone https://github.com/yourusername/inception.git
cd inception_public
make
```

---

## Conteneurs et Configuration

- **NGINX** - Sert de serveur web et de proxy inverse avec support SSL pour des connexions sécurisées.
- **MariaDB** - Fournit un backend de base de données compatible MySQL pour WordPress.
- **WordPress** - Système de gestion de contenu connecté à MariaDB pour le contenu dynamique.

---

## Structure du Projet

```
inception/
│
├── Makefile                 
└── srcs/
    ├── docker-compose.yml  
    ├── .env                 
    └── requirements/
        ├── mariadb/
        │   ├── Dockerfile
        │   ├── tools/
        │   └── conf/
        ├── nginx/
        │   ├── Dockerfile   
        │   └── conf/
        └── wordpress/
            ├── Dockerfile
            ├── tools/
            └── conf/
```

---

## Référence

- https://tuto.grademe.fr/inception/

---
