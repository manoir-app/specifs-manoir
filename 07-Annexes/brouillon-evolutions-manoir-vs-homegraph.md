# Évolutions MaNoir vs HomeGraph

## Vue d'ensemble

Ce document identifie les évolutions nécessaires pour transformer HomeGraph en MaNoir, en se basant sur l'analyse de l'existant et les nouveaux besoins spécifiés.

## Évolutions majeures par domaine

### 🏠 **Interface utilisateur et expérience**

#### Existant HomeGraph
- Interface technique/admin principalement
- Accès uniforme pour tous les utilisateurs
- APIs nombreuses mais interface basique

#### Évolutions MaNoir
- **Interfaces différenciées par profil** :
  - Administrateur : Interface technique complète + outils avancés
  - Adultes : Interface simplifiée axée utilisation quotidienne
  - Enfants : Interface ludique avec pictogrammes et gamification
  - Invités : Interface ultra-simplifiée temporaire
- **Responsive design** adapté mobile/tablette/desktop
- **Personnalisation** des dashboards par utilisateur

### 👥 **Gestion des utilisateurs et contrôles**

#### Existant HomeGraph
- Utilisateurs principaux/invités basiques
- Rôles admin/user simples
- Authentification par tokens

#### Évolutions MaNoir  
- **Contrôles parentaux avancés** :
  - Restrictions temporelles (plages horaires, temps d'écran)
  - Filtrage de contenu par âge
  - Validation parentale pour certaines actions
  - Rapports d'activité pour les parents
- **Système d'invités évolué** :
  - Accès temporaire avec expiration automatique
  - Isolation complète des données privées
  - Droits ultra-limités configurables
- **Évolution par âge** : Adaptation automatique des droits selon l'âge des enfants

### 🤖 **Intelligence et automatisation**

#### Existant HomeGraph
- Scènes et déclencheurs basiques
- Automatisations statiques
- Pas d'apprentissage

#### Évolutions MaNoir
- **Assistant intelligent** :
  - Apprentissage automatique des habitudes
  - Suggestions proactives d'optimisation
  - Adaptation des automatisations selon les retours
- **Scénarios intelligents** :
  - Détection des patterns d'usage
  - Automatisations prédictives
  - Optimisation énergétique automatique
- **Notifications contextuelles** :
  - Alertes personnalisées selon les préférences
  - Suggestions d'amélioration
  - Rappels intelligents

### 🏠 **Domotique avancée**

#### Existant HomeGraph (Agent Sarah)
- Support multi-protocoles excellent
- API complète de gestion
- Scènes et groupes fonctionnels

#### Évolutions MaNoir
- **Automatisations cross-domaines** :
  - Intégration éclairage + volets + capteurs + sécurité
  - Scénarios complexes multi-équipements
  - Apprentissage des préférences d'ambiance
- **Gestion énergétique** :
  - Monitoring consommation temps réel
  - Optimisations automatiques
  - Rapports d'efficacité énergétique
- **Maintenance prédictive** :
  - Détection des anomalies équipements
  - Alertes maintenance préventive
  - Historique santé des appareils

### 📱 **Applications et interfaces**

#### Existant HomeGraph
- APIs REST complètes
- Agents spécialisés
- Interface web basique

#### Évolutions MaNoir
- **Applications mobiles natives** :
  - iOS/Android avec interfaces adaptées par profil
  - Notifications push avancées
  - Mode hors-ligne pour fonctions critiques
- **Interface vocale améliorée** :
  - Extension de l'intégration Rhasspy existante
  - Commandes naturelles contextuelles
  - Réponses personnalisées par utilisateur
- **Tableaux de bord intelligents** :
  - Widgets adaptatifs selon l'usage
  - Informations contextuelles
  - Prédictions et suggestions

## Architecture technique - Évolutions

### Agents existants à faire évoluer

#### **Agent Sarah (Domotique)** → **Agent Sarah MaNoir**
- ✅ Conserver : Gestion multi-protocoles, scènes, API
- 🆕 Ajouter : IA d'apprentissage, automatisations avancées, gestion énergétique
- 🔄 Modifier : Interface adaptée par profil utilisateur

#### **Agent Aurore (Messages)** → **Agent Aurore MaNoir** 
- ✅ Conserver : Notifications, recherche, Rhasspy
- 🆕 Ajouter : Assistant intelligent, suggestions proactives
- 🔄 Modifier : Notifications contextuelles et personnalisées

#### **Agent Erza (Maintenance)** → **Agent Erza MaNoir**
- ✅ Conserver : Maintenance BDD, présence, nettoyage
- 🆕 Ajouter : Gestion des contrôles parentaux, surveillance mode invité
- 🔄 Modifier : Gestion utilisateurs avancée

### Nouvelles intégrations nécessaires

#### **Capteurs étendus**
- Capteurs de qualité d'air
- Détecteurs de fuite d'eau
- Capteurs de vibration/ouverture
- Stations météo domestiques

#### **Services externes**
- APIs météo locales avancées
- Services de géolocalisation
- Plateformes d'analyse énergétique
- Services de maintenance équipements

## Planning de développement suggéré

### Phase 1 : Fondations (2-3 mois)
- Mise à jour des profils utilisateurs existants
- Implémentation des contrôles parentaux de base
- Interface différenciée par profil
- Mode invité temporaire

### Phase 2 : Intelligence (2-3 mois)  
- Assistant intelligent et apprentissage
- Automatisations avancées cross-domaines
- Scénarios prédictifs
- Optimisations énergétiques

### Phase 3 : Applications (2-3 mois)
- Applications mobiles natives
- Interface vocale améliorée
- Tableaux de bord intelligents
- Intégrations étendues

### Phase 4 : Optimisations (1-2 mois)
- Performance et stabilité
- Fonctionnalités avancées
- Tests utilisateurs
- Documentation finale

## Critères de succès

### Techniques
- Migration sans perte de données depuis HomeGraph
- Performance maintenue ou améliorée
- Compatibilité ascendante des APIs critiques
- Sécurité renforcée (contrôles parentaux, mode invité)

### Fonctionnels
- Adoption par les différents profils (admin, adultes, enfants)
- Réduction du temps de configuration quotidienne
- Amélioration mesurable du confort et des économies d'énergie
- Satisfaction utilisateur supérieure à HomeGraph

## Liens croisés
- [État actuel HomeGraph](etat-actuel-homegraph.md)
- [Profils utilisateurs MaNoir](user-stories/)
- [Spécifications techniques](fonctionnalites/)
- [Architecture](../03-Architecture/)
