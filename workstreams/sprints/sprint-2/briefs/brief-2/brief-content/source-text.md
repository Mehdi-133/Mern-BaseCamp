# 📄 Original Brief 2 Text

> Source: text supplied by the learner in chat on 2026-10-09 and verified against the [official Simplonline brief](https://maghreb.simplonline.co/classrooms/4867b8e5-eb61-4ad3-a538-a88b9ebb5957/briefs/89986592-a062-464e-bd28-b1e00fe16171) on 2026-10-12. No material requirement difference was found.

## Contexte du projet

L'API LMS a déjà un catalogue de cours, modules et ressources. Besoin : gérer les droits visiteur, apprenant, formateur, administrateur. En binôme, reprenez une base saine, stabilisez le catalogue et ajoutez le coeur backend LMS.

## Objectifs

Être capable de :

- reprendre une API sans régression ;
- organiser un backlog de binôme avec tickets nominatifs ;
- sécuriser l'API : JWT, mots de passe hashés, rôles learner, trainer, admin, routes sensibles protégées ;
- gérer côté API cours/modules/ressources d'un LMS exploitable avec upload réel cadré ;
- implémenter inscriptions ;
- enregistrer, calculer et verrouiller la progression séquentielle apprenant ;
- exposer endpoints formateur ;
- tester scénarios critiques avec Postman/Insomnia et tests ciblés ;
- documenter l'API.

## Transition depuis le Brief 1

Avant développement :

- choisir base technique reprise ;
- geler état stable sur `main` ;
- vérifier installation, MongoDB, seed, routes catalogue ;
- lister endpoints conservés, modifiés, supprimés et reportés ;
- mettre à jour Jira et tickets.

Corrections de régression séparées des nouveautés. Tout manque ou erreur de conception révélé par l'implémentation doit justifier l'écart avec l'UML du Brief 1.

## Fonctionnalités attendues

### 1. Utilisateurs et authentification

API : inscription, connexion, profil connecté, hash mots de passe, token JWT, routes privées.

`User` respecte l'UML et couvre authentification, rôle et statut de compte.

Inscription publique = `learner` (`trainer` et `admin` jamais auto-attribués).

### 2. Rôles et permissions

Rôles : `learner`, `trainer`, `admin`.

Minimum : middleware auth, middleware authorize, réponses JSON cohérentes `401`/`403`.

Règles :

- visiteur = cours publiés ;
- apprenant = cours publiés + contenus inscrits ;
- formateur = ses propres cours ;
- admin = supervision ;
- trainer créé par seed/admin ou demande approuvée.

### 3. Gestion des cours, modules et ressources

Le formateur gère via API `Course`, `Module`, `Resource` : modules ordonnés, ressources associées.

Obligatoire :

- cours : créer, modifier les informations principales, publier et dépublier ;
- modules : créer dans un cours, modifier et lister dans l'ordre ;
- ressources : créer liée à un module, uploader un fichier réel et consulter seulement si les droits sont corrects.

Recommandé si le socle est stable :

- archiver cours, module et ressource ;
- modifier l'ordre des modules via un endpoint API simple et l'ordre des ressources ;
- filtrer les cours formateur par statut brouillon, publié ou archivé.

Possible à reporter et à documenter dans les limites connues :

- suppression définitive ;
- historique des changements ;
- stockage cloud ;
- workflow complet de demande formateur ;
- gestion avancée de plusieurs formateurs sur un même cours ;
- statistiques détaillées.

### 4. Inscriptions aux cours

Créer `Enrollment` reliant apprenant et cours, selon la conception et les règles de progression. Un apprenant peut suivre plusieurs cours en parallèle, mais une seule inscription active est autorisée pour un même couple apprenant-cours.

### 5. Ressources pédagogiques et upload

L'API associe à chaque module des ressources : article, vidéo ou lien externe, PDF ou image.

Upload réel attendu : stockage local contrôlé ou solution équivalente adaptée au sprint. Les fichiers sont liés au bon module et protégés par contrôle d'accès.

### 6. Progression apprenant

API :

- démarrer ou reprendre un cours ;
- marquer une ressource consultée ;
- terminer un module seulement si la règle de complétion est respectée ;
- empêcher l'accès ou la validation d'un module tant que le précédent n'est pas terminé ;
- exposer l'état du module : accessible, verrouillé, en cours, terminé ;
- calculer la progression globale ;
- empêcher les doublons incohérents ;
- permettre au formateur de consulter l'avancement des inscrits.

La progression séquentielle stricte est obligatoire et contrôlée côté backend.

### 7. Endpoints formateur

Le formateur peut consulter ses cours, les apprenants inscrits, l'état d'avancement d'un apprenant sur un cours, et les ressources/modules terminés.

Pas d'accès aux données d'un cours qui ne lui appartient pas, sauf administrateur.

### 8. Tests et validation

Deux niveaux :

1. collection Postman ou Insomnia pour rejouer les scénarios principaux ;
2. tests automatisés ciblés sur les comportements critiques.

Scénarios :

- création de compte, connexion, accès sans token ;
- rôle insuffisant, accès formateur à ses données, refus d'accès non autorisé ;
- inscription à un cours, refus d'une double inscription active ;
- progression ressource/module, refus d'accès ou de validation d'un module verrouillé.

## Contraintes techniques

- Stack : Node.js, Express, MongoDB, Mongoose.
- Bibliothèques : JWT `jsonwebtoken`, hash bcrypt ou bcryptjs, upload local Multer ou équivalent documenté.
- Sécurité : jamais de mots de passe en clair, jamais de secret commité.
- Architecture : routes, contrôleurs, modèles et middlewares séparés.
- Erreurs : JSON cohérentes, statuts HTTP adaptés.
- Tests : Jest + Supertest, ou Vitest + Supertest si justifié, plus collection Postman ou Insomnia.
- Documentation : Swagger/OpenAPI ou équivalent, README, `.env.example` à jour.
- Docker : Dockerfile API ou première conteneurisation API + MongoDB.

## Workflow Git et collaboration

Binôme :

- dépôt commun, convention branches/forks, tickets nominaux ;
- branches de fonctionnalité ou forks personnels ;
- commits réguliers et explicites ;
- `main` stable ;
- une pull request par fonctionnalité ou correction significative ;
- chaque membre relit et valide celle de l'autre avant fusion ;
- contributions individuelles documentées.

## Bonus

Seulement si le socle obligatoire est terminé :

- refresh token ;
- validation Zod plus complète ;
- endpoint de synthèse pour une future barre de progression React : pourcentage, modules terminés/total, module courant, prochain module accessible, modules verrouillés ;
- stockage compatible S3, R2, Supabase Storage ou MinIO ;
- couverture de tests élargie, logs applicatifs structurés, pagination avancée.

## Learning methods

- Début du brief : **05/10/2026**.
- Deadline : **16/10/2026**.
- Organisation : travail en binôme.
- Contributions : chaque membre doit avoir des contributions visibles — tickets, branches ou forks, pull requests, commits, documentation, tests ou corrections.
- Suivi : Jira et le README doivent rester à jour pendant le brief.

## Assessment methods

La soutenance dure environ 45 à 75 minutes par binôme, avec questions individuelles.

Le binôme doit présenter :

- contexte : base technique reprise, écarts avec l'UML du Brief 1 et leur justification, workflow de collaboration ;
- fonctionnalités : authentification, rôles et permissions, inscriptions, progression ;
- vérification : collection Postman/Insomnia et tests automatisés ciblés ;
- limites connues.

Questions possibles :

- Comment vérifiez-vous l'authentification et bloquez-vous l'accès aux ressources non autorisées ?
- Comment empêchez-vous l'auto-attribution du rôle formateur ?
- Comment garantissez-vous l'unicité du couple apprenant-cours ?
- Comment calculez-vous la progression ?
- Quelle fonctionnalité a été la plus risquée et comment l'avez-vous sécurisée ?

## Deliverables

- Dépôt GitHub du binôme, avec pull requests et revues visibles.
- Backlog Jira avec tickets nominaux.
- API sécurisée : modèles `User`, `Enrollment` et progression, middlewares auth et authorize, upload réel des ressources.
- Endpoints de gestion des cours, modules et ressources, documentés.
- Tests : collection Postman/Insomnia et tests automatisés ciblés.
- Documentation : README, documentation API et `.env.example` à jour.
- Docker : Dockerfile API ou configuration Docker API + MongoDB.

## Performance criteria

- Non-régression : l'API existante reste fonctionnelle.
- Sécurité : mots de passe hashés, authentification JWT, accès limités par rôle, erreurs claires sans fuite d'informations.
- Cours : un formateur peut construire un cours exploitable avec modules ordonnés, ressources et fichiers correctement associés.
- Apprentissage : inscriptions cohérentes, progression calculée côté backend, verrouillage séquentiel des modules effectif.
- Vérification : scénarios critiques rejouables dans Postman/Insomnia et couverts par des tests automatisés ciblés.
- Collaboration : les PR et revues rendent visibles les contributions individuelles du binôme.
- Documentation : le README permet de relancer le projet et liste les limites connues.
