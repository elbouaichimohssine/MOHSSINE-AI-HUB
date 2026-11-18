# MOHSSINE ACCOUNTING

Application web de gestion comptable destinée aux entreprises et cabinets comptables au Maroc.

## Objectif produit

Construire progressivement un logiciel multi-entreprises, sécurisé et vérifiable, adapté aux processus comptables marocains. Le prototype GitHub Pages actuel est une démonstration locale ; il ne doit pas être utilisé pour tenir une comptabilité légale ni pour déposer des déclarations fiscales.

## Principes non négociables

- Chaque écriture comptable doit être équilibrée : total débit = total crédit.
- Aucune écriture validée ne doit être supprimée silencieusement ; les corrections passent par contrepassation et traçabilité.
- Les factures, pièces justificatives, dates, journaux et utilisateurs doivent être traçables.
- Les règles fiscales et le Plan Comptable Général des Entreprises marocain doivent être vérifiés à partir de sources officielles et validés par un professionnel local avant une mise en production.
- Les données de chaque entreprise doivent être isolées.
- Authentification, autorisations, sauvegardes et journal d'audit sont obligatoires avant toute commercialisation.
- Ne jamais stocker de secrets, mots de passe ou clés API dans le code front-end ou dans GitHub.

## Feuille de route

### Étape 1 — Socle produit
- Identité visuelle professionnelle et navigation.
- Fiche entreprise : raison sociale, ICE, IF, RC, adresse, exercice comptable et devise.
- Paramètres et gestion des profils.
- Séparation claire entre données de démonstration et données réelles.

### Étape 2 — Référentiel comptable
- Plan comptable marocain vérifié et versionné.
- Journaux auxiliaires.
- Comptes clients, fournisseurs, banques, caisse, TVA et immobilisations.
- Import/export contrôlé du plan comptable.

### Étape 3 — Saisie comptable
- Écritures en brouillon puis validation.
- Contrôle automatique débit/crédit.
- Numérotation, pièces justificatives, verrouillage des périodes et piste d'audit.
- Grand livre, journal général et balance.

### Étape 4 — Gestion commerciale
- Clients et fournisseurs.
- Devis, factures de vente, factures d'achat et avoirs.
- Règlements, échéances, caisse et banque.
- Rapprochement bancaire.

### Étape 5 — Fiscalité et états
- Suivi TVA selon les règles applicables et leur date d'effet.
- États comptables : bilan, CPC et annexes selon le périmètre réglementaire validé.
- Exports PDF, XLSX et CSV.
- Contrôles et rapprochements.

### Étape 6 — Version SaaS commercialisable
- Backend et base de données relationnelle.
- Authentification robuste, rôles et permissions.
- Isolation multi-tenant et chiffrement des données sensibles.
- Sauvegardes et restauration testées.
- Journal d'audit, supervision, tests, documentation et conditions d'utilisation.
- Hébergement, nom de domaine, support et procédure de mise à jour.

## Architecture cible

- Frontend : application web responsive.
- Backend : API avec validation côté serveur.
- Base de données : PostgreSQL.
- Authentification : fournisseur éprouvé ou mécanisme serveur sécurisé.
- Stockage des pièces : stockage privé avec contrôle d'accès.
- Tests : tests unitaires des calculs, tests d'intégration comptables et tests d'autorisation.

La technologie définitive du backend sera choisie avant l'implémentation de la persistance réelle. GitHub Pages ne fournit pas de backend ni de base de données.

## État actuel

Prototype v0.1 :
- Saisie simple ventes/achats et calcul HT/TVA/TTC.
- Tableau de bord indicatif.
- Export CSV.
- Stockage local dans le navigateur.
- Journal simplifié non conforme à une tenue comptable complète.

**Statut : prototype de démonstration uniquement.**
