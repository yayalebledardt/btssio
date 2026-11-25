# Conception d'une base de données et développement d'une API

> **Fiche de situation professionnelle — Bloc 1 (Épreuve E5)** · Stage de 1re année chez Diginumia, semaine 3

## 1. IDENTIFICATION GÉNÉRALE
- **Titre de la réalisation :** Conception d'une base de données et développement d'une API
- **Cadre de réalisation :** [x] Stage 1  [ ] Stage 2  [ ] Atelier de professionnalisation  [ ] Projet de cours
- **Période de réalisation :** Juillet 2026 — semaine 3 du stage
- **Modalité :** [x] Individuel (sous la direction du tuteur de stage)  [ ] En équipe
- **Localisation / Organisation cliente :** Diginumia — agent de tri de mails pour Outlook, site d'un client, application du coach sportif

## 2. CONTEXTE ET OBJECTIFS
- **Contexte organisationnel :** La semaine où le stage a changé d'échelle : trois projets menés en parallèle.
- **Problématique / Besoin exprimé :** Trier automatiquement le courrier d'une boîte Outlook ; refaire entièrement le site d'un client ; donner à l'application sportive, vendue à des entreprises, un vrai socle technique.
- **Objectifs fixés :** Concevoir de zéro un agent de tri de mails sécurisé ; faire valider une maquette par le client avant de produire son site ; doter l'application sportive d'une base PostgreSQL, d'une API Node/Express, d'une authentification réelle et d'une gestion des rôles.

## 3. DÉMARCHE ET ENVIRONNEMENT TECHNIQUE
- **Environnement technologique mobilisé :**
  - *Base de données :* PostgreSQL (12 tables pour l'agent de tri)
  - *Back-end :* Node.js, Express, API OpenAI
  - *Sécurité :* chiffrement AES-256, double authentification, contrôle d'accès par rôles (RBAC), RGPD
  - *Outils :* Stitch (maquettes), Python
- **Démarche suivie étape par étape :**
  1. *Agent de tri de mails (lundi) :* matinée consacrée à la base PostgreSQL de douze tables (organisations, boîtes, règles, classifications, journaux, audit), interface entamée l'après-midi. L'agent surveille une boîte et classe chaque message reçu dans le bon dossier avec une couleur. Le tri se fait en cascade : les fiches clients d'abord, puis les règles d'expéditeur (domaine, préfixe), et l'API d'OpenAI seulement si rien n'a tranché. Les dossiers sont évalués de haut en bas, comme les règles d'un pare-feu. Quinze dossiers à l'arrivée : urgences, agréments d'assurance, clients prioritaires, échecs de remise…
  2. *Sécurité de l'agent (mardi) :* fin de l'interface, limite fixée sur l'usage de la clé API, page de connexion et double authentification, chiffrement de la base en AES-256 et masquage des adresses mail. Tests de l'application, sécurité comprise.
  3. *Site d'un client (mercredi) :* maquette produite avec Stitch à partir de mes consignes, envoyée au client pour validation, puis mise en page et génération du site. Rien n'était envoyé au client sans maquette validée d'abord.
  4. *Socle de l'application sportive (jeudi) :* base PostgreSQL, API Node/Express, inscription et connexion réelles, profil et mot de passe modifiables. Puis la couche métier : rôles et permissions, architecture multi-entreprises, routes protégées par rôle avec une page « Accès refusé », espace RGPD pour exporter ou supprimer ses données. Réflexion module par module sur ce que chacun contient et qui doit y accéder.
  5. *Entraînement (vendredi) :* petits programmes Python écrits à la main, dont un qui interroge une API.
- **Gestion des imprévus / Incidents rencontrés :**
  - *Problème :* un classement qui repose entièrement sur un modèle d'IA coûte à chaque message et reste imprévisible.
  - *Solution apportée :* le tri en cascade n'appelle l'IA qu'en dernier recours, et le tableau de bord affiche la part de courrier rangée sans elle.

## 4. RÔLE ET CONTRIBUTION PERSONNELLE
- **Responsabilité précise :** Conception de l'agent de tri de mails, du site du client et du back-end de l'application sportive.
- **Actions menées individuellement :**
  - Modélisation de la base de données et développement de l'interface de l'agent de tri.
  - Sécurisation de l'agent : connexion, double authentification, chiffrement, masquage des adresses.
  - Maquette et site du client.
  - API, authentification, gestion des rôles et espace RGPD de l'application sportive.

## 5. LIVRABLES ET PREUVES ASSOCIÉES
- Captures de l'agent de tri : tableau de bord, dossiers de classement avec critères, mots-clés et expéditeurs : [page du stage sur mon portfolio](https://yanis-haddou.vercel.app/stages/diginumia)

## 6. COMPÉTENCES DU BLOC 1 MOBILISÉES
> ⚠️ Proposition à valider avec le référentiel avant l'épreuve.

- [ ] **B1.1 — Gérer le patrimoine informatique**
- [ ] **B1.2 — Répondre aux incidents et demandes d'assistance et d'évolution**
- [x] **B1.3 — Développer la présence en ligne :** refonte complète du site d'un client.
- [x] **B1.4 — Travailler en mode projet :** maquette validée par le client avant toute production.
- [x] **B1.5 — Mettre à disposition des utilisateurs un service informatique :** agent de tri de mails sécurisé et testé.
- [ ] **B1.6 — Organiser son développement professionnel**

## 7. BILAN RÉFLEXIF ET AUTO-ÉVALUATION
- **Points forts :** Un tri prévisible partout où une règle existe, avec l'IA en dernier recours ; une base chiffrée en AES-256 ; une gestion des rôles et un espace RGPD dès le socle de l'application.
- **Axes d'amélioration :** *[À compléter]*
- **Compétences professionnelles consolidées :** Modélisation d'une base relationnelle, conception d'une API, contrôle d'accès par rôles et prise en compte du RGPD.
