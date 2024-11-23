# Image and Video Processing

Ce dépôt contient les travaux pratiques réalisés en Python dans le domaine du traitement d'images et de vidéos. Les exercices implémentent des algorithmes de détection de coins et d'arêtes, ainsi que des techniques avancées de suivi d'objets.

---

## 📋 Objectifs

1. **Extraction de caractéristiques dans les images** :
   - Détection de coins avec le détecteur de Harris.
   - Détection d'arêtes avec le filtre de Canny.

2. **Suivi d'objets dans des vidéos** :
   - Implémentation des filtres particulaires pour le suivi simple et complexe d'objets.

---

## 📂 Contenu du Dépôt

### 1. Traitement d'images : Détection de coins et d'arêtes

#### Harris Corner Detector
- **Description** : Localisation des coins dans une image en utilisant l'intensité des changements directionnels.
- **Étapes principales** :
  - Calcul des dérivées partielles.
  - Construction de la matrice d'auto-corrélation.
  - Suppression des non-maxima.
- **Visualisations** :
  - Réponse de Harris en niveaux de gris.
  - Coins détectés superposés à l'image d'entrée.
- **Robustesse** : Testé pour les translations, rotations, et variations d'intensité.


#### Canny Edge Detection
- **Description** : Détection des contours en identifiant les maxima locaux dans la dérivée première de l'image.
- **Étapes principales** :
  - Lissage gaussien.
  - Calcul des gradients (magnitude et direction).
  - Suppression des non-maxima.
  - Seuillage double.
- **Visualisations** :
  - Image lissée.
  - Magnitude et direction des gradients.
  - Arêtes détectées après suppression des non-maxima.

---

### 2. Traitement vidéo : Suivi d'objets

#### Suivi Simple avec Filtres Particulaires
- **Description** : Suivi d'un objet rectangulaire basé sur un histogramme de couleurs constant.
- **Techniques utilisées** :
  - Transition gaussienne pour prédire le mouvement.
  - Mise à jour des poids via la fonction de vraisemblance.
  - Resampling systématique.
- **Paramètres ajustables** :
  - Nombre de particules.
  - Histogramme de couleurs.
  - Modèle de transition.

#### Suivi Complexe avec Filtres Particulaires
- **Description** : Suivi d'objets articulés (par exemple, un corps humain ou une main) dans des vidéos simulées.
- **Points clés** :
  - Modèle de transition haute dimension.
  - Suivi séquentiel des parties de l'objet.
  - Gestion de la malédiction de la dimensionnalité.
- **Tests réalisés** :
  - Vidéos avec objets complexes et bruit de fond.
  - Vitesse variable des objets et occlusions.

---

## 🛠️ Technologies Utilisées
- **Python** (3.x)
- **Bibliothèques principales** :
  - `numpy` pour les calculs matriciels.
  - `scipy` pour le traitement d'images.
  - `matplotlib` pour les visualisations.
  - `opencv` pour le traitement vidéo.

---

## 🎥 Vidéos de Test
- **Sources** :
  - [Vidéo Seq23](https://drive.google.com/file/d/1k4RoERodDDEmLUzy_EhYPUaMlfzkRKVP/view?usp=drive_link)
  - Vidéos générées avec des formes simples (carrés, cercles, etc.) pour tester la robustesse.
- **Visualisations** :
  - Suivi de l'objet cible.
  - Comparaison des erreurs de suivi avec le groundtruth.

---

## 🌟 Points Forts
- Implémentation complète en Python.
- Visualisations détaillées pour mieux comprendre les résultats.
- Tests sur des cas simples et complexes.

---

## 👤 Auteur
- **[Ton Nom](https://github.com/ton_github)**  
Pour toute question ou suggestion, n'hésitez pas à me contacter.
