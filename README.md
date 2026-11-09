
# SkillTrack
## Cahier des charges et plan de développement

**Projet :** SkillTrack  
**Organisation :** llun, Club de programmation  
**Type :** SaaS de gestion et de suivi des apprentissages  
**Version :** 1.0 (MVP)  
**Langage principal :** Python  
**Statut :** En phase de conception

# 1. Présentation du projet

## 1.1. Contexte

SkillTrack est une application web destinée aux étudiants qui souhaitent mieux organiser leurs études, suivre leur progression et améliorer leur manière d'apprendre.

Aujourd'hui, plusieurs étudiants utilisent différentes applications pour gérer leurs tâches, consulter leur calendrier, prendre des notes ou organiser leurs révisions.

Cependant, ces outils ne permettent pas toujours d'identifier les matières qui nécessitent davantage de travail.

Un étudiant peut consacrer plusieurs heures à un cours sans réellement le maîtriser. Il peut également passer beaucoup de temps sur une matière qu'il connaît déjà, alors qu'une autre nécessite davantage d'attention.

SkillTrack souhaite répondre à ce problème en regroupant l'organisation des études, le suivi des apprentissages et la planification des révisions dans une seule application.

## 1.2. Objectif général

Développer une plateforme permettant aux étudiants de gérer leurs cours, leurs tâches et leurs séances de révision tout en bénéficiant de recommandations adaptées à leur niveau de maîtrise.

L'application doit aider les étudiants à mieux utiliser leur temps, à identifier leurs difficultés et à suivre leur évolution.

## 1.3. Objectifs spécifiques

SkillTrack devra permettre de :

1. Créer et gérer un compte personnel.
2. Ajouter et organiser ses propres cours.
3. Diviser les cours en chapitres et en notions.
4. Créer des tâches et définir des échéances.
5. Planifier des séances de révision.
6. Enregistrer le temps réellement consacré aux études.
7. Évaluer son niveau de compréhension.
8. Identifier les matières les moins maîtrisées.
9. Proposer une répartition adaptée du temps de révision.
10. Consulter des statistiques de progression.
11. Personnaliser son organisation et ses objectifs.
12. Recevoir des rappels concernant les tâches et les révisions.

# 2. Public cible

## 2.1. Utilisateurs principaux

La plateforme s'adresse principalement :

- Aux étudiants universitaires.
- Aux étudiants collégiaux.
- Aux personnes suivant des formations personnelles.
- Aux personnes souhaitant apprendre de nouvelles compétences.

## 2.2. Types d'apprentissage

SkillTrack prendra en charge deux catégories de cours.

### Cours académiques

Il s'agit des cours suivis dans un établissement d'enseignement.

Exemples :

- Algorithmique.
- Physique.
- Bases de données.
- Mathématiques.
- Programmation orientée objet.

### Apprentissage personnel

Il s'agit des compétences que l'utilisateur souhaite développer indépendamment de son programme d'études.

Exemples :

- Python.
- Développement web.
- Photographie.
- Montage vidéo.
- Cybersécurité.
- Apprentissage d'une langue.

L'utilisateur pourra gérer ces deux catégories depuis le même tableau de bord.

# 3. Fonctionnalités principales

## 3.1. Gestion des utilisateurs

Chaque utilisateur doit pouvoir créer un compte et accéder à son espace personnel.

### Fonctionnalités

- Inscription.
- Connexion.
- Déconnexion.
- Modification du profil.
- Modification du mot de passe.
- Réinitialisation du mot de passe.
- Configuration des préférences.
- Désactivation ou suppression du compte.

### Informations du profil

- Identifiant unique.
- Nom.
- Prénom.
- Adresse courriel.
- Mot de passe stocké sous forme de hachage sécurisé.
- Établissement d'enseignement (facultatif).
- Programme d'études (facultatif).
- Langue préférée.
- Fuseau horaire.
- Date de création du compte.

### Règles

Chaque utilisateur possède un espace personnel.

Les cours, tâches, évaluations et statistiques d'un utilisateur ne doivent pas être accessibles aux autres utilisateurs sans autorisation explicite.

## 3.2. Gestion des cours

L'utilisateur pourra créer ses propres cours.

### Fonctionnalités CRUD

**Create :** Ajouter un cours.

**Read :** Consulter ses cours et leurs informations.

**Update :** Modifier un cours existant.

**Delete :** Supprimer ou archiver un cours.

### Informations d'un cours

- Identifiant.
- Nom.
- Code du cours (facultatif).
- Description.
- Catégorie.
- Session académique.
- Niveau de difficulté.
- Objectif personnel.
- Date de début.
- Date de fin.
- Date d'examen (facultative).
- Nombre d'heures souhaité par semaine.
- Statut : actif, terminé ou archivé.


## 3.3. Gestion des chapitres et des notions

Un cours pourra contenir plusieurs chapitres.

Chaque chapitre pourra contenir plusieurs notions.

### Exemple

Cours : Python

Chapitre 1 : Introduction

Notions :
- Variables.
- Types de données.
- Opérateurs.

Chapitre 2 : Structures de contrôle

Notions :
- Conditions.
- Boucles.
- Instructions de contrôle.

Chapitre 3 : Fonctions

Notions :
- Définition des fonctions.
- Paramètres.
- Valeurs de retour.

### Fonctionnalités

- Ajouter un chapitre.
- Modifier un chapitre.
- Supprimer un chapitre.
- Consulter les chapitres.
- Ajouter une notion.
- Modifier une notion.
- Supprimer une notion.
- Réorganiser les chapitres et les notions.
- Associer des objectifs à une notion.
- Consulter le niveau de maîtrise d'une notion.

Le niveau de maîtrise sera calculé pour chaque notion et pourra ensuite être regroupé au niveau du chapitre et du cours.

## 3.4. Gestion des tâches

L'utilisateur pourra créer des tâches liées à ses cours ou à ses apprentissages personnels.

### Exemples

- Terminer le devoir d'info 1.
- Lire le chapitre 3.
- Réviser les fonctions Python.
- Résoudre 10 exercices.
- Préparer un examen.
- Terminer un projet personnel.

### Informations d'une tâche

- Identifiant.
- Titre.
- Description.
- Cours associé (facultatif).
- Notion associée (facultative).
- Date de création.
- Date d'échéance.
- Priorité.
- Durée estimée.
- Statut.
- Répétition éventuelle.

### Priorités

- Faible.
- Normale.
- Haute.
- Urgente.

### Statuts

- À faire.
- En cours.
- Terminée.
- Annulée.

### Fonctionnalités

- Créer une tâche.
- Consulter les tâches.
- Modifier une tâche.
- Supprimer une tâche.
- Marquer une tâche comme terminée.
- Filtrer les tâches par cours.
- Filtrer les tâches par priorité.
- Trier les tâches par échéance.
- Afficher les tâches dans le calendrier.

Une tâche terminée ne signifie pas automatiquement que la notion associée est maîtrisée.

# 4. Gestion des séances de révision

## 4.1. Objectif

Permettre à l'étudiant d'enregistrer le temps réellement consacré à chaque cours.

## 4.2. Fonctionnalités

- Démarrer une séance de révision.
- Mettre une séance en pause.
- Reprendre une séance.
- Terminer une séance.
- Enregistrer une séance manuellement.
- Modifier une séance.
- Supprimer une séance.
- Associer une séance à un cours.
- Associer une séance à une notion.
- Ajouter un commentaire après une séance.
- Consulter l'historique des séances.

## 4.3. Modes de révision

### Mode libre

L'étudiant démarre un chronomètre et travaille pendant la durée souhaitée.

### Mode Pomodoro

L'étudiant alterne des périodes de concentration et de pause.

Configuration initiale proposée :

- 25 minutes de travail.
- 5 minutes de pause.
- Pause longue après plusieurs cycles.

Ces durées devront être personnalisables.

## 4.4. Évaluation après une séance

À la fin d'une séance, l'application pourra demander :

1. Qu'as-tu étudié ?
2. Combien de temps as-tu réellement travaillé ?
3. As-tu atteint ton objectif ?
4. Quel est ton niveau de compréhension ?
5. Quelles difficultés as-tu rencontrées ?

Les réponses permettront d'alimenter le suivi de progression.

# 5. Suivi de maîtrise

## 5.1. Objectif

Le suivi de maîtrise permettra à l'étudiant d'identifier les notions qu'il comprend et celles qui nécessitent davantage de révision.

## 5.2. Niveaux de maîtrise

Niveau 1 : Très faible

L'étudiant ne comprend pas encore les bases.

Niveau 2 : Faible

L'étudiant comprend certains éléments, mais rencontre plusieurs difficultés.

Niveau 3 : Moyen

L'étudiant comprend la notion, mais commet encore des erreurs.

Niveau 4 : Bon

L'étudiant maîtrise la majorité des éléments et peut les appliquer.

Niveau 5 : Excellent

L'étudiant maîtrise la notion et peut l'expliquer ou l'appliquer de manière autonome.

## 5.3. Sources d'évaluation

La maîtrise pourra être estimée à partir :

- Des autoévaluations.
- Des résultats aux quiz.
- Des exercices réalisés.
- De l'évolution des résultats dans le temps.
- Des révisions effectuées.

Le temps passé à étudier ne doit pas être considéré comme une preuve de maîtrise.

## 5.4. Progression

L'application devra afficher :

- La maîtrise estimée par notion.
- La maîtrise estimée par chapitre.
- La maîtrise estimée par cours.
- L'évolution des résultats.
- Les notions à renforcer.
- Les notions considérées comme bien maîtrisées.

Les pourcentages seront des estimations et non des mesures exactes des connaissances.

# 6. Moteur de recommandation

## 6.1. Objectif

Le moteur de recommandation devra proposer davantage de révisions pour les notions que l'étudiant maîtrise moins bien.

Il devra également tenir compte des échéances et du temps disponible.

## 6.2. Critères

Les recommandations pourront utiliser :

1. Le niveau de maîtrise.
2. La proximité des examens.
3. Le temps depuis la dernière révision.
4. Les résultats des évaluations.
5. Les objectifs de l'étudiant.
6. Les disponibilités hebdomadaires.

## 6.3. Exemple

Un étudiant suit trois cours.

Physique :
- Maîtrise estimée : 35 %.
- Temps habituel : 2 heures par semaine.

Python :
- Maîtrise estimée : 80 %.
- Temps habituel : 3 heures par semaine.

Mathématiques :
- Maîtrise estimée : 55 %.
- Temps habituel : 2 heures par semaine.

L'application pourrait proposer d'augmenter le temps consacré à la physique et aux mathématiques.

La répartition finale devra respecter le nombre total d'heures disponibles.

## 6.4. Calcul de priorité

Pour la première version, le moteur utilisera un algorithme Python basé sur des règles.

Formule initiale proposée :

P = 0.50D + 0.30E + 0.20R

Avec :

P : Score de priorité.

D : Déficit de maîtrise, compris entre 0 et 100.

E : Urgence de l'examen, comprise entre 0 et 100.

R : Besoin de révision lié au temps écoulé, compris entre 0 et 100.

Ces coefficients sont des valeurs de départ qui devront être testées et ajustées.

Le score permettra de classer les notions, mais ne déterminera pas directement le nombre d'heures à leur consacrer.

## 6.5. Règles importantes

- Ne pas dépasser les disponibilités de l'étudiant.
- Respecter les périodes de repos.
- Éviter de surcharger une seule journée.
- Donner la priorité aux examens proches lorsque cela est pertinent.
- Ne pas supprimer automatiquement les révisions d'une matière bien maîtrisée.
- Permettre à l'étudiant de modifier ou refuser une recommandation.
- Expliquer pourquoi une matière est prioritaire.

# 7. Calendrier et planification

## 7.1. Fonctionnalités

- Afficher les tâches.
- Afficher les examens.
- Afficher les séances de révision.
- Créer un événement.
- Modifier un événement.
- Supprimer un événement.
- Déplacer une séance.
- Consulter le planning quotidien.
- Consulter le planning hebdomadaire.
- Consulter le planning mensuel.

## 7.2. Planning automatique

L'utilisateur pourra renseigner ses disponibilités.

Exemple :

Lundi : 2 heures.

Mardi : 1 heure.

Mercredi : 3 heures.

Jeudi : 2 heures.

Vendredi : indisponible.

Samedi : 2 heures.

Dimanche : repos.

Le système pourra générer un planning adapté aux matières prioritaires.

L'étudiant pourra accepter, modifier ou rejeter les séances proposées.

# 8. Tableau de bord

Le tableau de bord sera la page principale après la connexion.

Il devra présenter :

- Les cours actifs.
- Les tâches du jour.
- Les prochaines échéances.
- Les examens à venir.
- Le temps étudié cette semaine.
- L'objectif hebdomadaire.
- Les matières prioritaires.
- Les prochaines séances de révision.
- Les recommandations.
- La progression globale.

# 9. Statistiques

## 9.1. Statistiques générales

- Nombre total de cours.
- Nombre de tâches créées.
- Nombre de tâches terminées.
- Temps total étudié.
- Temps étudié par semaine.
- Nombre de séances réalisées.
- Pourcentage des objectifs atteints.

## 9.2. Statistiques par cours

- Temps consacré au cours.
- Nombre de notions étudiées.
- Nombre de notions maîtrisées.
- Évolution de la maîtrise.
- Résultats des évaluations.
- Fréquence des révisions.

## 9.3. Visualisations

Les statistiques pourront être affichées avec :

- Des graphiques linéaires.
- Des graphiques en barres.
- Des indicateurs de progression.
- Des tableaux récapitulatifs.
- Un calendrier d'activité.

# 10. Paramètres et personnalisation

Chaque utilisateur pourra personnaliser son expérience.

## 10.1. Paramètres généraux

- Nom.
- Prénom.
- Langue.
- Fuseau horaire.
- Thème clair ou sombre.
- Notifications.

## 10.2. Paramètres d'apprentissage

- Nombre d'heures souhaité par semaine.
- Durée préférée des séances.
- Durée des pauses.
- Jours disponibles.
- Heures disponibles.
- Objectifs hebdomadaires.
- Niveau de difficulté perçu.
- Préférences de révision.

## 10.3. Stratégies de révision

L'utilisateur pourra choisir entre :

### Mode équilibré

Répartir le temps entre les différentes matières.

### Mode difficultés

Favoriser les matières les moins maîtrisées.

### Mode examens

Favoriser les matières ayant des examens proches.

### Mode personnalisé

Permettre à l'étudiant de définir ses propres priorités.

# 11. Notifications

Le système pourra notifier l'étudiant concernant :

- Une tâche proche de son échéance.
- Un examen à venir.
- Une séance de révision programmée.
- Une notion qui nécessite une nouvelle révision.
- Un objectif hebdomadaire atteint.
- Une modification du planning.

Pour le MVP, les notifications seront principalement affichées dans l'application.

Les notifications par courriel pourront être ajoutées ultérieurement.

# 12. Pages de l'application

## 12.1. Pages publiques

1. Accueil.
2. Inscription.
3. Connexion.
4. Réinitialisation du mot de passe.
5. Présentation des fonctionnalités.
6. Politique de confidentialité.
7. Conditions d'utilisation.

## 12.2. Pages privées

1. Tableau de bord.
2. Mes cours.
3. Détails d'un cours.
4. Chapitres et notions.
5. Mes tâches.
6. Calendrier.
7. Séances de révision.
8. Quiz et évaluations.
9. Progression.
10. Statistiques.
11. Recommandations.
12. Notifications.
13. Profil.
14. Paramètres.

# 13. Technologies utilisées

## 13.1. Backend

Langage : Python.

Framework : Django.

API : Django REST Framework.

ORM : Django ORM.

## 13.2. Frontend

- HTML5.
- CSS3.
- JavaScript.
- Django Templates.

React pourra être envisagé dans une version ultérieure.

## 13.3. Base de données

PostgreSQL.

Une base de données relationnelle commune sera utilisée.

Chaque développeur disposera de son environnement local de développement.

## 13.4. Outils de collaboration

- Git.
- GitHub.
- Figma.
- Discord.

## 13.5. Tests et qualité

- pytest.
- pytest-django.
- Ruff.
- Tests des API.
- Tests des permissions.
- Tests des règles métier.



# 14. Architecture du projet

Le projet utilisera une architecture monolithique modulaire.

Chaque fonctionnalité importante sera développée dans une application Django distincte.


# 15. Modèle de données

## 15.1. Tables principales

### User

- id
- email
- password
- first_name
- last_name
- is_active
- date_joined

### Profile

- id
- user_id
- institution
- program
- language
- timezone

### Semester

- id
- user_id
- name
- start_date
- end_date

### Course

- id
- user_id
- semester_id
- title
- code
- description
- category
- difficulty
- weekly_target_hours
- status

### Chapter

- id
- course_id
- title
- description
- position

### Topic

- id
- chapter_id
- title
- description
- difficulty
- position

### Task

- id
- user_id
- course_id
- topic_id
- title
- description
- priority
- status
- estimated_duration
- due_date

### Availability

- id
- user_id
- day_of_week
- start_time
- end_time

### StudySession

- id
- user_id
- course_id
- topic_id
- started_at
- ended_at
- duration
- notes
- self_assessment

### Assessment

- id
- user_id
- topic_id
- score
- maximum_score
- assessment_type
- completed_at

### MasteryRecord

- id
- user_id
- topic_id
- mastery_score
- recorded_at

### StudyPlan

- id
- user_id
- week_start
- status
- created_at

### PlannedSession

- id
- study_plan_id
- topic_id
- start_time
- duration
- status

### Goal

- id
- user_id
- course_id
- title
- target_value
- due_date
- status

### Notification

- id
- user_id
- title
- message
- is_read
- created_at

### UserSettings

- id
- user_id
- weekly_study_hours
- preferred_session_duration
- break_duration
- revision_strategy
- notifications_enabled

## 15.2. Relations

Un utilisateur possède plusieurs cours.

Un utilisateur possède plusieurs tâches.

Un utilisateur possède plusieurs séances de révision.

Un cours appartient à un utilisateur.

Un cours peut appartenir à une session académique.

Un cours contient plusieurs chapitres.

Un chapitre contient plusieurs notions.

Une notion peut posséder plusieurs évaluations.

Une notion peut posséder plusieurs enregistrements de maîtrise.

Un planning contient plusieurs séances planifiées.

Les relations exactes et les comportements de suppression devront être validés pendant la conception du MCD et du MLD.

# 16. API REST

Les API permettront au frontend de communiquer avec le backend.

## 16.1. Authentification

POST /api/auth/register/

POST /api/auth/login/

POST /api/auth/logout/

GET /api/auth/me/

## 16.2. Cours

GET /api/courses/

POST /api/courses/

GET /api/courses/{id}/

PATCH /api/courses/{id}/

DELETE /api/courses/{id}/

## 16.3. Chapitres

GET /api/chapters/

POST /api/chapters/

GET /api/chapters/{id}/

PATCH /api/chapters/{id}/

DELETE /api/chapters/{id}/

## 16.4. Notions

GET /api/topics/

POST /api/topics/

GET /api/topics/{id}/

PATCH /api/topics/{id}/

DELETE /api/topics/{id}/

## 16.5. Tâches

GET /api/tasks/

POST /api/tasks/

GET /api/tasks/{id}/

PATCH /api/tasks/{id}/

DELETE /api/tasks/{id}/

## 16.6. Séances de révision

GET /api/study-sessions/

POST /api/study-sessions/

GET /api/study-sessions/{id}/

PATCH /api/study-sessions/{id}/

DELETE /api/study-sessions/{id}/

## 16.7. Évaluations

GET /api/assessments/

POST /api/assessments/

GET /api/assessments/{id}/

PATCH /api/assessments/{id}/

DELETE /api/assessments/{id}/

## 16.8. Progression

GET /api/mastery/

GET /api/mastery/courses/{id}/

GET /api/mastery/topics/{id}/

## 16.9. Planning

GET /api/study-plans/

POST /api/study-plans/generate/

GET /api/study-plans/{id}/

PATCH /api/study-plans/{id}/

## 16.10. Recommandations

GET /api/recommendations/

GET /api/recommendations/priorities/

## 16.11. Statistiques

GET /api/analytics/dashboard/

GET /api/analytics/courses/

GET /api/analytics/study-time/

GET /api/analytics/progress/

## 16.12. Paramètres

GET /api/settings/

PATCH /api/settings/

Les routes seront documentées avec OpenAPI.

Les opérations devront respecter les permissions de l'utilisateur connecté.

# 17. Sécurité

La plateforme devra respecter les exigences suivantes :

1. Utiliser le système de hachage des mots de passe de Django.
2. Protéger les endpoints nécessitant une authentification.
3. Vérifier les permissions pour chaque ressource.
4. Empêcher l'accès aux données d'autres utilisateurs.
5. Valider les données envoyées aux API.
6. Protéger les formulaires contre les attaques CSRF.
7. Utiliser HTTPS en production.
8. Conserver les secrets dans des variables d'environnement.
9. Ne jamais publier les mots de passe ou clés API sur GitHub.
10. Prévoir des sauvegardes de la base de données.
11. Prévoir une procédure de suppression des données personnelles.
12. Limiter les tentatives de connexion abusives.

# 18. Organisation collaborative

## 18.1. Principe

Chaque membre du club sera responsable d'un module.

Chaque module devra comprendre :

- Les modèles Django.
- Les migrations nécessaires.
- Les serializers.
- Les vues.
- Les endpoints API.
- Les validations.
- Les permissions.
- Les tests.
- La documentation.
- Les interfaces correspondantes.

## 18.2. Répartition proposée

Membre 1 : Authentification et profils.

Membre 2 : Cours et sessions académiques.

Membre 3 : Chapitres et notions.

Membre 4 : Tâches et objectifs.

Membre 5 : Disponibilités et calendrier.

Membre 6 : Séances de révision.

Membre 7 : Quiz et évaluations.

Membre 8 : Suivi de maîtrise.

Membre 9 : Planning et recommandations.

Membre 10 : Tableau de bord et statistiques.

La répartition pourra être adaptée au nombre réel de participants et à leur niveau.

Les membres débutants pourront travailler en binôme avec des membres plus expérimentés.

## 18.3. Règles GitHub

La branche principale sera `main`.

Chaque fonctionnalité devra être développée dans une branche distincte.

Exemples :

```text
feature/authentication
feature/courses-crud
feature/tasks-crud
feature/study-sessions
feature/mastery
feature/recommendations
```

Chaque modification devra passer par une Pull Request.

Avant de fusionner une Pull Request :

1. Vérifier que le code fonctionne.
2. Exécuter les tests.
3. Vérifier les permissions.
4. Vérifier les migrations.
5. Faire relire le code par un autre membre.
6. Mettre à jour la documentation si nécessaire.

Les modifications directes sur `main` seront évitées.

# 19. Méthodologie de développement

Le développement sera organisé en petites itérations.

Chaque membre devra régulièrement présenter l'avancement de son module.

Une séance de travail pourra comprendre :

1. Présentation des objectifs.
2. Répartition des tâches.
3. Développement individuel ou en binôme.
4. Résolution collective des difficultés.
5. Démonstration des fonctionnalités.
6. Définition des tâches suivantes.

Le projet devra encourager la compréhension du code et l'utilisation de la documentation officielle.

# 20. Ordre de développement

## Phase 1 : Analyse des besoins

Objectifs :

- Présenter SkillTrack.
- Identifier le problème à résoudre.
- Définir les utilisateurs.
- Valider les fonctionnalités du MVP.
- Rédiger le cahier des charges.

Livrable :

Cahier des charges validé.

## Phase 2 : Conception UI/UX

Objectifs :

- Identifier les pages.
- Définir les parcours utilisateurs.
- Réaliser les wireframes.
- Créer les maquettes Figma.
- Définir les composants visuels.

Livrable :

Prototype de l'interface.

## Phase 3 : Conception de la base de données

Objectifs :

- Identifier les entités.
- Définir les attributs.
- Définir les relations.
- Construire le MCD.
- Construire le MLD.
- Définir les contraintes d'intégrité.

Livrable :

Schéma de la base de données.

## Phase 4 : Conception des API

Objectifs :

- Définir les endpoints.
- Définir les méthodes HTTP.
- Définir les formats JSON.
- Définir les règles de validation.
- Définir les permissions.
- Préparer la documentation OpenAPI.

Livrable :

Contrat d'API.

## Phase 5 : Initialisation du projet

Objectifs :

- Créer le dépôt GitHub.
- Configurer Python.
- Initialiser Django.
- Configurer PostgreSQL.
- Installer Django REST Framework.
- Configurer les variables d'environnement.
- Créer les applications Django.
- Configurer les tests.

Livrable :

Projet Django fonctionnel en local.

## Phase 6 : Développement des modules

Objectifs :

- Développer les CRUD.
- Créer les modèles.
- Créer les API.
- Développer les interfaces.
- Ajouter les permissions.
- Tester chaque module.

Livrable :

Modules indépendamment fonctionnels.

## Phase 7 : Développement des recommandations

Objectifs :

- Calculer les priorités.
- Identifier les notions difficiles.
- Analyser les disponibilités.
- Proposer des séances de révision.
- Permettre la modification du planning.

Livrable :

Première version du moteur de recommandation.

## Phase 8 : Intégration

Objectifs :

- Connecter les modules.
- Vérifier les relations.
- Résoudre les conflits Git.
- Vérifier la navigation.
- Tester les parcours utilisateurs.

Livrable :

Application intégrée.

## Phase 9 : Tests et corrections

Objectifs :

- Tester les fonctionnalités.
- Vérifier les API.
- Tester les permissions.
- Tester les erreurs.
- Corriger les bugs.
- Tester avec de vrais étudiants.

Livrable :

Version MVP stable.

## Phase 10 : Déploiement

Objectifs :

- Configurer l'environnement de production.
- Déployer Django.
- Configurer PostgreSQL.
- Activer HTTPS.
- Configurer les sauvegardes.
- Publier l'application.
- Préparer une démonstration.

Livrable :

SkillTrack accessible en ligne.

# 21. Planning prévisionnel

Semaine 1 :
Analyse des besoins et cahier des charges.

Semaine 2 :
Maquettes UI/UX et parcours utilisateurs.

Semaine 3 :
MCD, MLD et conception des API.

Semaine 4 :
Initialisation Django, PostgreSQL et authentification.

Semaines 5 à 7 :
Développement des modules CRUD.

Semaines 8 à 9 :
Suivi de maîtrise, séances d'étude et recommandations.

Semaine 10 :
Intégration des modules.

Semaine 11 :
Tests et corrections.

Semaine 12 :
Déploiement et présentation du MVP.

Ce calendrier constitue une estimation initiale.

La durée pourra être ajustée selon le nombre de membres, leur niveau et leur disponibilité.

# 22. Périmètre du MVP

La première version devra contenir les fonctionnalités indispensables.

## Fonctionnalités obligatoires

- Inscription et connexion.
- Gestion des cours.
- Gestion des chapitres.
- Gestion des notions.
- Gestion des tâches.
- Configuration des disponibilités.
- Enregistrement des séances de révision.
- Autoévaluation de la maîtrise.
- Calcul des priorités.
- Génération d'un planning hebdomadaire.
- Tableau de bord.
- Statistiques essentielles.
- Paramètres utilisateur.

## Fonctionnalités secondaires

- Quiz complets.
- Notifications par courriel.
- Synchronisation avec Google Calendar.
- Importation de documents.
- Répétition espacée avancée.
- Partage de cours.
- Groupes d'étude.
- Fonctionnalités sociales.
- Génération de contenu par IA.
- Application mobile.

Ces fonctionnalités seront envisagées après la validation du MVP.

# 23. Critères de réussite

SkillTrack V1 sera considéré comme fonctionnel lorsqu'un utilisateur pourra :

1. Créer un compte.
2. Se connecter.
3. Ajouter plusieurs cours.
4. Organiser les cours en chapitres et notions.
5. Créer des tâches.
6. Définir ses disponibilités.
7. Enregistrer une séance d'étude.
8. Évaluer sa compréhension.
9. Consulter les matières prioritaires.
10. Générer un planning adapté.
11. Modifier les séances proposées.
12. Consulter ses statistiques.
13. Modifier ses préférences.
14. Utiliser l'application sans accéder aux données d'un autre utilisateur.

Les principales fonctionnalités devront disposer de tests automatisés.

# 24. Évolutions futures

Après le MVP, SkillTrack pourra évoluer vers une plateforme plus complète.

## Version 2

- Quiz personnalisés.
- Cartes mémoire.
- Répétition espacée.
- Importation de notes.
- Notifications avancées.
- Synchronisation de calendriers.
- Rapports mensuels.
- Partage de ressources.

## Version 3

- Groupes d'étude.
- Collaboration entre étudiants.
- Espaces pour établissements.
- Recommandations plus avancées.
- Application mobile.
- Fonctionnalités d'intelligence artificielle.

## Version commerciale

Une version commerciale pourra proposer :

- Une formule gratuite.
- Des fonctionnalités premium.
- Des espaces pour les établissements.
- Des tableaux de bord avancés.
- Des services adaptés aux organisations.

Le modèle économique sera étudié après les premiers retours utilisateurs.

# 25. Première réunion de développement

Durée proposée : 2 heures.

## Partie 1 : Présentation du projet

Durée : 20 minutes.

Présenter le problème, la vision et les objectifs de SkillTrack.

## Partie 2 : Validation du MVP

Durée : 25 minutes.

Examiner les fonctionnalités proposées et confirmer celles qui seront développées en priorité.

## Partie 3 : Parcours utilisateurs

Durée : 30 minutes.

Identifier les actions principales qu'un étudiant devra effectuer.

## Partie 4 : Organisation du travail

Durée : 30 minutes.

Présenter les modules, les responsabilités et les règles de collaboration.

## Partie 5 : Prochaines étapes

Durée : 15 minutes.

Définir les tâches de conception à réaliser avant la prochaine réunion.

## Livrables attendus

À la fin de cette réunion, l'équipe devra disposer :

- D'une vision commune.
- D'un MVP validé.
- D'une liste des modules.
- D'une première répartition des responsabilités.
- D'un calendrier de conception.
- D'une liste de tâches à réaliser.

# 26. Conclusion

SkillTrack est un projet de SaaS étudiant visant à améliorer l'organisation, le suivi des apprentissages et la gestion du temps de révision.

Sa principale particularité repose sur la capacité à identifier les notions moins maîtrisées et à proposer une organisation adaptée aux besoins de chaque étudiant.

Pour llun, ce projet représente également une occasion de découvrir le développement collaboratif d'une application complète.

Les membres pourront travailler sur des modules indépendants tout en apprenant à utiliser Python, Django, PostgreSQL, les API REST et GitHub.

L'objectif final est de construire un produit fonctionnel, évolutif et réellement utile aux étudiants.

# 27. Prochaine étape

La première étape consiste à faire valider ce cahier des charges par les membres du club.

Une fois le périmètre du MVP confirmé, l'équipe pourra commencer :

1. Les parcours utilisateurs.
2. Les wireframes et les maquettes Figma.
3. Le modèle conceptuel de données.
4. Le modèle logique de données.
5. La définition des API.
6. L'initialisation du dépôt GitHub.

Le développement des fonctionnalités commencera après la validation des fondations techniques.

**Projet : SkillTrack**
