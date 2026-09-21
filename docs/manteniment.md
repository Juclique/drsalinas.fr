# Manteniment i Assets

Aquest document explica com modificar la web sense trencar l'estil ni el
versionat dels assets.

## Editar contingut

El contingut visible de la pàgina és a:

```text
public/index.html
```

Normes:

- mantenir tot el text visible en francès;
- conservar les àncores existents si la navegació no canvia;
- revisar que els enllaços `href="#..."` apuntin a seccions existents;
- evitar rutes absolutes com `/static/...`, perquè poden fallar a GitHub Pages
  si la web es publica sota un subdirectori.

## Editar estils

L'estil actiu és:

```text
public/static/css/styles-v5.css
```

Les versions anteriors es conserven. Si es fa una nova direcció visual
important, crear:

```text
public/static/css/styles-v6.css
```

Després actualitzar la plantilla:

```html
<link rel="stylesheet" href="static/css/styles-v6.css">
```

## Versionat d'assets

Els assets s'han de versionar sempre al nom del fitxer.

Exemples correctes:

```text
logo-v4.svg
clinic-studio-v3.png
styles-v5.css
```

Exemples a evitar:

```text
logo.svg
hero.png
styles.css
```

Quan es substitueix un asset existent, no s'ha de sobreescriure el fitxer antic.
Cal crear una versió nova i actualitzar les referències HTML/CSS.

## Assets actuals

```text
public/static/assets/favicon-v1.svg
public/static/assets/logo-v4.svg
public/static/assets/smile-pattern-v1.svg
public/static/assets/clinic-studio-v3.png
public/static/css/styles-v5.css
```

## Proves recomanades després de canvis

Comprovar que la web estàtica no fa servir rutes absolutes incompatibles amb
GitHub Pages:

```bash
rg '"/static|url\("/static' public
```

Obrir la web en local:

```text
public/index.html
```

Revisar manualment la home abans de publicar.
