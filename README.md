# Projet E-commerce en Django

Ce projet est une application web e-commerce développée avec Django. Il a été réalisé en plusieurs étapes (Ateliers) pour mettre en place la structure du projet, la base de données PostgreSQL, les modèles, les vues, et l'intégration des templates HTML avec héritage. Ce document trace mon avancement sur le projet, étape par étape.

## 🎯 Objectifs du Projet
- Création d'une application e-commerce avec le framework Django.
- Gestion des produits et des catégories de produits.
- Mise en place et configuration d'une base de données **PostgreSQL**.
- Gestion de l'upload d'images via le système de médias de Django.
- Utilisation du système de templates Django (héritage pour optimiser le code).

---

## 🚀 Étapes de Réalisation (Démarche)

### Atelier 1 : Initialisation et Configuration de Base
Dans cette première étape, la structure de base du projet a été mise en place.

1. **Environnement et Installation :** Création de l'environnement virtuel et installation de Django via le terminal.
   - ![Installation terminal](Atelier1/Installation%20terminal.png)
   - ![Installation terminal 2](Atelier1/Installation%20terminal2.png)
   - ![Installation terminal 3](Atelier1/Installation%20terminal%203.png)
   
2. **Création du Projet et de l'Application :** 
   - Initialisation du projet principal `ecommerce`.
   - Création de l'application `products` et enregistrement de celle-ci dans la liste des `INSTALLED_APPS` (fichier `settings.py`).
   - ![Création app produit](Atelier1/creation%20app%20produit.png)
   - ![Ajout de products dans setting](Atelier1/Ajout%20de%20products%20dans%20setting.png)

3. **Vues et Routage (URLs) :**
   - Création de fonctions basiques dans `views.py` (de l'app `products`).
   - ![Ajout de fonctions dans views.py](Atelier1/ajout%20de%20fonctions%20dans%20views.py%20au%20niveau%20de%20products.png)
   - Configuration des URLs au niveau de l'application `products` et liaison au fichier `urls.py` principal du projet.
   - ![Création et modification urls.py products](Atelier1/creation%20et%20modification%20de%20urls.py%20au%20niveau%20de%20products%20.png)
   - ![Modification urls.py ecommerce](Atelier1/modification%20urls.py%20dans%20le%20dossier%20ecommerce.png)

4. **Templates Initiaux :** Création des fichiers HTML basiques pour l'affichage (`product_list.html` et `product_detail.html`).
   - ![Modification product_list](Atelier1/modification%20du%20html%20de%20product_list.png)
   - ![Modification product_detail](Atelier1/modification%20du%20html%20de%20product_detail.png)

5. **Démarrage :** Lancement du serveur de développement et test de l'affichage.
   - ![Lancer serveur vscode](Atelier1/lancer%20serveur%20dans%20vscode.png)
   - ![Affichage pages produits](Atelier1/Affichage%20de%20la%20page%20des%20produits.png)
   - ![Affichage détails produits](Atelier1/Affichage%20de%20la%20page%20des%20details%20des%20produits.png)

### Atelier 2 : Modèles, Base de Données et Administration
Cette étape s'est concentrée sur la persistance des données, la relations entre entités et l'interface d'administration.

1. **Création des Modèles de Données :**
   - Création du modèle `Product` et `Category` dans `models.py`.
   - ![Modification 1 models.py](Atelier2/1.modification%20du%20fichier%20models.py%20dans%20products.png)
   - ![Ajout category models.py](Atelier2/ajout%20de%20category%20dans%20models.py%20dans%20le%20dossier%20products.png)
   - ![Modification 2 models.py](Atelier2/4.modification%202%20du%20fichier%20modes.py%20dans%20products.png)

2. **Migrations et Mise à Jour de la Base de Données :**
   - ![Migration 1](Atelier2/2.Migration%20png.png)
   - ![Création table product](Atelier2/3.creation%20table%20product%20.png)
   - ![Mise a jour base de donnees](Atelier2/5.%20mise%20a%20jour%20de%20la%20base%20de%20donnee%20.png)

3. **Interface d'Administration :**
   - Enregistrement des modèles et personnalisation dans `admin.py`.
   - ![Modification admin.py](Atelier2/6.%20modification%20du%20fichier%20admin.png)
   - ![Modification admin 2](Atelier2/15.modification%20de%20admin.py%20dans%20le%20dossier%20product.png)

4. **Intégration de PostgreSQL :**
   - Configuration du fichier `settings.py` pour basculer de SQLite vers PostgreSQL.
   - ![Migration postgresql](Atelier2/17.Migration%20vers%20ma%20base%20de%20donnee%20creer%20sur%20postgresql.png)
   - ![Migration reussie](Atelier2/18.Migration%20reussi.png)

5. **Gestion des Fichiers Médias (Images) :**
   - ![Dossier images produits](Atelier2/12.ajout%20du%20dossier%20image%20pour%20les%20images%20produits.png)
   - ![Modification setting.py](Atelier2/13.modification%20de%20setting.py.png)

6. **Mise à jour des Vues, URLs et Templates :** 
   - Adaptation au vrai schéma de BDD.
   - ![Modification views.py](Atelier2/7.modification%20du%20fichier%20views.py%20dans%20products.png)
   - ![Modification urls.py products](Atelier2/8.modification%20du%20fichier%20urls.py%20dans%20products.png)
   - ![Modification urls.py ecommerce](Atelier2/14.modification%20de%20urls.py%20du%20dossier%20ecommerce.png)
   - ![Modification product_list.html](Atelier2/9.modification%20de%20product_list.html%20.png)
   - ![Modification category_list.html](Atelier2/10.modification%20de%20category_list.html.png)
   - ![Modification product_detail.html](Atelier2/11.modification%20de%20product_detail.html.png)

### Atelier 3 : Optimisation des Templates (Héritage)
Cette dernière étape a permis de factoriser le code HTML pour respecter le principe DRY.

1. **Création du Template de Base :** 
   - Création d'un fichier `base.html` structurant le socle commun des pages.
   - ![Heritage base.html](Atelier3/1.Heritage%20avec%20base.html.png)

2. **Héritage dans les vues existantes :** 
   - Utilisation de `{% extends 'products/base.html' %}`.
   - ![Product detail html](Atelier3/2.Product_detail.png)
   - ![Product list html](Atelier3/3.Product_list.html.png)

3. **Vérification de la base de données :**
   - Preuve des migrations vers la base de données PostgreSQL finales.
   - ![Migration base de donnée](Atelier3/Migration%20base%20de%20donne.png)
   - ![Migration réussie dans postgresql](Atelier3/Migration%20reussi%20dans%20postgresql.png)

---

## 🛠️ Technologies Utilisées
- **Backend :** Python, Django
- **SGBD (Base de données) :** PostgreSQL
- **Frontend :** HTML, CSS (moteur de Template Django)

---

## 📦 Instructions d'Installation (Local)

Si vous souhaitez cloner et tester ce projet en local, voici la marche à suivre :

1. **Cloner le dépôt :**
   ```bash
   git clone <URL_DU_DEPOT_GITHUB>
   cd ecommerce
   ```

2. **Créer et activer l'environnement virtuel :**
   ```bash
   # Création
   python -m venv myenv
   
   # Activation sous Windows
   myenv\Scripts\activate
   
   # Activation sous macOS / Linux
   source myenv/bin/activate
   ```

3. **Installer les dépendances requises :**
   ```bash
   pip install django psycopg2   # psycopg2 est le connecteur pour PostgreSQL
   ```

4. **Configuration de la Base de Données :**
   - Vous devez disposer d'un serveur PostgreSQL local ou distant.
   - Dans le fichier `ecommerce/settings.py`, modifiez le dictionnaire `DATABASES` avec vos propres informations d'identification (Nom DB, Utilisateur, Mot de passe).

5. **Exécuter les Migrations :**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Créer le compte Administrateur :**
   ```bash
   python manage.py createsuperuser
   ```

7. **Démarrer le Serveur :**
   ```bash
   python manage.py runserver
   ```
   Rendez-vous ensuite sur `http://127.0.0.1:8000/` pour visualiser l'application, et sur `http://127.0.0.1:8000/admin/` pour gérer les produits/catégories.
