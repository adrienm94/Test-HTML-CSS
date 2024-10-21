# TP-HTML-CSS-Diginamic


**Objectif** : Dans ce TP, vous allez styliser une page web en utilisant les différentes techniques que vous avez apprises : Flexbox, Grid, media queries, gestion des couleurs et typographies. Vous devrez également adapter la mise en page pour qu'elle soit réactive et s'affiche correctement sur différents écrans.

---

#### Étape 1 : Le Code HTML de Base

Voici la structure HTML de la page. Vous allez styliser cette page à l'aide du CSS en suivant les consignes ci-dessous.

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Portfolio</title>
</head>
<body>
    <header>
        <h1>Mon Portfolio</h1>
        <nav>
            <ul>
                <li><a href="#">Accueil</a></li>
                <li><a href="#">Projets</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="about">
        <h2>À Propos de Moi</h2>
        <p>Je suis un développeur web passionné par la création de sites élégants et performants.</p>
    </section>

    <section class="projects">
        <h2>Mes Projets</h2>
        <div class="project-grid">
            <article class="project">
                <h3>Projet 1</h3>
                <p>Une application web innovante que j'ai créée avec React.</p>
            </article>
            <article class="project">
                <h3>Projet 2</h3>
                <p>Un site e-commerce développé avec Django et Vue.js.</p>
            </article>
            <article class="project">
                <h3>Projet 3</h3>
                <p>Un blog responsive et moderne réalisé avec WordPress.</p>
            </article>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Mon Portfolio</p>
    </footer>
</body>
</html>
```

---

#### Étape 2 : Instructions pour Styliser la Page

##### **Mission** : Vous devez intégrer la maquette de votre portfolio.

![[tp.png]]

1. **Styling Global et Typographie :**
   - Appliquez une police de caractères agréable (utilisez Google Fonts par exemple).
   - Définissez une taille de police de base pour le document (`font-size` de 16px), et ajustez les titres en conséquence (`h1`, `h2`, `h3`).
   - Appliquez des marges internes (`padding`) et des marges externes (`margin`) pour espacer les éléments correctement.
   - Appliquez une couleur de fond douce et une couleur de texte qui contraste bien avec le fond.

   **Exigences :**
   - Utilisez les unités relatives (`rem`) pour les tailles de police.
   - Utilisez des couleurs contrastées pour assurer la lisibilité.

   > [!note] **Bonnes pratiques** : Assurez-vous d’utiliser des couleurs accessibles avec un bon contraste entre le texte et le fond.

2. **Flexbox : Créer un Header Responsive**
   - Utilisez **Flexbox** pour aligner les éléments du header : le titre `h1` à gauche et le menu de navigation (`nav ul`) à droite sur les grands écrans.
   - Sur les petits écrans (moins de 768px de large), faites en sorte que le menu s’affiche sous le titre `h1` et soit centré.

   **Exigences :**
   - Utilisez `display: flex` pour aligner les éléments du header.
   - Ajoutez une media query pour changer l’affichage sur les petits écrans.

   > [!note] **Bonnes pratiques** : Concevez d’abord pour mobile (*mobile-first*), puis utilisez des media queries pour adapter le design aux écrans plus larges.

3. **Grid : Créer une Grille pour les Projets**
   - Utilisez **CSS Grid** pour organiser les projets dans une grille avec trois colonnes sur les écrans de bureau.
   - Sur les petits écrans (moins de 768px de large), réorganisez les projets pour qu’ils s’affichent dans une seule colonne.

   **Exigences :**
   - Utilisez `display: grid` avec `grid-template-columns` pour créer la grille.
   - Ajoutez une media query pour que la grille devienne une colonne sur les petits écrans.

   > [!warning] **Mauvaise pratique** : Évitez d’utiliser des tailles de colonnes fixes comme `px`. Préférez des unités flexibles comme `fr` ou `%` pour rendre la grille réactive.

4. **Boutons de Navigation :**
   - Stylisez les liens de navigation (`a`) dans le header pour qu’ils ressemblent à des boutons (ajoutez des bordures arrondies et changez leur couleur de fond).
   - Ajoutez un effet de survol (`hover`) pour que les boutons changent légèrement de couleur lorsque la souris passe dessus.

   **Exigences :**
   - Utilisez des `pseudo-classes` comme `:hover` pour ajouter des effets interactifs.

5. **Footer Simple et Propre :**
   - Donnez au footer un fond contrasté par rapport au reste de la page et centrez le texte à l’intérieur.
   - Utilisez des marges et du padding pour bien espacer le texte du bord de la page.

   **Exigences :**
   - Utilisez `text-align: center` pour centrer le contenu du footer.

---

#### Étape 3 : Media Queries et Responsivité

Utilisez des **media queries** pour adapter la mise en page aux différentes tailles d’écran. Voici quelques consignes pour la version mobile (moins de 768px de large) :
- Le header doit avoir une disposition en colonne, avec le titre centré en haut et les liens de navigation sous le titre.
- La grille des projets doit devenir une seule colonne pour occuper toute la largeur de l’écran.

**Exemple de media query :**
```css
@media (max-width: 768px) {
  /* Styles pour les petits écrans */
}
```

---

### Critères d’Évaluation

Pour valider ce TP, assurez-vous d’avoir respecté les consignes suivantes :
- **Typographie et couleurs** : Application correcte des polices et couleurs avec une bonne lisibilité.
- **Flexbox** : Alignement correct des éléments dans le header, avec une bonne gestion de la réactivité.
- **Grid** : Organisation correcte des projets en grille, avec une adaptation fluide sur mobile.
- **Media Queries** : Application des styles spécifiques pour les petits écrans (moins de 768px de large).
- **Accessibilité et Bonnes Pratiques** : Respect des bonnes pratiques d’accessibilité (contraste des couleurs, tailles de texte, etc.).