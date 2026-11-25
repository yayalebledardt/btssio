# GSB — Application de gestion du matériel et des incidents (C#)

> **Fiche de situation professionnelle — Bloc 1 (Épreuve E5)** · Projet de cours, BTS SIO 2e année

## 1. IDENTIFICATION GÉNÉRALE
- **Titre de la réalisation :** GSB — Application de gestion du matériel et des incidents
- **Cadre de réalisation :** [ ] Stage 1  [ ] Stage 2  [ ] Atelier de professionnalisation  [x] Projet de cours
- **Période de réalisation :** Novembre 2026 (du 3 au 18 novembre)
- **Modalité :** [ ] Individuel  [x] En équipe (4 : Yanis, Sohan, Alae et Ayoub)
- **Localisation / Organisation cliente :** Lycée Henri Matisse — laboratoire Galaxy Swiss Bourdin (GSB), contexte fictif

## 2. CONTEXTE ET OBJECTIFS
- **Contexte organisationnel :** Le laboratoire pharmaceutique Galaxy Swiss Bourdin est né de la fusion de Galaxy et de Swiss Bourdin ; son siège européen est à Paris. Il compte 480 visiteurs médicaux en métropole et 60 outre-mer, répartis en 7 régions. Son site parisien aligne plus de 350 équipements terminaux, auxquels s'ajoutent des portables et des tablettes, sans uniformisation des machines.
- **Problématique / Besoin exprimé :** Le laboratoire veut une application pour gérer son parc informatique et surtout assurer l'assistance en cas de panne, avec une cellule qui traite les demandes en interrogeant le moins possible l'utilisateur.
- **Objectifs fixés :**
  1. Enregistrer chaque matériel : caractéristiques, logiciels installés, date d'achat ou de location, garantie, fournisseur et affectation.
  2. Suivre chaque demande sur un ticket horodaté, de l'état « Enregistrée » à « Clôturée », avec les interventions du technicien et le type de prise en charge (téléphone, télémaintenance, déplacement).
  3. Respecter les droits d'accès : un utilisateur ne voit que ses demandes, un technicien de niveau 1 ne voit que celles de niveau 1 de sa région, un technicien de niveau supérieur voit tout.
  4. Fournir des statistiques sur le fonctionnement de la cellule d'assistance.

## 3. DÉMARCHE ET ENVIRONNEMENT TECHNIQUE
- **Environnement technologique mobilisé :**
  - *Langage et interface :* C#, Windows Forms, .NET 10
  - *Base de données :* MySQL (connecteur MySql.Data), XAMPP, phpMyAdmin
  - *Conception et suivi :* Looping (MCD), GanttProject, Visual Studio, Git / GitHub
- **Démarche suivie étape par étape :**
  1. *Analyse :* lecture du sujet, répartition des tâches et Gantt prévisionnel.
  2. *Modélisation :* MCD sur Looping, puis MLD corrigé : identifiants en auto-incrément, horodatage automatique de la déclaration, dates de prise en charge et de résolution ajoutées pour les statistiques, mot de passe stocké chiffré en SHA2.
  3. *Base de données :* base `gsb_incidents` de 8 tables, données de test et 3 triggers :
     - `trg_incident_maj` renseigne la date de prise en charge et l'état « En cours de traitement », puis la date de résolution ;
     - `trg_intervention_ajout` refuse une intervention dont l'heure de fin précède l'heure de début, ou sur un incident clôturé ;
     - `trg_materiel_suppression` empêche de supprimer un matériel qui a encore un incident en cours.
  4. *Application :* classes métier (Personnel, Technicien qui en hérite, Incident, Intervention, Matériel, Fournisseur, Région, statistiques) et une classe statique `Bdd`, la seule à exécuter du SQL. Trois espaces :
     - *utilisateur :* déclarer un incident et suivre ses demandes ;
     - *technicien :* prendre en charge, saisir les interventions, résoudre puis clôturer ; gérer le matériel ;
     - *responsable :* gérer le personnel et les techniciens (matricule généré automatiquement), consulter les statistiques.
  5. *Sauvegarde :* script SQL qui copie toutes les tables dans une base `gsb_sauvegarde`, aussi lancé depuis l'application par le bouton « Sauvegarder la base ».
  6. *Livraison :* commentaires XML, diagramme de classes, documentation (écrans et clics, manuel utilisateur), setup ClickOnce avec le runtime .NET Desktop 10 en prérequis, Gantt effectif.
- **Gestion des imprévus / Incidents rencontrés :**
  - *Problème :* la première version du MLD ne permettait ni l'horodatage ni le calcul des délais.
  - *Solution apportée :* MLD corrigé le 5 novembre (dates de prise en charge et de résolution, renommage de `idTechnicien` et `idDeclarant`).
  - *Problème :* le nom du projet contenait un « # », gênant pour le setup.
  - *Solution apportée :* setup corrigé et renommé `GSB_Incidents`.

## 4. RÔLE ET CONTRIBUTION PERSONNELLE
- **Responsabilité précise :** D'après le Gantt effectif, j'ai participé à toutes les étapes, et j'ai pris seul en charge la fin du projet : code des fenêtres, sauvegarde, setup et documentation.
- **Actions menées en binôme :**
  - Lecture du sujet et répartition des tâches, MCD et MLD, script SQL, données de test et triggers (avec Sohan).
  - Interface, classes métier et classe `Bdd` (avec Alae).
- **Actions menées individuellement :**
  - Code des fenêtres et tests.
  - Diagramme de classes.
  - Script de sauvegarde et commentaires XML.
  - Génération du setup ClickOnce.
  - Documentation du projet.

## 5. LIVRABLES ET PREUVES ASSOCIÉES
- [Documentation du projet (PDF, 14 pages)](preuves/documentation-projet-gsb.pdf) : MCD, MLD, triggers et leurs tests, schéma de classes, écrans, manuel utilisateur, sauvegarde, setup, Gantt
- [MCD](preuves/mcd-gsb.png)
- Dépôt GitHub du projet : [Project-c-SOHAN-YANIS-ALAE-AYOUB-](https://github.com/yayalebledardt/Project-c-SOHAN-YANIS-ALAE-AYOUB-)
  - [Script de création de la base et des triggers](https://github.com/yayalebledardt/Project-c-SOHAN-YANIS-ALAE-AYOUB-/blob/main/BDD/script_bdd.sql)
  - [Script de sauvegarde](https://github.com/yayalebledardt/Project-c-SOHAN-YANIS-ALAE-AYOUB-/blob/main/BDD/sauvegarde_bdd.sql)
  - [Classe `Bdd`](https://github.com/yayalebledardt/Project-c-SOHAN-YANIS-ALAE-AYOUB-/blob/main/Project%20c%23%20Yanis%20Sohan%20Alae%20ayoub/Bdd.cs)
  - [Gantt (GanttProject)](https://github.com/yayalebledardt/Project-c-SOHAN-YANIS-ALAE-AYOUB-/blob/main/Documentation/Laboratoire%20GSB.gan)

## 6. COMPÉTENCES DU BLOC 1 MOBILISÉES
> ⚠️ Proposition à valider avec le référentiel avant l'épreuve.

- [x] **B1.1 — Gérer le patrimoine informatique :** recensement du matériel (composants, logiciels installés, garantie, mode d'acquisition, fournisseur) et de son affectation au personnel.
- [x] **B1.2 — Répondre aux incidents et demandes d'assistance et d'évolution :** cycle complet du ticket, de la déclaration horodatée à la clôture, avec les interventions et le type de prise en charge.
- [ ] **B1.3 — Développer la présence en ligne**
- [x] **B1.4 — Travailler en mode projet :** Gantt prévisionnel et Gantt effectif avec qui a fait quoi, travail en équipe de quatre sur GitHub.
- [x] **B1.5 — Mettre à disposition des utilisateurs un service informatique :** setup ClickOnce, manuel utilisateur et documentation des écrans.
- [ ] **B1.6 — Organiser son développement professionnel**

## 7. BILAN RÉFLEXIF ET AUTO-ÉVALUATION
- **Points forts :** L'application fait ce qui est demandé pour l'utilisateur, le technicien et le responsable. Les règles du sujet sont aussi tenues par la base, grâce aux 3 triggers. Le code est commenté avec des commentaires XML.
- **Axes d'amélioration :** Il n'y a pas de page de connexion : on choisit son espace puis son nom. Les identifiants et les mots de passe chiffrés en SHA2 sont déjà dans la base, c'est donc la prochaine chose à ajouter.
- **Compétences professionnelles consolidées :** *[À compléter]*
