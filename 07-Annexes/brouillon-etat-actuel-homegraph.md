# État actuel - HomeGraph existant

## Vue d'ensemble

Ce document décrit l'état actuel de la solution HomeGraph qui constitue la base du projet MaNoir. HomeGraph est une plateforme complète de domotique et d'automatisation domestique qui offre une architecture modulaire basée sur des agents spécialisés et un serveur central de gestion.

## Architecture existante

### Structure modulaire par agents

Le système actuel est organisé autour d'agents spécialisés :

#### **Home.Agents.Sarah** - Agent domotique principal
- **Responsabilité** : Gestion des appareils connectés et des scènes domotiques
- **Protocoles supportés** : Philips Hue, Shelly, Zigbee2MQTT, WLED, Samsung SmartThings, Divoom, ZipatoBox
- **Types d'appareils** : Lampes, interrupteurs, capteurs, boutons, prises, contrôleurs LED, enceintes
- **Fonctionnalités** : Scènes, groupes de scènes, déclencheurs, automatisations

#### **Home.Agents.Clara** - Agent planification et services
- **Responsabilité** : Calendriers, trajets, mails, actualités, tâches, téléchargements
- **Intégrations** : Transport.data.gouv.fr, MovieDB, RSS/Torrents
- **Services** : Planification, vérification des sources, gestion des réservations

#### **Home.Agents.Aurore** - Agent messages et communication
- **Responsabilité** : Messages, actualités, journaux, recherche, notifications
- **Intégrations** : Rhasspy (vocal), TypeSense (recherche)
- **Fonctionnalités** : Salutations, génération d'images, notifications utilisateur

#### **Home.Agents.Erza** - Agent maintenance et réseau
- **Responsabilité** : Maintenance BDD, vérifications réseau, présence, météo
- **Intégrations** : OVH (DNS), Git (synchronisation), APIs météo
- **Services** : Nettoyage système, gestion utilisateurs, intégrations sources

#### **Home.Agents.Freeia** - Agent Freebox et téléchargements
- **Responsabilité** : Intégration Freebox, téléchargements, statut réseau
- **Intégrations** : API Freebox (téléchargements, Wi-Fi, réseau)
- **Fonctionnalités** : Gestion des téléchargements, monitoring réseau

#### **Home.Agents.Gaia** - Agent déploiement et infrastructure
- **Responsabilité** : Déploiements, Kubernetes, MQTT, extensions
- **Intégrations** : Kubernetes, MQTT
- **Services** : JobRunner, déploiements système, gestion des extensions

## Fonctionnalités déjà implémentées

### 🏠 Domotique (via Agent Sarah)
✅ **Découverte automatique des appareils**
✅ **Support multi-protocoles** : Philips Hue, Shelly, Zigbee2MQTT, WLED, Samsung SmartThings, Divoom, ZipatoBox
✅ **Gestion des scènes et groupes de scènes**
✅ **Déclencheurs et automatisations**
✅ **API complète de gestion des appareils** (plus de 20 endpoints)

### 👥 Gestion des utilisateurs
✅ **Authentification multi-device** (web, mobile, IoT)
✅ **Gestion des rôles** (administrateurs, utilisateurs, invités)
✅ **Profils personnalisés** avec données custom
✅ **Détection de présence** automatique
✅ **Sessions persistantes** et tokens API

### 📱 Communications
✅ **Système de chat** avec canaux
✅ **Notifications push** (mobile et web)
✅ **Intégration vocale** via Rhasspy
✅ **Messages temps réel** entre utilisateurs et agents

### 📊 Gestion de données
✅ **Système de fichiers** hiérarchique sécurisé
✅ **Logs centralisés** avec filtrage avancé
✅ **Buckets d'information** personnalisables
✅ **Journalisation** complète des événements

### 💰 Gestion financière
✅ **Comptes bancaires multiples**
✅ **Import automatique** de relevés
✅ **Catégorisation** des transactions
✅ **Budget et suivi des dépenses**

### 🛒 Commerce et inventaire
✅ **Catalogue produits** avec codes-barres EAN
✅ **Listes de courses**
✅ **Gestion des stocks** et unités de stockage
✅ **Historique d'achats**

### 📅 Planification
✅ **Calendrier et événements**
✅ **Listes de tâches** multiples
✅ **Synchronisation** services externes
✅ **Gestion des présences** selon événements

### 🔗 Intégrations
✅ **OAuth** : Microsoft Graph, Spotify, Sonos, Twitch
✅ **APIs externes** : Plus de 200 endpoints documentés
✅ **Webhooks** entrants et sortants
✅ **Maillage réseau** multi-nœuds

## APIs existantes par domaine

### Domotique
- **DevicesController** : 15+ endpoints pour la gestion des appareils
- **SceneController** : 15+ endpoints pour les scènes et groupes
- **AutomationMeshController** : Triggers, extensions, intégrations

### Utilisateurs et sécurité
- **UsersController** : 25+ endpoints (authentification, présence, notifications, données custom)
- **ExternalTokensController** : Gestion des tokens externes
- **OAuthController** : 4 services (Microsoft, Spotify, Sonos, Twitch)

### Gestion de données
- **FilesController** : Accès sécurisé aux fichiers
- **InformationItemsController** : Buckets et éléments d'information
- **JournalController** : Pages et sections de journal

### Services applicatifs
- **TodosController** : Événements, tâches, listes
- **FinancesController** : Comptes, transactions, budget
- **ProductsController** : Produits, catégories, types
- **ShoppingController** : Courses et localisations magasins

## Architecture technique existante

### Base de données
- **MongoDB** pour le stockage principal
- **Collections** par domaine fonctionnel
- **Système d'entités** typées par agent

### Communication
- **MQTT** pour la communication inter-agents
- **HTTP/REST** pour les APIs externes
- **WebSockets** pour le temps réel
- **OAuth 2.0** pour les intégrations tierces

### Sécurité
- **Authentification** par tokens et cookies
- **Autorisation** par rôles et permissions
- **Isolation** des données par utilisateur
- **Audit** complet des actions

## Évolutions nécessaires pour MaNoir

Cette base solide permet d'identifier les évolutions à apporter :

1. **Interface utilisateur** : Nouvelle UI/UX adaptée aux profils définis
2. **Contrôles parentaux** : Système de restrictions pour les enfants
3. **Mode invité** : Accès temporaire et limité
4. **Optimisations domotique** : Amélioration des automatisations existantes
5. **Assistant intelligent** : IA pour l'apprentissage des habitudes
6. **Nouvelle architecture** : Possibles refactorisations pour simplifier

## Liens avec les spécifications MaNoir

- [Profils utilisateurs MaNoir](../user-stories/) : À adapter aux rôles existants
- [Fonctionnalités domotique](../fonctionnalites/domotique/) : Extension de l'agent Sarah
- [Architecture technique](../../03-Architecture/) : Évolution de l'existant
