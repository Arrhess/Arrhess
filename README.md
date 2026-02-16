## ÉVALUATION EN COURS DE FORMATION 
TP – Developpeur Web et Web Mobile

## Énoncé

**Votre examen comporte :**

✔ Cet énoncé qui vous présente le sujet de l’épreuve

✔ Une copie à rendre (Excel ou Word) que vous devez télécharger, remplir informatiquement et déposer dans l’espace de dépôt prévu à cet effet. 

Renommer votre copie à rendre Word ou Excel comme suit : ECF_TPDeveloppeurWebEtWebMobile_copiearendre_NOM_Prenom

# Objectifs de l’évaluation : 

L’évaluation en cours de formation que vous allez réaliser a pour vocation de figurer dans votre livret d’évaluation. Il sera donc remis à votre jury le jour des épreuves du titre professionnel accompagné de votre évaluation et du sujet initial. 
Nous vous demandons de vous mettre en situation d’examen. Prenez le temps de lire le sujet et de manipuler les annexes afin de répondre en situation professionnelle aux questions et problématiques évoquées dans le sujet.

## À vous de jouer ! 

## Informations

**Github** : (https://github.com/Arrhess/ECF_TPDeveloppeurWebEtWebMobile_copiearendre_RICOUARD_Romain)

**Démonstration** : <span style="color:red">**url du site**</span>

    Adresse email démo      : admin@viteetgourmand.fr
    Mot de passe démo       : admin


## Réflexion et configuration de l'environnement de travail

**Résumé du besoin et choix des technologies**

Les deux associés, Julie et José, ont besoin d'avoir un site leur permettant d'avoir plus de visibilité pour leur societé, mais également pour permettre aux clients de passer leurs commandes de manière rapide et simple.

Les associés ont besoin de sécuriser l'accès aux modifications des données et d'attribuer 3 rôles: administrateur, employés et visiteurs du site.

Julie et José ont besoin de montrer leurs différents menus. Pour cela un site dynamique sera en effet mis en évidence pour leur permettre de répondre à leurs besoins.

Pour le Backend, le langage PHP s'est imposé. Language très utilisé de nos jours, et des serveurs pouvant être simple à configurer. Les données seront confiées à MySQL pour répondre aux besoins de l'examen.

Pour la partie Frontend, le choix s'est tourné simplement sur une page web HTML avec du CSS.

## Configuration de l'environnement de travail

Travaillant sur un système d'exploitation de type Windows, les informations ci-dessous y seront donc destinées :

- **Serveur:**
    + Apache
    + PHP 8.2
    + MySQL 10.4 / PDO

- **Backend :**
    + PHP 8.2
    + MySQL 8.0 / PDO

- **Frontend :**
    + HTML 5
    + CSS 3
 

## Utilisation :

Pour commencer, il faut télécharger et installer le logiciel XAMPP depuis le lien suivant : https://www.apachefriends.org/fr/index.html


Ainsi que MySQL depuis le lien suiant : https://www.postgresql.org/


Une fois ces étapes réalisées, pour accéder au projet en local, il faudra télécharger le dossier ZIP de ce projet depuis le GitHub, dont le lien a été fourni plus haut.  Puis il faudra décompresser le fichier pour accéder à l'ensemble du projet depuis votre bureau.

## Les options de connection à la base de données :

Pour que le projet soit fonctionnel, il faudra faire attention à ce que les paramètres de votre serveur soient compatibles avec le projet. Pour ce faire, il faudra verifier les paramètres suivants depuis le panneau de contrôle XAMPP :

Apache --> Config --> config.inc.php
- **Authentication type and info :**
    + $cfg['Servers'][$i]['auth_type'] = 'config';
    + $cfg['Servers'][$i]['user'] = 'root';
    + $cfg['Servers'][$i]['password'] = '';
    + $cfg['Servers'][$i]['extension'] = 'mysqli';
    + $cfg['Servers'][$i]['AllowNoPassword'] = true;
    + $cfg['Lang'] = '';
    + $cfg['Servers'][$i]['port'] = 3307;
 
Mysql --> Config --> config.inc.php

    Port = 3307

## Création de la base de données en local :

Pour permettre de faire les liens avec la base de données, il faudra donc depuis votre serveur local créer une nouvelle base de données "vite&gourmand" contenant 3 tables :


**Table "user" :**

Attention de respecter la nomenclature des différents champs créés dans cette base de données :


+ "ID" --> Type 'INT' AUTO_INCREMENT
+ "Email" --> Type 'text'
+ "Password" --> Type 'VARCHAR (255)'
+ "prenom" --> Type 'VARCHAR (255)'
+ "telephone" --> Type 'VARCHAR (255)'
+ "ville" --> Type 'VARCHAR (255)'
+ "pays" --> Type 'VARCHAR (255)'
+ "adresse" --> Type 'VARCHAR (255)'
+ "Cp" --> Type 'INT(11)
+ "Role" --> Type 'VARCHAR (255)'

<img width="734" height="229" alt="Table_user" src="https://github.com/user-attachments/assets/da9c950f-861f-4c0b-863b-87b80ee3900b" />


**Table "menus" :**


Attention de respecter la nomenclature des différents champs créés dans cette base de données :


+ "menu_id" --> Type 'int(11)' AUTO_INCREMENT
+ "titre" --> Type 'varchar(50)'
+ "nb_pers_mini" --> Type 'int(11)'
+ "prix_pers" --> Type 'double'
+ "regime" --> Type 'varchar(50)'
+ "description" --> Type 'varchar(50)'
+ "quantite_restante" --> Type 'int(11)'
+ "libelle" --> Type 'varchar(255)'

<img width="763" height="185" alt="Table_menus" src="https://github.com/user-attachments/assets/92256a97-2751-46c2-91bc-1f6a5417deba" />


**Table "commande" :**

Attention de respecter la nomenclature des différents champs créés dans cette base de données :


+ "numero_commande" --> Type 'varchar(50)' AUTO_INCREMENT
+ "date_commande" --> Type 'date'
+ "date_prestation" --> Type 'date'
+ "heure_livraison" --> Type 'varchar(50)'
+ "prix_total" --> Type 'double'
+ "nombre_personne" --> Type 'int(11)'
+ "prix_livraison" --> Type 'double'
+ "statut" --> Type 'varchar(50)'
+ "pret_materiel" --> Type 'tinyint(1)'
+ "restitution_materiel" --> Type 'tinyint(1)'
+ "Email" --> Type 'varchar(255)'
+ "prenom" --> Type 'varchar(255)'
+ "adresse" --> Type 'varchar(255)'
+ "ville" --> Type 'varchar(255)'
+ "pays" --> Type 'varchar(255)'
+ "telephone" --> Type 'varchar(10)'
+ "mousse_chocolat" --> Type 'int(11)'
+ "flan" --> Type 'int(11)'
+ "tarte_pomme" --> Type 'int(11)'


<img width="576" height="334" alt="Table_commande" src="https://github.com/user-attachments/assets/dbc88ec3-66cd-47a3-91f2-4c7158b0db65" />

## Création du compte "Admin sur la base de données "user" :


## Lecture du projet en local depuis le navigateur :

Une fois toutes ces étapes réalisées, il est temps de naviguer sur ce projet depuis votre navigateur. Pour cela, ouvrez le fichier "index.php" sur votre navigateur.


Vous arrivez sur la page d'accueil du site. Il faudra pour commencer créer votre compte admin.


## Création du compte "Admin" depuis le site :


Dirigez-vous vers le menu "connection" puis cliquez sur "nouveau membre".


Voici les champs à remplir pour paramétrer votre compte admin :


+ "Email" --> "admin@viteetgourmand.fr"
+ "Mot de passe" --> "admin"
+ "prenom" --> "admin"
+ "telephone" --> "1234567890"
+ "ville" --> "Bordeaux"
+ "pays" --> "France"
+ "adresse" --> "4 rue de bordeaux"
+ "Cp" --> "33000"

  - Votre compte admin est maintenant créé dans la base de données. Ces identifiants vous permettront d'avoir accès à différentes parties du site auxquelles les "visiteurs" n'ont pas accès.
 

## Création du compte "Employé" depuis le site :

- Dirigez-vous vers le menu "espace administrateur" puis remplissez les champs suivants :

    + "Email" --> "employe@viteetgourmand.fr"
    + "Mot de passe" --> "employe"

- Appuyez sur le bouton "créer l'utilisateur" puis remplissez les champs suivants sans restriction de valeur :

    + "prenom" --> "employe"
    + "telephone" --> "1234567890"
    + "ville" --> "Bordeaux"
    + "pays" --> "France"
    + "adresse" --> "4 rue de bordeaux"
    + "Cp" --> "33000"

- Cochez obligatoirement la case "employé" puis cliquez sur "enregistrer".

  Votre compte "employé" est maintenant créé !

  ## Déscription du site :

  Maintenant que vos différents comptes ont été créés, vous pouvez vous ballader sur le site pour étudier l'ensemble des fonctionnalités.


  - Accueil :
  

  Cette page est accessible à tout le monde et vous permet de voir le profil des deux associés Julie et José.

  - Espace administrateur :
  

  Cette page est accessible uniquement aux membres de type "Admin" et "Employé". Elle vous permet d'avoir accès à l'ensemble des commandes et de modifier leurs statuts.
  Si le compte connecté est celui de l'admin, il aura donc la possibilité d'ajouter un nouvel utilisateur.


  Pour modifier le statut d'une commande, il suffit de remplir le champs "Cmd" avec le numéro de commande à modifier, puis de cliquer sur le bouton "modifier".


  Cela redirige l'utilisateur vers une page de modification de commande. Il lui faudra juste cocher la case correspondante à son souhait puis de cliquer sur "valider" pour mettre à jour l'état de la commande.


  - déconnexion :
  
  Ce lien permet simplement de déconnecter l'utilisateur et de le rediriger vers la page d'accueil.


   - tous les menus :

  Cette page vous donne accès aux différents menus proposés par les deux collaborateurs.


  Si vous ètes un "admin" ou un "employé" il vous sera possible de cliquer sur le bouton "nouveau menu" après avoir saisi le nom du menu que vous souhaitez ajouter.

  Il vous sera également possible de supprimer un menu en indiquant son nom, puis en cliquant sur le bouton "supprimer le menu".


  Pour tous les autres utilisateurs, cette page leur permet donc de visualiser les menus et d'en commander, en cliquant sur le titre du menu choisi.

  - ajout d'un menu :
 
  Lorsqu'un admin ou un employé souhaite ajouter un menu, après avoir cliqué sur le bouton "nouveau menu", il sera demandé de remplir les différents champs pour incrémenter la base de données, ainsi que de télécharger un fichier image qui servira d'illustration dans la page "tous les menus".


   - contact :
  
  Cette page vous donne accès au contact du restaurant.


  - Formulaire de commande de menu :
  

  Après avoir cliqué sur le titre du menu choisi, le site vous redirige vers le formulaire de commande.

  Il vous suffira de remplir les champs du formulaire puis de cliquer sur le bouton "valider la commande" pour avoir accès au récap de votre commande.


  - Récap de votre commande :
  
  Sur cette page, le récap de votre commande avec le tarif associé vous sera affiché. Si la commande vous convient, vous pouvez donc cliquer sur le bouton "valider la commande".

  Le site vous redirige automatiquement vers votre espace personnel où toutes les commandes étant associées à votre e-mail seront affichées.















