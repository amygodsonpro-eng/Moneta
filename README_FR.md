# MONETA 3.0 — Beta 1

Application web progressive (PWA) de gestion financière personnelle et multidevise, conçue pour GitHub Pages et le fonctionnement hors connexion.

## Installation / publication

1. Décompresser l'archive.
2. Ouvrir le dossier `MONETA_iPhone`.
3. Envoyer le contenu du dossier à la racine du dépôt GitHub Pages (ou remplacer les fichiers de l'ancienne version après sauvegarde).
4. Commit / push, puis ouvrir l'URL GitHub Pages dans Safari.
5. Sur iPhone : Safari → Partager → Sur l'écran d'accueil.

## Stockage et migration

- La version 3.0 conserve le nom de base IndexedDB `moneta_local_v1` et le magasin `state` de la version précédente.
- Au premier lancement, elle complète les données historiques avec un profil Personnel et les métadonnées manquantes. Les comptes, transactions et transferts existants restent dans la base.
- Une sauvegarde JSON de la version précédente peut aussi être importée depuis Paramètres.
- **Avant publication, faire une sauvegarde JSON de la version actuellement utilisée.** Ne pas effacer les données Safari / du site pendant la migration.

## Fonctions incluses dans cette bêta

- Profils financiers indépendants avec sélection et création.
- Comptes multidevises, soldes calculés et archivage.
- Revenus, dépenses, transferts, édition et suppression d'opérations.
- Taux globaux au format `1 USD = X devise` et taux historique par transaction.
- Budgets mensuels avec progression et seuils visuels.
- Objectifs d'épargne et contributions.
- Dettes / créances et enregistrement de remboursements.
- Analyses de revenus, dépenses, flux, taux d'épargne et catégories.
- Affichage du patrimoine converti ou soldes séparés par devise.
- Verrouillage local par PIN (hachage SHA-256), export JSON et CSV, restauration JSON.
- Cache PWA et mode hors ligne après première visite réussie.

## Limites connues de cette bêta

Cette version est une base de test fonctionnelle, pas encore la version commerciale finale décrite dans le cahier des charges.

- Les profils ne sont pas encore partageables entre utilisateurs.
- Pas de synchronisation cloud ni de comptes utilisateurs.
- Pas de paiement Premium ni de connexion bancaire.
- Face ID natif non intégré dans cette PWA.
- Les transferts entre profils, les frais en devise distincte, les opérations récurrentes, les pièces jointes, les imports bancaires avancés, les rapports PDF/Excel et la clôture mensuelle restent à développer.
- Les analyses convertissent les montants avec les taux actuellement enregistrés par opération ; elles ne constituent pas un conseil financier.
- Le PIN protège l'interface locale, mais ne chiffre pas à lui seul toute la base IndexedDB.

## Sécurité importante

Les données financières restent dans le stockage local du navigateur. GitHub Pages ne reçoit pas ces données. Faire régulièrement une sauvegarde JSON et la conserver dans un emplacement sûr (par exemple iCloud Drive). Ne jamais déposer une sauvegarde contenant des données personnelles dans le dépôt GitHub public.
