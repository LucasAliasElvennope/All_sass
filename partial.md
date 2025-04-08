# Comprendre l'utilité et le fonctionnement des partials dans SASS et l'importation (@import)

## 1. Qu'est-ce qu'un partial ?
Un **partial** en SASS est un fichier contenant une partie de ton code CSS. Ces fichiers sont utilisés pour organiser ton code en différentes sections, rendant ton code plus modulaire et réutilisable.

Les partials sont des fichiers qui ne sont pas compilés directement en CSS. Ils sont utilisés uniquement comme des morceaux que tu vas inclure dans un fichier principal avec `@import`.

### Exemple de fichier partial :
- `_variables.scss` : Contient des variables.
- `_buttons.scss` : Contient des styles pour les boutons.
- `_header.scss` : Contient des styles pour l'en-tête.

Les fichiers partials commencent par un **underscore** (`_`) pour indiquer qu'ils ne doivent pas être compilés seuls.

## 2. Pourquoi utiliser des partials ?
- **Organisation** : En découpant ton code en plusieurs fichiers, il devient plus facile à maintenir et à comprendre, surtout quand ton projet devient plus grand.
- **Réutilisation** : Les partials te permettent de réutiliser du code dans différents endroits de ton projet.
- **Clarté** : Chaque fichier partiel est responsable d'une partie spécifique de ton style (par exemple, boutons, couleurs, etc.), ce qui rend ton code plus lisible.

## 3. Utilisation de `@import` pour importer des partials

En SASS, tu utilises la directive **`@import`** pour importer tes partials dans ton fichier principal.

### Exemple de structure de fichiers :

1. **Fichier `_variables.scss`** :
    ```scss
    // _variables.scss
    $primary-color: #3498db;
    $secondary-color: #2ecc71;
    ```

2. **Fichier `_buttons.scss`** :
    ```scss
    // _buttons.scss
    .button {
      background-color: $primary-color;
      padding: 10px 20px;
      border: none;
      color: white;
      cursor: pointer;
    }

    .button-secondary {
      background-color: $secondary-color;
    }
    ```

3. **Fichier `_header.scss`** :
    ```scss
    // _header.scss
    header {
      background-color: $primary-color;
      padding: 20px;
      text-align: center;
    }
    ```

4. **Fichier principal `styles.scss`** :
    ```scss
    // styles.scss
    @import 'variables';
    @import 'buttons';
    @import 'header';
    ```

### Explication :
- **`@import`** permet d'inclure un fichier partiel dans ton fichier principal.
- Les partials sont inclus dans l'ordre, donc les fichiers qui contiennent des variables doivent être importés en premier (par exemple, `_variables.scss` avant `_buttons.scss`).

## 4. Compilation avec SASS
Lorsque tu compiles ton fichier principal (`styles.scss`), tous les fichiers partiels sont combinés et compilés en un seul fichier CSS. Le fichier CSS final contiendra toutes les règles des partials.

## 5. Passer à `@use` (SASS moderne)
Depuis la version 1.23 de SASS, la directive `@import` est obsolète et remplacée par **`@use`**. La directive `@use` permet de mieux gérer les variables et les mixins, et elle évite les conflits de noms.

### Exemple avec `@use` :
```scss
// styles.scss
@use 'variables';
@use 'buttons';
@use 'header';

Avec @use, les variables et mixins sont chargées dans un namespace, ce qui les rend plus faciles à gérer.
6. Résumé

    Partials : Divisent ton code en morceaux pour mieux l'organiser.

    @import : Permet d'inclure des partials dans un fichier principal pour les compiler ensemble.

    @use : La nouvelle façon d'importer des fichiers SASS, préférée pour éviter les conflits de noms et mieux gérer les namespaces.