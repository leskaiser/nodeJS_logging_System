# Laravel-style Logger for Node.js

Ce module est une adaptation en JavaScript du système de logs de Laravel pour les applications Node.js. Il offre une solution de journalisation structurée et facile à utiliser, inspirée par l'approche élégante de Laravel en matière de gestion des logs.

## Caractéristiques

- Structure de fichiers de logs organisée par année/mois/jour/heure
- Rotation automatique des fichiers de logs toutes les heures
- Niveaux de log similaires à Laravel (**info**, **error**, **warning**, **debug**)
- Compatibilité avec les environnements de développement et de production
- Utilisation de Winston pour une gestion robuste des logs

## Installation

```bash
npm install winston
```

## Configuration

- Placez le fichier `logger.js` dans un dossier approprié de votre projet (par exemple, `utils/`).
- Assurez-vous que le dossier `storage/logs/` existe à la racine de votre projet.


```javascript
const logger = require('./path/to/logger');

// Utilisation
logger.info('Ceci est un message d\'information');
logger.error('Une erreur est survenue', error);
logger.warning('Attention à ceci');
logger.debug('Information de débogage');
```

## Structure des Logs
Les logs sont organisés selon la structure suivante :

```text
storage/logs/YYYY/MM/DD/yourAppName_HH-YYYY-MM-DD.log
```

## Personnalisation
Vous pouvez facilement personnaliser le format des logs, les niveaux de log, et d'autres paramètres en modifiant le fichier `logger.js`.

## Environnement de Développement
En mode développement, les logs sont également affichés dans la console pour faciliter le débogage.

## Contribution
Les contributions sont les bienvenues ! N'hésitez pas à ouvrir une issue ou à soumettre une pull request.

## Licence
Ce projet est sous `licence MIT`. Voir le fichier LICENSE pour plus de détails.
Inspiré par Laravel

### Inspiré par Laravel
Ce système de logs s'inspire fortement du système de logs de [Laravel](https://laravel.com/docs/11.x/logging), adapté pour fonctionner dans un environnement Node.js.
