---
title: Luminochat
publishDate: 2023-04-01 00:00:00
img: /assets/luminochat.jpg
img_alt: Architecture Kubernetes pour interface de chat IA avec pipeline CI/CD
description: |
  Interface de chat IA déployée sur AKS avec Terraform, Helm et pipeline GitLab CI/CD complet
tags:
  - Kubernetes
  - AKS
  - Terraform
  - Helm
  - GitLab CI/CD
  - Docker
---

## Vue d'ensemble

Déploiement d'une interface de chat similaire à ChatGPT basée sur LibreChat (projet open-source), utilisant une architecture Kubernetes complète avec Infrastructure as Code et pipeline CI/CD automatisé.

## Objectifs du projet

Créer une plateforme de chat IA scalable et sécurisée permettant :
- **Interaction** avec des APIs de chat IA (Google AI Studio, Gemini)
- **Gestion complète** des utilisateurs et permissions
- **Haute disponibilité** via Kubernetes
- **Déploiement automatisé** avec GitLab CI/CD

## Architecture technique

### Infrastructure as Code
- **Terraform** pour le provisioning de l'infrastructure Azure
- **Azure Kubernetes Service (AKS)** comme cluster d'orchestration
- **Azure Container Registry (ACR)** pour le stockage d'images
- **Load Balancer** pour l'exposition publique des services

### Application Stack
- **Backend API** : Gestion de la logique métier et des requêtes
- **Frontend Web** : Interface utilisateur responsive
- **MongoDB Atlas** : Base de données pour les conversations et utilisateurs
- **Meilisearch** : Moteur de recherche pour l'indexation des conversations

### Orchestration Kubernetes
- **Helm Charts** pour la gestion des déploiements
- **Pod management** avec scaling automatique
- **Service LoadBalancer** pour l'accès externe
- **ConfigMaps et Secrets** pour la configuration sécurisée

## Pipeline CI/CD GitLab

### Étapes automatisées
```yaml
Stages:
1. Security Check (OWASP)
2. Build Stage (Docker Image)
3. Push to ACR
4. Deploy Stage (Helm Install)
```

### Sécurité intégrée
- **Scan OWASP** pour détecter les vulnérabilités
- **Images Docker** optimisées et sécurisées
- **Secrets management** via Kubernetes
- **Network policies** pour isoler les pods

## Déploiement et orchestration

### Conteneurisation
- **Multi-stage Docker builds** pour optimiser les images
- **Health checks** et readiness probes
- **Resource limits** et requests optimisés

### Kubernetes natif
- **Deployments** avec stratégies de rolling update
- **Services** pour la découverte de services
- **Ingress** pour le routage HTTP/HTTPS
- **Persistent Volumes** pour le stockage stateful

### Monitoring et observabilité
- **Logs centralisés** via Kubernetes logging
- **Métriques** de performance des pods
- **Health checks** automatiques

## Intégrations externes

### Services cloud
- **MongoDB Atlas** : Base de données managée
- **Azure services** : ACR, AKS, Load Balancer
- **Gemini API** : Intelligence artificielle conversationnelle

### Accès et sécurité
- **Authentification** multi-niveaux
- **HTTPS/TLS** terminaison
- **Access control** basé sur les rôles Kubernetes

## Résultats techniques

- ✅ **Déploiement automatisé** avec pipeline GitLab
- ✅ **Scalabilité horizontale** via Kubernetes HPA
- ✅ **Haute disponibilité** avec réplication des pods
- ✅ **Infrastructure as Code** reproductible
- ✅ **Sécurité intégrée** à tous les niveaux
- ✅ **Monitoring complet** de l'infrastructure

## Architecture réseau

**Flux de données :**
```
Users → Load Balancer → AKS Pods → MongoDB Atlas
                    ↓
                Gemini API (IA)
```

**Accès public :** `20.123.249.112` via Load Balancer Azure

## Technologies utilisées

Kubernetes • AKS • Terraform • Helm • GitLab CI/CD • Docker • MongoDB • Azure • LibreChat

## Points techniques avancés

- **Multi-environment** deployment (dev/staging/prod)
- **Blue-green deployment** strategy avec Helm
- **Resource optimization** pour les coûts cloud
- **Backup strategy** pour MongoDB Atlas