# Résumé des unités de mesure en CSS

## 1. **% (Pourcentage) 📊**
   - **Description** : Un pourcentage par rapport à la taille de l'élément parent.
   - **Utilisation** : Utilisé pour rendre les éléments réactifs, ajustant leur taille en fonction de la taille du parent.
   - **Exemple** :
     ```css
     .element {
       width: 50%; /* 50% de la largeur du parent */
     }
     ```

## 2. **px (Pixels) 🖥️**
   - **Description** : Unité fixe, indépendante de la taille de l'élément parent.
   - **Utilisation** : Utilisé quand tu veux que la taille d'un élément soit précise et ne change pas.
   - **Exemple** :
     ```css
     .element {
       width: 100px; /* Largeur fixe de 100px */
     }
     ```

## 3. **em (Relative à la taille de la police du parent) 🔤**
   - **Description** : Unité relative à la taille de la police de l'élément parent.
   - **Utilisation** : Utile quand tu veux que la taille d'un élément soit liée à la taille du texte du parent.
   - **Exemple** :
     ```css
     .element {
       font-size: 2em; /* 2 fois la taille de police du parent */
     }
     ```

## 4. **rem (Relative à la taille de la police de l'élément racine) 🌱**
   - **Description** : Unité relative à la taille de la police de l'élément racine (`<html>`).
   - **Utilisation** : Utilisé pour une taille cohérente et prévisible sur toute la page.
   - **Exemple** :
     ```css
     html {
       font-size: 16px;
     }
     .element {
       font-size: 2rem; /* 2 fois la taille de la police de l'élément racine */
     }
     ```

## Résumé rapide :

| Unité | Description | Utilisation |
|-------|-------------|-------------|
| `%`   | 📊 Relative au parent | Mise en page fluide et responsive |
| `px`  | 🖥️ Fixe | Taille précise, ne change pas |
| `em`  | 🔤 Relative à la taille de police du parent | Flexible, mais peut devenir complexe si imbriqué |
| `rem` | 🌱 Relative à la taille de la police de l'élément racine | Cohérence sur toute la page |
