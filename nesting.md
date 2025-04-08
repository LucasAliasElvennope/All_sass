1. Copie le contenu de la cheat-sheet :

Voici le contenu que tu peux copier dans un fichier texte (par exemple, cheatsheet_sass.txt).

### Cheat-sheet pour le Nesting en SASS

## 1. **Imbrication de sélecteurs** :
Imbrique les sélecteurs CSS dans un autre pour refléter la hiérarchie de ton HTML.

```scss
// HTML :
// <div class="container">
//   <p class="text">Hello!</p>
// </div>
```

```scss
.container {
  background-color: #f0f0f0;
  
  .text {
    color: #333;
    font-size: 16px;
  }
}
```

## 2. **Nesting pour les enfants** :
Chaque sélecteur imbriqué devient un enfant du sélecteur parent.

```scss
// HTML :
// <nav>
//   <ul>
//     <li><a href="#">Link</a></li>
//   </ul>
// </nav>
```

```scss
nav {
  background-color: #333;
  
  ul {
    list-style: none;
    
    li {
      display: inline-block;
      
      a {
        color: white;
        text-decoration: none;
        
        &:hover {
          color: #ff6347; // Changer la couleur quand on survole le lien
        }
      }
    }
  }
}
```

## 3. **Référence au sélecteur parent (&)** :
Utilise & pour référencer le sélecteur parent. Cela est utile pour les pseudo-classes, pseudo-éléments, ou pour ajouter des variantes.

```scss
// HTML :
// <button class="btn">Click me</button>
```

```scss
.btn {
  background-color: #3498db;
  color: white;
  
  &:hover { // Ajoute le style lorsque l'utilisateur survole le bouton
    background-color: #2980b9;
  }
  
  &:active { // Quand le bouton est pressé
    background-color: #1c6ca0;
  }
}
```

## 4. **Nesting pour les éléments imbriqués (pseudoclasses/pseudo-éléments)** :
Tu peux également imbriquer les pseudo-éléments comme :before, :after.

```scss
// HTML :
// <div class="box">Hello</div>

.box {
  position: relative;
  padding: 20px;
  
  &:before {
    content: "→ ";
    color: #3498db;
  }
  
  &:after {
    content: " ←";
    color: #e74c3c;
  }
}
```

## 5. **Nesting pour les media queries** :
Les media queries peuvent aussi être imbriquées pour cibler des tailles d'écran spécifiques.

```scss
.container {
  width: 100%;
  padding: 20px;
  
  @media (max-width: 768px) {
    width: 80%;
  }
  
  @media (max-width: 480px) {
    width: 100%;
    padding: 10px;
  }
}
```

## 6. **Limiter l'imbrication** :
Évite de trop imbriquer les sélecteurs pour ne pas rendre le code trop complexe. Il est recommandé de ne pas dépasser 3 à 4 niveaux d'imbrication.

```scss
// Trop d'imbrication
.main {
  .container {
    .content {
      .article {
        p {
          color: #333;
        }
      }
    }
  }
}

// Préférable
.main {
  .content {
    .article {
      p {
        color: #333;
      }
    }
  }
}
```
## 7. **Combiné avec les fonctions de SASS** :

Tu peux utiliser les fonctions SASS comme les variables, les boucles, ou les mixins avec l'imbrication.
 
```scss
$primary-color: #3498db;

.container {
  background-color: $primary-color;
  
  .header {
    background-color: darken($primary-color, 10%);
  }
  
  .footer {
    background-color: lighten($primary-color, 20%);
  }
}
```

    