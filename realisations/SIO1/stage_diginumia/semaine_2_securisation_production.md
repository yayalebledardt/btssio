# Sécurisation d'un environnement de production et refonte d'interface

> **Fiche de situation professionnelle — Bloc 1 (Épreuve E5)** · Stage de 1re année chez Diginumia, semaine 2

## 1. IDENTIFICATION GÉNÉRALE
- **Titre de la réalisation :** Sécurisation d'un environnement de production et refonte d'interface
- **Cadre de réalisation :** [x] Stage 1  [ ] Stage 2  [ ] Atelier de professionnalisation  [ ] Projet de cours
- **Période de réalisation :** Juin – juillet 2026 — semaine 2 du stage
- **Modalité :** [x] Individuel (sous la direction du tuteur de stage)  [ ] En équipe
- **Localisation / Organisation cliente :** Diginumia — application destinée à un coach sportif

## 2. CONTEXTE ET OBJECTIFS
- **Contexte organisationnel :** Diginumia conçoit des applications pour ses clients et les revend ensuite à d'autres entreprises.
- **Problématique / Besoin exprimé :** Avant de confier l'application au coach pour un essai, l'environnement de production devait être vérifié et l'interface modernisée. Les coachs utilisaient une interface séparée de celle des membres.
- **Objectifs fixés :** Auditer et renforcer la sécurité de l'environnement de production, moderniser l'accueil, unifier l'espace Coach avec celui des membres et livrer une version que le coach puisse essayer pendant le week-end.

## 3. DÉMARCHE ET ENVIRONNEMENT TECHNIQUE
- **Environnement technologique mobilisé :**
  - *Base de données :* PostgreSQL
  - *Outils :* Git (intégration sur la branche principale), variables d'environnement
- **Démarche suivie étape par étape :**
  1. *Audit de la production (lundi) :* configurations de sécurité vérifiées et reprises, variables d'environnement contrôlées automatiquement au démarrage de l'application (si une variable manque, l'application refuse de démarrer au lieu de tomber en route), base de données optimisée. Tentative d'écrire une authentification à deux facteurs à la main.
  2. *Accueil (mardi) :* intégration de composants visuels interactifs pour rendre l'interface plus vivante.
  3. *Navigation (mercredi) :* section principale réorganisée en deux colonnes, pied de page simplifié, espacements repris pour la lisibilité.
  4. *Espace Coach (jeudi) :* les coachs utilisent désormais la même interface que les membres, tout en gardant leurs fonctionnalités propres. Nouveaux boutons pour créer plus vite des conseils, des séances et des programmes ; conseils enrichis de catégories (Technique, Motivation, Nutrition) et d'images de couverture.
  5. *Intégration (vendredi) :* ensemble des développements intégré sur la branche principale, nettoyage du code et optimisations, pour que le coach puisse essayer l'application pendant le week-end.
- **Gestion des imprévus / Incidents rencontrés :**
  - *Problème :* l'authentification à deux facteurs écrite à la main ne fonctionnait pas correctement.
  - *Solution apportée :* aucune cette semaine ; le point a été noté comme à reprendre.

## 4. RÔLE ET CONTRIBUTION PERSONNELLE
- **Responsabilité précise :** Sécurisation de l'environnement de production et refonte de l'interface de l'application.
- **Actions menées individuellement :**
  - Audit et reprise des configurations de sécurité, contrôle automatique des variables d'environnement.
  - Refonte de l'accueil, de la navigation et de l'espace Coach.
  - Intégration de tous les développements sur la branche principale.

## 5. LIVRABLES ET PREUVES ASSOCIÉES
- Version intégrée sur la branche principale, livrée au coach pour un essai pendant le week-end
- Captures de l'application, dont les conseils du coach avec recherche et catégories : [page du stage sur mon portfolio](https://yanis-haddou.vercel.app/stages/diginumia)

## 6. COMPÉTENCES DU BLOC 1 MOBILISÉES
> ⚠️ Proposition à valider avec le référentiel avant l'épreuve.

- [x] **B1.1 — Gérer le patrimoine informatique :** fiabilisation d'un service existant — recenser ce dont dépend l'application, vérifier ces dépendances au démarrage et échouer tôt plutôt que tard.
- [ ] **B1.2 — Répondre aux incidents et demandes d'assistance et d'évolution**
- [ ] **B1.3 — Développer la présence en ligne**
- [ ] **B1.4 — Travailler en mode projet**
- [x] **B1.5 — Mettre à disposition des utilisateurs un service informatique :** un service qui reste disponible pour ses utilisateurs, et une version intégrée livrée au coach pour un essai.
- [ ] **B1.6 — Organiser son développement professionnel**

## 7. BILAN RÉFLEXIF ET AUTO-ÉVALUATION
- **Points forts :** Variables d'environnement contrôlées automatiquement au démarrage ; espace Coach unifié avec celui des membres ; tous les développements intégrés pour l'essai du coach.
- **Axes d'amélioration :** L'authentification à deux facteurs écrite à la main ne fonctionnait pas correctement. Je sais aujourd'hui pourquoi, et ce qu'il faudrait reprendre.
- **Compétences professionnelles consolidées :** Une application a un environnement de production, et cet environnement se vérifie. Une authentification à deux facteurs écrite à la main est plus difficile qu'elle n'en a l'air.
