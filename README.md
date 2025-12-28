# 📚 Bibliothèque scolaire – Base de données MySQL

## 📌 Description
Ce projet consiste à concevoir et implémenter une base de données relationnelle pour la gestion d’une **bibliothèque scolaire**.  
La base permet de gérer les auteurs, les ouvrages, les abonnés et les emprunts tout en garantissant l’intégrité et la cohérence des données.

---

## 🎯 Objectifs
- Analyser un besoin métier réel
- Concevoir un modèle entité–relation (ER)
- Appliquer les règles de normalisation (1NF, 2NF, 3NF)
- Implémenter la base de données sous MySQL
- Utiliser des contraintes pour assurer la cohérence des données

---

## 🗂️ Entités et attributs

### Auteur
- id (INT, clé primaire)
- nom (VARCHAR)

### Ouvrage
- id (INT, clé primaire)
- titre (VARCHAR)
- disponible (BOOLEAN)
- auteur_id (clé étrangère)

### Abonné
- id (INT, clé primaire)
- nom (VARCHAR)
- email (VARCHAR, unique)

### Emprunt
- ouvrage_id (clé étrangère)
- abonne_id (clé étrangère)
- date_debut (DATE)
- date_fin (DATE, optionnelle)

---

## 🔗 Relations
- Un **auteur** peut écrire plusieurs **ouvrages**
- Un **abonné** peut effectuer plusieurs **emprunts**
- Un **emprunt** relie un **abonné** à un **ouvrage**
- Un ouvrage ne peut pas être supprimé s’il est emprunté

---

## 🧩 Normalisation
- **1NF** : attributs atomiques
- **2NF** : dépendance complète à la clé primaire
- **3NF** : absence de dépendance transitive

---

## 🛠️ Technologies utilisées
- MySQL 8.0
- Moteur de stockage : InnoDB
- Encodage : UTF-8 (utf8mb4)

---


## Cptures décrans ;  
<img width="1303" height="272" alt="image" src="https://github.com/user-attachments/assets/fae85b32-1ab1-4bdd-b98a-ce5186383457" /> <br>
<img width="1103" height="725" alt="image" src="https://github.com/user-attachments/assets/73058db2-1ee3-4e85-9709-e3fba9e19d98" />

## Connexion à MySQL
```bash
mysql -u root -p --port=3307

