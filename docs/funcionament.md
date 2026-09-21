# Funcionament General

La web és una landing page en francès per al cabinet dental de Dr Salinas. Està
pensada per presentar el cabinet, explicar els tractaments principals i mostrar
les coordenades del cabinet.

## Objectiu

Els objectius principals són:

- transmetre una imatge editorial, tranquil·la i d'alta qualitat;
- explicar els serveis dentals sense sobrecarregar la pàgina;
- facilitar el contacte amb el cabinet;
- indicar que el cabinet és a `11 Rue du Maréchal de Boufflers, Songeons`;
- mostrar el telèfon `03 44 11 76 91` i el correu `rdv@drsalinas.fr`.

## Estructura de la pàgina

La plantilla principal és:

```text
public/index.html
```

Les seccions principals són:

- `header.site-header`: hero visual amb imatge de clínica, navegació i CTA.
- `section#cabinet`: presentació del cabinet i filosofia de treball.
- `section.feature-row`: tres valors del servei.
- `section#soins`: llista dels tractaments principals.
- `section#technologies`: bloc sobre tecnologia clínica.
- `section#rendez-vous`: coordonnades i informació de contacte.
- `footer.footer`: tancament i enllaç de retorn.

## Navegació

La navegació superior apunta a àncores internes:

```text
#cabinet
#soins
#technologies
#rendez-vous
```

No hi ha múltiples pàgines. Tot el contingut viu en una sola plantilla.

## Idioma

La web està íntegrament en francès:

```html
<html lang="fr">
```

Si es modifica contingut visible, cal mantenir-lo en francès.
