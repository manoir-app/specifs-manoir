# Spécification fonctionnelle – Gestion de l’éclairage

## Introduction

Cette spécification décrit les besoins fonctionnels et techniques pour la gestion de l’éclairage connecté dans le système MaNoir. L’objectif est de permettre le contrôle centralisé, l’automatisation et la personnalisation de l’éclairage dans toutes les pièces du domicile.

## Objectifs
- Contrôler à distance l’allumage, l’extinction et l’intensité des lumières
- Créer des scénarios d’ambiance (lecture, soirée, nuit, etc.)
- Automatiser l’éclairage selon la présence, la luminosité ou des horaires
- Optimiser la consommation énergétique

## Fonctionnalités principales
- Contrôle individuel et groupé des ampoules et luminaires
- Variation d’intensité et de couleur (si matériel compatible)
- Programmation horaire et scénarios personnalisés
- Automatisation selon capteurs (présence, luminosité)
- Retour d’état en temps réel
- Historique d’utilisation

## Contraintes techniques
- Compatibilité multi-protocoles (WiFi, Zigbee, Matter…)
- Intégration des équipements et API suivants :
  - **Shelly** (via leurs API)
  - **Zigbee** (via Zigbee2MQTT)
  - **Philips Hue** (via leur bridge officiel)
  - **W-Led**
- Sécurisation des commandes et retours d’état
- Réactivité < 1 seconde pour les actions manuelles

## Droits d’accès
- Administrateur : configuration complète
- Adultes : contrôle total
- Enfants : contrôle limité à leur chambre
- Invités : contrôle dans les espaces communs

## Liens croisés
- [README Domotique](../README.md)
- [Spécification volets](spec-volets.md)
- [Spécification capteurs](spec-capteurs.md)
- [User stories](../../user-stories/)
- [Entités](../../entites/)
- [Tests](../../../05-Tests/)
