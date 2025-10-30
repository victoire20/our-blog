# our-blog

Ce dépôt contient un modèle statique simple de blog (HTML + CSS) fourni ici uniquement pour s'exercer.

> Attention : ce projet est utilisé comme exercice et s'appuie sur une maquette fournie gratuitement par un designer sur Figma. Si vous voulez récupérer la maquette d'origine, suivez ce lien :

https://www.figma.com/community/file/1333753054895285708

Ce lien redirige vers le fichier Figma du designer qui a mis sa maquette à disposition gratuitement pour ceux qui veulent s'entraîner. Merci à l'auteur original, DINESH GADHIYA, pour le partage.

## Sommaire

- Description
- Structure du projet
- Comment l'utiliser localement
- Documentation extraite du code
- Ressources et crédits


## Description

`our-blog` est une petite maquette de site de type blog faite avec une seule page HTML (`index.html`) et une feuille de style (`style.css`), plus un dossier `assets/` contenant les images et icônes. Le but ici est pédagogique : explorer la structure, le HTML et le CSS d'une maquette responsive inspirée d'un design Figma.


## Structure du projet

Voici les fichiers et dossiers principaux présents à la racine :

- `index.html` : page principale (structure HTML des cartes d'articles, header, etc.)
- `style.css` : styles, variables CSS et règles responsive
- `assets/` : images et icônes
	- `articles/` : images d'articles
	- `icons/` : icônes (ex : `search-icon.svg`)
	- `writers/` : avatars des auteurs
- `LICENSE` : licence fournie avec le dépôt (vérifier le contenu pour réutilisation)


## Comment l'utiliser localement

1. Ouvrez `index.html` dans votre navigateur (double-clic ou `Fichier > Ouvrir` dans le navigateur).
2. Pour un flux de développement plus pratique, installez et utilisez une extension "Live Server" (VS Code) ou servez le dossier via un serveur HTTP simple (ex: `python -m http.server` si vous préférez).


## Documentation extraite du code

Ci-dessous se trouve un récapitulatif des éléments et conventions trouvés dans le code source (HTML & CSS) — utile pour comprendre la maquette et la personnaliser.

### HTML (`index.html`)

- Police et icônes :
	- Utilise la fonte `Inter` via Google Fonts.
	- Utilise `Material Symbols Outlined` et `Material Icons` pour certaines icônes.
- Structure principale :
	- `<header class="header">` : logo / titre / description et barre de recherche.
	- `<main class="main">` : conteneur principal avec les cartes d'articles.
	- Chaque article est rendu via `<article class="card">` qui contient :
		- une image (`.card__img`)
		- un badge de catégorie (`.card__badge`)
		- le titre et résumé (`.card__content__header`)
		- le footer auteur (`.card__footer`) avec image et nom

Extrait d'usage : copiez une carte d'article pour ajouter d'autres articles dans la maquette.


### CSS (`style.css`) — points importants

- Variables CSS (:root) :
	- Couleurs : `--gray-50`, `--gray-300`, `--gray-400`, `--gray-500`, `--gray-900`.
	- Couleurs primaires : `--primary-50`, `--primary-700`, `--primary-900`.
	- Poids : `--weight-regular`, `--weight-medium`, `--weight-semibold`.
	- Ombrages : `--shadow-xs`, `--shadow-lg`.

- Composants et classes clés :
	- `.container` : largeur max et padding horizontal basé sur des vw.
	- `.header` : zone supérieure avec fond clair et texte centré.
	- `.search__bar` et `.search__bar__input` : barre de recherche avec icône en background.
	- `.row` : conteneur flex pour les cartes, avec `gap` et `flex-wrap`.
	- `.card` : style principal des cartes (fond blanc, padding, ombre, responsive).
	- `.card__badge`, `.card__content__header`, `.card__footer`, `.card__writter__infos` : structure et typographie interne.

- Responsive :
	- `@media (min-width: 760px)` : disposition 2 colonnes pour `.card`.
	- `@media (min-width: 1280px)` : disposition 3 colonnes pour `.card`.


## Bonnes pratiques pour personnaliser

- Remplacez les images dans `assets/articles/` et `assets/writers/` pour visualiser vos propres contenus.
- Modifiez les variables dans `:root` pour changer l'identité visuelle (couleurs, ombres, poids).
- Ajoutez des liens réels aux titres et badges si vous voulez rendre la maquette interactive.


## Ressources et crédits

- Maquette originale (utilisée pour s'exercer) :
	https://www.figma.com/community/file/1333753054895285708

	Ceci est juste pour s'exercer — le fichier Figma mentionné est une maquette mise gratuitement à disposition par son auteur. Si vous réutilisez ou publiez dérivés, respectez la licence et l'attribution indiquées par l'auteur sur Figma.

- Polices & icônes : Google Fonts (Inter, Material Symbols, Material Icons).


## Licence

Vérifiez le fichier `LICENSE` fourni dans le dépôt pour connaître les conditions d'utilisation et de redistribution.


## Remarques finales

Ce README a été rédigé en extrayant et en résumant la documentation déjà présente dans le code HTML et CSS du projet. Il vise à faciliter la lecture et l'apprentissage pour toute personne qui souhaite s'exercer à partir de la maquette fournie.

Si vous voulez que je :
- génère une version Markdown plus courte ou plus technique ;
- ajoute des instructions pour déployer sur GitHub Pages ;
- ou encore que j'intègre des scripts de build (npm, vite, etc.) — dites-le et je continue.
