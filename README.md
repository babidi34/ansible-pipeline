# Ansible Pipeline Playbooks

Bienvenue dans le repository **Ansible Pipeline Playbooks**. Ce projet contient une collection de playbooks Ansible prêts à l'utilisation pour automatiser et faciliter la gestion de vos pipelines CI/CD. Le repository est public et peut être cloné ou fork pour une utilisation directe dans vos propres pipelines.

## Table des matières

- [Introduction](#introduction)
- [Prérequis](#prérequis)
- [Utilisation](#utilisation)
- [Contribuer](#contribuer)
- [Licence](#licence)

## Introduction

Ce projet vise à fournir des playbooks Ansible modulaires et réutilisables pour diverses tâches courantes dans les pipelines CI/CD. Que vous soyez DevOps, administrateur système ou développeur, ces playbooks peuvent vous aider à automatiser vos workflows et améliorer l'efficacité de vos déploiements.

## Prérequis

Avant de commencer, assurez-vous d'avoir les éléments suivants installés sur votre système:

- Ansible (version 2.9+)
- Git


## Utilisation

Pour utiliser les playbooks dans vos pipelines, vous pouvez les intégrer directement dans vos fichiers de configuration CI/CD. Voici un exemple d'utilisation avec GitLab CI:

stages:
  - prepare
  - deploy

prepare:
  stage: prepare
  script:
    - apt-get update
    - apt-get install -y ansible
    - git clone https://gitlab.com/babidi34/ansible-pipeline.git
    - ansible-playbook ansible-pipeline/playbooks/setup.yml

deploy:
  stage: deploy
  script:
    - ansible-playbook ansible-pipeline/playbooks/deploy.yml

## Contribuer

Les contributions sont les bienvenues! Pour contribuer:

1. Forkez le projet
2. Créez votre branche feature (git checkout -b feature/amazing-feature)
3. Commitez vos changements (git commit -m 'Add some amazing feature')
4. Poussez votre branche (git push origin feature/amazing-feature)
5. Ouvrez une Pull Request

## Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus d'informations.
