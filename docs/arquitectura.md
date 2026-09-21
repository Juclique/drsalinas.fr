# Arquitectura Tècnica

El projecte publica una web estàtica amb GitHub Pages. La carpeta activa de
publicació és `public/`.

## Estructura

```text
public/index.html           HTML publicat
public/static/css/          Fulls d'estil publicats
public/static/assets/       Imatges, logos i icones publicats
.github/workflows/pages.yml Deploy automàtic a GitHub Pages
```

## GitHub Pages

El workflow és:

```text
.github/workflows/pages.yml
```

Responsabilitats:

- executar-se en cada push a `main`;
- pujar `public/` com a artefacte de GitHub Pages;
- desplegar-lo a l'entorn `github-pages`.

Per activar-ho a GitHub:

```text
Settings > Pages > Build and deployment > Source: GitHub Actions
```

## Web publicada

La web és una pàgina pública sense formulari de cita ni zona privada.
El repositori no ha de contenir secrets, claus API, paràmetres SMTP ni
configuracions privades del correu.

Les dades públiques principals configurades al contingut són:

- cabinet: Dr Salinas;
- formació indicada: Universitat de Barcelona;
- adreça: `11 Rue du Maréchal de Boufflers, Songeons`;
- telèfon: `03 44 11 76 91`;
- correu: `rdv@drsalinas.fr`.
- horari: `9h30 - 13h00` i `14h00 - 18h00`.

## Validació

La validació bàsica consisteix a comprovar que no hi ha rutes absolutes que
trenquin GitHub Pages quan es publica sota un subdirectori:

```bash
rg '"/static|url\("/static' public
```
