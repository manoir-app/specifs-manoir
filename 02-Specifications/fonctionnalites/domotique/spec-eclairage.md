# Spécification fonctionnelle – Gestion de l'éclairage

## Introduction

Cette spécification décrit les besoins fonctionnels et techniques pour la gestion de l'éclairage connecté dans le système MaNoir. L'objectif est de permettre le contrôle centralisé, l'automatisation et la personnalisation de l'éclairage dans toutes les pièces du domicile.

## Fonctionnalités principales

### Contrôle d'éclairage
- Contrôle individuel et groupé des ampoules et luminaires
- Variation d'intensité et de couleur (si matériel compatible)
- Retour d'état en temps réel
- Gestion par zones et pièces

### Automatisation
- Programmation horaire
- Déclenchement par capteurs (présence, luminosité)
- Scénarios personnalisés
- Apprentissage des habitudes

### Interface utilisateur
- Interface adaptée par profil utilisateur (administrateur, adultes, enfants, invités)
- Contrôles parentaux avec restrictions temporelles  
- Mode invité avec accès limité et temporaire
- Contrôle vocal et gestuel

## Contraintes techniques
- Intégration des équipements et API suivants :
  - **Shelly** (via leurs API REST)
  - **Zigbee** (via Zigbee2MQTT)  
  - **Philips Hue** (via leur bridge officiel)
  - **W-Led** (via API HTTP)
  - **MQTT** pour les communications inter-modules
- Sécurisation des commandes et retours d'état
- Réactivité < 1 seconde pour les actions manuelles
- Compatibilité multi-plateforme (web, mobile, vocal)

## Droits d'accès
- **Administrateur** : configuration complète du système
- **Adultes** : contrôle total de l'éclairage
- **Enfants** : contrôle limité selon restrictions parentales
- **Invités** : accès aux espaces communs uniquement

## Liens croisés
- [Spécification volets](spec-volets.md)
- [Spécification capteurs](spec-capteurs.md)
- [Profils utilisateurs](../../user-stories/)
- [Architecture technique](../../../03-Architecture/)
