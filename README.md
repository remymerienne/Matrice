# 1. Matrice

---

- [1. Matrice](#1-matrice)
  - [1.1. Git](#11-git)
    - [1.1.1. Installation](#111-installation)
    - [1.1.2. Vérification de version](#112-vérification-de-version)
    - [1.1.3. Configuration](#113-configuration)
      - [1.1.3.1. Error message](#1131-error-message)
    - [1.1.4. Initialisation](#114-initialisation)
    - [1.1.5. Les commits](#115-les-commits)
      - [1.1.5.1. Rédaction des commits](#1151-rédaction-des-commits)
        - [1.1.5.1.1. Les types](#11511-les-types)
        - [1.1.5.1.2. Modèle de commit](#11512-modèle-de-commit)
    - [1.1.6. Les branches](#116-les-branches)
    - [1.1.7. Les remotes](#117-les-remotes)
    - [1.1.8. Fetch](#118-fetch)
    - [1.1.9. Les tags](#119-les-tags)
    - [1.1.10. Gitignore](#1110-gitignore)
    - [1.1.11. Diff](#1111-diff)
  - [1.2. Badges Markdown](#12-badges-markdown)
    - [1.2.1. Grandes tailles](#121-grandes-tailles)
    - [1.2.2. Badges normaux](#122-badges-normaux)
    - [1.2.3. Markdown Emoji Markup](#123-markdown-emoji-markup)
  - [1.3. A TRAVAILLER !!!](#13-a-travailler-)

---

## 1.1. Git

![https://a11ybadges.com/badge?logo=git](https://a11ybadges.com/badge?logo=git)

[Site officiel](http://git-scm.com)

### 1.1.1. Installation

`$ brew install git`

### 1.1.2. Vérification de version

`$ git --version`

### 1.1.3. Configuration

Pour un apperçu de la configuration actuelle :

`$ git config --list`

Enregistrer son nom et son e-mail :

`$ git config --global user.name "John Doe"`

`$ git config --global user.email "johndoe@example.com"`

Activer les couleurs :

`$ git config --global color.diff auto`

`$ git config --global color.status auto`

`$ git config --global color.branch auto`

Définir VSCode come éditeur par défaut :

`$ git config --global core.editor "code --wait"`

`$ git config --global diff.tool vscode`

`$ git config --global merge.tool vscode`

#### 1.1.3.1. Error message

Il peut parfois arriver qu’un message d’erreur apparaisse lors d’un commit ou d’un merge de type :

```bash
error: There was a problem with the editor 'core --wait'.Please supply the message using either -m or -F option.
```

Dans ce cas, ouvrir la palette de commande (command + shift + p)
Taper ‘code’ dans l’invite et sélectionner la commande :

`Shell Command: Install 'code' command in PATH`

### 1.1.4. Initialisation

Nouveau projet :

`$ git init`

Cloner un projet existant :

`$ git clone <https://mon-repo-distant>`

### 1.1.5. Les commits

Inclures tous les fichiers modifiés au prochain commit :

`$ git add -A`

Commit :

`$ git commit -m "message de commit"`

Modifier le message du dernier commit :

`$ git commit --amend -m "nouveau message"`

Annuler le dernier commit :

`$ git revert HEAD`

notes : Va créer un nouveau commit “d’annulation” ce qui ne posera pas de problème lors d’un prochain push vers un dépot distant.

#### 1.1.5.1. Rédaction des commits

##### 1.1.5.1.1. Les types

- feat : Ajout d’ue nouvelle fonctionnalité
- fix : Correction d’un bug
- build : Changement lié au systèmes de build ou qui concerne les dépendances.
- docs : Ajout ou modification de la documentation
- perf : Amélioration des performances
- refactor : Remaniment du code qui ne modifie pas le rendu.
- style : Changement lié au style du code
- test : Ajout ou modification de tests
- revert : Annulation d’un précédent commit
- chore : toute autre modification

##### 1.1.5.1.2. Modèle de commit

```bash
[FIX] index (#9): change alt text images

Alt text images must be different than images name in "Activity"

section.Closes #9
```

### 1.1.6. Les branches

Lister les branches locales :

`$ git branch`

Lister les branches distantes :

`$ git branch -r`

Lister toutes les branches :

`$ git branch -a -v`

Créer une nouvelle branche :

`$ git branch <ma-nouvelle-branche>`

Se rendre sur une autre branche :

`$ git checkout <ma-branche-de-destination>`

Créer une nouvelle branche et aller directement dessus :

`$ git checkout -b <ma-nouvelle-branche>`

Renommer une branche :

`$ git branch -m <ancien-nom> <nouveau-nom>`

Supprimer une branche locale :

`$ git branch -d <ma-branche>`

Forcer la suppression d’une branche :

`$ git branch -D <ma-branche>`

Supprimer une branche distante :

`$ git push <remote> --delete <ma-branche>`

Publier une branche sur le dépot distant :

`$ git push <remote> <ma-branche>`

Récupérer une branche distante :

`$ git pull <remote> <ma-branche>`

Merger une branche en conservant l’historique :

`$ git merge --no-ff <branche-à-merger>`

### 1.1.7. Les remotes

Lister les remotes :

`$ git remote`

Créer une remote :

`$ git remote add origin <https://mon-repo-distant>`

Mettre à jour le HEAD aprés changement de branche par défaut :

`$ git remote set-head origin -a`

### 1.1.8. Fetch

Mise à jour des changements entre dépot local et distant :

`$ git fetch <remote>`

Suppression des branches supprimées et réstées en mémoire localement :

`$ git fetch --prune`

### 1.1.9. Les tags

Repertorier les tags :

`$ git tag`

Création d’un tag simple :

`$ git tag <tagname>`

(tagname est à remplacer par un identifiant sémantique de type v1.0.0)

Création d’un tag annoté :

`$ git tag -a <tagname>`

Un tag annoté contiendra des métadonnées supplémentaires sous forme de message, telles que le nom du créateur, la date, son email.

Envoyer le tag sur un dépot distant :

`$ git push origin <tagname>`

### 1.1.10. Gitignore

Pour désindexer des fichiers ajoutés au .gitignore :

`$ git rm -r --cached .`

`$ git add .`

`$ git commit -m "fixed untracked files`

### 1.1.11. Diff

`$ git diff main..develop`

Indique les différence entre la brache Main et la branche Develop.

---

## 1.2. Badges Markdown

![https://a11ybadges.com/badge?logo=markdown](https://a11ybadges.com/badge?logo=markdown)

### 1.2.1. Grandes tailles

[GitHub - a11y-badges/a11y-markdown-badges: accessible markdown badges for profile and project READMEs (and everything else!) via a11y badges](https://github.com/a11y-badges/a11y-markdown-badges)

### 1.2.2. Badges normaux

[GitHub - Ileriayo/markdown-badges: Badges for your personal developer branding, profile, and projects.](https://github.com/Ileriayo/markdown-badges)

[GitHub - alexandresanlim/Badges4-README.md-Profile: 👩‍💻👨‍💻 Improve your README.md profile with these amazing badges.](https://github.com/alexandresanlim/Badges4-README.md-Profile)

[150+ Badges for GitHub](https://dev.to/envoy_/150-badges-for-github-pnk)

### 1.2.3. Markdown Emoji Markup

[Complete list of github markdown emoji markup](https://gist.github.com/rxaviers/7360908)

---

## 1.3. A TRAVAILLER !!!

```json
 "scripts": {
    "sass": "sass ./sass/main.scss ./dist/css/style.css --watch --style compressed",
    "build": "webpack --config webpack.config.js",
    "purge": "purgecss --css ./dist/css/style.css --content ./index.html ./dist/js/bootstrap.bundle.min.js ./dist/js/index.bundle.min.js --output ./dist/css/ -font -keyframes",
    "prefix": "postcss ./dist/css/style.css --use autoprefixer -d ./dist/css/"
  }
```

```json
 "devDependencies": {
    // Autoprefixer
    "autoprefixer": "latest",
    "postcss": "latest",
    "postcss-cli": "latest",
    // Eslint
    "eslint": "latest",
    // Purgecss
    "purgecss": "latest",
    // Sass
    "sass": "latest",
    // Webpack avec Babel et "Transform Arrow Functions"
    "@babel/core": "latest",
    "@babel/plugin-transform-arrow-functions": "latest",
    "@babel/preset-env": "latest",
    "babel-loader": "latest",
    "webpack": "latest",
    "webpack-cli": "latest"
  }
```

Hiérarchie des commentaires

```html
<!--  !   Red     - End -->
<!--  -   Orange  - End -->
<!--  +   Yellow  - End -->
<!--  ^   Green   - End -->
<!--  =   Blue    - End -->
<!--  *   Pink    - End -->
```

OLD
1.2. npm

1.2.1. Initialisation de npm

```bash
npm init -y
```

1.2.2. Liste des commandes de base

![supply/img_readme/npm-basic-commands.png](supply/img_readme/npm-basic-commands.png)

Lien vers les options de package.json :  
[https://docs.npmjs.com/cli/v8/configuring-npm/package-json](https://docs.npmjs.com/cli/v8/configuring-npm/package-json)

1.2.3. Installation des dépendances de développement

Liste des dépendances :

- Webpack :
  - webpack
  - webpack-cli
- babel-loader :
  - babel-loader
  - @babel/core
  - @babel/preset-env
  - @babel/- plugin-transform-arrow-functions
- Préprocesseur :
  - sass
- Linter :
  - eslint
- testing :
  - jest
  - @testing-library/dom
  - @types/jest

@testing-library/jest-dom => a voir pour les customes matchers et user-event

Coller dans package.json :

```json
"devDependencies": {
  "@babel/core": "^7.17.5",
  "@babel/plugin-transform-arrow-functions": "^7.16.7",
  "@babel/preset-env": "^7.16.11",
  "@testing-library/dom": "^8.11.3",
  "@types/jest": "^27.4.1",
  "babel-loader": "^8.2.3",
  "eslint": "^8.10.0",
  "jest": "^27.5.1",
  "sass": "^1.49.9",
  "webpack": "^5.70.0",
  "webpack-cli": "^4.9.2"
}
```

Installer les dépendances :

```bash
npm install
```

Mise à jour des dépendances (optionnelle) :

```bash
npm update
```

Commandes npm à coller dans package.json :

```json
"build": "webpack --config webpack.config.js",
"sass": "sass src/sass/app.scss css/app.css --watch",
"purge": "purgecss --css css/app.css --content dist/index.html dist/app.bundle.js -o dist",
"test": "jest --watch --verbose",
"test-cov": "jest --coverage",
"server-src": "live-server --port=8080 --open=\"src/index.html\"",
"server-dist": "live-server --port=8080 --open=\"dist/index.html\""
```
