# Funcionament General

La web és una landing page en francès per al cabinet dental de Dr Salinas. Està
pensada per presentar el cabinet, explicar els tractaments principals i mostrar
les coordenades del cabinet.

## Objectiu

Els objectius principals són:

- transmetre una imatge editorial, tranquil·la i d'alta qualitat;
- presentar el tracte familiar i la història de la casa, amb la referència més antiga coneguda de 1658;
- facilitar el contacte amb el cabinet i la reserva de cita amb Google Calendar;
- indicar que el cabinet és a `11 Rue du Maréchal de Boufflers, Songeons`;
- mostrar el telèfon `03 44 11 76 91` i el correu `rdv@drsalinas.fr`.
- mostrar l'horari `9h30 - 13h00` i `14h00 - 18h00`.

## Estructura de la pàgina

La plantilla principal és:

```text
public/index.html
```

Les seccions principals són:

- `header.site-header`: hero visual amb imatge de clínica, navegació i CTA.
- `section#cabinet`: presentació del cabinet i filosofia de treball.
- `section.house-story`: referència històrica de 1658 i comparació del plànol de 1764 amb Google Maps.
- `section#technologies`: bloc sobre tecnologia clínica.
- `section#rendez-vous`: reserva de cita en línia i informació de contacte.
- `footer.footer`: tancament i enllaç de retorn.

## Navegació

La navegació superior apunta a àncores internes:

```text
#cabinet
#technologies
#rendez-vous
```

No hi ha múltiples pàgines. Tot el contingut viu en una sola plantilla.

## Reserva de cita

El botó «Prendre rendez-vous» de la capçalera i el de la secció de cita obren
la pàgina de reserves de Google Calendar en la mateixa pestanya:

https://calendar.app.google/PrZpYBvFLjgStx2JA

Els horaris disponibles i les reserves es gestionen a Google Calendar.
La web conserva el telèfon i el correu com a alternatives. Per canviar la
pàgina de reserves, cal actualitzar els dos enllaços a `public/index.html`.
No calen scripts, claus API ni formularis locals.

## Idioma

La web està íntegrament en francès:

```html
<html lang="fr">
```

Si es modifica contingut visible, cal mantenir-lo en francès.
