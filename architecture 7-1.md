# 🧑‍💻 Architecture **7-1** en SASS 🌈

L'architecture **7-1** est une méthode super efficace pour organiser ton code **SASS** (ou **SCSS**) de manière claire et structurée. Elle sépare ton code en **7 catégories** distinctes et un fichier principal pour les importer facilement. 🚀

### 🎯 Pourquoi utiliser l'architecture 7-1 ?
- **🔑 Organisation** : Chaque type de style a son propre fichier.
- **📖 Lisibilité** : Le code est bien organisé et facile à naviguer.
- **♻️ Réutilisation** : Les styles, mixins et fonctions sont réutilisables partout.

---

## 📂 Les 7 Catégories de l'Architecture **7-1**

### 1. **Variables** (`_variables.scss`) 🎨
Les variables contiennent les **valeurs réutilisables** dans tout ton projet, comme les couleurs, les tailles de police, les espacements, etc.

**Exemple** :
```scss
// _variables.scss
$primary-color: #3498db;  // Couleur principale
$font-size: 16px;         // Taille de police
$margin: 20px;            // Marge globale
```

### 2. **Mixins** (`_mixins.scss`) 🔄

Les mixins sont des morceaux de code réutilisables. Ils sont très utiles pour appliquer des styles qui se répètent, comme des bordures arrondies.

**Exemple** :

```scss
// _mixins.scss
@mixin border-radius($radius) {
  border-radius: $radius;  // Application du rayon de bordure
}
```

### 3. **Functions** (`_functions.scss`) 🔢

Les fonctions sont des morceaux de code qui retournent une valeur. Par exemple, tu peux créer une fonction pour doubler une valeur numérique.

**Exemple** :

```scss
// _functions.scss
@function double($value) {
  @return $value * 2;  // Retourne la valeur doublée
}
```

### 4. **Base** (`_base.scss`) 🏗️

Les styles de base concernent les éléments HTML généraux comme body, h1, a, etc. Ce fichier est parfait pour définir une réinitialisation des styles ou des valeurs par défaut.

**Exemple** :

```scss
// _base.scss
body {
  font-family: Arial, sans-serif;
  margin: 0;  // Réinitialisation des marges par défaut
}
```

### 5. **Layout** (`_layout.scss`) 🏠

Le fichier layout contient les styles relatifs à la disposition générale de la page : les grilles, les conteneurs, les colonnes, etc.

**Exemple** :

```scss
// _layout.scss
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;  // Centrage du contenu
}
```

### 6. **Components** (`_components.scss`) ⚙️

Les composants sont des éléments réutilisables du site comme les boutons, les cartes, les formulaires, etc. Chaque composant peut avoir son propre fichier.

**Exemple** :

```scss
// _components.scss
.btn {
  padding: 10px 20px;
  background-color: $primary-color;
  color: white;
  border: none;
  cursor: pointer;
  @include border-radius(5px);  // Application du mixin de bordure arrondie
}
```

### 7. **Pages** (`_pages.scss`) 📄

Ce fichier contient les styles spécifiques aux pages. Par exemple, si tu veux personnaliser l'apparence de ta page d'accueil ou de ta page de contact, c'est ici que ça se passe.

**Exemple** :

```scss
// _pages.scss
.homepage {
  background-color: lightgray;
}
```

📝 Le Fichier Principal (main.scss)

Enfin, tu as un fichier principal qui importe tous les autres fichiers SCSS dans un seul endroit pour que ton projet soit facile à gérer.

**Exemple** :

```scss
// main.scss
@use 'variables';    // Import des variables
@use 'mixins';       // Import des mixins
@use 'functions';    // Import des fonctions
@use 'base';         // Import des styles de base
@use 'layout';       // Import de la disposition
@use 'components';   // Import des composants
@use 'pages';        // Import des pages spécifiques
```

📂 Structure du Projet

Voici à quoi ressemble la structure de ton projet SCSS avec l'architecture 7-1 :

```bash
project/
├── sass/
│   ├── base/
│   │   └── _base.scss      (styles de base, reset)
│   ├── components/
│   │   └── _buttons.scss   (composants comme les boutons)
│   ├── layout/
│   │   └── _layout.scss    (structure du site, grilles)
│   ├── pages/
│   │   └── _homepage.scss  (styles spécifiques à la page d'accueil)
│   ├── _functions.scss     (fonctions personnalisées)
│   ├── _mixins.scss        (mixins)
│   ├── _variables.scss     (variables globales)
│   └── main.scss           (fichier principal qui importe tout)
└── css/
    └── styles.css          (fichier CSS généré)
```

✅ Résumé

L'architecture 7-1 te permet de garder ton projet SCSS bien organisé, lisible et facile à maintenir. Chaque type de style a son propre fichier, ce qui facilite la gestion du code à long terme.
