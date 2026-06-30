# Product

## Register

brand

## Users

Urban Indian buyers, roughly 25 to 50, who follow astrology and vedic
remedies and act on them: a recommended gemstone for a specific planet,
a birthstone, a stone chosen to balance a chart. They are discerning
shoppers, not bargain hunters. Many already buy premium goods elsewhere (apparel,
skincare, electronics) and expect the same standard of polish, clarity,
and trust when they spend on something meaningful.

Their context: browsing on a phone, often after a consultation with an
astrologer or after reading about a remedy, looking to verify
authenticity before committing. The job to be done is "help me buy the
right stone with confidence, from a seller I can trust, without feeling
like I walked into a roadside astrology stall."

## Product Purpose

SoulStones is a premium e-commerce storefront for loose, certified
natural gemstones: ruby, blue sapphire, yellow sapphire, emerald, pearl,
coral, hessonite, cat's eye, opal, and the rest of the astrological and
fine-gem range. It exists to make buying a spiritually significant stone
feel as trustworthy and considered as buying fine jewellery. Success looks like a visitor who arrived skeptical
of online gemstone sellers leaving convinced this one is credible, and
either purchasing or reaching out for a consultation.

The current build is plain HTML, CSS, and JavaScript, structured so it
can later be ported to Django templates. Payment integration is out of
scope for now; the cart leads toward a WhatsApp consultation rather than
checkout.

## Brand Personality

Reverent, refined, reassuring. The voice treats the stones with genuine
gravity and treats the buyer as an intelligent adult, never as a mark.
It explains rather than mystifies. Emotional goals: calm confidence and a
sense of quiet luxury. The experience should feel curated and personal,
closer to a private jeweller than a marketplace.

## Core User Flows

1. **Browse by category.** Land on a clear, unhurried home or category
   view. Browse gemstones by stone (ruby, blue sapphire, emerald, and so
   on) or by intent (planetary remedy, birthstone, zodiac). Categories
   are presented as collections, not as a dense grid of identical
   thumbnails. Each item shows enough to judge quality at a glance: real
   photography, name, weight, and price.

2. **Product detail.** A focused page that earns trust: large imagery,
   the stone's name and origin, certification or authenticity notes,
   intended remedy or significance, weight or size, and price. Supporting
   guidance ("who this is for", "how to wear it") sits below the buy
   decision, never above it.

3. **Add to cart.** A discreet, reliable cart that holds selections.
   Adding feels confirmed and calm, not gamified. Because there is no
   payment integration yet, the cart's role is to gather intent and hand
   off to consultation.

4. **WhatsApp consultation CTA.** A persistent, trustworthy path to talk
   to a human before buying. Presented as a service ("speak with us about
   the right stone"), available from product pages and the cart. This is
   the primary conversion path while payments are pending, so it must
   feel premium and personal, not like a pop-up nag.

## Competitive Differentiation

Generic gemstone and vedic-remedy sites compete on volume, urgency, and
mystical theatre: cluttered grids, neon gold and purple, countdown
timers, exclamation-heavy copy, stock photos, and unverifiable claims.
They read as kitschy and lower trust precisely where trust matters most.

SoulStones differentiates by treating the category the way a premium
retailer would:

- **Trust as the product.** Provenance, certification, and honest
  description carry more weight than promises and planetary fear.
- **Editorial restraint over marketplace clutter.** Space, real
  photography, and considered typography signal quality the way a
  fine-jewellery brand does.
- **Guidance, not pressure.** Consultation is offered as a service, not
  as a manipulative upsell. No timers, no scarcity tricks, no astrology
  scaremongering.
- **Considered, not kitschy.** The spiritual subject is honored with
  gravity and taste, never with gaudy mysticism.

## Anti-references

- Generic vedic-remedy and gemstone marketplaces (IndiaMART-style dense
  listings, GemPundit / generic astrology-shop clutter).
- Gaudy gold-and-purple "mystical" theming, glows, sparkles, zodiac
  iconography as decoration.
- Conversion-pressure patterns: countdown timers, "only 2 left",
  exclamation-heavy urgency copy, intrusive pop-ups.
- Stock-photo spirituality and unverifiable miracle claims.
- Anything that reads as a roadside astrology stall translated to a web
  page.

## Design Principles

- **Trust through restraint.** Quiet, spacious, and precise beats loud
  and crowded. Every element should raise credibility.
- **Provenance over promise.** Show authenticity, sourcing, and
  certification; let evidence do the persuading instead of fear or hype.
- **Honor the subject, skip the theatre.** Treat the stones with genuine
  reverence and the buyer as discerning; never lean on mystical kitsch.
- **Guide, do not pressure.** Consultation and education are services,
  offered calmly, never gamified or nagging.
- **Premium retail standard.** Hold the experience to the bar of fine
  jewellery and considered consumer brands, not astrology-shop norms.

## Accessibility & Inclusion

Target WCAG 2.1 AA. Maintain sufficient contrast despite a restrained,
luxurious palette; never rely on color alone to convey meaning (for
example, do not encode category or availability only by hue). Respect
`prefers-reduced-motion` for any transitions. Ensure the WhatsApp CTA and
cart are reachable and operable by keyboard and screen reader. Design
mobile-first, since most of this audience shops on phones.
