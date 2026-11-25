# Développement d'un outil de chiffrage et intégration d'un paiement en ligne

> **Fiche de situation professionnelle — Bloc 1 (Épreuve E5)** · Stage de 1re année chez Diginumia, semaine 4

## 1. IDENTIFICATION GÉNÉRALE
- **Titre de la réalisation :** Développement d'un outil de chiffrage et intégration d'un paiement en ligne
- **Cadre de réalisation :** [x] Stage 1  [ ] Stage 2  [ ] Atelier de professionnalisation  [ ] Projet de cours
- **Période de réalisation :** Juillet 2026 — semaine 4 du stage (jusqu'au vendredi 17 juillet)
- **Modalité :** [x] Individuel (sous la direction du tuteur de stage) — le site du podcast est un dépôt partagé avec un autre développeur ; seule ma part est décrite ici.
- **Localisation / Organisation cliente :** Diginumia — un client qui chiffre des chantiers de peinture, et le site public d'un podcast

## 2. CONTEXTE ET OBJECTIFS
- **Contexte organisationnel :** Une semaine tournée vers le concret commercial : un outil qui produit des devis, une journée sur la sécurité, et l'intégration d'un système de paiement.
- **Problématique / Besoin exprimé :** Un nouveau client voulait refondre son site et chiffrer ses chantiers plus vite, surtout pour produire ses devis. Le site public d'un podcast devait pouvoir encaisser des dons et des sponsorings.
- **Objectifs fixés :** Concevoir un outil qui calcule surfaces et quantités et génère le devis ; présenter une démonstration hébergée au client ; intégrer un paiement en ligne sécurisé.

## 3. DÉMARCHE ET ENVIRONNEMENT TECHNIQUE
- **Environnement technologique mobilisé :**
  - *Hébergement :* Vercel
  - *Paiement :* Stripe (carte bancaire, Google Pay)
- **Démarche suivie étape par étape :**
  1. *Outil de chiffrage (lundi) :* chaque chantier est rattaché à un client et découpé en pièces ; on saisit les dimensions des murs et de leurs ouvertures. L'outil en déduit la surface brute, les ouvertures à retirer et la surface nette à peindre (plafond et sol en option), calcule les quantités de matériaux et génère le devis : préparation, peinture, fournitures, main-d'œuvre, TVA, total. Un tableau de bord suit le chiffre d'affaires signé, le taux de conversion et les objectifs. Démonstration hébergée sur Vercel pour le client.
  2. *Cybersécurité (mardi) :* côté défense, protéger un formulaire d'authentification, limiter les requêtes, poser une double authentification ; côté attaque, comprendre la force brute, la recherche de vulnérabilités applicatives et les failles web courantes.
  3. *Stripe en démonstration (mercredi) :* la sécurité du paiement est déléguée à Stripe ; il reste à récupérer les clés API de chaque produit et à les brancher sur le site. Résultat : un paiement par carte ou Google Pay qui fonctionne.
  4. *Cycle de vie du devis (jeudi) :* brouillon, envoi, validation, et mise en forme du document généré. ⚠️ *Journée absente du rapport de stage : à confirmer avant l'oral.*
  5. *Paiement en production (vendredi 17 juillet, d'après l'historique Git) :* mise en paiement du site public d'un podcast, avec deux tunnels : le don ponctuel, où le visiteur choisit son montant, et le sponsoring, où chaque emplacement de logo sur la voiture du podcast est un produit avec un stock.
- **Gestion des imprévus / Incidents rencontrés :**
  - *Problème :* écrire les produits Stripe en dur aurait obligé à retoucher le code du paiement à chaque nouvel emplacement de sponsoring.
  - *Solution apportée :* le produit correspondant à l'emplacement et au mode de paiement est retrouvé automatiquement côté serveur.

## 4. RÔLE ET CONTRIBUTION PERSONNELLE
- **Responsabilité précise :** Conception de l'outil de chiffrage et intégration des paiements Stripe.
- **Actions menées individuellement :**
  - Développement de l'outil de chiffrage et de son tableau de bord, mise en ligne de la démonstration sur Vercel.
  - Intégration de Stripe sur un projet de démonstration, puis en production sur le site du podcast.

## 5. LIVRABLES ET PREUVES ASSOCIÉES
- Démonstration de l'outil de chiffrage hébergée sur Vercel et présentée au client
- Captures du site du podcast : don ponctuel par Stripe, tunnel sponsor avec emplacements et tarifs, page de paiement Stripe en environnement de test : [page du stage sur mon portfolio](https://yanis-haddou.vercel.app/stages/diginumia)
- Historique Git du site du podcast (commits datés du vendredi 17 juillet)

## 6. COMPÉTENCES DU BLOC 1 MOBILISÉES
> ⚠️ Proposition à valider avec le référentiel avant l'épreuve.

- [ ] **B1.1 — Gérer le patrimoine informatique**
- [ ] **B1.2 — Répondre aux incidents et demandes d'assistance et d'évolution**
- [ ] **B1.3 — Développer la présence en ligne**
- [x] **B1.4 — Travailler en mode projet :** cycle démonstration → retour du client → corrections → validation.
- [x] **B1.5 — Mettre à disposition des utilisateurs un service informatique :** démonstration hébergée sur Vercel pour le client, paiement Stripe mis en production sur un site public (dons et sponsoring).
- [ ] **B1.6 — Organiser son développement professionnel**

## 7. BILAN RÉFLEXIF ET AUTO-ÉVALUATION
- **Points forts :** Surfaces, matériaux et devis calculés automatiquement ; démonstration présentée au client ; paiement Stripe en production deux jours après sa découverte.
- **Axes d'amélioration :** *[À compléter]*
- **Compétences professionnelles consolidées :** Voir un projet aller jusqu'au client : une maquette validée, une démonstration hébergée, un retour, des corrections.
