# VetCampus – EISMV Dakar (frontend)

Fichiers : index.html, style.css, data.js, app.js (à placer dans le même dossier).
Lancer : ouvrir index.html (ou clic droit > Open with Live Server dans VS Code).

## Où modifier
- data.js : maquette de formation (12 semestres, UE, EC, crédits).
- style.css : couleurs (variables --pri, --navy en haut du fichier).
- app.js : pages, filtres, espace administrateur, comptes.

## Organisation
- 6 niveaux : L1 (S1+S2), L2 (S3+S4), L3 (S5+S6), M1 (S7+S8), M2 (S9+S10), D1 (S11+S12).
- Chaque matière (élément constitutif d'une UE) a sa propre page : cours, TD, TP, présentations, anciens sujets.

## Administration (démo)
Compte principal initial : admin@eismv.sn / Admin2026!  (à changer à la première connexion, onglet « Mon compte »)
- Administrateur principal (unique) : crée, désactive et supprime les administrateurs, réinitialise les mots de passe,
  choisit les niveaux autorisés de chacun, gère les UE et leurs matières, consulte le journal.
- Administrateurs : ajoutent, renomment et suppriment documents et sujets, uniquement dans leurs niveaux.
ATTENTION : en frontend seul, les comptes sont stockés dans le navigateur. Ce n'est PAS sécurisé.
Pour la vraie version, passer à Supabase (Auth + Postgres + Storage) en remplaçant :
DB.load / DB.save, hs() et login(), addDoc, addExam, addUe, addAcc, togAcc, resetPw, delAcc.
