# Spécification fonctionnelle – Gestion des capteurs (présence, luminosité, température, humidité)

## Introduction

Cette spécification décrit les besoins fonctionnels et techniques pour l’intégration et l’exploitation des capteurs dans le système MaNoir. Les capteurs sont essentiels pour l’automatisation intelligente et la surveillance de l’environnement domestique.

## Objectifs
- Collecter et centraliser les données des capteurs (présence, luminosité, température, humidité)
- Déclencher des automatisations selon les valeurs mesurées
- Surveiller l’environnement et générer des alertes en cas d’anomalie

## Fonctionnalités principales
- Intégration de capteurs multi-protocoles (Zigbee, Z-Wave, WiFi, etc.)
- Visualisation en temps réel des mesures
- Historique et analyse des données
- Déclenchement d’actions (éclairage, volets, alertes) selon scénarios
- Notifications en cas de dépassement de seuils

## Contraintes techniques
- Compatibilité multi-protocoles
- Sécurisation des données collectées
- Conservation de l’historique configurable

## Droits d’accès
- Administrateur : accès complet aux données et paramétrage
- Adultes : consultation et scénarios
- Enfants : consultation restreinte
- Invités : pas d’accès

## Liens croisés
- [README Domotique](../README.md)
- [Spécification éclairage](spec-eclairage.md)
- [Spécification volets](spec-volets.md)
- [User stories](../../user-stories/)
- [Entités](../../entites/)
- [Tests](../../../05-Tests/)
