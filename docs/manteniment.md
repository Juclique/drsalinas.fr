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
public/static/css/styles-v10.css
```

Les versions anteriors es conserven. Si es fa una nova direcció visual
important, crear:

```text
public/static/css/styles-v11.css
```

Després actualitzar la plantilla:

```html
<link rel="stylesheet" href="static/css/styles-v11.css">
```

## Versionat d'assets

Els assets s'han de versionar sempre al nom del fitxer.

Exemples correctes:

```text
logo-v4.svg
clinic-studio-v3.png
styles-v5.css
styles-v10.css
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
public/static/css/styles-v10.css
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

## Fotografies del cabinet (v1)

- `dr-salinas-portrait-v1.jpg`: retrat de la doctora.
- `cabinet-soins-v1.jpeg`: sala de tractament, no utilitzada.
- `cabinet-reception-v1.jpeg`: recepció i sala d’espera, portada.
- `cabinet-imagerie-v1.jpeg`: radiologia.

Les còpies de les fotos es conserven sense retoc. Els enquadraments visibles
es defineixen amb `object-fit` i `object-position` a `styles-v10.css`, amb una
composició adaptada a mòbil. `dr-salinas-travail-v1.jpg` mostra la doctora treballant a la segona secció.
El retrat es mostra a la secció de cita.
La versió anterior dels estils i la imatge anterior es conserven.

## Retrat v2 i relat de la casa

`dr-salinas-portrait-v2.png` és el retrat actiu, editat amb ImageGen integrat.
Original conservat en v1. Instrucció: eliminar la marca Vericat i arreglar els
cabells solts, preservant identitat, expressió, roba i blanc i negre.
La referència més antiga coneguda de la casa és de 1658, segons el propietari. No és la data
d’obertura del cabinet. La comparació del plànol de 1764 amb Google Maps,
aportada pel propietari, es conserva sense retoc en
`cabinet-plan-1764-comparaison-v1.png`.
