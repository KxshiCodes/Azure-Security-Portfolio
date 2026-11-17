
[🇬🇧 English](README.md) | [🇫🇷 Français](README.fr.md)

# Portfolio Cybersécurité Azure <img src="https://img.shields.io/badge/Statut-Terminé-green" />

Un portfolio pratique consacré à la sécurité dans Microsoft Azure, avec un accent particulier sur les fondamentaux de la sécurité cloud, la protection des identités, la détection des menaces, la supervision et la réponse aux incidents.

Ce dépôt présente plusieurs projets pratiques visant à démontrer les compétences attendues d'un analyste SOC ou d'un analyste en sécurité cloud Azure. Ils couvrent notamment la sécurisation des ressources Azure, l'analyse des événements de sécurité, l'investigation des menaces et l'amélioration de la posture de sécurité des environnements cloud.

---

# Objectifs du portfolio

Ce portfolio a pour objectifs de :

- Développer une expérience pratique en sécurité Azure
- Comprendre les principaux concepts et services de sécurité d'Azure
- Mettre en œuvre des contrôles de sécurité liés aux identités et aux accès
- Déployer des capacités de supervision et de détection des menaces
- Analyser et investiguer des incidents à l'aide des outils de sécurité Microsoft
- Documenter les choix de sécurité, les résultats des investigations et les enseignements tirés

---

# Organisation du portfolio

Les projets suivent les différentes étapes de la sécurisation et de la supervision d'un environnement Azure :

Fondations Azure → Sécurité des identités → Sécurité réseau → Supervision et détection des menaces → Simulation d'attaques → Réponse aux incidents

---

# Projets

## 1. Fondations Azure

Mise en place de l'environnement Azure de base nécessaire à la supervision de sécurité et aux investigations.

**Axes de travail :**

- Configuration des ressources Azure
- Déploiement d'un espace de travail Log Analytics
- Déploiement de Microsoft Sentinel
- Collecte des données et journaux de sécurité (*Security Telemetry*)
- Vérification et validation des requêtes KQL

## 2. Sécurité des identités

Sécurisation des identités et de la gestion des accès dans Azure à l'aide de Microsoft Entra ID et du contrôle d'accès basé sur les rôles (RBAC).

**Axes de travail :**

- RBAC et principe du moindre privilège
- Gestion des identités et des accès (IAM)
- Authentification et authentification multifacteur (MFA)
- Accès conditionnel (*Conditional Access*)
- Protection des identités (*Identity Protection*)
- Gestion des accès privilégiés
- Principes du Zero Trust

## 3. Sécurité réseau

Mise en œuvre de mécanismes de sécurité pour protéger les réseaux et les communications dans Azure.

**Axes de travail :**

- Segmentation réseau
- Groupes de sécurité réseau (*Network Security Groups*)
- Azure Firewall
- Sécurisation des connexions réseau

## 4. Supervision et détection des menaces

Mise en place de capacités de visibilité, de supervision et de détection des activités suspectes.

**Axes de travail :**

- Microsoft Sentinel
- Microsoft Defender
- Analyse des alertes de sécurité
- Analyse des journaux (*Log Analysis*)
- Ingénierie de détection (*Detection Engineering*)

## 5. Simulation d'attaques

Réalisation de scénarios d'attaque contrôlés afin de mieux comprendre les techniques utilisées par les attaquants et de vérifier l'efficacité des mécanismes de sécurité mis en place.

**Axes de travail :**

- Accès aux identifiants (*Credential Access*)
- Techniques d'exécution (*Execution*)
- Élévation de privilèges (*Privilege Escalation*)
- Contournement des mécanismes de défense (*Defence Evasion*)
- Déplacements latéraux (*Lateral Movement*)

## 6. Réponse aux incidents

Investigation et traitement des incidents de sécurité en suivant une méthodologie de travail inspirée des processus utilisés dans un SOC.

**Axes de travail :**

- Qualification et tri des alertes (*Alert Triage*)
- Investigation des incidents
- Analyse des indicateurs de compromission (IOC)
- Documentation des incidents
- Recommandations et mesures de remédiation

---

# Technologies utilisées

- Microsoft Azure
- Microsoft Entra ID
- Microsoft Sentinel
- Microsoft Defender for Cloud
- Microsoft Defender for Office 365
- Azure Monitor
- Log Analytics Workspace
- KQL (Kusto Query Language)
- PowerShell

---

# Objectif final

L'objectif de ce portfolio est de démontrer des compétences pratiques en sécurité Azure à travers la mise en œuvre de contrôles de sécurité, l'investigation de menaces et la documentation technique.

Chaque projet vise à comprendre non seulement **comment** configurer les mécanismes de sécurité, mais également **pourquoi** ils sont nécessaires et comment ils contribuent à protéger des environnements cloud dans un contexte professionnel.
