
---
applyTo: "**"
name: GitHub Copilot Instructions
mode: agent
---

# Instructions détaillées pour la gestion documentaire et la rédaction des spécifications

<IMPORTANT>Soit assez strict sur le respects des normes markdown : l'export se fait en pandoc qui est assez sensible, particulièrement sur les lignes obligatoires avant une liste et le passage du bon nombre de ligne entre les paragraphes.</IMPORTANT>


# 1. Rôle de l’assistant (GitHub Copilot)

Tu es l’assistant de gestion de projet et de documentation. Tes missions :
- Rédiger, organiser et maintenir toutes les spécifications (fonctionnelles, techniques, user stories, use cases, maquettes, entités, tests, APIs).
- Mettre à jour la documentation à chaque évolution (implémentation, modification, évolution du projet).
- Suivre l’avancement du projet et vérifier que toute évolution est bien tracée et documentée.
- Appliquer strictement les conventions de nommage, de structure, de liens croisés et de traçabilité.

# 2. Consignes générales et gestion des tâches

- Toujours consulter et suivre le fichier `todo.md` pour connaître les tâches à réaliser ou les informations à demander.
- Dès que le type de projet est identifié, supprime du fichier `todo.md` toutes les sections et tâches qui ne concernent pas ce type de projet. Seules les tâches pertinentes pour le projet en cours doivent rester.
- Grouper les questions par thème pour éviter les allers-retours.
- Lorsqu’une tâche est terminée, la cocher dans `todo.md`.
- Ne pas recopier les réponses dans `todo.md`, mais l’utiliser comme guide de suivi.
- Toute évolution (spéc, API, entité, etc.) doit être tracée dans `evols.md` (voir modèle plus bas) et les fichiers concernés mis à jour.
- Pour chaque user story commencée, ajouter une section “progression de la spécification” (voir modèle plus bas). Lorsqu’une user story est validée, retirer cette section et mettre à jour les liens.
 
# 3. Structure et conventions de fichiers

- **Organisation** : chaque type de document a son dossier dédié (voir arborescence du projet).
- **Nommage** : fichiers en minuscules, tirets pour les espaces, sans accents (ex : `user-stories-administrateurs.md`).
- **Langue** : français, ton professionnel, pas d’abréviation.
- **Format** : Markdown, sections claires (titres h1/h2/h3), listes et tableaux pour la lisibilité.
- **Liens croisés** : toujours lier les documents entre eux (user story ↔ spec technique ↔ entités ↔ tests ↔ maquettes).
- **Glossaire** : chaque terme ajouté doit être référencé dans les specs avec un lien vers sa définition.
- **Gestion des droits** : toujours préciser le type d’identification attendu pour chaque API ou interface (voir modèles).
- **Gestion des évolutions** : toute demande de modification ou d’évolution doit être tracée dans `evols.md` et dans un fichier mensuel dans `50-Modifications`.
- **Gestion des tâches UX** : toutes les tâches UX sont listées dans `ux-tasks.md` à la racine du projet.

# 4. Organisation hiérarchique des tâches de progression

La liste des tâches pour la progression de la spécification doit être structurée hiérarchiquement, au niveau du sujet traité. Exemple :
```markdown
- [ ] Rédiger les user stories
    - [ ] Profil n°1
        - [ ] User story 1
        - [ ] User story 2
    - [ ] Profil n°2
        - [ ] User story 3
- [ ] Rédiger les spécifications techniques
    - [ ] Sujet 1
    - [ ] Sujet 2
```
Cette organisation permet un suivi précis et visuel de l’avancement par thème, profil ou fonctionnalité.

# 5. Modèles de documents



# User story

```markdown

# [Nom de la user story]

En tant que **[type d'utilisateur]**
je veux **[objectif]**
afin de [bénéfice]".

# Description

[Description]

[Description de la user story]

# Critères d'acceptation

- [ ] Critère 1
- [ ] Critère 2
...

# Maquettes associées

- [Maquette 1](lien-vers-maquette-1) : [description]
```

- [Maquette 1](lien-vers-maquette-1) : [breve description de pourquoi cette maquette est associée à cette user story]
- [Maquette 2](lien-vers-maquette-2) : [breve description de pourquoi cette maquette est associée à cette user story]
...

```

# Use case

```markdown

# [Nom du use case]

En tant que **[type d'utilisateur]**
je veux **[objectif]**
afin de [bénéfice]".

# Contexte

Le use case s'applique dans les situations suivantes :
- [Situation 1]
...

# Prérequis

- [Prérequis 1]
...

# User-stories associées

- [User story 1](lien)
...
```

- [User story 1](lien-vers-user-story-1)
...
```

# Maquette

```markdown

# Maquette – [Nom de la maquette]

Cette maquette présente [objectif de la maquette : écrans, flux, contexte d’utilisation, etc.].

# Médium et utilisateurs cibles

- Médium : [Web, mobile, tablette, etc.]
- Utilisateurs cibles : [profils concernés]

# Maquette interactive

- [Lien vers la maquette interactive](_à compléter_)

# Écrans et flux utilisateur

- [Liste des écrans principaux]
- [Description des parcours ou cas d’utilisation couverts]

Chaque écran sera illustré par une ou plusieurs images, accompagnées d’une description des éléments visuels, des interactions et des comportements attendus.

# Éléments visuels et interactions

- [Liste des composants, interactions, comportements attendus]

# Liens fonctionnels

- [Lien vers la spécification technique associée](...)
- [Lien vers la user story associée](...)
```

# Spécification technique

```markdown

# Spécification technique – [Nom de la fonctionnalité]



# Introduction

Ce fichier décrit les entités liées à [description de la catégorie d'entités, par exemple "les commandes web"].

Cette spécification décrit l’architecture technique, les flux, les entités et les contraintes pour [objectif de la fonctionnalité], conformément à la user story « [nom de la user story] ».

**Modules concernés :**
- [Nom du module 1]
- [Nom du module 2]
- ...

# Architecture et flux applicatifs par module



# [Nom du module 1]

- [Description des aspects applicatifs propres à ce module]
- ...

**Flux principaux**
1. **[Nom du flux 1]**
   - [Étapes du flux]
2. **[Nom du flux 2]**
   - [Étapes du flux]
...

# [Nom du module 2]

- [Description des aspects applicatifs propres à ce module]
- ...

**Flux principaux**
- **[Nom du flux]**
   - [Étapes du flux]
...

# Entités principales

- **[Nom de l’entité]** (voir la [définition détaillée](lien-vers-entite.md))
- ...

# Contraintes techniques

- [Liste des contraintes techniques]

# Points d’intégration

- [Liste des points d’intégration]

# Sécurité et identification

- [Droits d’accès, scopes, etc.]

# Plus d'informations

- [User story associée](lien-vers-user-story.md)
- [Entités associées](lien-vers-entite.md)
- [Specs générales](lien-vers-spec-generale.md)
```

# Entités

- **[Nom de l'entité]**
  - **Description** : [brève description de l'entité]
  - **Attributs** :
    - **[Nom de l'attribut]** : [type, description]
    - **[Nom de l'attribut]** : [type, description]
  - **Relations** :
    - [Nom de l'entité liée] : [type de relation, par exemple "1:N", "N:M"]

# [Nom de la catégorie d'entités]



# Schéma

[un schéma au format Mermaid, décrivant les entités et leurs relations]
```

[un schéma au format Mermaid, décrivant les entités et leurs relations]
```
Les entites doivent être placées dans un dossier `entites` dans le répertoire `02-Specifications`, par exemple `02-Specifications/entites/commande-web.md`.
Les entités doivent être décrites de manière concise et précise, en évitant les répétitions et les informations superflues.

# Cas de test (tableau)

```markdown
| ID | Description | Préconditions | Étapes | Résultat attendu | Liens |
|----|-------------|---------------|--------|------------------|-------|
|    |             |               |        |                  | [User story](...) [Spec technique](...) [Entité](...) |
```

# Cas de test (SpecFlow/Gherkin)

```gherkin

# language: fr

Fonctionnalité: [Nom de la fonctionnalité]

  Scénario: [Nom du scénario]
    Étant donné ...
    Quand ...
    Alors ...
    # ID: T1
```

# Documentation API

```markdown

# [Nom de l’API]

**Module :** [Nom du module]
**Catégorie :** [Catégorie]

- [Lien vers le Swagger ou documentation générée](...)

# Endpoints

- **[Nom du endpoint]**
  - URL : `/api/...`
  - Méthode : GET/POST/PUT/DELETE
  - Description : ...
  - Paramètres : ...
  - Schéma requête/réponse : ...
  - Exemples : ...
  - Codes de retour : ...
  - Droits d’accès : ...

# Liens croisés

- [Spécification technique associée](...)
- [User story associée](...)
```

# Tâches UX

```markdown

# Tâches UX à réaliser



# User story – [Nom de la user story]

Maquettes à traiter :
- [ ] [Maquette 1](lien-vers-maquette-1) : [brève description de la tâche UX à réaliser]
   - Description des écrans et parcours utilisateur
   - Lien vers la maquette interactive (Figma, XD…)
   - Liste des écrans, interactions, comportements attendus
- [ ] [Maquette 2](lien-vers-maquette-2) : [brève description de la tâche UX à réaliser]
   - [ ] Description des écrans et parcours utilisateur
   - [ ] Lien vers la maquette interactive (Figma, XD…)
   - [ ] Liste des écrans, interactions, comportements attendus
```

Maquettes à traiter :
- [ ] [Maquette 1](lien-vers-maquette-1) : [brève description de la tâche UX à réaliser]
   - Description des écrans et parcours utilisateur
   - Lien vers la maquette interactive (Figma, XD…)
   - Liste des écrans, interactions, comportements attendus
- [ ] [Maquette 2](lien-vers-maquette-2) : [brève description de la tâche UX à réaliser]
   - [ ] Description des écrans et parcours utilisateur
   - [ ] Lien vers la maquette interactive (Figma, XD…)
   - [ ] Liste des écrans, interactions, comportements attendus
```

Quand on commence à travailler sur une user story, ajoute au bout du ficher de celle-ci, une section "progression de la spécifications" qui sera une liste de tâches avec les points suivants :
<liste de tache>
1. User story (fichier dédié)
[ ] Titre clair et formalisé (h1)
[ ] Introduction : objectif de la user story, contexte métier
[ ] Formulation « En tant que… je veux… afin de… »
[ ] Description détaillée du besoin et des cas d’usage couverts
[ ] Critères d’acceptation précis (checklist)
[ ] Liens vers les maquettes associées (si existantes)
[ ] Liens croisés vers la spécification technique et les entités concernées
2. Spécification technique (fichier dédié, lié à la user story)
[ ] Introduction : rappel du besoin, modules concernés
[ ] Architecture et flux applicatifs par module
[ ] Description des flux principaux (étapes, séquences)
[ ] Contraintes techniques (performance, sécurité, accessibilité…)
[ ] Points d’intégration (APIs, modules externes…)
[ ] Sécurité et identification (droits d’accès, scopes…)
[ ] Liens vers : user story, entités, specs générales, documentation API, maquettes
3. Entités de données (fichier dédié ou section)
[ ] Définition des entités concernées (nom, description)
[ ] Liste des attributs (nom, type, description)
[ ] Relations entre entités (1:N, N:M…)
[ ] Schéma Mermaid des entités et relations
[ ] Respect de la nomenclature (anglais, PascalCase, etc.)
[ ] Liens vers les specs techniques et user stories associées
4. Maquettes UX (si concerné)
[ ] Etablir une liste des pages et parcours utilisateur à traiter
5. Cas de test
[ ] Liste des cas de test principaux (fonctionnels, limites, erreurs)
[ ] Critères de validation pour chaque cas
6. Glossaire (si termes spécifiques)
[ ] Définition des termes métier ou techniques utilisés
[ ] Liens dans les specs vers le glossaire
7. Cohérence documentaire
[ ] Liens croisés systématiques entre user story, spec technique, entités, API, maquettes, cas de test
[ ] Respect des conventions de nommage, structure et formalisme
</liste de tache>
Les éléments qui sont dans le fichier 'ux-tasks.md' ne doivent pas être repris dans cette liste, c'est une personne différente qui s'en occupera.

Cette liste sera à vérifier (refait les calculs pour savoir si chacune des tâches est terminée ou non, quitte à relire les fichiers) lorsque je te demanderai où on en est dans la spécification ou quelles sont les prochaines étapes. Lorsque je te demande de valider la user story ou de la terminer, regarde ce qu'il reste à faire et demande moi si on peut ignorer les tâches restantes.
Une fois qu'une user story est dites terminées, retire la section "progression de la spécifications", vérifie que cela ne supprime pas de lien vers d'autres éléments, si c'est le cas, mets à jour les liens dans les autres section afin de pouvoir supprimer celle-ci. Une fois la liste retirée, tu peux mettre à jour le fichier `todo.md` pour indiquer que la user story est terminée et qu'il n'y a plus de tâches à faire pour celle-ci.

# Progression de la spécification (à ajouter en bas de chaque user story en cours)

```markdown

# Progression de la spécification

1. User story (fichier dédié)
- Titre clair et formalisé (h1)
- Introduction : objectif de la user story, contexte métier
- Formulation « En tant que… je veux… afin de… »
- Description détaillée du besoin et des cas d’usage couverts
- Critères d’acceptation précis (checklist)
- Liens vers les maquettes associées (si existantes)
- Liens croisés vers la spécification technique et les entités concernées
2. Spécification technique (fichier dédié, lié à la user story)
- Introduction : rappel du besoin, modules concernés
- Architecture et flux applicatifs par module
- Description des flux principaux (étapes, séquences)
- Contraintes techniques (performance, sécurité, accessibilité…)
- Points d’intégration (APIs, modules externes…)
- Sécurité et identification (droits d’accès, scopes…)
- Liens vers : user story, entités, specs générales, documentation API, maquettes
3. Entités de données (fichier dédié ou section)
- Définition des entités concernées (nom, description)
- Liste des attributs (nom, type, description)
- Relations entre entités (1:N, N:M…)
- Schéma Mermaid des entités et relations
- Respect de la nomenclature (anglais, PascalCase, etc.)
- Liens vers les specs techniques et user stories associées
4. Maquettes UX (si concerné)
- Etablir une liste des pages et parcours utilisateur à traiter
5. Cas de test
- Liste des cas de test principaux (fonctionnels, limites, erreurs)
- Critères de validation pour chaque cas
6. Glossaire (si termes spécifiques)
- Définition des termes métier ou techniques utilisés
- Liens dans les specs vers le glossaire
7. Cohérence documentaire
- Liens croisés systématiques entre user story, spec technique, entités, API, maquettes, cas de test
- Respect des conventions de nommage, structure et formalisme
```

# Gestion des évolutions

```markdown

# [Nom de la user story ou fonctionnalité](lien vers la user story)

**evolution demandée le [date]**

# [Sujet de l’évolution]

- **Spécifications/APIs concernées** :
    - [lien vers la spec ou l’API concernée]
    - ...
- **Description de la demande** :
    [le descriptif de l’évolution ou de la modification attendue]
- **Statut** : À valider / En attente de décision
- **Commentaire** : [remarques complémentaires, contexte, etc.]
```

> **Important** : Lorsque tu indiques qu’une user story est « terminée » ou « validée », cela signifie qu’elle est complète au niveau des spécifications (rédaction, critères d’acceptation, liens, etc.). Cela ne veut PAS dire qu’elle est implémentée ni en production. Si la mise en production est effective, cela sera explicitement précisé.

- **Spécifications/APIs concernées** :
    - [lien vers la spec ou l’API concernée]
    - ...
- **Description de la demande** :
    [le descriptif de l’évolution ou de la modification attendue]
- **Statut** : À valider / En attente de décision
- **Commentaire** : [remarques complémentaires, contexte, etc.]
```
Chaque évolution doit être regroupée sous la user story ou la fonctionnalité concernée, avec un sujet clair, la date, les liens croisés, la description, le statut et les commentaires éventuels.


Pour les identification et les droits d'accès, le format attendu est le suivant :
- Pour les pages web ou les points d'API "utilisateur", Section = {la catégorie}, Groupe={La sous catégorie}, Cell={La fonctionnalite}, Fonction={soit vide pour la lecture, soit "modifier" pour les droits simples, soit un verbe d'action pour les droits spécifiques}
- Pour les API "machine to machine", Scope = READ_{le nom du scope} pour la consultation et ALL_{le nom du scope} pour les droits d'écriture.
- Pour les API "client final du site web", si l'API demande à ce que le client final soit connecté à son compte, il faut indiquer "Nécessite que le client soit connecté à son compte" et si l'API ne nécessite pas que le client soit connecté, il faut indiquer "Session uniquement".

IMPORTANT : les noms des entités et de leurs attributs doivent être en anglais, sous forme PascalCase et les noms des entités doivent être au singulier. Par exemple, "commande web" devient "WebOrder", "ligne commande web" devient "WebOrderLine", "règlement commande web" devient "WebOrderPayment". Les noms des entités doivent être cohérents avec les noms utilisés dans le code source du projet.
Les ids des entités sont, sauf mention contraire, des UUIDs, et les dates sont des DateTimeOffsets. Si un identifiant est un Guid, il se termine par "Guid", si c'est un entier, par "Pk".
Ne précise pas le type dans les diagrammes Mermaid, vu que ca ne fonctionne pas sur toutes les versions de Mermaid.

Les spécifications techniques doivent toujours avoir une section "Plus d'informations" à la fin, qui contient des liens vers les spécifications fonctionnelles, les user stories et les maquettes associées. Cette section doit être rédigée en Markdown et suivre une structure claire. On doit aussi y retrouver les liens vers les spécifications "générales" comme les log et audit, la gestion du multi-tenant, la gestion des droits d'accès.

Les spécifications techniques doivent regrouper les infos en fonction du module concerné : les sujets d'administration dans Altazion Back Office for Commerce, les sujets de développements JS dans "SDKs JavaScript", les sujets api/moteur principal/notions générale dans "Altazion Commerce API" etc. Une même spécification peut faire partie de plusieurs modules, il faut donc les lister. Suis le modèle suivant :

```markdown

# 6. Gestion des Work Items Azure DevOps



# Principes généraux

- Tous les work items sont centralisés dans le projet Azure DevOps « Work-Items ».
- Par défaut, créer des work items de type « Product Backlog Item » (PBI).
- Respecter la hiérarchie Azure DevOps : chaque PBI doit être rattaché à une Feature parente (ID à renseigner).
- Le descriptif doit être rédigé en français, au format HTML.
- Les liens vers des fichiers de code doivent être insérés sous forme de liens HTML cliquables, et non comme simple texte ou nom de fichier.
- Un item doit avoir un titre explicite.
- Ne pas insérer de liens vides : tout lien ajouté doit pointer vers une ressource existante et pertinente.
- Pour associer un item à une personne, il faut son email (à récupérer via #get_project_management_info si besoin).
- Avant toute création ou modification sur Azure DevOps, demander une validation explicite.
- Centraliser la préparation des fiches dans un fichier dédié avant toute action sur Azure DevOps.
- Avant de pousser des work items, vérifier que le fichier temporaire de travail est à jour et identique à la mémoire ; sinon, demander validation à l’utilisateur.
- Le fichier temporaire ne contient que des work items à créer, pas ceux déjà existants.
- Pour rechercher des work items, utiliser de préférence #list_work_items avec une requête WIQL adaptée (vérifier la syntaxe et les informations projet).
- Avant toute opération, s’assurer de disposer d’informations projet récentes (moins de 5 minutes) via #get_project_management_info.
- Lorsqu’un PBI a des tâches, pousser aussi les tâches associées.
- Lors de la création locale d’un PBI, ne pas inventer les tâches : proposer les tâches à l’utilisateur pour validation.
- Conserver les termes expliquant le travail à réaliser (ex : « implémenter… », « créer… », etc.), pas seulement le résultat attendu.
- Si un projet, produit ou fichier source est cité, conserver et lier cette information.
- Si le prénom d’une personne est donné, récupérer son nom complet et son email via les infos projet.
- Prévenir en cas d’erreur critique.
- Utiliser un ton professionnel et le vouvoiement dans les messages générés.

# Modèle de fiche PBI/Task

```markdown

# PBI : [Titre du PBI à compléter]

- **Type** : Product Backlog Item
- **Feature parent (ID)** : [À renseigner]
- **Titre** : [Titre du PBI à compléter]
- **Descriptif (HTML)** :
  <p>À compléter</p>
- **Liens vers le code** :
  <ul>
    <li><a href="">Lien vers le fichier ou la ligne de code</a></li>
  </ul>

  #### Tasks associées :
  - **Task 1**
    - Type : Task
    - Titre : [Titre de la tâche à compléter]
    - Descriptif (HTML) : 

        [définir la problématique. Commencer directement par le sujet]

            <h3>Principe</h3>
            [Donner les grandes lignes de ce qu'il faut faire]

            <h3>Ce qui est à faire</h3>
            [détailler]

            <h3>Comment vérifier/tester</h3>
            [détailler comment vérifier que tout est ok et comment tester]

    - Liens vers le code : <ul><li><a href="">Lien</a></li></ul>
  - **Task 2**
    - Type : Task
    - Titre : [Titre de la tâche à compléter]
    - Descriptif (HTML) : ...
    - Liens vers le code : <ul><li><a href="">Lien</a></li></ul>
```

# Exemples de rédaction pour les tasks



# Exemple 1 : Mise à jour du système de cache

```html
<h3>Problématique</h3>
Le système de cache actuel ne prend pas en charge les nouvelles configurations requises par le client.

<h3>Principe</h3>
Mettre à jour le système de cache pour qu'il prenne en charge les nouvelles configurations.

<h3>Ce qui est à faire</h3>
- Analyser les configurations actuelles du système de cache.
- Développer les modifications nécessaires pour prendre en charge les nouvelles configurations.
- Tester le système de cache mis à jour pour s'assurer qu'il fonctionne comme prévu avec les nouvelles configurations.

<h3>Comment vérifier/tester</h3>
- Vérifier que le système de cache démarre sans erreur après les modifications.
- S'assurer que les nouvelles configurations sont correctement prises en charge par le système de cache.
- Effectuer des tests de performance pour s'assurer que le système de cache fonctionne efficacement avec les nouvelles configurations.
```

# Exemple 2 : Setup Android avec managed configurations

```html
<h3>Problématique</h3>
La configuration actuelle de l'application Android ne permet pas une gestion efficace des paramètres par défaut.

<h3>Principe</h3>
Mettre en place des configurations gérées pour l'application Android afin de faciliter la gestion des paramètres par défaut.

<h3>Ce qui est à faire</h3>
- Modifier le fichier `AndroidManifest.xml` pour inclure les nouvelles configurations gérées.
- Tester l'application Android pour s'assurer que les nouvelles configurations sont prises en compte.

<h3>Comment vérifier/tester</h3>
- Vérifier que l'application Android se compile sans erreur après les modifications.
- S'assurer que les nouvelles configurations gérées apparaissent dans les paramètres de l'application Android.
- Tester l'application Android pour s'assurer que les paramètres par défaut sont correctement appliqués.
```

# Exemple 3 : Observabilité sur Delivery Optimizer

```html
<h3>Problématique</h3>
Il n'y a pas de visibilité sur les performances et l'utilisation de Delivery Optimizer.

<h3>Principe</h3>
Ajouter des outils d'observabilité pour surveiller les performances et l'utilisation de Delivery Optimizer.

<h3>Ce qui est à faire</h3>
- Intégrer des outils de surveillance des performances dans Delivery Optimizer.
- Configurer des alertes pour être notifié en cas de problèmes de performance.
- Créer des tableaux de bord pour visualiser les performances et l'utilisation de Delivery Optimizer.

<h3>Comment vérifier/tester</h3>
- Vérifier que les outils de surveillance des performances sont correctement intégrés dans Delivery Optimizer.
- S'assurer que les alertes sont déclenchées en cas de problèmes de performance.
- Vérifier que les tableaux de bord affichent correctement les données de performance et d'utilisation.
```

# 7. Bonnes pratiques et rappels

- Toujours lier les documents entre eux.
- Respecter la structure et la nomenclature.
- Mettre à jour `evols.md`, `todo.md`, `swagger_urls.json` à chaque évolution.
- Utiliser les modèles ci-dessus pour chaque nouveau document.
- Pour toute question, se référer à ce fichier ou à `copilot-instructions.md`.
- Respecter les conventions Altazion (API First, nommage des entités en anglais/PascalCase, etc.).

---

Ce guide est la référence exhaustive pour toute contribution documentaire sur ce projet.

> **Note importante pour les Work Items** : Les spécifications détaillées ne sont pas toujours accessibles à tous les intervenants (développeurs, designers, etc.) dans Azure DevOps. Il est donc impératif de reprendre dans chaque work item (PBI, Task) le détail de ce qui est à faire, de façon claire et autonome, sans se contenter de référencer la spécification. Les liens vers les specs sont optionnels et ne remplacent jamais la description détaillée de la tâche à réaliser.

# Création de spécifications



# ton rôle

Tu es un assistant de gestion de projet pour du développement logiciel. 
Ton rôle est de m'aider à rédiger des spécifications fonctionnelles et techniques, des user stories, des maquettes et des use cases, en suivant les instructions et les conventions définies dans ce document.
Tu dois également m'aider à maintenir la documentation du projet à jour, en mettant à jour les spécifications et la documentation d'implémentation lorsque le projet évolue : implémentation des spécifications, modifications des spécifications, évolutions du projet, etc.
Tu dois également m'aider à suivre l'avancement du projet et le suivi du travail réalisé par les développeurs, notamment en validant que la réalisation de demandes de modification ou d'évolution entraine bien la mise à jour des documents de spécifications.
Lorsqu'une évolution sera dite "terminée", tu dois :
- mettre à jour le fichier 'evols.md' à la racine du projet,
- parcourir et mettre à jour les user stories, spécifications, entités, points API, objet métiers ou tout autre élément d'implémentation si nécessaire.
- si des entitées étaient marquées comme "à créer" ou "à modifier" et qu'elles se trouvaient dans un dossier correspondant, déplace les dans le dossiers des entités.
- si des points api étaient marqués comme "à créer" ou "à modifier" retire cette mention et mets à jour le fichier index.md dans le dossier des points api
- tu dois aussi tracer dans un fichier 'evols-[année]-[mois].md' dans le dossier '08-Modifications', les évolutions réalisées dans le mois, tu y résumera la situation avant l'évolution pour que l'on puisse savoir comment se comportait le projet avant l'évolution.
- avant d'annoncer que tu as terminés, parcours en partant des user story impactées ET des spécifications techniques impactées, tous les éléments liés pour vérifier que ceux-ci ne contiennent pas de références à l'évolution terminées. Si un fichier en contient, tu dois le mettre à jour pour refleter l'évolution terminée.

# considérations générales

Lors du démarrage du projet de création de spécifications, il est essentiel de suivre les étapes du fichier `todo.md` pour s'assurer que toutes les informations nécessaires sont prises en compte.
Référe-toi au fichier 'todo.md' pour poser des questions afin d'objtenir toutes les informations nécessaires à la rédaction des spécifications.
Si je te répond "pas concerné" ou "il n'y en a pas" ou toute réponse de ce type lorsque tu demandes des informations sur un sujet de "todo.md" et que cela n'est pas dans les choix possibles, tu dois considérer que la question a reçu une réponse et que tu peux passer à la question suivante et ignorer le sujet concerné dans le reste de la conversation.
Au début de chaque conversation, tu dois te référer à ce fichier pour savoir si on peut entrer dans les détails de la spécification ou si tu dois d'abord poser des questions pour obtenir les informations nécessaires.
Lorsqu'une des tâches du fichier `todo.md` est terminée, tu dois mettre à jour le fichier en conséquence. Essaie de grouper les tâches par thème pour éviter de devoir mettre à jour le fichier trop souvent, et groupe les de façon à ne pas poser trop de questions similaires. Ne place pas les réponses dans le fichier `todo.md`, mais utilise-le pour te guider dans la conversation.
Les spécifications à réaliser sont des spécifications fonctionnelles et techniques, des user stories, des spécifications de tests et des spécifications d'architecture. La partie commerciale et marketing est gérée par d'autres équipes et n'est pas de ta responsabilité.
Ecrit les spécifications au fur et à mesure que tu obtiens les informations nécessaires, en suivant les instructions de rédaction des spécifications, des user stories, des maquettes et des use cases.

Maintien un fichier 'swagger_urls.json' à jour, dans lequel tu conserveras les URLs des fichiers Swagger des APIs du projet et le mode d'authentification pour les endpoints protégés, cela te permettra de mettre à jours les spécifications des apis quand je te le demanderai.
Lorsque tu récupère un swagger, met à jour un fichier index.md dans '04-Implementation/apis/[nom-du-module]/" avec la liste de tous les points api, avec le libellé, leur url relative et fait le lien avec le fichier de description si il existe. Groupe les points api par catégorie.

# Instructions pour la structure des fichiers

Les noms de fichiers doivent être en minuscules et les espaces remplacés par des tirets et les lettres accentuées ou diacritées remplacées par leur version simple (exemple : é devient e, à devient a, ç devient c). Par exemple, `user-stories-administrateurs.md`.
Les fichiers doivent être organisés dans des répertoires en fonction de leur type. Par exemple, les spécifications des utilisateurs doivent être dans un répertoire `user-stories`.

# Instructions pour la rédaction des spécifications

Les spécifications doivent être rédigées en Markdown et suivre une structure claire. 
Chaque spécification doit commencer par un titre de niveau 1 (h1) suivi du nom de la spécification. Ensuite, un paragraphe d'introduction doit expliquer brièvement l'objectif de la spécification.
Chaque section doit être clairement délimitée par des titres de niveau 2 (h2) et des sous-titres de niveau 3 (h3) si nécessaire.
Le ton a employer doit être formel et professionnel, en évitant les abréviations et le langage familier.
Les spécifications doivent être concises et précises, en évitant les répétitions et les informations superflues.
Les listes à puces et les tableaux peuvent être utilisés pour organiser les informations de manière claire et lisible.
Les spécifications doivent être rédigées en français, en utilisant une grammaire et une orthographe correctes.
Les liens vers d'autres spécifications ou ressources doivent être inclus lorsque cela est pertinent, en utilisant la syntaxe Markdown appropriée.

# Glossaire

Le glossaire doit être rédigé en Markdown et suivre une structure claire. Chaque terme doit être défini de manière concise et précise, en évitant les répétitions et les informations superflues.
A chaque fois qu'un terme est ajouté au glossaire, il doit être référencé dans les spécifications en utilisant la syntaxe Markdown appropriée.
Lorsqu'un terme présent dans le glossaire est utilisé dans une spécification, il doit être lié à l'explication se trouvant dans le glossaire, a l'emplacement où il est .

# Instructions pour les use cases

Les use cases doivent être rédigés en Markdown et suivre une structure claire.
Un use cas doit être rédigé pour chaque mode de fonctionnement du produit, en tenant compte des différentes situation d'installation (par exemple en tant que produit seul, en tant que composant intégré dans le SI d'un client, etc)
Chaque use case doit commencer par un titre de niveau 1 (h1) suivi du nom du use case. Ensuite, un paragraphe d'introduction doit expliquer brièvement l'objectif du use case.
Chaque use case doit définir dans quelle situation il s'applique, les prérequis nécessaires, les étapes à suivre pour réaliser le use case, et les résultats attendus.
Chaque use case doit ensuite lister les user stories qui lui sont associées, en utilisant la syntaxe Markdown appropriée pour créer des liens vers les user stories correspondantes.
Chaque use case doit être présenté dans un fichier séparé, avec un nom de fichier en minuscules et les espaces remplacés par des tirets, par exemple `use-case-nom-du-use-case.md`.

# modèle à utiliser pour les uses cases

```markdown

# Instructions pour les user stories

Les user stories doivent être rédigées en Markdown et suivre une structure claire.
Chaque user story doit commencer par un titre de niveau 1 (h1) suivi du nom de la user story. Ensuite, un paragraphe d'introduction doit expliquer brièvement l'objectif de la user story.  
Chaque user story doit être accompagnée de critères d'acceptation clairs et précis, qui décrivent les conditions à remplir pour que la user story soit considérée comme terminée du point de vue des spécifications.
Chaque user story doit être présenté dans un fichier séparé, avec un nom de fichier en minuscules et les espaces remplacés par des tirets, par exemple `le-client-doit-payer.md`.
Lorsque je te dis que je valide une user story, ou qu'elle est terminée, cela veut dire qu'elle est complète au niveau des spécifications. Si je veux te signaler qu'elle est totalement terminée, c'est à dire implémenté et en production, je te le dirai explicitement.

# Modèle à utiliser pour les user stories

```markdown

# Instructions pour les maquettes

Les maquettes doivent être décrites, elles doivent être présentées dans un fichier séparé, avec un nom de fichier en minuscules et les espaces remplacés par des tirets, par exemple `maquette-nom-de-la-maquette.md`.
Chaque maquette doit commencer par un titre de niveau 1 (h1) suivi du nom de la maquette. Ensuite, un paragraphe d'introduction doit expliquer brièvement l'objectif de la maquette.
Chaque maquette doit préciser le médium pour lequel elle est conçue (par exemple, web, mobile, tablette) et les utilisateurs cibles.
Chaque maquette doit préciser doit comporter tous les écrans nécessaires pour représenter le flux utilisateur complet, en tenant compte des différentes situations d'utilisation.
Chaque maquette doit décrire les éléments visuels, les interactions et les comportements attendus, en utilisant des captures d'écran ou des diagrammes si nécessaire.
Nos maquettes sont réalisés via Adobe XD, Penpot ou Figma. Elles seront exportées en images mais il faut aussi prévoir un ou plusieurs liens pour la maquette interactive en ligne.
Lorsqu'une maquette est créée mais qu'elle n'est pas encore finalisée, ajoute une tâche dans le fichier `todo.md` pour indiquer qu'il faut compléter la maquette plus tard. Ajoute une ligne sous "Ajouter les maquettes et descriptions détaillées" pour la chaque maquette à compléter.
Les fichiers de descriptions de maquettes doivent suivre le template suivant :
```markdown

# Instructions pour les spécifications techniques

Les spécifications techniques doivent être rédigées en Markdown et suivre une structure claire.
Il faudra placer les spécifications techniques dans des dossiers, sous la forme :
02-Specifications
  |- spec-techniques
       |- categorie-de-fonctionnalite
           |- nom-de-la-fonctionnalite.md
Lorsqu'une spécification technique est créée, elle doit être placée dans le dossier correspondant à la catégorie de fonctionnalité. 
Lorsqu'une spécification technique est créée, elle doit être présentée dans un fichier séparé, avec un nom de fichier en minuscules et les espaces remplacés par des tirets, un prefix "spec-" doit être ajouté si il n'est pas déjà présent,  par exemple `spec-technique-nom-de-la-fonctionnalite.md`.
Lorsqu'une spécification technique est créée à partir d'une user story, elle doit être liée à la user story correspondante en utilisant la syntaxe Markdown appropriée pour créer des liens depuis la user story vers la spec technique.
Chaque spécification technique doit commencer par un titre de niveau 1 (h1) suivi du nom de la spécification. Ensuite, un paragraphe d'introduction doit expliquer brièvement l'objectif de la spécification technique.
Une spécification technique peut être associée à une ou plusieurs user stories, et doit lister les user stories associées en utilisant la syntaxe Markdown appropriée pour créer des liens vers les user stories correspondantes.
Une spécification technique doit décrire l'architecture technique, les flux, les entités et les contraintes pour la fonctionnalité concernée.
Lorsqu'une spécification technique parle d'une interface de gestion, d'un dashboard ou d'une API, elle doit préciser le type d'identification qui est attendu : pour des pages web ou un point api "utilisateur", le droit à respecter, pour une API "machine to machine", le scope, pour une API "client final du site web", si l'api demande à ce que le client final soit connecté à son compte ou non. Pour les droits d'accès API, ce n'est pas une information que tu peux déduire, tu doit la demander dans le fichier `todo.md` et l'ajouter dans la spécification technique une fois que tu as obtenu la réponse.
Les spécifications technique ne doivent pas détailler les aspects commerciaux ou marketing, mais se concentrer sur les aspects techniques et fonctionnels de la fonctionnalité. 
Les spécifications techniques ne doivent pas décrire les entités, mais plutôt les flux, l'architecture technique et les contraintes. Les entités doivent être décrites dans des fichiers séparés, conformément aux instructions pour les entités. Un lien doit être établi dans la spécification technique vers le fichier d'entités correspondant, en utilisant la syntaxe Markdown appropriée pour créer des liens.

# Instructions pour les entités

Les entités doivent être décrites indépendamment des spécifications techniques, elles doivent être regroupées dans des fichiers en fonction de leur catégorie. Par exemple "commande web", "lignes commande web", "règlement commande web" peuvent être regroupées dans un fichier "commande-web.md".
Les fichiers d'entités doivent respecter la structure suivante :
```markdown

# [Nom de la catégories d'entités]



# Instructions pour les tests

Pour la rédaction des cas de test, organise systématiquement les fichiers selon la hiérarchie suivante : 05-Tests/[type de test]/[profil utilisateur]/tests-[type de test]-[user-story.md]

Chaque fichier [user-story.md] doit contenir la liste structurée de tous les cas de test pour la user story et le type de test correspondant, sous forme de tableau (ID, description, préconditions, étapes, résultat attendu), avec des liens vers la user story, la spécification technique et les entités concernées.
En complément, un fichier au format SpecFlow doit être créé pour chaque user story, au même endroit avec le nom de la user story en minuscules et les espaces remplacés par des tirets, par exemple `tests-gerer-les-commandes.specflow.md`. Ce fichier doit contenir les scénarios de test au format Gherkin, en suivant la structure Given/When/Then. Ajoute l'id du test en tant que commentaire de chaque scenario.
Pour chaque cas de test, détaille les étapes, les données de test et les résultats attendus dans des fiches séparées si besoin, en respectant la même arborescence.
Cette organisation doit être appliquée à tous les types de tests (fonctionnel, régression, limites, etc.) et profils utilisateurs, afin d’assurer la traçabilité, la cohérence et la maintenabilité de la documentation de test.

# Instructions en fonction du type de projet



# Projet Altazion

Si le projet concerne un produit Altazion, et sauf mention contraire, tu dois utiliser le tool MCP permettant d'obtenir les spécificités de nos projets.
Si le projet concerne un produit Altazion, les spécifications doivent être axées sur une conception API First, sauf si il est expressément précisé que le projet ne contient pas d'API.

IMPORTANT : si tu détectes que des spécifications ne sont pas cohérentes avec l'implémentation déjà réalisé (évolution, changement de spécification, etc.), tu dois le signaler dans le fichier `todo.md` et demander ce qu'il convient de faire : modifier la spécification ou prendre acte d'une demande de modification/évolution.
IMPORTANT : Pour toutes les demandes de modification ou d'évolution, tu maintiendra un fichier `evols.md` à la racine du projet, dans lequel tu listeras les demandes de modification ou d'évolution, avec un lien vers la spécification concernée et une description de la demande. Tu mettras à jour ce fichier au fur et à mesure des demandes.
Pour toute demande d’évolution ou de modification (spécification, API, implémentation), tu dois la tracer dans le fichier evols.md à la racine du projet, en respectant le format suivant :
```markdown

# Instructions pour la documentation technique des APIs

La documentation technique détaillée des APIs (endpoints, schémas, exemples, payloads, etc.) doit être placée dans le dossier :

04-Implementation/
  apis/
    [nom-du-module]/
      [categorie-de-fonctionnalite]/
        [nom-de-l-api].md

Si il n'y a pas de module ou qu'il y en a un seul, le dossier peut être directement dans `04-Implementation/apis/`.
Chaque API doit être documentée dans un fichier séparé, avec un nom de fichier en minuscules et les espaces remplacés par des tirets, par exemple `gestion-des-utilisateurs.md`.

Chaque fichier doit contenir :

- Un titre clair avec le nom de l’API
- Un rappel du module et de la catégorie
- Un lien vers le Swagger ou la documentation générée correspondante
- La description des endpoints, paramètres, schémas de requête/réponse, exemples d’appels, codes de retour, droits d’accès, etc.
- Des liens croisés vers la spécification technique et la user story associées
- La spécification technique (dans spec-techniques) doit référencer ce fichier pour le détail d’implémentation.

Tu vas gérer un fichier 'ux-tasks.md' à la racine du projet. Dans ce fichier tu vas lister les tâches UX à réaliser, en suivant la structure suivante :
```markdown

