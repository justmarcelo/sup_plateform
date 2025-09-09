Structure du code:
orientation_plateform/
├── .gitignore
├── README.md
├── requirements.txt
├── orientation_platform/      # Dossier principal du projet Django
│   ├── manage.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── apps/
│       ├── accounts/
│       ├── formations/
│       ├── voeux/
│       ├── dashboard/
│       ├── diplomes/
│       └── notifications/
├── static/                    # Fichiers statiques (CSS, JS, images)
└── templates/                 # Templates globaux (optionnel)



# Orientation Plateform - MVP

Plateforme d'orientation académique inspirée de Parcoursup, développée avec Django et MariaDB.

## Prérequis
- Python 3.10+
- MariaDB
- Apache2 (ou Nginx) avec mod_wsgi

## Installation
1. Cloner le dépôt :
   ```bash
   git clone https://github.com/ton_utilisateur/orientation_plateform.git
   cd orientation_plateform
