SUP – Plateforme d’Orientation pour l’Enseignement Supérieur

Domaine : sup.koyebisa.ovh

Présentation

SUP est une plateforme innovante conçue pour faciliter l’orientation et la gestion des candidatures dans l’enseignement supérieur en République du Congo. Elle vise à offrir une expérience simplifiée, sécurisée et centralisée aux étudiants, établissements et institutions partenaires.

Structure du projet

sup/
├── backend/
│   ├── manage.py
│   ├── sup_backend/        # Config Django
│   ├── users/              # App gestion utilisateurs (étudiants, écoles, admins)
│   ├── voeux/              # App gestion des vœux et candidatures
│   ├── formations/         # App gestion des formations
│   ├── diplomes/           # App gestion diplômes numériques
│   ├── notifications/      # App notifications/rappels
│   └── ...
├── frontend/
│   ├── package.json
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/       # Appels API
│   │   └── App.js
│   └── public/
└── README.md


Schéma de base de données (exemple simplifié)

Utilisateur
- id
- type (étudiant, école, admin)
- nom, prénom, date de naissance
- email, mot de passe
- numéro INE (généré)
- date création

Formation
- id
- nom formation
- type diplôme
- domaine
- établissement
- localisation

Vœu
- id
- utilisateur_id (FK)
- formation_id (FK)
- priorité
- statut (en cours, accepté, refusé)
- fichiers (CV, lettre de motivation)

Diplôme
- id
- utilisateur_id (FK)
- fichier (PDF)
- code vérification

Notification
- id
- utilisateur_id (FK)
- texte
- type (mail, in-app)
- date


Plan des routes API principales (exemple)





/api/register (POST) : inscription utilisateur



/api/login (POST) : connexion



/api/voeux/ (GET/POST/PUT/DELETE) : gestion des vœux



/api/formations/ (GET) : liste/recherche formations



/api/candidatures/ (GET) : suivi candidatures



/api/diplomes/ (GET/POST) : diplômes numériques



/api/notifications/ (GET) : notifications

Instructions d’installation (développement)





Prérequis :





Python 3.10+



Node.js 18+ et npm



MariaDB



Git



Cloner le dépôt :
git clone https://github.com/ton-org/sup.git



Backend (Django) :





Créer un environnement virtuel Python : python -m venv venv



Activer l’environnement virtuel : source venv/bin/activate



Installer les dépendances : pip install -r requirements.txt



Configurer la base MariaDB (créer la base et l’utilisateur, mettre à jour settings.py)



Appliquer les migrations : python manage.py migrate



Lancer le serveur : python manage.py runserver



Frontend (React) :





Se placer dans le dossier frontend : cd frontend



Installer les dépendances : npm install



Lancer le serveur de développement : npm start



Accès à l’application :





Backend : http://localhost:8000/



Frontend : http://localhost:3000/

Fonctionnalités principales (aperçu)





Inscription sécurisée pour étudiants, établissements et administrateurs



Soumission et classement des vœux de formations (universités, écoles spécialisées, etc.)



Tableau de bord pour le suivi des candidatures et notifications



Recherche avancée de formations avec filtres multiples



Gestion numérique et sécurisée des diplômes



Interface dédiée pour les établissements (gestion des candidatures, communication)



Notifications et rappels automatiques pour les utilisateurs

NB : Certains détails techniques, algorithmes et fonctionnalités stratégiques ne sont pas rendus publics dans ce dépôt pour des raisons de confidentialité et de protection de la propriété intellectuelle.

Accès au code source

Le code source complet, les spécifications techniques détaillées et les modules stratégiques sont réservés aux collaborateurs autorisés et partenaires validés. Pour toute demande de collaboration, de démonstration ou d’accès, merci de contacter : contact@koyebisa.ovh

Propriété intellectuelle

Ce projet et son concept sont protégés par les lois sur la propriété intellectuelle. Toute reproduction, utilisation ou diffusion non autorisée, partielle ou totale, est strictement interdite.

Licence

Tous droits réservés © 2025 Gael / koyebisa.ovh
Ce dépôt n’est pas open source.

Important





Ce dépôt est privé et son accès est restreint.



Tout collaborateur ou partenaire doit signer un accord de confidentialité (NDA) avant d’accéder au code ou à la documentation technique.

Contact





Responsable projet : Gael (contact@koyebisa.ovh)



Domaine : https://sup.koyebisa.ovh
