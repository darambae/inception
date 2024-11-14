
# Inception

![image](https://github.com/user-attachments/assets/c7a1a6ac-ae6f-4dab-a306-0ae480f70b10)

## 목차

- [소개](#소개)
- [기능](#기능)
- [설치](#설치)
- [컨테이너 및 구성](#컨테이너-및-구성)
- [프로젝트 구조](#프로젝트-구조)
- [참고 자료](#참고-자료)

---

## 소개

Inception은 각각 NGINX, WordPress 및 MariaDB가 개별 컨테이너에서 실행되는 안전한 웹 인프라를 구축하는 것을 목표로 하는 Docker 기반 프로젝트입니다. 이 프로젝트는 Ecole 42 커리큘럼의 일환으로 시스템 관리, 컨테이너화 및 네트워킹의 기본 개념을 학습할 수 있도록 돕습니다.

---

## 기능

- 전체 웹 서비스 스택을 위한 다중 컨테이너 Docker 설정.
- SSL 지원이 포함된 안전한 NGINX 구성.
- MariaDB 및 WordPress를 위한 Docker 볼륨을 사용하여 데이터 영구 저장.
- 보안 강화를 위한 컨테이너 간 네트워크 분리.

---

## 설치

```bash
git clone https://github.com/yourusername/inception.git
cd inception_public
make
```

---

## 컨테이너 및 구성

- **NGINX** - SSL 지원을 통한 안전한 연결을 제공하는 웹 서버 및 역방향 프록시 역할.
- **MariaDB** - WordPress에 대한 MySQL 호환 데이터베이스 백엔드를 제공.
- **WordPress** - MariaDB에 연결된 콘텐츠 관리 시스템으로 동적 콘텐츠 제공.

---

## 프로젝트 구조

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

## 참고 자료

- https://tuto.grademe.fr/inception/

---
