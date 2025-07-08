# Semantic Similarity NLP API

Ce projet est une **API REST** développée avec **Flask**, utilisant un modèle de traitement du langage naturel (NLP) basé sur **Sentence Transformers** (`all-mpnet-base-v2`) pour analyser la similarité sémantique entre des questions posées par un utilisateur et une base de FAQ stockée dans une base de données **MySQL**.

---

## Fonctionnalités principales

- 🔍 **Analyse de similarité sémantique**  
  Calcule la similarité entre une question utilisateur et un ensemble de questions FAQ existantes pour trouver la réponse la plus pertinente.

- 🧹 **Prétraitement avancé du texte**  
  Nettoyage, suppression de la ponctuation, lemmatisation afin d'améliorer la qualité des embeddings.

- 📋 **Support pour requêtes simples et multiples**  
  Endpoints pour analyser une question unique ou un lot de questions en une seule requête.

- 🔗 **Connexion dynamique à une base MySQL**  
  Récupération des questions et réponses FAQ en temps réel.

- ⚙️ **Seuil de similarité configurable**  
  Garantie la pertinence des réponses proposées (seuil par défaut : 50%).

---

## Endpoints API

| Endpoint                | Méthode | Description                                     |
|-------------------------|---------|------------------------------------------------|
| `/similarityQuestion`   | POST    | Obtenir la meilleure réponse pour une question unique. |
| `/similarityQuestions`  | POST    | Obtenir les meilleures réponses pour une liste de questions. |
| `/allQuestions`         | GET     | Récupérer toutes les questions FAQ disponibles. |

---

## Technologies utilisées

- 🐍 **Python** & **Flask** (API REST)  
- 🤗 **Sentence Transformers** (`all-mpnet-base-v2`) pour l'encodage sémantique  
- 📚 **NLTK** pour le prétraitement linguistique  
- 🛢️ **MySQL** pour la gestion des données FAQ  

---

## Cas d’usage

Cette API est idéale pour intégrer un système de FAQ intelligent dans un service client, un chatbot ou toute application web nécessitant une compréhension sémantique avancée des questions utilisateurs pour fournir des réponses pertinentes automatiquement.

