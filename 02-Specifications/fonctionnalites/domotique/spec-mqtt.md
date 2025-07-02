# Spécification technique – Intégration MQTT

## Introduction

Cette spécification décrit l’intégration du protocole MQTT dans le système MaNoir. MQTT est utilisé comme bus de communication pour de nombreux équipements domotiques (Zigbee2MQTT, Shelly, W-Led, etc.) et permet l’échange d’informations en temps réel entre les différents modules de la plateforme.

## Objectifs
- Assurer la communication temps réel entre les équipements et la plateforme MaNoir
- Centraliser les échanges de données domotiques (états, commandes, alertes)
- Garantir la fiabilité et la sécurité des échanges

## Fonctionnalités principales
- Connexion à un broker MQTT local ou distant
- Publication et souscription aux topics nécessaires (états, commandes, alertes)
- Gestion des topics dynamiques pour la découverte automatique des équipements
- Support des QoS 0, 1 et 2 selon les besoins
- Reconnexion automatique en cas de coupure
- Journalisation des échanges pour audit et diagnostic

## Contraintes techniques
- Support du protocole MQTT v3.1.1 et v5
- Authentification par login/mot de passe et/ou certificat
- Chiffrement TLS pour les échanges sensibles
- Gestion fine des droits d’accès par topic
- Compatibilité avec les principaux brokers (Mosquitto, EMQX, etc.)
- Surveillance de la latence et de la disponibilité du broker

## Droits d’accès
- Administrateur : configuration complète du broker et des topics
- Adultes : accès en lecture aux topics d’état, publication sur les commandes autorisées
- Enfants : accès très restreint, lecture sur topics non critiques
- Invités : aucun accès direct

## Liens croisés
- [Spécification générale domotique](spec-eclairage.md)
- [Spécification Zigbee2MQTT](spec-zigbee.md)
- [Spécification Shelly](spec-shelly.md)
- [Spécification W-Led](spec-wled.md)
- [User stories](../../user-stories/)
- [Entités](../../entites/)
