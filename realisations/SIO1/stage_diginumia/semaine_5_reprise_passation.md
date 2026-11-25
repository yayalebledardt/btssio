# Reprise, documentation et passation des projets

> **Fiche de situation professionnelle — Bloc 1 (Épreuve E5)** · Stage de 1re année chez Diginumia, semaine 5

> ⚠️ **À relire avant l'oral :** cette semaine est absente du rapport de stage. Ce qui concerne le site du podcast est relevé dans l'historique Git (commits datés du 20 au 23 juillet) ; le reste est marqué *à confirmer*.

## 1. IDENTIFICATION GÉNÉRALE
- **Titre de la réalisation :** Reprise, documentation et passation des projets
- **Cadre de réalisation :** [x] Stage 1  [ ] Stage 2  [ ] Atelier de professionnalisation  [ ] Projet de cours
- **Période de réalisation :** Juillet 2026 — semaine 5 du stage (à partir du lundi 20 juillet)
- **Modalité :** [x] Individuel (sous la direction du tuteur de stage) — le site du podcast est un dépôt partagé avec un autre développeur ; seule ma part est décrite ici.
- **Localisation / Organisation cliente :** Diginumia — site public d'un podcast et projets du stage

## 2. CONTEXTE ET OBJECTIFS
- **Contexte organisationnel :** Dernière semaine du stage : refermer les chantiers ouverts plutôt que d'en ouvrir de nouveaux.
- **Problématique / Besoin exprimé :** Le site du podcast encaisse désormais de l'argent : il devait être durci et mis en conformité. Les projets devaient rester compréhensibles par quelqu'un d'autre après mon départ.
- **Objectifs fixés :** Durcir le site du podcast et publier ses pages légales ; corriger ce qui restait ; documenter et transmettre les projets.

## 3. DÉMARCHE ET ENVIRONNEMENT TECHNIQUE
- **Environnement technologique mobilisé :**
  - *Sécurité web :* jetons anti-CSRF, signature du webhook de paiement, garde anti-spam, politique de sécurité du contenu (CSP)
  - *Outils :* Stripe, Google Forms, Git
- **Démarche suivie sur le site du podcast (d'après l'historique Git) :**
  1. *Lundi :* ajout d'une section « Participer » pour être invité, proposer un sujet ou raconter une anecdote ; l'entrée de menu « Soutenir » devient « Embarquer ».
  2. *Mardi :* retrait des dons récurrents, seuls les dons ponctuels subsistent : un abonnement aurait demandé de gérer dans le temps les annulations et les prélèvements qui échouent.
  3. *Mercredi :* durcissement (anti-CSRF, webhook signé, anti-spam, CSP réellement appliquée) ; correction des dix constats d'une revue de code ; panier d'un sponsoring retenu dix minutes ; capacité des emplacements ramenée à la réalité ; pages légales (mentions, confidentialité, conditions de vente) avec éditeur et hébergeur ; corrections de référencement ; retrait du contenu de démonstration.
  4. *Jeudi :* formulaire de participation branché sur un Google Form ; autoliquidation de la TVA rendue actionnable depuis l'espace d'administration.
- **Reste de la semaine (*à confirmer*) :**
  - Point sur ce qui restait ouvert et mise en ordre par priorité.
  - Retour sur l'authentification à deux facteurs de la semaine 2, pour comprendre où elle se rompait.
  - Tests et corrections, vérification des protections par rôle sur les routes ajoutées.
  - Documentation de passation : comment lancer chaque projet, quelles variables d'environnement il attend, ce qui reste à faire.
  - Démonstration des cinq semaines et bilan avec le tuteur.
- **Gestion des imprévus / Incidents rencontrés :**
  - *Problème :* le durcissement a cassé la construction du site : la protection anti-CSRF n'était pas compatible avec la version épinglée de la dépendance.
  - *Solution apportée :* resynchroniser le fichier de verrouillage pour que les deux tiennent ensemble.

## 4. RÔLE ET CONTRIBUTION PERSONNELLE
- **Responsabilité précise :** Durcissement et mise en conformité du site du podcast ; passation des projets du stage.
- **Actions menées individuellement :**
  - Sécurisation du site en production et correction des constats de revue de code.
  - Rédaction et publication des pages légales.
  - Documentation de passation (*à confirmer*).

## 5. LIVRABLES ET PREUVES ASSOCIÉES
- Pages légales publiées sur le site du podcast
- Captures du site du podcast (section Participer, invités, accueil, épisodes, événements, site en entier) : [page du stage sur mon portfolio](https://yanis-haddou.vercel.app/stages/diginumia)
- Historique Git du site du podcast (commits datés du 20 au 23 juillet)

## 6. COMPÉTENCES DU BLOC 1 MOBILISÉES
> ⚠️ Proposition à valider avec le référentiel avant l'épreuve.

- [ ] **B1.1 — Gérer le patrimoine informatique**
- [ ] **B1.2 — Répondre aux incidents et demandes d'assistance et d'évolution**
- [x] **B1.3 — Développer la présence en ligne :** pages légales, référencement et section « Participer » du site du podcast.
- [ ] **B1.4 — Travailler en mode projet**
- [x] **B1.5 — Mettre à disposition des utilisateurs un service informatique :** durcissement d'un service en production qui encaisse des paiements.
- [ ] **B1.6 — Organiser son développement professionnel**

## 7. BILAN RÉFLEXIF ET AUTO-ÉVALUATION
- **Points forts :** Site en production durci (CSRF, webhook signé, anti-spam, CSP) ; dix constats de revue de code corrigés ; pages légales publiées.
- **Axes d'amélioration :** *[À compléter]*
- **Compétences professionnelles consolidées :** Sécuriser une application qui encaisse de l'argent ; connaître les obligations légales d'un site (mentions, confidentialité, conditions de vente).
