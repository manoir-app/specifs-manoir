# Spécification fonctionnelle – Gestion des volets

## Introduction

Cette spécification décrit les besoins fonctionnels et techniques pour la gestion des volets roulants et stores motorisés dans le système MaNoir. L’objectif est de permettre un contrôle centralisé, des automatisations et une intégration avec les autres équipements domotiques.

## Objectifs
- Contrôler à distance l’ouverture et la fermeture des volets
- Automatiser selon la luminosité, la météo ou des horaires
- Intégrer les volets dans des scénarios d’ambiance ou de sécurité

## Fonctionnalités principales
- Contrôle individuel et groupé des volets
- Programmation horaire et scénarios personnalisés
- Automatisation selon capteurs (luminosité, température, présence)
- Retour d’état en temps réel
- Historique d’utilisation

## Contraintes techniques
- Compatibilité multi-protocoles (WiFi, Zigbee, Somfy, Matter…)
- Intégration des équipements et protocoles suivants :
  - **MQTT** (pour la communication avec Zigbee2MQTT, Shelly, W-Led, etc.)
- Sécurisation des commandes et retours d’état
- Réactivité < 2 secondes pour les actions manuelles

## Droits d’accès
- Administrateur : configuration complète
- Adultes : contrôle total
- Enfants : contrôle limité à leur chambre
- Invités : contrôle dans les espaces communs

## Liens croisés
- [README Domotique](../README.md)
- [Spécification éclairage](spec-eclairage.md)
- [Spécification capteurs](spec-capteurs.md)
- [User stories](../../user-stories/)
- [Entités](../../entites/)
- [Tests](../../../05-Tests/)
