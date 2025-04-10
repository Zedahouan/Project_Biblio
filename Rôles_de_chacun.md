 Voici une version très détaillée, claire et pédagogique des rôles pour chacun de vous trois (TPZ, BONI JERIEL, MOHAMMAD), en expliquant chaque technologie (PHP, HTML, CSS, JavaScript) avec leurs fonctions en français, et qui doit faire quoi exactement dans le projet. L’objectif est que même en tant que débutants, vous puissiez comprendre votre mission.

⸻

1. TPZ — Administrateur / Chef de projet

Son rôle principal :
	•	Gérer tout le contenu de la bibliothèque (livres, utilisateurs…)
	•	Superviser que le travail avance bien et que tout fonctionne
	•	Accéder à un tableau de bord réservé à l’administrateur (page /admin)
	•	Tester ce que les autres ont codé

Ce que TPZ va utiliser :

PHP (langage serveur) :
	•	Pour créer les pages de gestion (ajouter/modifier/supprimer un livre)
	•	Pour afficher les statistiques : combien de livres empruntés, combien d’utilisateurs, etc.
	•	Pour afficher les listes de livres et d’utilisateurs dans des tableaux dynamiques

HTML (structure de page) :
	•	Créer les éléments de la page : formulaires, tableaux, boutons, titres

CSS (design/esthétique) :
	•	Utiliser un style simple et propre pour bien présenter la page admin (peut utiliser Bootstrap qui est une bibliothèque de design prête à l’emploi)

JavaScript (interactions dynamiques, en option) :
	•	Par exemple : afficher une alerte avant de supprimer un livre
	•	Ou recharger une partie de la page sans tout actualiser (niveau plus avancé, pas obligatoire au début)

Tâches concrètes à faire pour TPZ :
	•	Créer la page /admin avec des onglets :
	•	Gérer les livres : ajouter, modifier, supprimer
	•	Gérer les utilisateurs
	•	Voir les statistiques
	•	Protéger l’accès à cette page (elle ne doit être visible que si l’utilisateur est “admin”)
	•	Tester les pages créées par les autres membres

⸻

2. BONI JERIEL — Développeur expérimenté

Son rôle principal :
	•	Gérer la connexion des utilisateurs
	•	Créer le lien entre le site et la base de données
	•	Faire en sorte que les livres puissent être empruntés ou réservés
	•	S’occuper de la sécurité du site (comptes, mots de passe, etc.)

Ce que BONI va utiliser :

PHP (langage serveur) :
	•	Pour faire fonctionner la logique du site :
	•	Connexion et déconnexion
	•	Vérifier que les données sont correctes
	•	Ajouter un livre à la base de données
	•	Enregistrer un emprunt ou une réservation
	•	PHP va récupérer les données entrées dans les formulaires HTML et les traiter

MySQL (base de données) :
	•	Créer les tables pour stocker :
	•	les utilisateurs
	•	les livres
	•	les emprunts
	•	les réservations

HTML (structure de page) :
	•	Créer les formulaires de connexion et d’inscription
	•	Créer les champs pour permettre à un utilisateur de réserver ou emprunter

CSS (design) :
	•	Appliquer un style simple aux formulaires pour que ça soit lisible

JavaScript (optionnel) :
	•	Valider les champs avant l’envoi (ex : vérifier que l’email est bien écrit)
	•	Afficher des messages d’erreur sans recharger la page (ex : “mot de passe incorrect”)

Tâches concrètes à faire pour BONI :
	•	Créer la base de données avec les tables nécessaires (users, books, borrows…)
	•	Créer les pages /register, /login, /profile
	•	Protéger les pages privées (ex : on ne peut accéder au profil que si on est connecté)
	•	Créer les actions pour emprunter ou réserver un livre (page /books/:id)

⸻

3. MOHAMMAD — Développeur front-end

Son rôle principal :
	•	Créer les pages visibles au public
	•	Afficher les livres, les détails d’un livre, la page d’accueil, etc.
	•	S’assurer que le site est joli et agréable à utiliser

Ce que MOHAMMAD va utiliser :

HTML (structure de page) :
	•	Construire l’apparence des pages :
	•	Titres
	•	Images des livres
	•	Résumés
	•	Liens vers les détails

CSS (design/esthétique) :
	•	Embellir les pages (couleurs, marges, polices…)
	•	Rendre le site responsive (qui s’adapte aux téléphones et tablettes)

PHP (affichage dynamique) :
	•	Utiliser PHP pour afficher les livres depuis la base de données
	•	Exemples :
	•	afficher automatiquement la liste des livres sur la page /books
	•	afficher les détails d’un livre avec son titre, auteur, couverture…

JavaScript (facultatif pour les filtres) :
	•	Ajouter des filtres sans recharger la page (ex : trier par genre)
	•	Ou afficher un message quand un livre est cliqué

Tâches concrètes à faire pour MOHAMMAD :
	•	Créer la page d’accueil (/) avec :
	•	le logo
	•	un message d’accueil
	•	un bouton pour s’inscrire/se connecter
	•	une sélection de livres populaires
	•	Créer la page /books avec les filtres et la liste de tous les livres
	•	Créer la page /books/:id avec les infos détaillées d’un seul livre
	•	Créer la page d’erreur 404

⸻

Résumé des tâches principales

Nom	Tâches principales	Technologies utilisées
TPZ (admin)	Tableau de bord admin, supervision du projet	PHP (logique), HTML/CSS (structure et style), un peu JavaScript
BONI (dev back-end)	Authentification, base de données, logique des emprunts	PHP (traitement), MySQL (données), HTML/CSS, un peu JavaScript
MOHAMMAD (dev front-end)	Pages publiques, design, affichage des livres	HTML/CSS (front), PHP (affichage dynamique), un peu JavaScript


