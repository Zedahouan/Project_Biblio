Guide Complet GitHub/VSCode pour Votre Projet Collaboratif

📌 1. Configuration Initiale (Pour tous les membres)

# Configurer Git (à faire une seule fois par machine)
git config --global user.name "VotreNomGitHub"
git config --global user.email "VotreEmailGitHub"
git config --global init.defaultBranch main

# Vérifier la configuration
git config --list

# Installer l'extension GitHub dans VSCode :
# 1. Onglet Extensions (Ctrl+Shift+X)
# 2. Chercher "GitHub"
# 3. Installer



🚀 2. Pour le Propriétaire du Dépôt (Création Initiale)

# Créer un nouveau projet dans VSCode
# Initialiser le dépôt Git
git init

# Créer les fichiers initiaux (index.html, style.css, etc.)
# Ajouter les fichiers
git add .

# Premier commit
git commit -m "Initial commit"

# Lier à GitHub (après avoir créé le dépôt sur GitHub)
git remote add origin https://github.com/votreNom/bibliotheque-en-ligne.git

# Pousser vers GitHub
git push -u origin main





👥 3. Pour les Collaborateurs (Premier Accès au Projet)

# Cloner le dépôt (chaque collaborateur fait ceci une fois)
git clone https://github.com/votreNom/bibliotheque-en-ligne.git

# Se déplacer dans le dossier du projet
cd bibliotheque-en-ligne

# Ouvrir dans VSCode
code .




🔄 4. Workflow Collaboratif Quotidien
Avant de commencer à travailler (toujours):

# Se synchroniser avec les dernières modifications
git pull origin main

# Créer une nouvelle branche pour votre feature
git checkout -b nom-branche-descriptive
# Exemple: git checkout -b feature-ajout-livres

Pendant le travail:

# Vérifier les modifications
git status

# Ajouter les fichiers modifiés
git add nom-fichier
# Ou pour tout ajouter
git add .

# Faire un commit descriptif
git commit -m "Description claire des modifications"
# Exemple: git commit -m "Ajout de la fonctionnalité de recherche"

Après avoir fini une tâche:

# Pousser la branche vers GitHub
git push -u origin nom-branche-descriptive

# Sur GitHub:
# 1. Aller dans l'onglet "Pull requests"
# 2. Cliquer "New pull request"
# 3. Sélectionner votre branche
# 4. Décrire les modifications
# 5. Demander une revue aux autres

Après approbation de la Pull Request:


# Revenir sur la branche main
git checkout main

# Mettre à jour la branche main locale
git pull origin main

# Supprimer la branche locale (optionnel)
git branch -d nom-branche-descriptive




🛠 5. Gestion des Conflits (Si plusieurs modifient les mêmes fichiers)

# Quand un conflit survient pendant git pull:
# 1. Ouvrir les fichiers avec conflits dans VSCode
# 2. Résoudre manuellement (VSCode aide avec les marqueurs <<<<<<<)
# 3. Après résolution:
git add nom-fichier-conflit
git commit -m "Résolution du conflit dans nom-fichier"
git push origin nom-branche



🔍 6. Commandes Utiles Supplémentaires

# Voir l'historique des commits
git log --oneline --graph

# Annuler des modifications non commitées
git restore nom-fichier

# Annuler le dernier commit (sans perdre les modifications)
git reset --soft HEAD~1

# Récupérer une branche distante que quelqu'un d'autre a créée
git fetch origin
git checkout nom-branche-distante



📋 7. Bonnes Pratiques pour Votre Équipe
Branches :

Toujours travailler sur des branches séparées

Nommer les branches clairement : feature/nom, fix/nom, refactor/nom

Commits :

Messages clairs et descriptifs

Un commit par idée/logique

Synchronisation :

Toujours faire git pull avant de commencer à travailler

Pousser (push) régulièrement votre travail

Review :

Toujours faire des Pull Requests

Demander au moins une revue avant de merger

Fichiers à ajouter :

Créez un .gitignore pour exclure les fichiers inutiles

Gardez un fichier COMMANDS.md avec ces instructions

Ce workflow permettra à vos 3 collaborateurs de travailler efficacement ensemble sur la bibliothèque en ligne. Chaque modification passera par un processus de review avant d'être intégrée au projet principal.
