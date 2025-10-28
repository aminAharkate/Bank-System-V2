 =========================================================== 
 ===========            English           ================== 
 =========================================================== 
# Banking System

A comprehensive C++ console-based banking application that provides complete banking operations including client management, user authentication, currency exchange, and transaction processing.

## Features

### Authentication & Security
- **User Login System** with attempt limiting
- **Role-based permissions** with granular access control
- **Login audit trail** tracking all system access
- **Secure password management**

### Client Management
- **Add new clients** with account creation
- **Update client information** and balances
- **Delete client records** with confirmation
- **Search clients** by account number
- **View all clients** in formatted lists

### Transaction Processing
- **Deposit funds** into client accounts
- **Withdraw funds** with balance validation
- **Transfer money** between accounts
- **Transaction logging** with complete audit trail
- **Balance calculations** and total summaries

### Currency Exchange
- **Multi-currency support** with exchange rates
- **Currency conversion calculator**
- **Real-time rate updates**
- **International banking capabilities**

### User Management
- **Add/Remove system users**
- **Permission management** with bitmask system
- **User activity monitoring**
- **Access control enforcement**

## System Architecture

### Core Classes
- **`clsBankClient`** - Client accounts and transactions
- **`clsUser`** - User authentication and permissions  
- **`clsCurrency`** - Currency exchange operations
- **`clsPerson`** - Base class for personal information

### Utility Classes
- **`clsDate`** - Comprehensive date handling
- **`clsString`** - String manipulation utilities
- **`clsInputValidate`** - Input validation
- **`clsUtil`** - General utilities and helpers

### Screen Classes
- **`clsMainScreen`** - Main application navigation
- **`clsLoginScreen`** - User authentication
- **Transaction Screens** - Deposit, Withdraw, Transfer
- **Management Screens** - Client, User, Currency management

## Project Structure

BankingSystem/
├── Core Classes/
│ ├── clsBankClient.h # Client account management
│ ├── clsUser.h # User authentication & permissions
│ ├── clsPerson.h # Base person class
│ └── clsCurrency.h # Currency exchange
├── Utility Classes/
│ ├── clsDate.h # Date operations
│ ├── clsString.h # String utilities
│ ├── clsInputValidate.h # Input validation
│ └── clsUtil.h # General utilities
├── Screen Classes/
│ ├── Client Screens/ # Client management UI
│ ├── User Screens/ # User management UI
│ ├── Currency Screens/ # Currency exchange UI
│ └── Transaction Screens/# Banking operations UI
├── Data Files/
│ ├── Clients.txt # Client database
│ ├── Users.txt # User database
│ ├── Currencies.txt # Exchange rates
│ ├── TransfersLog.txt # Transaction history
│ └── LoginRegister.txt # Login audit trail
└── main.cpp # Application entry point

## Permission System

The system uses a bitmask-based permission system:

Permission	    Value	    Description
List Clients    	1	      View client lists
Add Client    	  2	      Create new clients
Delete Client    	4	      Remove clients
Update Client    	8	      Modify client info
Find Client    	  16	    Search clients
Transactions    	32    	Process banking operations
Manage Users    	64	    User administration
View Logs    	    128	    Access audit trails
Full Access    	 -1	      All permissions

## Data Persistence
All data is stored in text files:

- Clients.txt - Client accounts and balances

- Users.txt - User credentials and permissions

- Currencies.txt - Exchange rates and currency data

- TransfersLog.txt - Complete transaction history

- LoginRegister.txt - User login records

## Key Design Patterns

- Object-Oriented Design with inheritance and polymorphism

- MVC Architecture separating data, logic, and presentation

- Singleton Pattern for global objects like CurrentUser

- Factory Methods for object creation

- RAII for resource management

## Workflow

- Login → Authentication with attempt limiting

- Main Menu → Navigation based on user permissions

- Operations → Client/User/Currency management

- Transactions → Deposit, withdraw, transfer funds

- Audit Trail → All actions logged for security

## Security Features

1. Login attempt limiting (3 attempts max)

2. Permission-based access control

3. Transaction logging and audit trails

4. Input validation and error handling

5. Secure data persistence

## Sample Data Files

The system includes structured data storage with field separation using #//# delimiters for reliable parsing and data integrity.
 =========================================================== 
 ===========            Française         ================== 
 =========================================================== 
# Système Bancaire

Une application bancaire complète en C++ basée sur la console, offrant toutes les opérations bancaires : gestion des clients, authentification des utilisateurs, change de devises et traitement des transactions.

## Fonctionnalités

### Authentification & Sécurité
- **Système de connexion utilisateur** avec limitation des tentatives
- **Permissions basées sur les rôles** avec contrôle d'accès granulaire
- **Historique des connexions** pour suivre tous les accès au système
- **Gestion sécurisée des mots de passe**

### Gestion des Clients
- **Ajout de nouveaux clients** avec création de compte
- **Mise à jour des informations et soldes des clients**
- **Suppression des dossiers clients** avec confirmation
- **Recherche de clients** par numéro de compte
- **Affichage de tous les clients** sous forme de listes formatées

### Traitement des Transactions
- **Dépôt de fonds** sur les comptes clients
- **Retrait de fonds** avec validation du solde
- **Transfert d'argent** entre comptes
- **Journalisation des transactions** avec historique complet
- **Calculs de soldes** et résumés totaux

### Change de Devises
- **Support multi-devises** avec taux de change
- **Calculateur de conversion de devises**
- **Mise à jour des taux en temps réel**
- **Fonctionnalités bancaires internationales**

### Gestion des Utilisateurs
- **Ajout/Suppression d'utilisateurs du système**
- **Gestion des permissions** avec système de masques de bits
- **Suivi de l'activité des utilisateurs**
- **Application du contrôle d'accès**

## Architecture du Système

### Classes Principales
- **`clsBankClient`** - Comptes clients et transactions
- **`clsUser`** - Authentification et permissions des utilisateurs  
- **`clsCurrency`** - Opérations de change
- **`clsPerson`** - Classe de base pour les informations personnelles

### Classes Utilitaires
- **`clsDate`** - Gestion complète des dates
- **`clsString`** - Utilitaires de manipulation de chaînes
- **`clsInputValidate`** - Validation des entrées
- **`clsUtil`** - Fonctions utilitaires générales

### Classes d’Interface
- **`clsMainScreen`** - Navigation principale de l’application
- **`clsLoginScreen`** - Authentification des utilisateurs
- **Écrans de transaction** - Dépôt, Retrait, Transfert
- **Écrans de gestion** - Gestion des clients, utilisateurs, devises

## Structure du Projet

BankingSystem/  
├── Core Classes/  
│ ├── clsBankClient.h # Gestion des comptes clients  
│ ├── clsUser.h # Authentification & permissions  
│ ├── clsPerson.h # Classe de base pour les personnes  
│ └── clsCurrency.h # Change de devises  
├── Utility Classes/  
│ ├── clsDate.h # Opérations sur les dates  
│ ├── clsString.h # Utilitaires de chaînes  
│ ├── clsInputValidate.h # Validation des entrées  
│ └── clsUtil.h # Fonctions utilitaires  
├── Screen Classes/  
│ ├── Client Screens/ # Interface de gestion des clients  
│ ├── User Screens/ # Interface de gestion des utilisateurs  
│ ├── Currency Screens/ # Interface de change de devises  
│ └── Transaction Screens/ # Interface des opérations bancaires  
├── Data Files/  
│ ├── Clients.txt # Base de données des clients  
│ ├── Users.txt # Base de données des utilisateurs  
│ ├── Currencies.txt # Taux de change  
│ ├── TransfersLog.txt # Historique des transactions  
│ └── LoginRegister.txt # Journal des connexions  
└── main.cpp # Point d’entrée de l’application

## Système de Permissions

Le système utilise un masque de bits pour gérer les permissions :

| Permission             | Valeur | Description                        |
|------------------------|--------|------------------------------------|
| Lister les clients     | 1      | Voir les listes de clients         |
| Ajouter un client      | 2      | Créer de nouveaux clients          |
| Supprimer un client    | 4      | Supprimer des clients              |
| Modifier un client     | 8      | Mettre à jour les informations     |
| Rechercher un client   | 16     | Rechercher par numéro de compte    |
| Transactions           | 32     | Effectuer des opérations bancaires |
| Gérer les utilisateurs | 64     | Administration des utilisateurs    |
| Voir les journaux      | 128    | Accéder aux historiques            |
| Accès complet          | -1     | Toutes les permissions             |

## Persistance des Données

Toutes les données sont stockées dans des fichiers texte :

- Clients.txt - Comptes clients et soldes  
- Users.txt - Identifiants et permissions  
- Currencies.txt - Taux de change et devises  
- TransfersLog.txt - Historique complet des transactions  
- LoginRegister.txt - Journal des connexions utilisateurs

## Principaux Modèles de Conception

- Programmation orientée objet avec héritage et polymorphisme  
- Architecture MVC séparant les données, la logique et l’interface  
- Singleton pour les objets globaux comme `CurrentUser`  
- Méthodes de fabrique pour la création d’objets  
- RAII pour la gestion des ressources

## Flux de Travail

- Connexion → Authentification avec limitation des tentatives  
- Menu principal → Navigation selon les permissions  
- Opérations → Gestion des clients, utilisateurs, devises  
- Transactions → Dépôt, retrait, transfert de fonds  
- Journalisation → Toutes les actions sont enregistrées

## Fonctionnalités de Sécurité

1. Limitation des tentatives de connexion (3 max)  
2. Contrôle d’accès basé sur les permissions  
3. Journalisation des transactions et audit  
4. Validation des entrées et gestion des erreurs  
5. Persistance sécurisée des données

## Fichiers de Données Exemple

Le système utilise un format structuré avec des délimiteurs `#//#` pour garantir l'intégrité des données et faciliter l'analyse.
