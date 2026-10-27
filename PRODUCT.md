# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Owners of local small businesses in the US (salons, barbershops, bakeries, real estate, shops, and similar service businesses) who need a clear brand, a useful website, and design help but have no in-house team. Some are Spanish-speaking, and serving them in Spanish is a goal.

They usually arrive deciding whether to trust one freelancer with their brand and site, and want to know what they'd get, how it works, and how to start.

## Product Purpose

Hello Rivers is a freelance design practice offering website design and build, branding, UX/UI, monthly creative support, social media maintenance, and hosting and website care. The site exists to turn a visiting business owner into a project inquiry.

A dedicated offer for real estate agents (added 2026-10-27): listing photography with edited photos back in 48 hours, keeping their site's listings up to date plus hosting, social posts for every listing in English and Spanish, and a personal brand that works within brokerage rules. The Brazos & Bloom concept (`public/demos/brazos-bloom/`) is the sample agent site.

Success means a visitor sends a project inquiry through the contact form (which opens a drafted email) or by email.

## Positioning

Ongoing monthly support is the differentiator: Hello Rivers stays on after launch with a flexible monthly plan covering site updates, social graphics, brand assets, UX/UI improvements, and hosting care, instead of a one-off handoff. One creative partner covers brand, website, social, and hosting together.

## Operating Context

- Inquiry email: hola@marcosuriel.com (confirmed 2026-10-26). The on-page form opens a draft to it in the visitor's email app, so the address must also be shown visibly as a fallback.
- WhatsApp / phone: (956) 738-8487, offered as a second way to reach Hello Rivers.
- Reply time promise: within one business day (confirmed 2026-10-26).
- Scope and price are agreed before work begins; larger one-off projects are quoted separately.
- Clients keep ownership of every account (hosting, domains) and approve outside costs first.

## Capabilities and Constraints

- Static single-page site: `public/index.html` is the live file, deployed to Cloudflare Workers from `./public` on every push to `main`. The root `index.html` is a kept-in-sync copy.
- No Node on the owner's machine; edits are made to the static files directly.
- This repo (framesrivers/design-shop) is separate from the owner's personal portfolio (framesrivers/portafolio) and must never be combined with it.
- Projects are offered in Spanish (confirmed); the site may say "Se habla español". A full Spanish version of the site is not built yet; how it will be offered (toggle, separate page, bilingual copy) is undecided.
- No pricing is published; pricing is discussed per project.

## Brand Commitments

- Name: Hello Rivers, run by Marcos. Logo file: `hello-rivers-logo-blue.png`.
- Portrait of Marcos: `public/marcos-rivers.webp` (studio photo, white shirt, black chair). No town or location is shown, by choice.
- Voice: playful and bold — energetic, a bit cheeky, lots of personality, while staying clear for busy small-business owners. Written in first person ("I").

## Evidence on Hand

- Real client: Vanilla Bake by Erika — live site at https://vanillacakesbyerika.com/, built in Spanish (confirmed 2026-10-26) (preview: `public/vanilla-bake-preview.webp`).
- Concept/demo work, not paying clients: Northside (barbershop), Vanity (beauty salon), Luxury real estate (`public/demos/`, preview images in `public/`). Never present these as client work.
- Sunday Frame product assets in `public/assets/sunday-frame/`.
- The Selected work section currently shows "Coming soon" while a new collection is prepared.
- No testimonials, client logos, reviews, metrics, or press exist. Do not fabricate any.

## Product Principles

1. Lead with the relationship, not the launch: monthly support is the reason to choose Hello Rivers.
2. Make starting easy: every section points toward a low-effort project inquiry.
3. Show only truthful proof: real client work is labeled as such, concepts as concepts.
4. Speak like a person, not an agency: plain, playful first-person language a busy owner understands at a glance.
5. Be ready for Spanish-speaking owners as the site grows.
