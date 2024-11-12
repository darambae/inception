# Inception

![image](https://github.com/user-attachments/assets/c7a1a6ac-ae6f-4dab-a306-0ae480f70b10)


## Table of Contents


- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Containers and Configuration](#containers-and-configuration)
  - [English](#english)
  - [Français](#français)
  - [한국어](#한국어)
- [Project Structure](#project-structure)
- [Reference](#reference)
  
## Introduction

Inception is a Docker-based project where the goal is to create a secure web infrastructure consisting of NGINX, WordPress, and MariaDB, each running in its own container. This project, part of the Ecole 42 curriculum, teaches fundamental concepts of system administration, containerization, and networking.

Inception est un projet basé sur Docker où le but est de créer une infrastructure web sécurisée comprenant NGINX, WordPress et MariaDB, chacun fonctionnant dans son propre conteneur. Ce projet, faisant partie du programme de l'école 42, enseigne les concepts fondamentaux de l'administration système, de la conteneurisation et du réseau.

Inception은 각각 NGINX, WordPress 및 MariaDB가 개별 컨테이너에서 실행되는 안전한 웹 인프라를 구축하는 것을 목표로 하는 Docker 기반 프로젝트입니다. 이 프로젝트는 Ecole 42 커리큘럼의 일환으로 시스템 관리, 컨테이너화 및 네트워킹의 기본 개념을 학습할 수 있도록 돕습니다.

---

## Features

- Multi-container Docker setup for a complete web service stack.
- Secure NGINX configuration with SSL support.
- Persistent data storage using Docker volumes for MariaDB and WordPress.
- Network isolation between containers for added security.
<br><br>
- Configuration multi-conteneur Docker pour une pile de services web complète.
- Configuration sécurisée de NGINX avec prise en charge SSL.
- Stockage de données persistant à l'aide de volumes Docker pour MariaDB et WordPress.
- Isolation du réseau entre les conteneurs pour une sécurité accrue.
<br><br>
- 전체 웹 서비스 스택을 위한 다중 컨테이너 Docker 설정.
- SSL 지원이 포함된 안전한 NGINX 구성.
- MariaDB 및 WordPress를 위한 Docker 볼륨을 사용하여 데이터 영구 저장.
- 보안 강화를 위한 컨테이너 간 네트워크 분리.

---

## Installation

```bash
git clone https://github.com/yourusername/inception_public.git
cd inception_public
make
```

---

## Containers and Configuration

### English
- **NGINX** - Acts as a web server and reverse proxy with SSL support for secure connections.
- **MariaDB** - Provides a MySQL-compatible database backend for WordPress.
- **WordPress** - Content management system connected to MariaDB for dynamic content.

### Français
- **NGINX** - Sert de serveur web et de proxy inverse avec support SSL pour des connexions sécurisées.
- **MariaDB** - Fournit un backend de base de données compatible MySQL pour WordPress.
- **WordPress** - Système de gestion de contenu connecté à MariaDB pour le contenu dynamique.

### 한국어
- **NGINX** - SSL 지원을 통한 안전한 연결을 제공하는 웹 서버 및 역방향 프록시 역할.
- **MariaDB** - WordPress에 대한 MySQL 호환 데이터베이스 백엔드를 제공.
- **WordPress** - MariaDB에 연결된 콘텐츠 관리 시스템으로 동적 콘텐츠 제공.

---

## Project Structure

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
## Reference
- https://tuto.grademe.fr/inception/
---
