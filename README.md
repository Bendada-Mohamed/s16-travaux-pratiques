# Séance 16 – Travaux Pratiques : Concevoir une application avec Redux

##  Description
Cette Application est un **exemple pratique d'application React intégrant Redux** pour gérer une liste d'articles.  
L'application permet :

- L'affichage d'une liste d'articles existants
- L'ajout de nouveaux articles via un formulaire
- La gestion centralisée du state avec Redux

Ce TP permet de comprendre **l'architecture Redux** et son intégration dans React.

---

##  Objectifs pédagogiques

- Comprendre les concepts clés de Redux : **state, actions, reducer, store**
- Apprendre à connecter Redux à une application React avec `react-redux`
- Appliquer les concepts pour gérer un **state global** au lieu d'utiliser seulement `useState`
- Organiser un projet React de manière professionnelle

---

##  Architecture du projet
src/
│
├── components/
│ ├── AddArticle.js # Formulaire pour ajouter un nouvel article
│ └── Article.js # Affichage d'un article
│
├── containers/
│ └── Articles.js # Container connecté à Redux
│
├── store/
│ ├── actionCreators.js # Fonctions pour créer les actions
│ ├── actionTypes.js # Définition des types d'actions
│ └── reducer.js # Reducer pour gérer le state
│
├── App.js # Composant principal
└── index.js # Point d'entrée de l'application

---

##  Fonctionnement du projet

### 1. Redux : état global

- **Store** : contient l'état global `articles`
- **Reducer** : met à jour le state en fonction des actions
- **Actions** : objets décrivant les modifications à appliquer au state
- **Connect** : permet à un composant React d'accéder au state et de dispatcher des actions

### 2. Ajouter un article

- L'utilisateur remplit le formulaire `AddArticle`
- Le formulaire déclenche `saveArticle(article)` (dispatch vers Redux)
- Le reducer ajoute le nouvel article à la liste
- La liste affichée par `Articles` se met automatiquement à jour

---

##  Installation et Lancement

### 1. Redux : état global

git clone https://github.com/Bendada-Mohamed/s16-travaux-pratiques.git

### 2. Installer les dependances

cd s16-travaux-pratiques
npm install

### 2. Lancer L'application

npm start

---

##  Conclusion

Ce TP permet de :

+ Maîtriser les bases de Redux dans une application React
+ Séparer la logique métier (state) de la présentation (composants)
+ Créer un projet structuré et maintenable pour de futurs projets plus complexes

##  Mohamed Bendada - Junior Web developper - bendada.mohamed@outlook.com
