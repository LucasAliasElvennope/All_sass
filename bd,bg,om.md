# ✨ Appliquer des Bordures, Ombres et Arrière-plans en CSS

## 1. **Bordures 🖊️**

Les bordures permettent de dessiner des lignes autour de tes éléments.

```css
.element {
  border: 2px solid red; /* Bordure de 2px, rouge et solide */
}
```

*Explication* :

    2px : L'épaisseur de la bordure.

    solid : Le style de la bordure (solide, pointillé, etc.).

    red : La couleur de la bordure.

## 2. Ombres 🕶️

Les ombres créent un effet de profondeur autour de l'élément.

```css
.element {
  box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5); /* Ombre décalée de 5px à droite et 5px en bas */
}
```

*Explication* :

    5px 5px : Décalage de l'ombre horizontalement et verticalement.

    10px : Le flou de l'ombre.

    rgba(0, 0, 0, 0.5) : Couleur noire avec 50% de transparence.

## 3. Arrière-plans 🌈

Tu peux personnaliser l'arrière-plan avec des couleurs, des images ou des dégradés.

*Couleur de fond* :

```css
.element {
  background-color: lightblue; /* Fond bleu clair */
}
```

*Image de fond* :

```css
.element {
  background-image: url('image.jpg'); /* Image comme fond */
}
```

*Dégradé* :

```css
.element {
  background: linear-gradient(to right, red, yellow); /* Dégradé de rouge à jaune */
}
```

*Résumé rapide* 📚 :

| Propriété | Description | Exemple |
|---------|-------------|---------|
| Bordure | Dessine une ligne autour de l'élément | `border: 2px solid red;` |
| Ombre | Crée une ombre portée | `box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);` |
| Arrière-plan | Définit la couleur ou l'image de fond | `background-color: lightblue;`<br>`background-image: url('image.jpg');`<br>`background: linear-gradient(to right, red, yellow);` |

Avec ces propriétés CSS, tu peux rapidement personnaliser l'apparence de tes éléments ! 😎
