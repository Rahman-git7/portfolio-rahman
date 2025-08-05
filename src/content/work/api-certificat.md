---
title: API Certificat
publishDate: 2023-08-01 00:00:00
img: /assets/api-cert.jpg
img_alt: Pipeline GitLab CI/CD pour API de gestion de certificats
description: |
  API REST sécurisée en Go pour génération et vérification de certificats avec pipeline DevOps automatisé
tags:
  - Go
  - Gin Tonic
  - PocketBase
  - GitLab CI/CD
  - AWS ECS
  - Docker
---

## Vue d'ensemble

Développement d'une API REST complète en Go pour la génération et la vérification de certificats, intégrée dans une usine logicielle DevOps pour un déploiement continu. Cette solution sécurise divers services d'entreprise nécessitant une gestion centralisée des certificats.

## Liens du projet

🔗 **Repository GitLab** : [gitlab.com/Rahman-S/api-certificats](https://gitlab.com/Rahman-S/api-certificats)

## Objectifs du projet

L'API vise à centraliser la gestion des certificats pour différents services de l'entreprise, en offrant une solution sécurisée, scalable et conforme aux réglementations (RGPD, ISO).

## Architecture technique

### Backend API
- **Go** comme langage principal pour les performances
- **Gin Tonic** comme framework web léger et rapide
- **PocketBase** pour l'authentification et la gestion des utilisateurs
- Architecture RESTful avec endpoints sécurisés

### Fonctionnalités principales
- **Gestion des utilisateurs** et des droits d'accès
- **Génération automatique** de certificats sécurisés
- **Vérification** et validation des certificats existants
- **Gestion du cycle de vie** des certificats (création, renouvellement, révocation)

## Pipeline DevOps

### GitLab CI/CD
Le fichier `.gitlab-ci.yml` automatise l'ensemble du processus :

**Stages du pipeline :**
- **Build** : Compilation de l'application Go
- **Test** : Exécution des tests unitaires et d'intégration
- **Deploy** : Déploiement automatique sur AWS ECS

**Fonctionnalités avancées :**
- **Cache** pour accélérer les builds
- **Images Docker** optimisées
- **Déploiement conditionnel** par branche
- **Rollback automatique** en cas d'échec

### Conteneurisation et déploiement
- **Docker** pour la conteneurisation de l'application
- **AWS ECS** pour l'orchestration et la scalabilité
- **Load Balancer** pour la haute disponibilité
- **Auto-scaling** basé sur la charge

## Sécurité et conformité

### Standards de sécurité
- **Authentification** multi-niveaux avec PocketBase
- **Chiffrement** des certificats et des communications
- **Audit logs** pour la traçabilité
- **Rate limiting** pour prévenir les abus

### Conformité réglementaire
- **RGPD** : Protection des données personnelles
- **ISO 27001** : Standards de sécurité de l'information
- **Bonnes pratiques** de développement sécurisé

## Résultats et impact

- ✅ **Centralisation** de la gestion des certificats
- ✅ **Automatisation** complète du pipeline DevOps
- ✅ **Sécurité renforcée** avec authentification robuste
- ✅ **Conformité** aux normes réglementaires
- ✅ **Scalabilité** avec AWS ECS et auto-scaling
- ✅ **Monitoring** et observabilité complète

## Technologies utilisées

Go • Gin Tonic • PocketBase • Docker • GitLab CI/CD • AWS ECS • Load Balancer


