# Structure et fonctionnalités du projet

## Structure du projet

### Dossier `Agents`
- Contient plusieurs sous-dossiers correspondant à différents agents :
  - `Home.Agents.Aurore`
  - `Home.Agents.Clara`
  - `Home.Agents.Erina`
  - `Home.Agents.Erza`
  - `Home.Agents.Freeia`
  - `Home.Agents.Gaia`
  - `Home.Agents.Sarah`

### Dossier `Common`
- Contient :
  - `Home.Common` : Composants communs.
  - `Home.Graph.Common` : Composants communs pour le graphe.

### Dossier `HomeGraph`
- Contient :
  - Dossiers :
    - `Home.Graph.Public` : Partie publique du graphe.
    - `Home.Graph.Server` : Serveur du graphe.

## Fonctionnalités

Le projet HomeGraph est une plateforme complète de domotique et d'automatisation domestique qui offre une architecture modulaire basée sur des agents spécialisés et un serveur central de gestion. Voici les principales fonctionnalités organisées par domaine :

### 🏠 **Gestion de la Maison et des Appareils**

#### **Appareils Connectés**
- **Découverte automatique** : Détection et enregistrement automatique d'appareils sur le réseau
- **Gestion multi-protocoles** : Support de Philips Hue, Shelly, Zigbee2MQTT, WLED, Samsung SmartThings, Divoom, ZipatoBox
- **Types d'appareils** : Lampes, interrupteurs, capteurs, boutons, prises, contrôleurs LED, enceintes
- **Association utilisateur** : Liaison des appareils mobiles aux utilisateurs
- **Contrôle d'état** : Surveillance et modification en temps réel des états des appareils
- **Gestion d'images** : Upload et gestion des images associées aux appareils

#### **Scènes et Automatisation**
- **Groupes de scènes** : Organisation hiérarchique des scènes par groupes
- **Exécution automatique** : Déclenchement programmé ou conditionnel des scènes
- **Gestion d'images** : Personnalisation visuelle des scènes
- **Scénarios globaux** : Gestion des modes globaux de la maison (jour, nuit, vacances, etc.)

#### **Déclencheurs et Événements**
- **Déclencheurs multiples** : Temporels, webhooks, détection de présence, changements d'état
- **Webhooks** : Points d'entrée HTTP pour intégrations externes
- **Messages personnalisés** : Envoi de messages customisés lors des déclenchements

### 👥 **Gestion des Utilisateurs et Identité**

#### **Authentification et Autorisation**
- **Connexion multi-device** : Support web, mobile et appareils IoT
- **Gestion des rôles** : Administrateurs, utilisateurs standard, invités
- **Sessions persistantes** : Cookies et tokens d'authentification longue durée
- **Sécurité API** : Clés d'API pour l'accès programmatique

#### **Profils Utilisateurs**
- **Données personnalisées** : Stockage flexible de métadonnées utilisateur
- **Centres d'intérêt** : Gestion des préférences et intérêts personnels
- **Avatars** : Upload et gestion des images de profil
- **Utilisateurs invités** : Système d'invités temporaires avec expiration automatique

#### **Présence et Localisation**
- **Détection automatique** : Suivi de la présence par géolocalisation et détection réseau
- **Localisations multiples** : Gestion de plusieurs emplacements et probabilités de présence
- **Historique d'activité** : Journalisation des activités et déplacements
- **Notifications de changement** : Alertes en temps réel des changements de présence

### 📱 **Communications et Notifications**

#### **Système de Chat**
- **Canaux multiples** : Organisation des conversations par canaux
- **Messages temps réel** : Communication instantanée entre utilisateurs et agents
- **Historique** : Récupération des messages par date et canal

#### **Notifications Push**
- **Notifications mobiles** : Push vers applications mobiles avec importance configurable
- **Notifications web** : Système de notifications dans l'interface web
- **Gestion de lecture** : Marquage automatique et manuel des notifications lues
- **Nettoyage automatique** : Suppression des anciennes notifications lues

#### **Interactions Vocales**
- **Rhasspy Integration** : Traitement des commandes vocales via Rhasspy
- **Réponses contextuelles** : Génération de réponses personnalisées selon l'utilisateur et l'appareil
- **Salutations personnalisées** : Messages d'accueil adaptés par utilisateur et contexte

### 📊 **Gestion de Données et Informations**

#### **Système de Fichiers**
- **Stockage hiérarchique** : Organisation des fichiers par type et dossiers
- **Accès sécurisé** : Contrôle d'accès aux fichiers selon les permissions utilisateur
- **Types multiples** : Support de différents types de contenu (images, documents, médias)

#### **Journalisation et Logs**
- **Logs centralisés** : Collecte et stockage des événements système
- **Filtrage avancé** : Recherche par source, période, type d'événement
- **Nettoyage automatique** : Purge des anciens logs selon la politique de rétention

#### **Informations Contextuelles**
- **Buckets d'information** : Organisation des données par catégories personnalisables
- **Éléments d'information** : Stockage et récupération de données structurées
- **Marquage et conservation** : Système de tags et de conservation des éléments importants

### 💰 **Gestion Financière**

#### **Comptes Bancaires**
- **Multi-comptes** : Gestion de plusieurs comptes bancaires
- **Import automatique** : Importation de relevés dans différents formats
- **Catégorisation** : Classification automatique et manuelle des transactions
- **Historique complet** : Suivi des transactions et soldes

#### **Budget et Dépenses**
- **Catégories personnalisées** : Création et gestion de catégories de budget
- **Suivi des dépenses** : Monitoring en temps réel des dépenses par catégorie
- **Rapports** : Génération de rapports financiers détaillés

### 🛒 **Commerce et Inventaire**

#### **Gestion des Produits**
- **Catalogue complet** : Base de données de produits avec codes-barres EAN
- **Catégorisation** : Organisation par catégories et types de produits
- **Recherche avancée** : Recherche textuelle et par attributs
- **Images** : Gestion des images produits

#### **Achats et Shopping**
- **Listes de courses** : Création et gestion de listes d'achats
- **Localisations magasins** : Gestion des magasins et emplacements d'achat
- **Historique d'achats** : Suivi des achats et habitudes de consommation

#### **Stock et Stockage**
- **Unités de stockage** : Gestion des espaces de rangement (armoires, étagères, etc.)
- **Suivi des stocks** : Monitoring des quantités et emplacements
- **Unités de mesure** : Système flexible d'unités de mesure

### 🍽️ **Cuisine et Repas**

#### **Recettes et Cuisine**
- **Base de recettes** : Stockage et organisation de recettes personnalisées
- **Catégories culinaires** : Classification par type de cuisine et catégorie
- **Planification des repas** : Organisation des menus et repas

### 📅 **Planification et Tâches**

#### **Calendrier et Événements**
- **Événements multiples** : Gestion de différents types d'événements
- **Sources externes** : Synchronisation avec des services de calendrier externes
- **Présence intégrée** : Mise à jour automatique de la présence selon les événements
- **Nettoyage automatique** : Suppression des événements passés

#### **Listes de Tâches**
- **Listes multiples** : Organisation par listes personnalisées et maillage
- **Statuts avancés** : Suivi détaillé de l'état des tâches
- **Synchronisation** : Support de sources externes de tâches
- **Opérations en lot** : Modification multiple de tâches

### 🔗 **Intégrations et Connectivité**

#### **OAuth et Services Externes**
- **Microsoft Graph** : Intégration complète avec l'écosystème Microsoft
- **Spotify** : Contrôle de la musique et des playlists
- **Sonos** : Gestion des systèmes audio multiroom
- **Twitch** : Intégration avec les diffusions en direct

#### **Maillage et Réseau**
- **Gestion de maillage** : Coordination de plusieurs nœuds du système
- **Extensions** : Système de plugins pour étendre les fonctionnalités
- **Intégrations agent** : Connecteurs vers différents agents spécialisés
- **Monitoring réseau** : Surveillance de la connectivité et performance

#### **APIs et Webhooks**
- **API REST complète** : Plus de 200 endpoints documentés
- **Webhooks entrants** : Points d'entrée pour intégrations externes
- **Tokens sécurisés** : Gestion des tokens d'accès pour services externes

### 📥 **Téléchargements et Médias**

#### **Gestion des Téléchargements**
- **File d'attente** : Système de queue pour les téléchargements
- **Suivi d'état** : Monitoring des téléchargements en cours et terminés
- **Liens intelligents** : Association automatique avec du contenu existant
- **Nettoyage** : Gestion du cycle de vie des téléchargements

### 🏗️ **Infrastructure et Administration**

#### **Circuits et Équipements**
- **Circuits électriques** : Gestion des circuits électriques de la maison
- **Monitoring** : Surveillance de l'état des équipements

#### **Localisation et Géographie**
- **Emplacements multiples** : Gestion de différents lieux et bâtiments
- **Météo locale** : Intégration des données météorologiques
- **Dangers météo** : Alertes et notifications des conditions dangereuses

#### **Sécurité et Confidentialité**
- **Mode privé** : Activation/désactivation du mode confidentialité
- **Contrôle d'accès** : Gestion fine des permissions par utilisateur et rôle
- **Audit complet** : Traçabilité de toutes les actions utilisateur

### Agents
Les agents semblent être des modules ou services distincts, chacun ayant des fonctionnalités spécifiques. Par exemple :
- `Home.Agents.Aurore` : Gestion des messages et des actualités.
  - Gestion des messages spécifiques à Aurore via `AuroreMessageHandler`.
  - Service de gestion des actualités via `AuroreNewsItemService`.
  - Aide pour la gestion des journaux via `JournalHelper`.
  - Aide pour la gestion de la parole via `SpeechHelper`.
  - Gestion des salutations via le dossier `Greetings`.
  - Générateurs d'images via le dossier `ImageGenerators`.
  - Notifications utilisateur via le dossier `UserNotifications`.
  - Fonctionnalités de recherche via le dossier `Search`.
  - Intégrations diverses via le dossier `Integrations`.
- `Home.Agents.Clara` : 
  - Gestion des calendriers via le dossier `Calendars`.
  - Gestion des trajets via le dossier `Commute`.
  - Services domestiques via le dossier `HomeServices`.
  - Gestion des mails via `MailServiceThread` et le dossier `Mails`.
  - Vérification des actualités via `NewsChecker` et le dossier `NewsItems`.
  - Gestion des tâches de planification via `MainScheduleThread` et `PimSchedulerThread`.
  - Aide pour les vidéos et les téléchargements via `VideoAndDownloadsHelper`.
  - Intégrations SaaS via le dossier `SaaS`.
  - Gestion des tâches via le dossier `Todos`.
  - Vérification des sources de téléchargement via `DownloadSourceChecker` et ses variantes.
  - Gestion des messages spécifiques à Clara via `ClaraMessageHandler`.
- `Home.Agents.Erina` : Gestion des messages.
- `Home.Agents.Erza` : Maintenance de la base de données et vérifications réseau.
  - Gestion de la maintenance de la base de données via `DatabaseMaintenanceThread`.
  - Fournisseur d'intégrations via `ErzaIntegrationsProvider`.
  - Gestion des messages spécifiques à Erza via `ErzaMessageHandler`.
  - Aide pour la gestion des réseaux maillés via `MeshHelper`.
  - Vérifications réseau via `NetworkChecker` et ses variantes.
  - Gestion de la présence via `PresenceHelper` et ses sous-modules.
  - Nettoyage système via `SystemCleanup`.
  - Aide pour la gestion des utilisateurs via `UserHelper`.
  - Intégrations des sources via le dossier `SourceIntegration`.
  - Fournisseurs de données météo via le dossier `WeatherProviders`.
- `Home.Agents.Freeia` : 
  - Gestion des téléchargements via `DownloadHelper`.
  - Intégration avec Freebox pour les téléchargements, outils réseau, statut et Wi-Fi via `FreeboxHelper` et ses sous-modules.
  - Gestion des messages spécifiques à Freeia via `FreeiaMessageHandler`.
- `Home.Agents.Gaia`
  - Aide pour les déploiements via `DeploymentHelper`.
  - Gestion des téléchargements via `DownloadHelper`.
  - Gestion des messages spécifiques à Gaia via `GaiaMessageHandler`.
  - Aide pour l'exécution des tâches via `JobRunnerHelper`.
  - Vérification des configurations Kubernetes via `KubernetesChecker`.
  - Gestion des communications MQTT via `MqttHandler`.
- `Home.Agents.Sarah`
  - Gestion des appareils via `DeviceManager` et ses sous-modules.
    - Protocoles domotiques pris en charge : Philips Hue, Shelly, Zigbee2MQTT, WLED, Samsung SmartThings, Divoom, ZipatoBox.
    - Types de devices gérés : lampes, interrupteurs, capteurs de température, boutons, prises connectées, contrôleurs LED, enceintes connectées, et autres appareils domotiques.
  - Nettoyage pour l'automatisation domestique via `HomeAutomationCleanup`.
  - Gestion des scènes via le dossier `Scenes`.
  - Vérification des déclencheurs via `TriggersChecker`.
  - Gestion des messages spécifiques à Sarah via `SarahMessageHandler`.
  - Fournisseur d'intégrations via `SarahIntegrationsProvider`.

### Common
- Fournit des composants réutilisables pour les agents et le graphe.

### HomeGraph
- Implémente un graphe pour la gestion des données et des interactions.

## Points API pour AutomationMeshController-Apps.cs

- Aucun point API détecté dans ce fichier.

## Points API pour AutomationMeshController-Extensions.cs

- **GET** `/local/extensions` : Récupère la liste des extensions.
- **POST** `/local/extensions` : Ajoute ou met à jour une extension.
- **GET** `/local/extensions/{extensionId}` : Récupère une extension spécifique.
- **GET** `/local/extensions/{extensionId}/restart` : Redémarre une extension spécifique.
- **GET** `/local/extensions/{extensionId}/install` : Installe une extension spécifique.
- **GET** `/local/extensions/{extensionId}/uninstall` : Désinstalle une extension spécifique.
- **GET** `/local/extensions/{extensionId}/setinstalled` : Met à jour le statut d'installation d'une extension.
- **DELETE** `/local/extensions/{extensionId}` : Supprime une extension spécifique.

## Points API pour AutomationMeshController-General.cs

- **GET** `/{name}/location` : Récupère la localisation d'un maillage.
- **POST** `/{name}/location` : Définit la localisation d'un maillage.
- **GET** `/{name}/location/set/{locationId}` : Définit la localisation d'un maillage par ID.
- **GET** `/settings/available/language` : Récupère les langues disponibles.
- **GET** `/settings/available/timezone` : Récupère les fuseaux horaires disponibles.
- **POST** `/{name}/settings` : Définit les paramètres d'un maillage.
- **GET** `/local/graph/version` : Récupère la version du graphe.
- **GET** `/local/graph/check` : Vérifie l'existence du graphe.
- **GET** `/local/privacymode/set` : Définit le mode de confidentialité.
- **GET** `/local/privacymode/clear` : Efface le mode de confidentialité.
- **GET** `/local/privacymode/isenabled` : Vérifie si le mode de confidentialité est activé.
- **GET** `/local/globalscenario/all` : Récupère tous les scénarios globaux.
- **POST** `/local/globalscenario/all` : Ajoute ou met à jour un scénario global.
- **DELETE** `/local/globalscenario/all/{code}` : Supprime un scénario global.
- **POST** `/local/globalscenario/all/{code}/images/{imagecode}` : Ajoute ou met à jour une image de scénario global.
- **DELETE** `/local/globalscenario/all/{code}/images/{imagecode}` : Supprime une image de scénario global.
- **GET** `/local/globalscenario/all/{code}` : Récupère un scénario global spécifique.
- **GET** `/local/globalscenario/current` : Récupère le scénario global actuel.
- **POST** `/local/globalscenario/current` : Définit le scénario global actuel.
- **DELETE** `/local/globalscenario/current` : Efface le scénario global actuel.
- **GET** `/local/globalscenario/current/clear` : Efface le scénario global actuel.

## Points API pour AgentsController.cs

- **POST** `/v1.0/agents/all/send/{topic}` : Envoie un message à tous les agents.
- **GET** `/v1.0/agents/{agent}` : Récupère les informations d'un agent spécifique.
- **GET** `/v1.0/agents/{agentName}/restart` : Redémarre un agent spécifique.
- **GET** `/v1.0/agents/{agent}/ping` : Envoie un ping à un agent spécifique.
- **POST** `/v1.0/agents/{agent}/status` : Met à jour le statut d'un agent.
- **POST** `/v1.0/agents/{agent}/configuration` : Met à jour la configuration d'un agent.
- **GET** `/v1.0/agents/all` : Récupère la liste des agents locaux.
- **GET** `/v1.0/agents/all/clearobsolete` : Supprime les agents obsolètes.

## Points API pour AutomationMeshController-Integrations.cs

- **GET** `/local/integrations` : Récupère la liste des intégrations.
- **GET** `/local/integrations/byagent/{agentId}` : Récupère les intégrations d'un agent spécifique.
- **POST** `/local/integrations` : Ajoute ou met à jour une intégration.
- **POST** `/local/integrations/raw` : Ajoute ou met à jour une intégration brute.
- **GET** `/local/integrations/{integrationId}` : Récupère une intégration spécifique.
- **GET** `/local/integrations/{integrationId}/config` : Configure une intégration.
- **GET** `/local/integrations/{integrationId}/config/{instanceId}` : Récupère la configuration d'une instance d'intégration.
- **POST** `/local/integrations/{integrationId}/config/{instanceId}` : Configure une instance d'intégration.

## Points API pour AutomationMeshController-Internet.cs

- **GET** `/local/internet-connections` : Récupère les connexions Internet locales.
- **POST** `/local/internet-connections` : Met à jour une connexion Internet locale avec les informations fournies.

## Points API pour AutomationMeshController-LocationInfo.cs

- **POST** `/local/location/infos/weatherhazard` : Définit les dangers météorologiques pour une localisation.
- **POST** `/local/location/infos/weather` : Définit les informations météorologiques pour une localisation.

## Points API pour AutomationMeshController-Logs.cs

- **GET** `/local/logs` : Récupère les logs locaux avec des paramètres optionnels (source, sourceId, durée, nombre maximal).

## Points API pour AutomationMeshController-Triggers.cs

- **GET** `/local/triggers` : Récupère la liste des déclencheurs.
- **POST** `/local/triggers` : Ajoute ou met à jour un déclencheur.
- **GET** `/local/triggers/{triggerId}` : Récupère un déclencheur spécifique.
- **GET** `/local/triggers/{triggerId}/settings` : Définit les paramètres d'un déclencheur spécifique.
- **GET** `/local/triggers/{triggerId}/raise` : Déclenche un événement pour un déclencheur spécifique.
- **POST** `/local/triggers/{triggerId}/raise` : Déclenche un événement pour un déclencheur spécifique.
- **DELETE** `/local/triggers/{triggerId}` : Supprime un déclencheur spécifique.

## Points API pour AutomationMeshController.cs

- **POST** `/local/source-code-integration` : Associe un code source à un maillage local.
- **GET** `/local/associate-account/{accountGuid}` : Associe un compte Manoir App à un maillage local.
- **GET** `/local/interactions/greetings/general` : Récupère les salutations générales.
- **GET** `/{name}` : Récupère les informations d'un maillage spécifique.
- **GET** `/local/agents` : Récupère la liste des agents locaux.
- **POST** `/local/agents/register` : Enregistre un agent local.

## Points API pour ChatController.cs

- **POST** `/v1.0/chat/messages/{channelId}` : Envoie un message dans un canal spécifique.
- **GET** `/v1.0/chat/messages/{channelId}` : Récupère les messages d'un canal spécifique depuis une date donnée.
- **GET** `/v1.0/chat/channels` : Récupère la liste des canaux de chat.
- **GET** `/v1.0/chat/channels/{channelId}` : Récupère les informations d'un canal spécifique.
- **POST** `/v1.0/chat/channels` : Ajoute ou met à jour un canal de chat.
- **DELETE** `/v1.0/chat/channels/{channelId}` : Supprime un canal de chat spécifique.

## Points API pour DataRedirectionController.cs
- **GET** `/data/{entityType}/{entityId}` : Redirection vers une URL basée sur le type et l'identifiant de l'entité.
- **GET** `/products/container/{entityId}` : Redirection vers une URL pour un conteneur spécifique.

## Entités spécifiques aux agents

Les entités suivantes sont spécifiques aux traitements des agents et incluent des données provenant d'APIs externes ou des modules particuliers :

#### `Home.Agents.Aurore`

##### Entités communes

- **TodoItem** : Événements et tâches planifiées.
- **HomeStatusItem** : Éléments de statut pour le maillage global.

##### Entités spécifiques aux APIs externes

- **RhasspyService** : Gestion des phrases et commandes vocales.
- **TypeSenseSearchProvider** : Synchronisation des produits avec TypeSense.
- **UserChangeNotificationHandler** : Gestion des notifications liées aux utilisateurs.

#### `Home.Agents.Clara`

##### Entités communes

- **ClaraNewsSource** : Sources d'actualités configurées pour les utilisateurs.
- **RssTorrentSource** : Sources de torrents RSS.
- **HomeServicesConfig** : Configuration des services domestiques.

##### Entités spécifiques aux APIs externes

- **TransportDataGouvFrProvider** : Intégration avec les données de transport.
- **MovieDbSearchResult** : Résultats de recherche de films via MovieDB.
- **Reservation** : Gestion des réservations (train, avion, hôtel, etc.).

#### `Home.Agents.Freeia`

##### Entités communes

- **DeviceStatus** : Statut des appareils connectés.
- **Trigger** : Déclencheurs liés aux événements réseau.
- **NetworkDeviceData** : Données des appareils réseau.

##### Entités spécifiques aux APIs externes

- **ApiVersion** : Informations sur l'API Freebox.
- **LoginAppRequest** et **LoginAppResponse** : Gestion des sessions d'authentification avec la Freebox.
- **DownloadStatusResponse** : Statut des téléchargements.
- **ApNeighborsResult** : Informations sur les réseaux Wi-Fi voisins.

#### `Home.Agents.Erza`

##### Entités communes

- `LogData` : Gestion des logs (nettoyage des anciens logs).
- `User` : Gestion des utilisateurs, y compris les invités.
- `PresenceActivityData` : Activités de présence des utilisateurs.
- `PresenceUpdateData` : Mise à jour des données de présence.
- `Integration` : Intégrations actives et disponibles.
- `IntegrationInstance` : Instances des intégrations.

##### Entités spécifiques aux APIs externes

- `OvhApi` : Intégration avec OVH pour la gestion des DNS et des enregistrements.
- `CreateRecordRequest` : Requête pour créer un enregistrement DNS.
- `UpdateRecordRequest` : Requête pour mettre à jour un enregistrement DNS.
- `ConsumerKeyResult` : Résultat de la clé consommateur pour l'authentification OVH.
- `GitSync` : Synchronisation des configurations et automatisations avec un dépôt Git.
- `WeatherIntegration` : Intégration pour récupérer les informations météorologiques.

#### `Home.Agents.Gaia`

##### Entités communes

- `MeshExtension` : Extensions du maillage local.
- `Agent` : Agents locaux et leurs configurations.
- `Device` : Appareils enregistrés dans le maillage.

##### Entités spécifiques aux APIs externes

- `KubernetesClientConfiguration` : Configuration pour les interactions avec Kubernetes.
- `V1Deployment` : Déploiements Kubernetes.
- `V1Service` : Services Kubernetes.
- `V1Ingress` : Ingress Kubernetes.
- `DownloadItemMessage` : Messages pour la gestion des téléchargements.
- `SystemDeploymentMessage` : Messages pour les actions de déploiement système.

### Entités manipulées par Home.Agents.Sarah

#### Entités communes (MongoDB)
- `Device`
- `Scene`
- `SceneGroup`
- `SceneStep`
- `Integration`
- `IntegrationInstance`
- `DeviceStateChangedMessage`
- `ExecuteScenarioHomeAutomationMessage`

#### Entités spécifiques aux API externes
- `HueDeviceBase` (Philips Hue)
- `ShellyDeviceBase` (Shelly)
- `Z2MqttDeviceBase` (Zigbee2MQTT)
- `WledDeviceBase` (WLED)
- `SmartThingsDeviceBase` (Samsung SmartThings)
- `DivoomDeviceBase` (Divoom)
- `ZipatoDeviceBase` (ZipatoBox)

## Points API pour DevicesController-DeviceManagement.cs
- **POST** `/register/{agentId}` : Enregistre des appareils pour un agent spécifique.
- **GET** `/find` : Recherche des appareils selon des critères (agentId, type, rôle, etc.).
- **GET** `/all/{deviceId}` : Récupère les informations d'un appareil par son ID.
- **DELETE** `/all/{deviceId}/images/{imagecode}` : Supprime une image associée à un appareil.
- **PATCH** `/all/{deviceId}/status` : Met à jour les données et le statut d'un appareil.
- **POST** `/all/{deviceId}/status/data` : Modifie les données d'un appareil.
- **GET** `/all/{deviceId}/status/data` : Récupère les données d'un appareil.
- **POST** `/all/{deviceId}/images/{imagecode}` : Ajoute ou met à jour une image associée à un appareil.

## Points API pour DevicesController-Discovery.cs
- **GET** `/discovered` : Récupère les appareils découverts selon des critères (type, agent).
- **GET** `/discovered/clearolds` : Supprime les anciens appareils découverts.
- **GET** `/discovery/enable` : Active le mode découverte via une requête GET.
- **POST** `/discovery/enabled` : Active le mode découverte.
- **GET** `/discovery/enabled` : Vérifie si le mode découverte est activé.

## Points API pour DevicesController-mobiledevices.cs

- **POST** `/all/{deviceId}/change-app` : Modifie l'application associée à un appareil mobile.
- **POST** `/all/{deviceId}/force-refresh` : Force la mise à jour des données d'un appareil mobile.
- **GET** `/all/{deviceId}/force-refresh` : Récupère le statut de la mise à jour forcée d'un appareil mobile.

## Points API pour DevicesController-self-DirectInteractions.cs

- **GET** /self/interactions/greetings : Récupère les salutations pour les interactions directes.

## Points API pour DevicesController-self.cs

- **POST** /self/associatedUser
- **DELETE** /self/associatedUser
- **PATCH** /self/status
- **GET** /self

## Points API pour DevicesController.cs

- Aucun point API détecté dans ce fichier.

## Points API pour DownloadsController.cs
- **POST** `/v1.0/downloads` : Crée un nouvel enregistrement de téléchargement.
- **GET** `/v1.0/downloads/find/byprivateId` : Récupère un téléchargement par son identifiant privé.
- **GET** `/v1.0/downloads/{status}` : Récupère les téléchargements par statut.
- **GET** `/v1.0/downloads/all` : Récupère tous les téléchargements.
- **GET** `/v1.0/downloads/{id}/linked` : Récupère les éléments liés à un téléchargement.
- **POST** `/v1.0/downloads/{id}/linkTo/{linkedItemId}` : Lie un élément à un téléchargement.
- **POST** `/v1.0/downloads/{id}/queue` : Ajoute un téléchargement à la file d'attente.
- **POST** `/v1.0/downloads/all/clear` : Efface tous les téléchargements.
- **POST** `/v1.0/downloads/all/abandon/byids` : Abandonne plusieurs téléchargements par leurs identifiants.
- **POST** `/v1.0/downloads/{id}/abandon` : Abandonne un téléchargement.
- **POST** `/v1.0/downloads/{id}/markascompleted` : Marque un téléchargement comme terminé.
- **POST** `/v1.0/downloads/{id}/markascompleted` avec fichiers : Termine un téléchargement et gère les fichiers associés.

## Points API pour EntitiesController-BasicOperations.cs
- **GET** `/v1.0/entities/weather`
- **GET** `/v1.0/entities/devices`
- **GET** `/v1.0/entities/all`
- **POST** `/v1.0/entities/all`
- **DELETE** `/v1.0/entities/all/{entityId}`
- **GET** `/v1.0/entities/all/{entityId}`

## Points API pour EntitiesController.cs
- Aucun point API détecté dans ce fichier.

## Points API pour ExternalTokensController.cs
- **GET** /v1.0/security/tokens/self/foradmin
- **GET** /v1.0/security/tokens/all
- **GET** /v1.0/security/tokens/{user}/{type}
- **PUT** /v1.0/security/tokens/{user}/{type}
- **DELETE** /v1.0/security/tokens/{user}/{type}

## Points API pour FilesController.cs
- **GET** `/v1.0/services/files/{type}/{folder}/{folder2}/{folder3}/{folder4}/{file}`
- **GET** `/v1.0/services/files/{type}/{folder}/{folder2}/{folder3}/{file}`
- **GET** `/v1.0/services/files/{type}/{folder}/{folder2}/{file}`
- **GET** `/v1.0/services/files/{type}/{folder}/{file}`

## Points API pour FinancesController-BankAccounts.cs
- **GET** `/v1.0/finances/bank/accounts` : Récupère la liste des comptes bancaires.
- **GET** `/v1.0/finances/bank/accounts/{accountId}` : Récupère les détails d'un compte bancaire spécifique.
- **POST** `/v1.0/finances/bank/accounts` : Crée un nouveau compte bancaire.
- **DELETE** `/v1.0/finances/bank/accounts/{accountId}` : Supprime un compte bancaire spécifique.

## Points API pour FinancesController-BankRecords.cs
- **GET** `/v1.0/finances/bank/records`
- **POST** `/v1.0/finances/bank/records`
- **POST** `/v1.0/finances/bank/records/upload/{format}/content`
- **POST** `/v1.0/finances/bank/records/upload/{format}`
- **GET** `/v1.0/finances/bank/records/{recordId}/categorize/{categoryId}`

## Points API pour FinancesController-BankRecordsParsing.cs
- Aucun point API détecté dans ce fichier.

## Points API pour FinancesController-Budget.cs
- **GET** `/categories` : Récupère toutes les catégories de budget.
- **POST** `/categories` : Ajoute ou met à jour une catégorie de budget.
- **DELETE** `/categories/{categoryId}` : Supprime une catégorie de budget et met à jour les enregistrements associés.

## Points API pour FinancesController.cs
- Aucun point API détecté dans ce fichier.

## Points API pour GlobalSettingsController-Units.cs
- **GET** `/units` : Récupère la liste des unités de mesure.
- **GET** `/units/{unitId}` : Récupère une unité de mesure spécifique par son ID.
- **POST** `/units` : Ajoute ou met à jour une unité de mesure.
- **DELETE** `/units/{unitId}` : Supprime une unité de mesure spécifique.

## Points API pour GlobalSettingsController.cs
- Aucun point API détecté dans ce fichier.

## Points API pour GraphToolsController.cs
- **GET** `/v1.0/graphserver/commands/search` : Recherche de commandes avec un préfixe optionnel.

## Points API pour HomeCircuitController.cs
- **GET** `/v1.0/home/circuits` : Récupère la liste des circuits domestiques.
- **GET** `/v1.0/home/circuits/{circuitId}` : Récupère un circuit domestique spécifique par son ID.
- **POST** `/v1.0/home/circuits` : Ajoute ou met à jour un circuit domestique.
- **DELETE** `/v1.0/home/circuits/{circuitId}` : Supprime un circuit domestique spécifique par son ID.

## Points API pour InformationItemsController-Buckets.cs
- **GET** `/v1.0/home/circuits/{user}/buckets` : Récupère les buckets d'un utilisateur.
- **POST** `/v1.0/home/circuits/{user}/buckets` : Ajoute ou met à jour un bucket pour un utilisateur.
- **DELETE** `/v1.0/home/circuits/{user}/buckets/{bucketId}` : Supprime un bucket spécifique pour un utilisateur.
- **POST** `/v1.0/home/circuits/{user}/buckets/{bucketId}/clear` : Efface les éléments d'un bucket spécifique pour un utilisateur.

## Points API pour InformationItemsController-Items.cs
- **GET** `/v1.0/home/circuits/{user}/items` : Récupère les éléments d'information pour un utilisateur avec des filtres optionnels.
- **POST** `/v1.0/home/circuits/{user}/items` : Ajoute ou met à jour des éléments d'information pour un utilisateur.
- **GET** `/v1.0/home/circuits/{user}/items/{id}/read` : Marque un élément comme lu.
- **GET** `/v1.0/home/circuits/{user}/items/{id}/keep` : Marque un élément comme conservé.

## Points API pour InformationItemsController.cs
- Route : `v1.0/pim/informations`
- Méthodes HTTP : Aucun point API détecté.

## Points API pour JournalController-PagesAndSections.cs
- **GET** `/pages` : Récupère la liste des pages.
- **GET** `/pages/{pageId}` : Récupère une page spécifique par son ID.
- **GET** `/find/pages` : Récupère une page par son chemin et l'ID utilisateur.

## Points API pour JournalController-Properties.cs
- **POST** `/sections/{sectionId}/properties` : Met à jour les propriétés d'une section spécifique.

## Points API pour JournalController.cs
- Aucun point API détecté dans ce fichier.

## Points API pour LocationsController.cs
- **GET** `/v1.0/locations` : Récupère toutes les localisations.
- **GET** `/v1.0/locations/{id}` : Récupère une localisation spécifique par son ID.
- **POST** `/v1.0/locations` : Met à jour une localisation.

## Points API pour MealsController-RecipesCategories.cs

- **GET** `/recipes/categories` : Récupère toutes les catégories de recettes.
- **POST** `/recipes/categories` : Ajoute ou met à jour une catégorie de recette.
- **DELETE** `/recipes/categories/{categoryId}` : Supprime une catégorie de recette et met à jour les enregistrements associés.

## Points API pour MealsController-RecipesCuisines.cs

- **GET** `/recipes/cuisines` : Récupère toutes les cuisines de recettes.
- **GET** `/recipes/cuisines/{accountId}` : Récupère une cuisine de recette spécifique par son ID.
- **POST** `/recipes/cuisines` : Ajoute ou met à jour une cuisine de recette.
- **DELETE** `/recipes/cuisines/{accountId}` : Supprime une cuisine de recette et met à jour les recettes associées.

## Points API pour MealsController.cs

- Route : `v1.0/meals`
- Méthodes HTTP : Aucun point API détecté dans ce fichier.

## Points API pour OAuthController-Microsoft.cs

- **GET** `/microsoft/geturl` : Récupère l'URL d'autorisation Microsoft OAuth (Graph API ou Azure Management).
- **GET** `/microsoft/return` : Gère le retour d'autorisation Microsoft OAuth et échange le code d'autorisation contre un token.
- **GET** `/microsoft/token/me` : Récupère le token d'accès Microsoft de l'utilisateur connecté.
- **GET** `/microsoft/token/{user}` : Récupère le token d'accès Microsoft pour un utilisateur spécifique.

## Points API pour OAuthController-Sonos.cs

- **GET** `/sonos/geturl` : Récupère l'URL d'autorisation Sonos OAuth pour le contrôle de lecture.
- **GET** `/sonos/return` : Gère le retour d'autorisation Sonos OAuth et échange le code d'autorisation contre un token.
- **GET** `/sonos/token/me` : Récupère le token d'accès Sonos de l'utilisateur connecté.
- **GET** `/sonos/token/{user}` : Récupère le token d'accès Sonos pour un utilisateur spécifique.

## Points API pour OAuthController-Spotify.cs

- **GET** `/spotify/geturl` : Récupère l'URL d'autorisation Spotify OAuth avec des scopes complets (lecture, modification, playlists).
- **GET** `/spotify/return` : Gère le retour d'autorisation Spotify OAuth et échange le code d'autorisation contre un token.
- **GET** `/spotify/token/me` : Récupère le token d'accès Spotify de l'utilisateur connecté.
- **GET** `/spotify/token/{user}` : Récupère le token d'accès Spotify pour un utilisateur spécifique.

## Points API pour OAuthController-Twitch.cs

- **GET** `/twitch/geturl` : Récupère l'URL d'autorisation Twitch OAuth pour la lecture et modification des diffusions.
- **GET** `/twitch/return` : Gère le retour d'autorisation Twitch OAuth et échange le code d'autorisation contre un token.
- **GET** `/twitch/token/me` : Récupère le token d'accès Twitch de l'utilisateur connecté.
- **GET** `/twitch/token/{user}` : Récupère le token d'accès Twitch pour un utilisateur spécifique.

## Points API pour OAuthController.cs

- Route : `oauth`
- Méthodes HTTP : Aucun point API détecté dans ce fichier.

## Points API pour ProductsController-ProductCategories.cs

- **GET** `/categories` : Récupère toutes les catégories de produits.
- **GET** `/categories/{categoryId}` : Récupère une catégorie de produit spécifique par son ID.
- **POST** `/categories` : Ajoute ou met à jour une catégorie de produit.
- **DELETE** `/categories/{categoryId}` : Supprime une catégorie de produit avec vérification des dépendances.

## Points API pour ProductsController-Products.cs

- **GET** `/get/{productId}` : Récupère un produit spécifique par son ID.
- **GET** `/find/all` : Récupère tous les produits avec pagination (page et pageSize optionnels).
- **GET** `/find/ean/{ean}` : Recherche un produit par son code-barres EAN.
- **GET** `/find/category/{categoryId}` : Récupère les produits d'une catégorie spécifique avec pagination.
- **POST** `/find/label` : Recherche de produits par texte de libellé (recherche textuelle).
- **POST** `` : Ajoute ou met à jour un produit (upsert).
- **DELETE** `/{productId}` : Supprime un produit spécifique par son ID.

## Points API pour ProductsController-ProductTypes.cs

- **GET** `/types` : Récupère tous les types de produits.
- **GET** `/types/{typeId}` : Récupère un type de produit spécifique par son ID.
- **POST** `/types` : Ajoute ou met à jour un type de produit.
- **DELETE** `/types/{typeId}` : Supprime un type de produit avec vérification des dépendances.

## Points API pour ProductsController.cs

- Route : `v1.0/products`
- Méthodes HTTP : Aucun point API détecté dans ce fichier - classe de base partielle uniquement.

## Points API pour RhasspyController.cs

- **POST** `/{id}/intent/handle` : Traite une intention vocale Rhasspy et retourne une réponse appropriée.

## Points API pour SceneController.cs

- **GET** `/groups` : Récupère tous les groupes de scènes.
- **GET** `/groups/{id}` : Récupère un groupe de scènes spécifique par son ID.
- **POST** `/groups/{id}/activeScenes` : Met à jour les scènes actives pour un groupe.
- **DELETE** `/groups/{id}/activeScenes` : Supprime une scène active d'un groupe.
- **GET** `/clearall` : Supprime tous les groupes et scènes.
- **DELETE** `/groups/{groupId}` : Supprime un groupe de scènes et toutes ses scènes.
- **POST** `/groups` : Ajoute ou met à jour un groupe de scènes.
- **GET** `/groups/{groupid}/scenes` : Récupère les scènes d'un groupe spécifique.
- **GET** `/scenes` : Récupère toutes les scènes.
- **GET** `/execute/{id}` : Exécute une scène spécifique.
- **GET** `/scenes/{id}` : Récupère une scène spécifique par son ID.
- **POST** `/scenes` : Ajoute ou met à jour une scène.
- **DELETE** `/scene/{id}` : Supprime une scène spécifique.
- **DELETE** `/scene/{id}/images/{imagecode}` ou `/scenes/{id}/images/{imagecode}` : Supprime une image associée à une scène.
- **POST** `/scene/{id}/images/{imagecode}` ou `/scenes/{id}/images/{imagecode}` : Ajoute ou met à jour une image associée à une scène.

## Points API pour SchedulerController.cs

- **GET** `/wakeuptime/next` : Récupère les heures de réveil programmées pour tous les utilisateurs principaux.
- **POST** `/wakeuptime/next` : Définit l'heure de réveil pour un utilisateur spécifique.

## Points API pour ShoppingController-Items.cs

- Aucun point API détecté dans ce fichier.

## Points API pour ShoppingController-Locations.cs

- **GET** `/locations` : Récupère toutes les localisations de magasins.
- **GET** `/locations/{locationId}` : Récupère une localisation de magasin spécifique par son ID.
- **POST** `/locations` : Ajoute ou met à jour une localisation de magasin.
- **DELETE** `/locations/{locationId}` : Supprime une localisation de magasin avec vérification des dépendances.

## Points API pour ShoppingController.cs

- Route : `v1.0/shopping`
- Méthodes HTTP : Aucun point API détecté dans ce fichier - classe de base partielle uniquement.

## Points API pour StockController-StorageUnits.cs

- **GET** `/storageUnits` : Récupère toutes les unités de stockage.
- **GET** `/storageUnits/{storageUnitId}` : Récupère une unité de stockage spécifique par son ID.
- **POST** `/storageUnits` : Ajoute ou met à jour une unité de stockage.
- **DELETE** `/storageUnits/{storageUnitId}` : Supprime une unité de stockage avec vérification des dépendances.

## Points API pour StockController.cs

- Route : `v1.0/stock`
- Méthodes HTTP : Aucun point API détecté dans ce fichier - classe de base partielle uniquement.

## Points API pour StorageController-StorageUnits.cs

- **GET** `/storageunits` : Récupère toutes les unités de stockage (avec filtre optionnel par roomId).
- **GET** `/storageunits/{unitId}` : Récupère une unité de stockage spécifique par son ID.
- **POST** `/storageunits` : Ajoute ou met à jour une unité de stockage.
- **DELETE** `/storageunits/{unitId}` : Supprime une unité de stockage spécifique.

## Points API pour StorageController.cs

- Route : `v1.0/storage`
- Méthodes HTTP : Aucun point API détecté dans ce fichier - classe de base partielle uniquement.

## Points API pour TestsController.cs

- **GET** `/greetings/{userName}` : Récupère les salutations pour un utilisateur spécifique (pour tests).

## Points API pour TodosController-Event.cs

- **GET** `/events/fromScheduleSource/{sourceId}` : Récupère les événements d'une source de planification spécifique.
- **DELETE** `/events/{eventId}` : Supprime un événement spécifique.
- **GET** `/events/{eventId}/start` : Démarre un événement avec mise à jour de présence optionnelle.
- **GET** `/events/{eventId}/end` : Termine un événement avec mise à jour de présence.
- **GET** `/events` : Récupère les événements avec filtres (utilisateur, liste, service de sync, jours, statut).
- **GET** `/events/mesh` : Récupère les événements du maillage avec filtres similaires.
- **GET** `/events/clearInPast` : Supprime les événements passés (plus de 30 jours).
- **GET** `/events/temp` : Supprime les événements temporaires spécifiques (ménage sans planification).

## Points API pour TodosController-Items.cs

- **GET** `/todoItems` : Récupère les tâches TODO avec filtres (utilisateur, liste, service de sync, jours, statut).
- **GET** `/todoItems/mesh` : Récupère les tâches TODO du maillage avec filtres similaires.
- **POST** `/all` : Ajoute ou met à jour une tâche TODO.
- **POST** `/all/bulk` : Ajoute ou met à jour plusieurs tâches TODO en lot.
- **DELETE** `/todoItems/{itemId}` : Supprime une tâche TODO spécifique.
- **GET** `/todoItems/{itemId}/markasdone` : Marque une tâche TODO comme terminée.
- **GET** `/todoItems/markasdone` : Marque plusieurs tâches TODO comme terminées.

## Points API pour TodosController-List.cs

- **GET** `/lists` : Récupère les listes TODO de l'utilisateur connecté.
- **GET** `/mesh/lists` : Récupère les listes TODO du maillage (créé automatiquement si nécessaire).
- **GET** `/users/{userId}/lists` ou `/lists` : Récupère les listes TODO d'un utilisateur spécifique.
- **GET** `/lists/{listId}` : Récupère une liste TODO spécifique par son ID.
- **POST** `/lists` : Ajoute ou met à jour une liste TODO.
- **DELETE** `/lists/{listId}` : Supprime une liste TODO avec option de remplacement.

## Points API pour TodosController.cs

- Route : `v1.0/todos`
- Méthodes HTTP : Aucun point API détecté dans ce fichier - classe de base partielle uniquement.

## Points API pour UsersController-CustomData.cs

- **GET** `/me/data/custom` : Récupère les données personnalisées de l'utilisateur connecté.
- **GET** `/{user}/data/custom` : Récupère toutes les données personnalisées d'un utilisateur spécifique.
- **POST** `/{user}/data/custom` : Ajoute ou met à jour des données personnalisées pour un utilisateur.
- **GET** `/{user}/data/custom/{dataCode}` : Récupère une donnée personnalisée spécifique d'un utilisateur par son code.
- **DELETE** `/{user}/data/custom/{dataCode}` : Supprime une donnée personnalisée spécifique d'un utilisateur.

## Points API pour UsersController-DirectUserInteraction.cs

- **GET** `/interactions/greetings/fromdevice` : Récupère les salutations pour l'utilisateur associé à un appareil (authentification requise en tant qu'appareil).
- **GET** `/interactions/greetings/all/{userName}` : Récupère les salutations pour un utilisateur spécifique.
- **POST** `/interactions/greetings/all/{userName}` : Envoie de nouvelles salutations à un utilisateur et les diffuse sur ses appareils mobiles.

## Points API pour UsersController-Interests.cs

- **GET** `/me/interests` : Récupère les centres d'intérêt de l'utilisateur connecté.
- **GET** `/all/{user}/interests` : Récupère tous les centres d'intérêt d'un utilisateur spécifique.
- **POST** `/me/interests` : Ajoute ou met à jour un centre d'intérêt pour l'utilisateur connecté.
- **POST** `/all/{user}/interests` : Ajoute ou met à jour un centre d'intérêt pour un utilisateur spécifique.
- **GET** `/me/interests/{interestId}` : Récupère un centre d'intérêt spécifique de l'utilisateur connecté.
- **GET** `/all/{user}/interests/{interestId}` : Récupère un centre d'intérêt spécifique d'un utilisateur.
- **DELETE** `/me/triggers/{interestId}` : Supprime un centre d'intérêt de l'utilisateur connecté.
- **DELETE** `/{user}/interests/{interestId}` : Supprime un centre d'intérêt d'un utilisateur spécifique.

## Points API pour UsersController-Login.cs

- **POST** `/login` : Authentification utilisateur avec identifiants (accès anonyme autorisé).
- **GET** `/logout` : Déconnexion de l'utilisateur (nécessite authentification Admin ou User).
- **POST** `/login/device` : Authentification depuis un appareil avec association optionnelle et gestion de cookies.

## Points API pour UsersController-Notify.cs

- **GET** `/{user}/notifications/clearreaditems` : Supprime les notifications lues anciennes (plus d'une minute) d'un utilisateur.
- **GET** `/{user}/notifications/markallasread` : Marque toutes les notifications d'un utilisateur comme lues.
- **GET** `/{user}/notifications` : Récupère toutes les notifications d'un utilisateur triées par date décroissante.
- **GET** `/{user}/notifications/{notifId}/markasread` : Marque une notification spécifique comme lue.
- **POST** `/{user}/notify` ou `/{user}/notifications` : Envoie une notification à un utilisateur avec option d'envoi mobile.

## Points API pour UsersController-Presence.cs

- **GET** `/presence/mesh/local/all` : Récupère tous les utilisateurs actuellement présents localement.
- **POST** `/presence/notifyactivity` : Notifie une activité de présence (envoie vers les agents locaux).
- **GET** `/presence/{userName}/forcelocation/{locationId}/{status}` : Force manuellement le statut de présence d'un utilisateur à une localisation.
- **POST** `/all/{userName}/presence` : Met à jour les données de présence d'un utilisateur (localisation, activités, probabilités).

## Points API pour UsersController.cs

- **GET** `/main` : Récupère la liste des utilisateurs principaux.
- **GET** `/all` : Récupère tous les utilisateurs.
- **GET** `/all/{userName}` : Récupère un utilisateur spécifique par son nom.
- **DELETE** `/mains/{userName}` : Supprime un utilisateur principal (protection si c'est le dernier).
- **DELETE** `/all/{userName}` : Supprime un autre utilisateur (non principal).
- **GET** `/non-guests` : Récupère tous les utilisateurs non invités.
- **GET** `/guests` : Récupère tous les utilisateurs invités.
- **POST** `/guests/upsert` : Ajoute ou met à jour un utilisateur invité.
- **POST** `/all/{userName}` : Ajoute ou met à jour un utilisateur avec options de mot de passe et code PIN.
- **POST** `/all/{userName}/avatar/set` : Met à jour l'avatar d'un utilisateur.
- **GET** `/me/identity` : Récupère l'identité de l'utilisateur connecté.
- **GET** `/me/is-admin` : Vérifie si l'utilisateur connecté est administrateur.
- **GET** `/all/{userName}/setmain/{main}` : Change le statut principal d'un utilisateur.

## Points API pour WebhookController.cs

- **GET** `/raise/{hookid}` : Déclenche un événement webhook par son ID avec source optionnelle (accès anonyme autorisé).
