# Utilité et fonctionnement de `@extend` en SASS 🎨

## Qu'est-ce que `@extend` ? 🤔

`@extend` permet de réutiliser les styles d'un sélecteur dans un autre, évitant la duplication du code. ♻️

## Pourquoi utiliser `@extend` ? ✅

- **Réduction de code** : Réutilise les styles sans les répéter 🔄.
- **Maintenance facilitée** : Les changements sont appliqués à tous les sélecteurs qui étendent un style commun 🔧.

## Exemple 👨‍💻

### SCSS

```scss
// Style de base
.btn {
  padding: 10px 20px;
  border-radius: 5px;
}

// Bouton primaire
.btn-primary {
  @extend .btn;
  background-color: blue;
  color: white;
}

// Bouton secondaire
.btn-secondary {
  @extend .btn;
  background-color: gray;
  color: white;
}
```

### CSS généré 🖥️

```css
.btn, .btn-primary, .btn-secondary {
  padding: 10px 20px;
  border-radius: 5px;
}

.btn-primary {
  background-color: blue;
  color: white;
}

.btn-secondary {
  background-color: gray;
  color: white;
}
```

### Conclusion 🎯

`@extend` simplifie la gestion des styles en réutilisant les règles CSS, mais il faut être vigilant avec la spécificité des sélecteurs pour éviter des conflits ⚠️.