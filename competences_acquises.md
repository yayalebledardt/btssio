# 📋 Tableau de Bord d'Acquisition des Savoirs (Bloc 1 — Épreuve E5)

Ce document assure la traçabilité de votre montée en compétences sur le **Bloc 1 : Support et mise à disposition de services informatiques** (Unité U4).

> **Consignes pour l'étudiant :**
> 1. À votre arrivée en BTS, tous les savoirs ci-dessous sont au format barré (`~~...~~`).
> 2. Lorsqu'un savoir a été mis en œuvre, compris et validé lors d'un TP, d'un projet en Atelier de Professionnalisation (AP) ou d'un stage :
>    * Retirez les tildes `~~` pour repasser le code et son intitulé en texte clair / gras.
>    * Cochez la case `[x]`.
>    * Renseignez le contexte ou collez le lien vers votre fiche de situation / commit Git.
> 3. Commitez régulièrement votre fichier (`git commit -m "docs: acquisition du savoir S4 suite TP PRA"`).
>
> ⚠️ **Pré-rempli à partir de mes réalisations :** savoirs cochés et pistes « En cours » à relire avant l'épreuve.

---

### Activité 1.1 : Gérer le patrimoine informatique

- [x] **S1 — Patrimoine informatique et système informatique :** définition, outils de gestion et de recensement des actifs (CMDB), composants matériels et logiciels.  
  *Preuve / Contexte de validation :* [Gestion de parc sous GLPI](realisations/SIO1/gestion_de_parc/fiche_glpi.md) — inventaire et structuration des actifs du parc ; [projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) — inventaire du matériel (composants, logiciels, garantie, fournisseur, affectation).

- [ ] ~~**S2 — Systèmes d'exploitation et gestion des habilitations :** gestion des comptes utilisateurs, droits d'accès, privilèges, groupes et politiques d'authentification.~~  
  *Preuve / Contexte de validation :* En cours — droits d'accès par rôle dans le [projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) (un utilisateur ne voit que ses demandes, un technicien de niveau 1 seulement celles de sa région) et rôles applicatifs (RBAC, [stage semaine 3](realisations/SIO1/stage_diginumia/semaine_3_base_de_donnees_api.md)) ; pas encore d'authentification, la page de connexion reste à faire.

- [ ] ~~**S3 — Disponibilité et continuité d'activité :** enjeux techniques, économiques et juridiques de la disponibilité ; plans de continuité (PCA) et plans de reprise d'activité (PRA).~~  
  *Preuve / Contexte de validation :* 

- [ ] ~~**S4 — Sauvegardes et restaurations :** typologies (totale, incrémentale, différentielle), supports physiques et logiques, stratégies de sauvegarde et protocoles de test de restauration.~~  
  *Preuve / Contexte de validation :* En cours — script de sauvegarde de toute la base et bouton « Sauvegarder la base » dans le [projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) ; reste à tester une restauration.

- [ ] ~~**S5 — Cadre juridique et contractuel du patrimoine :** typologie des licences logicielles, tarification, contrats de prestation, obligations légales d'archivage des données, valeur juridique de la charte informatique et responsabilité du salarié utilisateur.~~  
  *Preuve / Contexte de validation :* 

---

### Activité 1.2 : Répondre aux incidents et aux demandes d'assistance et d'évolution

- [x] **S6 — Gestion des incidents et assistance (Helpdesk) :** outils de ticketing, cycle de traitement des demandes, normes et référentiels (ITIL), bases de connaissances, procédures de télé-assistance.  
  *Preuve / Contexte de validation :* [Gestion de parc sous GLPI](realisations/SIO1/gestion_de_parc/fiche_glpi.md) — traitement des demandes par tickets, de l'ouverture à la clôture ; [projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) — tickets horodatés, de « Enregistrée » à « Clôturée », avec interventions et type de prise en charge.

- [ ] ~~**S7 — Diagnostic et résolution :** méthodologie d'analyse causale de panne, recherche de causes racines, outils de diagnostic technique et de test dégressif.~~  
  *Preuve / Contexte de validation :* 

- [ ] ~~**S8 — Fondamentaux des réseaux et des équipements :** modèles de référence (OSI, TCP/IP), médias d'interconnexion, protocoles de base, plan d'adressage IP, sous-réseaux, routage, services de nommage (DNS) et composants matériels clients/serveurs.~~  
  *Preuve / Contexte de validation :* 

- [ ] ~~**S9 — Systèmes et virtualisation :** fonctionnalités des systèmes d'exploitation clients et serveurs (Linux, Windows), rôles et principes fondamentaux de la virtualisation.~~  
  *Preuve / Contexte de validation :* En cours — découverte de Docker Desktop ([stage semaine 1](realisations/SIO1/stage_diginumia/semaine_1_prise_en_main.md)).

- [x] **S10 — Développement et automatisation système :** algorithmique de base, structures de données, langages de commande et scripts d'administration/automatisation (Bash, PowerShell).  
  *Preuve / Contexte de validation :* [Projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) : application C# orientée objet, script SQL et triggers ; petits programmes Python écrits à la main ([stage semaine 3](realisations/SIO1/stage_diginumia/semaine_3_base_de_donnees_api.md)).

- [ ] ~~**S11 — Niveaux de service (SLA) :** ententes de niveau de service, contrats d'assistance, indicateurs GTR/GTI, obligations de moyens et de résultats, pénalités associées.~~  
  *Preuve / Contexte de validation :* 

---

### Activité 1.3 : Développer la présence en ligne de l'organisation

- [x] **S12 — Technologies et programmation Web :** normes HTML/CSS, langages clients/serveurs, requêtage et manipulation de données, déploiement et paramétrage d'un CMS, conventions d'écriture et référencement (SEO).  
  *Preuve / Contexte de validation :* [Terminal](realisations/SIO1/developpement_web/fiche_terminal.md) (HTML/CSS, Bootstrap, SEO) et [KetaYaso](realisations/SIO1/developpement_web/fiche_ketayaso.md) (CMS PrestaShop, référencement produit).

- [x] **S13 — Cadre économique et juridique du Web :** e-réputation d'une organisation, responsabilités respectives de l'éditeur et de l'hébergeur, mentions légales, conditions générales d'utilisation (CGU), conformité RGPD appliquée au web, droits sur les contenus et gestion des noms de domaine.  
  *Preuve / Contexte de validation :* Stage Diginumia — espace RGPD d'export et de suppression des données ([semaine 3](realisations/SIO1/stage_diginumia/semaine_3_base_de_donnees_api.md)), pages légales d'un site en production ([semaine 5](realisations/SIO1/stage_diginumia/semaine_5_reprise_passation.md)).

---

### Activité 1.4 : Travailler en mode projet

- [x] **S14 — Gestion de projet :** principes de planification prédictive et séquentielle (cycle en V, diagramme de Gantt) vs démarches agiles (Scrum, Kanban, sprints, itérations).  
  *Preuve / Contexte de validation :* [Projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) : Gantt prévisionnel puis Gantt effectif avec qui a fait quoi ; cahier des charges et charte graphique de [KetaYaso](realisations/SIO1/developpement_web/fiche_ketayaso.md).

- [ ] ~~**S15 — Outils de suivi de projet :** environnements collaboratifs de gestion de tickets, tableaux de bord de projet, calcul des charges, indicateurs d'avancement et analyse des écarts.~~  
  *Preuve / Contexte de validation :* En cours — Gantt effectif du [projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) avec les écarts constatés (MLD corrigé, 3 triggers au lieu de 2, pas de page de connexion).

---

### Activité 1.5 : Mettre à disposition des utilisateurs un service informatique

- [x] **S16 — Architecture et déploiement de services :** composants structurels d'un service applicatif ou d'infrastructure, protocoles réseaux associés, techniques de paquetage logiciel et outils de distribution/déploiement.  
  *Preuve / Contexte de validation :* Stage Diginumia — API Node/Express et PostgreSQL ([semaine 3](realisations/SIO1/stage_diginumia/semaine_3_base_de_donnees_api.md)), démonstration déployée sur Vercel et paiement Stripe en production ([semaine 4](realisations/SIO1/stage_diginumia/semaine_4_chiffrage_paiement.md)) ; [projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) — application en couches (classes métier, classe d'accès aux données, fenêtres) et setup ClickOnce.

- [x] **S17 — Validation et recette :** élaboration et réalisation de jeux d'essais, tests d'intégration et d'acceptation utilisateur, rédaction du procès-verbal de recette et support d'accompagnement au changement.  
  *Preuve / Contexte de validation :* [Projet GSB](realisations/SIO2/GSB_gestion_incidents_CSharp/fiche_de_situation_professionnelle_gsb.md) : données de test, tests des triggers et manuel utilisateur ; tests de l'agent de tri, sécurité comprise ([stage semaine 3](realisations/SIO1/stage_diginumia/semaine_3_base_de_donnees_api.md)). Reste à rédiger un procès-verbal de recette.

---

### Activité 1.6 : Organiser son développement professionnel

- [x] **S18 — Veille et développement de carrière :** méthodologies de veille informationnelle et technologique, outils de curation et flux, gestion de son e-réputation et de son identité numérique professionnelle, techniques de valorisation de profil (CV, réseaux pro) et cartographie des métiers du numérique.  
  *Preuve / Contexte de validation :* [Ma veille technologique](veille.md) sur l'IA dans le développement logiciel, ce portfolio, mes profils [GitHub](https://github.com/yayalebledardt) et [LinkedIn](https://www.linkedin.com/in/yanis-h-7988043a5/).
