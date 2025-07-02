# Spécification technique – Intégration Shelly

## Introduction

Cette spécification décrit l’intégration des équipements Shelly dans le système MaNoir via leurs API officielles. L’objectif est de permettre le contrôle, la supervision et l’automatisation des modules Shelly (relais, variateurs, capteurs, etc.) au sein de la plateforme domotique.

## Objectifs
- Contrôler à distance les modules Shelly (allumage, extinction, variation)
- Récupérer l’état en temps réel des équipements
- Intégrer Shelly dans les scénarios d’automatisation
- Superviser la consommation énergétique

## Fonctionnalités principales
- Découverte automatique des modules sur le réseau
- Contrôle individuel et groupé
- Programmation horaire et scénarios personnalisés
- Retour d’état et notifications d’anomalie
- Historique d’utilisation et de consommation

## Contraintes techniques
- Utilisation des API REST Shelly (authentification, sécurité)
- Gestion des versions d’API et compatibilité ascendante
- Réactivité < 1 seconde pour les actions manuelles
- Sécurisation des échanges (HTTPS)

## Droits d’accès
- Administrateur : configuration complète
- Adultes : contrôle total
- Enfants : contrôle limité à leur chambre
- Invités : contrôle dans les espaces communs

## Liens croisés
- [Spécification générale éclairage](spec-eclairage.md)
- [User stories](../../user-stories/)
- [Entités](../../entites/)
