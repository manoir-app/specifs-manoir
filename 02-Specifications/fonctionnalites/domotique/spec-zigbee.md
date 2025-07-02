# Spécification technique – Intégration Zigbee (via Zigbee2MQTT)

## Introduction

Cette spécification décrit l’intégration des équipements Zigbee dans le système MaNoir via Zigbee2MQTT. L’objectif est de permettre le contrôle, la supervision et l’automatisation des modules Zigbee (ampoules, capteurs, relais, etc.) au sein de la plateforme domotique.

## Objectifs
- Contrôler à distance les équipements Zigbee
- Récupérer l’état en temps réel
- Intégrer Zigbee dans les scénarios d’automatisation
- Superviser la consommation énergétique

## Fonctionnalités principales
- Découverte automatique des équipements via Zigbee2MQTT
- Contrôle individuel et groupé
- Programmation horaire et scénarios personnalisés
- Retour d’état et notifications d’anomalie
- Historique d’utilisation et de consommation

## Contraintes techniques
- Utilisation de Zigbee2MQTT (MQTT broker, configuration)
- Gestion des versions de firmware et compatibilité
- Réactivité < 1 seconde pour les actions manuelles
- Sécurisation des échanges (authentification MQTT)

## Droits d’accès
- Administrateur : configuration complète
- Adultes : contrôle total
- Enfants : contrôle limité à leur chambre
- Invités : contrôle dans les espaces communs

## Liens croisés
- [Spécification générale éclairage](spec-eclairage.md)
- [User stories](../../user-stories/)
- [Entités](../../entites/)
