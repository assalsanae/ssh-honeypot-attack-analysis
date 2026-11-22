

# 🛡️ Analyse des Attaques SSH avec un Honeypot

Ce projet consiste en la conception et la réalisation d'un **Honeypot SSH** destiné à détecter, enregistrer et analyser les tentatives d'intrusions (attaques par force brute) sans exposer un serveur réel.

## 🎯 Objectifs du projet
* Simuler un serveur SSH vulnérable pour attirer et observer les comportements suspects.
* Enregistrer les informations des tentatives de connexion (adresse IP, nom d'utilisateur, mot de passe testé, date, pays d'origine) dans une base de données locale
* Visualiser les statistiques et les tendances des attaques en temps réel via un tableau de bord web interactif.

## 🏗️ Architecture de la solution
1. **Honeypot SSH (`honeypot.py`) :** Faux serveur SSH développé avec la bibliothèque **Paramiko** qui collecte les tentatives et refuse systématiquement l'accès réel.
2. **Base de données (`database.py`) :** Stockage structuré des tentatives dans une base **SQLite**.
3. **Serveur Web & API (`app.py`) :** Backend développé avec **Flask** exposant les données collectées au format JSON.
4. **Dashboard Web (`dashboard.html`) :** Interface utilisateur permettant de consulter le nombre total d'attaques, les IP uniques, ainsi que les identifiants les plus utilisés.

## 🛠️ Technologies utilisées
* **Langage :** Python
* **Cybersécurité & Réseau :** Paramiko (SSHv2)
* **Base de données :** SQLite
* **Web & Visualisation :** Flask, HTML/CSS, JavaScrip

## 📸 Aperçu du projet
![Aperçu 1](SSH1.jpeg)
![Aperçu 2](SHH2.jpeg)

## 📄 Documentation
Vous trouverez dans ce dépôt le rapport complet du projet (`rapport analyse des attaques .pdf`) détaillant l'état de l'art, l'architecture, l'implémentation et les tests réalisés.

---
*Projet académique réalisé à l'Université Chouaïb Doukkali (UCD) – Encadré par Dr. Aaroud Abdessadek.*
