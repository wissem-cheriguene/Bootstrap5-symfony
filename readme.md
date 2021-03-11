# Notes + installation bootstrap 5 + WebpackEncore
```
composer require symfony/webpack-encore-bundle
npm i
```
- Dans dossier assets > changer *app.css* en .scss et *app.js* (mettre a jour l'import)
- Decommenter l.59 enablesassLoader() fichier *webpack.config.js*
- Installer compiler SASS => `npm install sass-loader@^9.0.1 node-sass --save-dev`
- Decommenter dans fichier *base.html.twig* les fichiers CSS/JS
- **desinstaller la v.5 de node-sass et prendre la 4.1.14**
- Install PostCSS => `npm i postcss-loader autoprefixer --dev`
- jouter a la racine => postcss.config.js 
```
module.exports = {
    plugins: {
        // include whatever plugins you want
        // but make sure you install these via yarn or npm!

        // add browserslist config to package.json (see below)
        autoprefixer: {}
    }
}
```
- Installer bootstrap => `npm i bootstrap@next`
- Ajouter dans app.js => 
```
// You can specify which plugins you need
import { Tooltip, Toast, Popover } from 'bootstrap';
```

- Importer bootstrap CSS dans *app.scss* 
```
@import "custom";
@import "~bootstrap/scss/bootstrap";
```

- Créer un fichier custom.scss pour customizer bootstrap ex :
```
$primary:       #FFBE0B;
$secondary:     #FB5607;
$success:       #3A86FF;
$info:          #FF006E;
$light:         #8338EC;
```
- [Doc Bootstrap5](https://getbootstrap.com/docs/5.0/getting-started/webpack/)
- [Article tuto](https://yoandev.co/bootstrap-5-avec-symfony-5-et-webpack-encore)