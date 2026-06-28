# Simple Omelette Recipe Page

> A responsive recipe page built with HTML and CSS as part of the Frontend Mentor challenge.

##  Aperçu du projet

Page de recette d'omelette simple avec :
- Structure HTML sémantique
- Style CSS intégré
- Design responsive

##  Technologies utilisées

| Technologie | Utilisation |
|-------------|-------------|
| **HTML5** | Structure et sémantique |
| **CSS3** | Flexbox, couleurs HSL, mise en page |

## Approche de développement

### 1. Structure HTML
- Utilisation de balises sémantiques : `<main>`, `<h1>`, `<h2>`, `<h3>`, `<ul>`, `<ol>`
- Image avec attribut `alt` pour l'accessibilité
- Contenu structuré : titre, description, temps de préparation, ingrédients, instructions, nutrition

### 2. Style CSS
- **Police** : Young Serif (titres) + Outfit (texte)
- **Couleurs** : Palette définie dans le style-guide (Stone, Brown, Rose)
- **Mise en page** : Flexbox pour l'alignement
- **Responsive** : Largeur fixe de 500px pour la carte

### 3. Points clés
- Correction du chemin d'image (chemin relatif `./assets/...`)
- Utilisation des couleurs HSL depuis le style-guide
- Design en carte avec bord arrondi

##  Couleurs utilisées

```css
--Stone-100: hsl(30, 54%, 90%)      /* Fond principal */
--Stone-600: hsl(30, 10%, 34%)      /* Texte */
--Brown-800: hsl(14, 45%, 36%)      /* Titres h2 */
--Rose-800: hsl(332, 51%, 32%)      /* Titre préparation */
--Rose-50: hsl(330, 100%, 98%)      /* Fond sections */
```

##  Structure

```
recipe-page-main/
├── index.html          # Page principale
├── assets/
│   └── images/
│       └── image-omelette.jpeg
├── design/             # Fichiers de design
└── style-guide.md      # Guide de style
```
### Stratégie d'Adaptation Mobile et Nettoyage des Flux

L'intégration responsive d'une page de contenu linéaire (comme cette fiche de recette) repose sur la libération des dimensions rigides imposées sur grand écran. Pour assurer une transition fluide vers les terminaux mobiles, la stratégie consiste à nettoyer les décalages du conteneur principal et à cibler précisément les éléments structurels majeurs :

```css
@media (max-width: 480px) and (min-width: 360px) {
  main {
    width: 100vw;           /* Transition vers une largeur fluide sur toute l'interface */
    height: auto;      
    margin-left: 0;         /* Annulation des décalages et marges fixes du desktop */
    min-height: 100vh;  
    padding: 10px; 
    box-sizing: border-box; /* Neutralisation de l'impact du padding sur le modèle de boîte */
  }

  #recette {
    width: 92%;             /* Redimensionnement adaptatif de la carte principale */
    margin: 15px auto;      /* Centrage horizontal automatique par le navigateur */
    padding: 15px; 
    box-sizing: border-box;
  }
}

##  Auteur

- GitHub : [@rmArchiviste](https://github.com/rmArchiviste)
