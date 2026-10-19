# LMS-API Quiz, notifications, qualité et contrat API React

> **Source:** learner-provided Simplonline text export, received 2026-10-19.
>
> **Official page:** [Simplonline brief](https://maghreb.simplonline.co/classrooms/4867b8e5-eb61-4ad3-a538-a88b9ebb5957/briefs/cd3bcdac-0d28-4946-8f78-fdde2cee3546)
>
> **Source boundary:** the pasted export says the rest of section 6 is in `brief-03-sprint-02-version-simplonline.pdf`; that PDF was not supplied with this intake.

## Metadata

- Platform status shown: Assigned
- Locale shown: `fr`
- Displayed creator: ML — Mehdi Laraibi
- Created: 13/10/26
- Start: 19/10/2026
- Deadline: 30/10/2026
- Work mode: squad
- Resource named by the source: `brief-03-sprint-02-version-simplonline.pdf`

## Frameworks / competencies shown

- `[2023] Application designer and developer`
- `Harnessing fundamental soft skills in a professional environment`

## Mission

Livrez une API LMS finale : stable, testée, documentée, avec quiz, emails, cron jobs, statistiques et contrat React.

## Project context

Le backend LMS entre en phase de livraison.

Le Sprint 3 React aura besoin d'une API claire : endpoints stables, données de démonstration, erreurs prévisibles, statistiques simples, notifications traçables et lancement local reproductible.

## Objectifs

À la fin du brief, vous devez être capable de :

- livrer une API backend en squad ;
- stabiliser une base commune ;
- corriger les régressions du Brief 2 ;
- développer quiz, tentatives, score backend et feedback formateur ;
- intégrer emails, templates HTML et cron jobs configurables ;
- exposer des statistiques utiles à React ;
- documenter, tester et lancer l'API avec Docker Compose ;
- tracer les contributions individuelles.

## Transition depuis le Brief 2

Avant les nouvelles fonctionnalités, la squad doit :

- choisir une base technique commune ;
- stabiliser `main` ;
- vérifier installation, seed, auth, rôles, inscriptions, ressources, upload et progression ;
- lister les régressions ;
- créer des tickets séparés : corrections, quiz, emails, configuration, jobs, statistiques, tests, documentation, Docker.

Une régression doit être corrigée ou explicitement tracée.

## Fonctionnalités attendues

### 1. Quiz de module

Créer un modèle `Quiz` rattaché à un module avec :

- questions ;
- choix proposés ;
- bonnes réponses stockées côté backend ;
- activation du quiz ;
- score minimum de réussite ;
- statut obligatoire ou optionnel.

Les bonnes réponses ne doivent jamais être exposées aux apprenants.

### 2. Tentatives et progression

Créer un modèle `QuizAttempt` avec apprenant, quiz, réponses, score, date et statut.

Règles attendues :

- l'apprenant soumet ses réponses ;
- le backend calcule le score ;
- le résultat et un feedback minimal sont consultables après soumission ;
- le formateur consulte les résultats des apprenants sur ses cours ;
- quiz obligatoire : le score minimum valide le module et débloque la suite ;
- quiz optionnel : l'échec ne bloque pas la progression.

### 3. Feedback formateur

Créer un modèle `Feedback` lié à un formateur, un apprenant, un cours et une progression.

Règles attendues :

- un formateur laisse un feedback sur ses propres cours ;
- un admin peut intervenir sur tous les cours ;
- un apprenant consulte les feedbacks qui le concernent.

### 4. Notifications email

Intégrer un service email configurable.

Situations email obligatoires :

- inscription utilisateur ;
- inscription à un cours ;
- mot de passe oublié avec token ou lien simulé ;
- rappel apprenant inactif ;
- résumé formateur avec statistiques simples.

Attendus :

- au moins deux templates HTML : apprenant et formateur ;
- contenu dynamique : nom, cours, score, date, lien ou résumé ;
- provider au choix : Mailtrap, Ethereal Email, service similaire ou SMTP personnel ;
- mode dev obligatoire : `EMAIL_DRIVER=log` ou équivalent ;
- aucun secret SMTP, token, clé API ou mot de passe dans Git.

### 5. Configuration notifications et jobs

Ajouter une configuration applicative protégée.

L'administrateur plateforme peut :

- activer ou désactiver les emails ;
- choisir le mode d'envoi : log, sandbox ou SMTP réel ;
- configurer les fréquences des jobs ;
- configurer les seuils, par exemple `INACTIVE_DAYS` ;
- consulter les dernières exécutions des jobs.

Le formateur peut :

- s'abonner ou se désabonner au résumé formateur ;
- choisir les cours concernés ;
- choisir une fréquence parmi les options prévues ;
- recevoir uniquement les données de ses cours.

Ces configurations doivent être exposées par des endpoints CRUD protégés. Les secrets techniques restent dans l'environnement.

### 6. Tâches planifiées

Le texte fourni indique : **« Reste du brief en pièce jointe PDF »**. Les exigences détaillées de cette section restent à importer depuis la ressource officielle.

## Learning methods

- Début du brief : 19/10/2026.
- Deadline : 30/10/2026.
- Le travail se fait en squad.
- Les contributions individuelles doivent rester visibles.

## Assessment methods

La soutenance dure environ 30 à 45 minutes par squad, avec questions individuelles.

Le débriefing porte sur la livraison finale du projet LMS API : stabilisation, choix backend, qualité de livraison et fonctionnalités livrées.

La squad doit présenter :

- base reprise et régressions traitées ;
- quiz, tentatives, score, progression et feedbacks ;
- emails, templates HTML et mode `log` ou sandbox ;
- configuration admin, préférences formateur, fréquences et seuils ;
- cron jobs et déclenchement manuel ;
- statistiques préparées pour React ;
- tests, collection Postman/Insomnia, documentation ;
- Docker Compose et contrat React ;
- contributions individuelles.

## Deliverables

- Dépôt GitHub de squad avec PR et revues visibles.
- Backlog Jira avec tickets nominaux.
- API LMS complète : `Quiz`, `QuizAttempt`, `Feedback`, emails, jobs, stats.
- Configuration : CRUD administrateur plateforme et préférences formateur.
- Tests : collection Postman/Insomnia complète et tests automatisés ciblés.
- Documentation : OpenAPI complète, README final, `.env.example`, contrat React.
- Docker : Docker Compose API + MongoDB.
- Données : données de démonstration.
- Traçabilité : contributions individuelles visibles.

## Performance criteria

- L'API démarre sans erreur.
- Docker Compose lance API + MongoDB.
- Le seed génère des données exploitables.
- Les fonctionnalités du Brief 2 restent fonctionnelles.
- Les quiz calculent les scores côté backend.
- La progression respecte le caractère obligatoire ou optionnel du quiz.
- Les feedbacks respectent les droits formateur/admin.
- Les emails couvrent les cinq situations attendues.
- Les jobs sont configurables et déclenchables.
- Les statistiques sont consommables par React.
- Les tests et la collection API sont exécutables.
- La documentation permet de lancer, tester et consommer l'API.
- Les contributions individuelles sont visibles.
