---
name: Volt Market
description: Better parts. Better picture. Your next build starts here.
colors:
  primary: "#4d8bff"
  primary-soft: "#79aaff"
  page: "#0c0e12"
  surface: "#12151b"
  surface-raised: "#171b22"
  text: "#f0f2f6"
  muted: "#a1a8b5"
  border: "#252a34"
typography:
  display:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(48px, 6.5vw, 78px)"
    fontWeight: 670
    lineHeight: 0.99
    letterSpacing: "-0.075em"
  title:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(22px, 2.5vw, 29px)"
    fontWeight: 640
    lineHeight: 1.2
    letterSpacing: "-0.055em"
  body:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "Inter, ui-sans-serif, system-ui, sans-serif"
    fontSize: "10px"
    fontWeight: 700
    letterSpacing: "0.1em"
rounded:
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "20px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "13px"
  lg: "18px"
  xl: "24px"
  section: "72px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "#ffffff"
    rounded: "{rounded.sm}"
    padding: "0 16px"
    height: "42px"
  button-quiet:
    backgroundColor: "#171b22"
    textColor: "{colors.text}"
    rounded: "{rounded.sm}"
    padding: "0 16px"
    height: "42px"
  card-product:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    rounded: "{rounded.md}"
    padding: "13px 14px 12px"
---

# Design System: Volt Market

## Overview

**Creative North Star: "The Night Signal"**

Volt Market is a cinematic, high-contrast electronics showroom: the dark canvas quiets the frame while cobalt controls and carefully staged product photography make the next useful action unmistakable. The experience should feel precise and easy to scan, not like a dense parts spreadsheet. Clear compatibility cues, honest demo boundaries, and legible product details are part of the visual promise.

The default mode is ink-dark, with a restrained light mode using the same hierarchy and blue accent. Product imagery carries most of the color and texture; interface chrome stays calm, with confident primary actions and subtle motion rather than constant glow.

**Key Characteristics:**
- Cinematic ink surfaces with electric cobalt signals.
- Product-led, spacious layouts that remain practical on mobile.
- Refined controls and explicit status, price, and compatibility cues.

## Colors

The palette pairs a near-black blue-neutral foundation with a single electric-cobalt action color; green and red are reserved for meaningful status.

### Primary
- **Electric Cobalt** (#4d8bff): Primary buttons, links, selected controls, and active navigation.
- **Signal Blue** (#79aaff): Softer accents, hero emphasis, and decorative highlights.

### Neutral
- **Ink** (#0c0e12): Default page canvas.
- **Raised Ink** (#12151b): Cards, menus, and primary contained surfaces.
- **Lifted Slate** (#171b22): Secondary surfaces, input fills, and hover backgrounds.
- **Soft White** (#f0f2f6): Main text and high-priority icons.
- **Cool Mist** (#a1a8b5): Supporting copy and secondary labels.
- **Graphite Line** (#252a34): Dividers and default component borders.

### Named Rules
**The Signal Rule.** Reserve cobalt for actions, active states, and short emphasis; do not turn every surface into an accent-colored panel.

## Typography

**Display Font:** Inter (with a system sans-serif fallback)  
**Body Font:** Inter (with a system sans-serif fallback)  
**Label/Mono Font:** Inter; keyboard hints use the system monospace only where needed.

**Character:** Compact, contemporary sans-serif typography balances editorial hero headlines with high-density product facts. Tight tracking is reserved for large headings; labels remain small but clear and consistently weighted.

### Hierarchy
- **Display** (670, `clamp(48px, 6.5vw, 78px)`, 0.99 line-height): Campaign headline and major feature moments.
- **Headline** (640, `clamp(22px, 2.5vw, 29px)`, approximately 1.2 line-height): Section headings and page titles.
- **Title** (660, 13px, 1.4 line-height): Product names and compact card headings.
- **Body** (400, 14px, 1.55 line-height): General descriptions and explanatory copy.
- **Label** (700, 9–11px, 0.07–0.13em tracking): Eyebrows, metadata, ratings, and utility labels; use uppercase selectively.

### Named Rules
**The One-Scale Rule.** Use the system sans stack throughout; create hierarchy through size, weight, and spacing rather than decorative font mixing.

## Layout

Center content in a 1320px maximum-width shell, with the home surface allowed to reach 1400px. The desktop catalog uses four product columns and a four-column category grid; collapse to two product columns on mobile, keeping the filter panel accessible as a drawer. Preserve generous section spacing (about 72px on desktop) while tightening vertical rhythm on small screens. The sticky header and mobile bottom navigation provide persistent wayfinding without covering page content.

## Elevation & Depth

Depth is hybrid but restrained: tonal surface shifts and thin borders establish structure at rest; soft shadows are saved for floating menus, overlays, and hover lift. The default shadow is `0 18px 45px rgba(0, 0, 0, .24)`. Keep accent glows subtle and localized.

### Shadow Vocabulary
- **Ambient** (`0 18px 45px rgba(0, 0, 0, .24)`): Hovered product cards, menus, and floating panels.
- **Accent action** (`0 5px 17px rgba(62, 127, 250, .18)`): Primary button at rest; strengthen slightly on hover.

### Named Rules
**The Quiet Surface Rule.** Use tonal layering and borders first; shadows indicate lift or interaction, not decoration.

## Shapes

Use compact, softly rounded geometry: 8px controls, 12px product cards, 16px panels, and 20px campaign containers. Borders are thin and low-contrast at rest, strengthening on focus or hover. Product imagery may use larger editorial masks in feature areas, but keep utility controls and data tables plainly rectangular and predictable.

The reusable scale describes the foundation, not every one-off treatment: tiny metadata, circular status marks, and translucent image overlays may use context-specific sizes, radii, and color values to stay legible and fit their component.

## Components

### Buttons
- **Shape:** 8px radius; 42px minimum height for the main action.
- **Primary:** Electric cobalt fill, white text, and confident medium-bold type.
- **Hover / Focus:** Lift by 2px on hover; shift to a lighter blue. Use a visible 2px cobalt focus ring with a 3px offset.
- **Secondary / Ghost:** Quiet surfaces or transparent fill with a fine border; use muted text until hover.

### Chips
- **Style:** Small, compact labels with a softly tinted background and clear semantic text.
- **State:** Use cobalt for selected or promotional states; reserve green and red for status meaning.

### Cards / Containers
- **Corner Style:** 12px product cards; 16px utility panels.
- **Background:** Raised ink against the page canvas, or the lifted slate token for nested controls.
- **Shadow Strategy:** Border-first at rest; ambient shadow and a small upward lift on hover.
- **Border:** One-pixel graphite line, strengthened on hover.
- **Internal Padding:** About 13–14px in product information areas; 18–28px for larger panels.

### Inputs / Fields
- **Style:** Surface fill, 1px line border, 8–9px radius, and compact horizontal padding.
- **Focus:** Cobalt border and a restrained outer ring.
- **Error / Disabled:** Use red only for validation errors; disabled controls are visibly muted and non-interactive.

### Navigation
- **Style:** Sticky, translucent ink header with a fine bottom border; muted links become high-contrast on hover.
- **Active:** Cobalt identifies the current mobile destination and selected navigation state.
- **Mobile:** Persistent bottom navigation with icon-and-label pairs and a clear active treatment.

### Product Imagery
Large, lazy-loaded photography anchors campaign and category surfaces. Product cards crop images consistently; detail galleries give the selected item more space and expose alternate views without shifting product information.

### Admin Product Management
The private catalog workspace uses the same ink surfaces, blue primary action, fine borders, and restrained card depth as the storefront. Keep product editing focused on compact, labeled fields; separate destructive deletion from the primary save action and provide explicit success and error feedback.

## Do's and Don'ts

### Do:
- **Do** keep controls and copy legible in both dark and light themes.
- **Do** make product price, stock, rating, and compatibility easy to scan.
- **Do** preserve clear keyboard focus and touch-friendly targets.
- **Do** use the product image or a restrained blue field as the main visual event.

### Don't:
- **Don't** use cobalt as a large, repeated card background.
- **Don't** rely on color alone for stock, error, or compatibility meaning.
- **Don't** compress mobile product cards until names and prices become unreadable.
- **Don't** imply that illustrative stock, reviews, payment, or order data is live.
