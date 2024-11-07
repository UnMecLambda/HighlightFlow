# **HighlightFlow - Recommandation des Meilleures Actions Sportives**

**HighlightFlow** est une application qui recommande chaque jour les meilleures actions de sport de tes équipes et joueurs préférés. L'application te permet de suivre en temps réel les moments marquants, toujours mis à jour toutes les 24 heures.

## Fonctionnalités

- **Recommandations Quotidiennes** : Chaque jour, HighlightFlow met en avant les meilleures actions sportives (dunks, touchdowns, interceptions, etc.) des joueurs et équipes que tu suis.
- **Personnalisation** : L'application apprend de tes préférences pour recommander les actions les plus pertinentes selon tes goûts sportifs.
- **Mises à Jour en Temps Réel** : Grâce à des flux de données en direct (via Kafka et Java), les moments forts sont constamment actualisés, offrant un contenu frais et dynamique.

## Architecture

### **Technologies utilisées**
- **Backend (Java & Kafka)** : Utilisation de **Java** pour le traitement des données en temps réel et la gestion des flux avec **Kafka**.
- **Recommandations (Python)** : Des algorithmes de machine learning sont utilisés pour recommander des moments marquants basés sur les préférences des utilisateurs.
- **API** : Une API RESTful construite avec **Spring Boot** pour gérer les préférences des utilisateurs et exposer les recommandations.
- **Frontend** : Une interface utilisateur simple et réactive développée avec **React** pour afficher les meilleurs moments du jour.
- **Base de Données** : **MongoDB** pour stocker les données des utilisateurs et des actions recommandées.

### **Flow des Données** 
1. **Flux Kafka** : Kafka gère le flux en temps réel des événements de match et des actions marquantes, qui sont ensuite traités par l'application Java.
2. **Recommandations** : L'algorithme de recommandation Python analyse les événements collectés et génère une liste personnalisée pour chaque utilisateur, qui est ensuite renvoyée via l'API Spring Boot.
3. **Stockage des données** : Les données des utilisateurs et des actions recommandées sont stockées dans MongoDB pour permettre un accès rapide et une personnalisation continue.
4. **Interface Utilisateur** : L'interface React affiche les moments forts en temps réel et permet aux utilisateurs de personnaliser leurs préférences de recommandations.

## Installation

### Prérequis
- **Java 11+** pour le backend.
- **Kafka** pour le streaming des données en temps réel.
- **Python 3.x** et **pip** pour installer les dépendances Python.
- **Node.js** et **npm** pour l'interface frontend.

### **Backend**
1. Clone ce repository :
   ```bash
   git clone https://github.com/ton-utilisateur/HighlightFlow.git
