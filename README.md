# Dr Salinas

Site web statique en français pour une clinique dentaire, prêt pour GitHub Pages.

## Documentation

La documentation de fonctionnement est disponible dans [`docs/`](./docs/README.md).

## Site statique

La version publiée par GitHub Pages est dans:

```text
public/
```

Fichiers principaux:

```text
public/index.html
public/static/css/styles-v10.css
public/static/assets/
```

Tous les assets créés pour le site sont versionnés dans leur nom (`*-v1.*`, `*-v2.*`, etc.).

## GitHub Pages

Le déploiement est configuré avec GitHub Actions:

```text
.github/workflows/pages.yml
```

À chaque push sur `main`, GitHub publie le contenu de `public/`.

Dans GitHub, activer Pages avec:

```text
Settings > Pages > Build and deployment > Source: GitHub Actions
```

## Sécurité

Le dépôt peut être public: il ne contient pas de backend, pas de base de données
et pas de secrets. Ne pas ajouter de mots de passe, clés API, paramètres SMTP,
DNS privés ou fichiers de configuration mailbox.org au dépôt.

La publication GitHub Pages utilise uniquement le contenu de `public/`.

## Tester en local

Comme la web est statique, il suffit d'ouvrir:

```text
public/index.html
```
