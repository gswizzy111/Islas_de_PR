---
name: Islas de PR
description: A colorful island travel journal with generous photography and ocean accents.
colors:
  paper: "oklch(.97 .013 88)"
  white: "oklch(.995 .004 88)"
  ink: "oklch(.28 .035 215)"
  blue: "oklch(.43 .075 215)"
  ocean: "oklch(.54 .085 210)"
  aqua: "oklch(.89 .04 186)"
  sand: "oklch(.91 .03 85)"
  sun: "oklch(.84 .125 80)"
  coral: "oklch(.69 .14 40)"
  muted: "oklch(.46 .025 215)"
  line: "oklch(.82 .02 88)"
  shade: "oklch(.17 .025 215 / .55)"
typography:
  display:
    fontFamily: "Gloock, Georgia, serif"
    fontSize: "clamp(52px,6.5vw,94px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-.035em"
  headline:
    fontFamily: "Gloock, Georgia, serif"
    fontSize: "clamp(36px,4.2vw,62px)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-.035em"
  title:
    fontFamily: "Gloock, Georgia, serif"
    fontSize: "27px"
    fontWeight: 400
    lineHeight: 1.25
  body:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "16px"
    lineHeight: 1.65
  label:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "13px"
    fontWeight: 600
rounded:
  control: "3px"
  circle: "50%"
  hero: "140px 3px 3px 3px"
  journal: "3px 100px 3px 3px"
spacing:
  compact: "12px"
  control: "16px 23px"
  grid: "24px"
  section: "85px 6%"
components:
  button-primary:
    backgroundColor: "{colors.blue}"
    textColor: "{colors.paper}"
    typography: "{typography.label}"
    rounded: "{rounded.control}"
    padding: "{spacing.control}"
  button-light:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "{spacing.control}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "{spacing.control}"
  field:
    backgroundColor: "{colors.white}"
    textColor: "{colors.ink}"
    height: "46px"
    rounded: "{rounded.control}"
    padding: "0 13px"
  navigation:
    textColor: "{colors.ink}"
    padding: "15px 0"
  collection-link:
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "10px 17px"
  post-card:
    backgroundColor: "{colors.white}"
    textColor: "{colors.ink}"
---
# Design System: Islas de PR

## Overview

**Creative North Star: "The Island Travel Journal"**

A colorful travel journal brings Puerto Rico into view through large island photographs, ocean accents, warm paper, and expressive serif headlines. The approved direction is implemented in code: imagery leads discovery, while compact sans-serif labels keep navigation and excursion comparisons clear.

**Key Characteristics:**
- Large island photographs with generous editorial spacing.
- Ocean blue actions on warm paper, with aqua, sand, and sunshine accents.
- Serif headlines paired with compact, readable sans-serif controls.

## Colors

### Primary
Ocean blue (`blue`) defines actions, active tabs, headline emphasis, and full-width social bands. The brighter `ocean` supports text-link hover feedback.

### Secondary
Shallow-water aqua (`aqua`) backs guide features and post previews. Warm `sand` separates excursions, checklists, and quieter content regions.

### Tertiary
Sunshine (`sun`) accents the circular photo stamp, journal label, and text selection. Coral (`coral`) is the keyboard focus color.

### Neutral
Warm `paper` is the page canvas; `white` is the slightly brighter input and post surface. `ink` carries primary text; `muted` carries supporting descriptions. `line` provides quiet separators. Transparent `shade` supports readable photo captions.

## Typography

Gloock with Georgia fallback supplies the editorial display and headline roles. DM Sans supplies body copy, navigation, fields, and metadata. Tour titles use the serif title token; general third-level headings use DM Sans at 23px with a 1.25 line height.

Hero and section headings scale fluidly. Uppercase tour metadata is 10px with .065em tracking; photo and travel-journal labels remain compact. Body paragraphs usually narrow to 310–650px depending on context. Mobile rules adjust titles without changing the font pairing.

## Layout

The main content container caps at 1440px with 85px vertical and 6% horizontal section padding. The hero caps at 1600px and divides text and photography into 43%/57% columns. Destination tiles use an asymmetric 1.4fr/1fr/1fr grid; excursions use three equal columns with 24px horizontal gaps. Journals and guide features use two columns.

At 1100px and below, sections tighten to 65px and 5%, the hero becomes 46%/54%, and the header action is hidden. At 760px, the mobile navigation replaces desktop links, editorial features stack, section spacing becomes 55px and 6%, and tours and social posts use two columns. At 420px those grids become a single column. Destination tabs and the place strip scroll horizontally where necessary. At 1600px and above the hero photo grows to 660px minimum height.

## Elevation & Depth

The system uses no box shadows. Depth comes from photographs, flat colored regions, fine borders, and dark gradients behind photo captions. The circular sun stamp and slightly rotated journal label suggest collected travel ephemera. Avoid adding floating-card shadows to the existing flat surface language.

## Shapes

Controls and ordinary tiles have restrained 3px corners. Hero photography has one large upper-left corner; journal imagery has one large upper-right corner. Circular controls are reserved for photo saves and the sun stamp. One-pixel separators organize lists and content regions; tabs use a stronger 3px active underline.

## Components

Primary buttons use ocean blue, paper text, a 52px minimum height, and a subtle 2px hover lift. Light buttons reverse the surface for blue bands; outlined buttons remain transparent. Controls share the coral 3px focus outline with 5px offset.

Fields use bright paper, a fine neutral border, and a 46px height. Collection links are compact bordered rectangles with sand hover fills. Desktop navigation uses a 2px underline for the current page and hover. Mobile navigation opens as a full-width paper panel beneath the header.

Tour cards place unboxed editorial content beneath 4:3 photography. Their circular save buttons fill blue when selected and also expose pressed state. Destination cards overlay white titles on image gradients. Social cards use bordered white surfaces with aqua, sand, or sunshine preview panels; official embeds load on request. Travel notes use native disclosures and a checklist with struck-through completed labels.

Motion is brief and functional: route entry lasts .4s, buttons use .2s background and .3s transform transitions, and image hover zoom uses .6–.8s. The easing curve is cubic-bezier(.16,1,.3,1). Reduced-motion preferences disable entry animations, zoom, lift, and smooth scrolling.

## Do's and Don'ts

- Do use the existing ocean palette and warm paper surfaces.
- Do preserve image credits and legible captions over photography.
- Do retain visible focus, touch-sized controls, and reduced-motion behavior.
- Don't replace destination imagery with generic interface decoration.
- Don't add shadows to the flat editorial surfaces.
- Don't hide active navigation or saved states behind color alone.
