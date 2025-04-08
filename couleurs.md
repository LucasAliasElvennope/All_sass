# Les différentes notations de couleurs en CSS

En CSS, tu peux définir des couleurs de plusieurs façons. Voici les principales :

## 1. Couleurs nommées

Tu peux utiliser des **noms de couleurs** prédéfinis comme `red`, `blue`, `green`, etc.

```css
color: red; /* texte en rouge */
background-color: blue; /* fond bleu */
```

## 2. Couleurs hexadécimales (Hex)

Les couleurs en hex commencent par un #, suivi de six caractères pour définir la couleur. Par exemple, #FF5733 est un rouge-orangé.

```css
color: #FF5733; /* rouge-orangé */
background-color: #4287f5; /* bleu */
```

## 3. Couleurs RGB

Les couleurs en RGB utilisent trois chiffres pour représenter le rouge, le vert et le bleu, chaque composant allant de 0 à 255. Par exemple, rgb(255, 87, 51) est un rouge-orangé.

```css
color: rgb(255, 87, 51); /* rouge-orangé */
background-color: rgb(66, 135, 245); /* bleu */
```

## 4. Couleurs RGBA (avec transparence)

RGBA est comme RGB, mais tu peux ajouter une transparence (de 0 à 1). Par exemple, rgba(255, 87, 51, 0.5) est un rouge-orangé à 50% de transparence.

```css
color: rgba(255, 87, 51, 0.5); /* rouge-orangé à 50% de transparence */
```

## 5. Couleurs HSL (Teinte, Saturation, Luminosité)

Les couleurs en HSL sont définies par trois valeurs :

    Teinte (de 0 à 360 degrés)

    Saturation (en %)

    Luminosité (en %)

```css
color: hsl(12, 100%, 60%); /* rouge-orangé */
```

## Conclusion

Voici les principales notations de couleurs en CSS :

- Nom : red, blue, etc.

- Hex : #FF5733, #4287f5

- RGB : rgb(255, 87, 51)

- RGBA : rgba(255, 87, 51, 0.5)

- HSL : hsl(12, 100%, 60%)

Ces méthodes te permettent de définir des couleurs en CSS de manière flexible selon tes besoins !
