---
name: SoulStones
description: Premium modern-vedic storefront for loose, certified natural gemstones.
colors:
  off-white: "#F7F3EA"
  surface: "#FFFDF8"
  black: "#16120B"
  black-soft: "#221C12"
  gold: "#C9A24B"
  gold-soft: "#E8D5A8"
  gold-deep: "#876521"
  ink: "#1A160F"
  muted-brown: "#8A7B6C"
typography:
  hero-script:
    fontFamily: "Cormorant Garamond, Georgia, serif"
    fontSize: "clamp(1.4rem, 3vw, 2rem)"
    fontStyle: "italic"
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: "normal"
    note: "Hero accent line only. One Script Rule: appears once per page, never in UI or body."
  display:
    fontFamily: "Gloock, Georgia, serif"
    fontSize: "clamp(2.6rem, 5.4vw, 4.2rem)"
    fontWeight: 400
    lineHeight: 1.05
    letterSpacing: "-0.025em"
    note: "Hero title and largest editorial statements. Gloock 400 only — no bold weight available."
  headline:
    fontFamily: "Gloock, Georgia, serif"
    fontSize: "clamp(2rem, 4vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.08
    letterSpacing: "-0.02em"
    note: "Section titles. Stat figures and step numbers also use Gloock 400."
  title:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "normal"
    note: "Product names, card titles, category names. Inter 600 — NOT the display serif."
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "normal"
  body-emphasis:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 500
    lineHeight: 1.65
    letterSpacing: "normal"
    note: "Section lede, consult body. Slightly larger than base body."
  label:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: "0.1em"
    note: "Uppercase labels. 0.06em for tighter labels, 0.1em for structural/wide labels."
rounded:
  card: "12px"
  badge: "6px"
  pill: "999px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "40px"
  section-mobile: "56px"
  section: "96px"
components:
  button-primary:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "14px 30px"
    typography: "{typography.label}"
  button-primary-hover:
    backgroundColor: "{colors.gold-soft}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "14px 30px"
  button-secondary:
    backgroundColor: "{colors.off-white}"
    textColor: "{colors.gold-deep}"
    rounded: "{rounded.pill}"
    padding: "13px 29px"
    typography: "{typography.label}"
  button-secondary-hover:
    backgroundColor: "{colors.gold-soft}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "13px 29px"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "20px"
  badge-new:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.gold-deep}"
    rounded: "{rounded.badge}"
    padding: "4px 10px"
    typography: "{typography.label}"
---

# Design System: SoulStones

## 1. Overview

**Creative North Star: "The Atelier in Black & Gold"**

SoulStones is dressed like a private jeweller, not an astrology stall. The
system runs on three notes: a warm off-white that carries most of the
page, deep black grounds that frame the most important moments, and gold
that signals headings, actions, and accents throughout. The effect is
quiet luxury: a sunlit boutique where the few black-and-gold moments feel
ceremonial. Reverence is carried by restraint and material quality, never
by mystical theatre.

The palette is split between lightness and weight. Off-white (#F7F3EA)
and warm-white surfaces (#FFFDF8) hold the catalog, so the stones,
photographed large, are the loudest thing on the page. Black (#16120B)
grounds the statement bands (stats, consultation) and the footer, where
gold reads at its most precious. Gold itself comes in two registers:
bright gold (#C9A24B) for buttons, icons, and anything set on black, and a
deeper antique gold (#876521) for headings and labels on light surfaces,
where bright gold would be too pale to read.

This system explicitly rejects the generic gemstone-and-vedic-remedy look:
gaudy gold-and-purple gradients, sparkle effects, zodiac iconography as
decoration, neon, IndiaMART-style dense grids, and conversion-pressure
clutter. If a screen could be mistaken for a roadside astrology shop
translated to the web, it has failed.

**Key Characteristics:**
- Off-white canvas, black statement grounds, gold headings and actions.
- Gloock for editorial authority at display scale, Inter for trustworthy clarity.
- Pill buttons (gold fill, dark text), 12px cards, soft warm shadows.
- Wide breathing room (96px desktop sections) that signals premium.
- Gold reads as a precious metal, never as decorative wallpaper.

## 2. Colors

A warm three-note palette: off-white, black, and gold, with gold doing the
expressive work.

### Primary
- **Bright Gold** (#C9A24B): The brand's signature metal. Button fills, the
  "NEW" badge border, icons, thin rules, and every heading or accent set on
  a black ground. Used deliberately, the way a jeweller uses a hallmark.
- **Deep Antique Gold** (#876521): Gold for light surfaces. Headings,
  product names, eyebrows, and links on off-white, where Bright Gold would
  fail contrast. Same metal, darkened just enough to stay legible.

### Secondary
- **Champagne Gold** (#E8D5A8): The soft, lit side of gold. Button-hover
  fills, soft section tints, and quiet highlights on both light and black.

### Neutral
- **Off-White** (#F7F3EA): The default page background. Warm and
  unclinical; the canvas products sit on.
- **Warm White** (#FFFDF8): Card and surface fills that lift one step off
  the off-white. Product cards, panels, the "NEW" badge ground.
- **Black** (#16120B): A warm near-black for statement grounds: the stats
  band, the consultation band, and the footer. Never pure #000.
- **Soft Black** (#221C12): A lifted black for surfaces inside black
  sections (placeholder slots, video frames).
- **Ink** (#1A160F): The primary text color on light. A warm near-black so
  body copy reads softly on off-white.
- **Muted Brown** (#8A7B6C): Secondary and supporting text on light:
  captions, metadata, placeholders, subtle borders.

### Named Rules
**The Two-Golds Rule.** Bright Gold (#C9A24B) is for black grounds,
buttons, and icons. Deep Antique Gold (#876521) is for headings and labels
on light. Never set bright gold as text on off-white; it fails contrast
and looks washed out.

**The Black-as-Punctuation Rule.** Black is a ground for statement moments,
not a default. Most of the page is off-white. Black appears for the stats
band, the consultation band, and the footer, where gold reads as precious.

**The Warm-Neutral Rule.** No pure black, no pure white, no cold grey.
Text is Ink (#1A160F); the lightest surface is Warm White (#FFFDF8); the
darkest is Black (#16120B). Every neutral is tinted warm.

## 3. Typography

**Display Font:** Gloock (with Georgia, serif fallback)
**Body Font:** Inter (with system-ui, sans-serif fallback)
**Hero Script:** Cormorant Garamond italic (with Georgia, serif fallback)

**Character:** Gloock is a 2022 calligraphic display serif with high-contrast
strokes and open, rounded counters. It brings editorial refinement without
the Victorian/English associations of Playfair Display, and has near-zero
template saturation in the Indian e-commerce space. It ships at weight 400
only, which enforces a deliberate principle: the display serif earns its
place through scale and precision, not bold weight. Inter keeps all
functional copy crisp, trustworthy, and legible at small sizes. Cormorant
Garamond italic appears once, in the hero, as the single flourish.

**Font scale (6 fixed steps + fluid display):**
0.75rem / 0.875rem / 1rem / 1.125rem / 1.25rem / 1.5rem + clamp()

### Hierarchy
- **Hero Script** (Cormorant Garamond italic, 500, clamp(1.4rem, 3vw, 2rem), 1.2):
  The hero accent line only. One per page, never in UI or body.
- **Display** (Gloock 400, clamp(2.6rem, 5.4vw, 4.2rem), 1.05, -0.025em):
  The hero's primary statement headline.
- **Headline** (Gloock 400, clamp(2rem, 4vw, 3rem), 1.08, -0.02em):
  Section titles, stat figures, step numbers.
- **Title** (Inter 600, 1.25rem, 1.3): Product names, card titles, category
  names. Inter, not Gloock: the display serif is for large editorial moments
  only. Below ~1.5rem the serif's character is lost; Inter 600 is cleaner.
- **Body** (Inter 400, 1rem, 1.65): All running copy. Cap measure at 65–75ch.
- **Body Emphasis** (Inter 500, 1.125rem, 1.65): Section lede, consult body.
- **Label** (Inter 600, 0.75rem, 0.1em tracking, uppercase): Buttons,
  badges, eyebrows, category tags, metadata labels.

### Named Rules
**The One Script Rule.** Cormorant Garamond appears once per page, in the
hero, and never in body, buttons, or UI. Its rarity is what makes it feel
precious.

**The Serif-for-Soul, Sans-for-Service Rule.** Gloock carries emotion and
editorial identity (section titles, hero, stat figures, step numbers). Inter
carries function (copy, controls, prices, card titles). The display serif is
editorial-only: it earns its place at large scale. Below ~1.5rem, use Inter.
Never set running body copy in Gloock.

## 4. Elevation

The system is near-flat and warm. Depth comes from layering Warm White
cards over the Off-White page plus soft, low, diffuse shadows that read
like daylight on a counter, not the hard drop-shadows of a 2014 app.
Shadows are tinted toward the warm neutrals (ink-black), never neutral grey
or pure black. Black sections create depth through tone, not shadow.

### Shadow Vocabulary
- **Resting Card** (`box-shadow: 0 2px 8px rgba(26, 22, 15, 0.07)`): The
  default lift for product and content cards off the off-white background.
- **Raised Hover** (`box-shadow: 0 10px 28px rgba(26, 22, 15, 0.14)`): The
  hover state for interactive cards. Pairs with a small upward translate.
- **Overlay** (`box-shadow: 0 16px 48px rgba(26, 22, 15, 0.22)`): Reserved
  for the cart drawer and floating surfaces.

### Named Rules
**The Daylight Shadow Rule.** Shadows are soft, wide, and warm-tinted (rgba
of Ink, low alpha). If a shadow looks dark, tight, or grey, it is wrong.
Blur is large, offset is small, opacity stays under 0.22.

## 5. Components

### Buttons
- **Shape:** Fully pill-shaped (999px radius). A signature of the system.
- **Primary:** Bright Gold fill (#C9A24B) with Ink text (#1A160F), Label
  type. Padding 14px 30px. The default call to action, including "Add to
  Cart". Hovers to Champagne Gold (#E8D5A8).
- **Secondary:** Transparent or off-white ground with a Bright Gold outline
  (1px) and Deep Antique Gold text. Padding 13px 29px. Used for
  lower-priority actions and the WhatsApp consultation CTA on light. On
  black grounds, the WhatsApp button is solid Bright Gold with Ink text.
- **Hover / Focus:** Secondary fills with Champagne Gold and text shifts to
  Ink. All buttons show a visible focus-visible ring (2px Bright Gold, 2px
  offset). Transitions ease out ~180ms. Respect `prefers-reduced-motion`.

### Cards
- **Corner Style:** Gently curved (12px radius).
- **Background:** Warm White (#FFFDF8) lifting off the Off-White page.
- **Shadow Strategy:** Resting Card at rest, Raised Hover on hover, paired
  with a 2px upward translate. Never animate layout.
- **Border:** None by default; an optional hairline Bright Gold border for
  featured items only.
- **Internal Padding:** ~20px, generous around product imagery.
- **"NEW" Badge:** Small chip, Warm White ground with a 1px Bright Gold
  border and Deep Antique Gold Label text. Anchored top-left of the image.

### Inputs / Fields
- **Style:** Warm White fill, 1px hairline border, 12px radius. Ink text,
  Muted Brown placeholder. On black (footer newsletter), a translucent fill
  with a warm gold-tinted border and off-white text.
- **Focus:** Border shifts to Bright Gold with a soft 2px gold glow ring.
- **Error / Disabled:** Error border in a muted red; never rely on color
  alone, pair with an icon or helper text.

### Navigation
- **Style:** Slim top bar on translucent Off-White, Inter links in Ink,
  wordmark with "Stones" in Deep Antique Gold.
- **States:** Hover and active links carry a thin Bright Gold underline and
  shift to Deep Antique Gold.
- **Mobile:** Collapses to a single menu affordance; the consultation CTA
  stays reachable. Sections compress to 56px spacing.

### Statement Bands (signature)
Black (#16120B) grounds for the stats band, the consultation CTA, and the
footer. Headings and figures in Bright Gold, body in warm off-white at
reduced opacity, primary action as a solid Bright Gold pill. These are the
page's punctuation; everything between breathes on off-white.

## 6. Do's and Don'ts

### Do:
- **Do** keep the page mostly off-white (#F7F3EA), and use black (#16120B)
  only for the statement bands and footer.
- **Do** use gold for headings, buttons, icons, and accents: Bright Gold
  (#C9A24B) on black and for buttons, Deep Antique Gold (#876521) for
  headings and labels on light.
- **Do** make primary buttons gold fill with Ink text; secondary buttons
  gold outline with gold text.
- **Do** keep buttons fully pill-shaped (999px) and cards 12px-radius Warm
  White with soft, warm-tinted shadows.
- **Do** set large editorial headings (section titles, hero, stats) in Gloock 400.
  Set card titles, product names, and sub-heads in Inter 600. All functional copy in Inter (400/500/600).
- **Do** breathe: 96px section spacing on desktop, 56px on mobile, with
  large product photography carrying the page.

### Don't:
- **Don't** set Bright Gold (#C9A24B) as text on off-white; it fails
  contrast. Use Deep Antique Gold (#876521) for gold text on light.
- **Don't** use gaudy gold-and-purple "mystical" theming, glows, sparkles,
  or zodiac iconography as decoration. No purple anywhere.
- **Don't** use pure #000 or pure #fff or cold grey. Neutrals stay warm.
- **Don't** ship conversion-pressure patterns: countdown timers, "only 2
  left", exclamation-heavy urgency copy, or auto-opening pop-ups.
- **Don't** set the hero script (Cormorant Garamond) anywhere but the hero,
  and never more than once per page.
- **Don't** set running body copy in Gloock; that is Inter's job. Don't use Gloock below ~1.5rem — the display serif's character is lost at small sizes and Inter is cleaner.
- **Don't** use hard, dark, tight drop-shadows. If a card looks like a 2014
  app, the shadow is too dark and the blur is too small.
- **Don't** build IndiaMART-style dense grids of identical thumbnails;
  present categories as curated collections.
- **Don't** add gradient text, side-stripe borders, or decorative
  glassmorphism.
