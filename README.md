# Matrice

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
