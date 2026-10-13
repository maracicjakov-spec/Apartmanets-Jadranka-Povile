# Apartments Jadranka — Povile

A demo website for **Apartments Jadranka Povile** (Dugno 40, Povile, 51250 Novi Vinodolski, Croatia). It is a static single-page site: HTML, CSS and vanilla JS, with no build step and no dependencies. Croatian is the default language and English is complete.

Status: **client demo**. The inquiry form does not send messages yet (see *Contact form*).

---

## Project structure

```
index.html     the whole site (inline CSS + JS, structured data, HR/EN i18n)
images/        28 photos as responsive WebP (480–2400 px) + og-image.jpg (1200×630)
fonts/         self-hosted DM Serif Display + Manrope (woff2, latin + latin-ext)
README.md
```

- **Croatian text** lives in the markup. **English** strings are in the `EN` object in the script, keyed by `data-i18n` / `data-i18n-html` / `data-i18n-attr`. Gallery captions live in the `G` array (HR + EN).
- The language toggle is in the header and the mobile menu. The choice is remembered in `localStorage`, and `?lang=en` opens English directly. The site does not auto-detect browser language, which avoids layout shift on load.
- **Configuration** is the `CONFIG` object at the top of the script: `inquiryEmail`, `bookingUrl`, and unit capacities used by form validation.

## Design notes

- Palette: ivory `#F8F6F1`, sand `#E9E1D4`, Adriatic `#183C4A`, sea `#7297A3` and charcoal `#252C2E`. There is one accent, ochre `#C99A45`, taken from the house's own façade.
- Type: DM Serif Display for headings and Manrope for body text. Both render Croatian diacritics (č ć š ž đ) properly.
- The signature element is the *"Od vrata do mora"* distance chart. It lists the real distances to the beaches, restaurant, heritage site, viewpoint and airport. Line lengths use a compressed (logarithmic) scale so 20 m and 34 km fit one view.
- Motion is limited to one hero load sequence, image wipe-reveals, the distance lines drawing in, hover zoom and the menu and lightbox transitions. Everything respects `prefers-reduced-motion`.

## Image sources and usage permission

All 28 photos are the property's own photos, published by the host on the **Booking.com** listing
<https://www.booking.com/hotel/hr/apartments-jadranka-povile.hr.html>. They were downloaded from Booking's public image CDN (`cf.bstatic.com`). No access controls were bypassed, and guest-uploaded photos were excluded.

> ⚠️ **Permission:** the photos belong to the owner. Using them on this demo shown *to the owner* is reasonable. **Before the site goes public, get the owner's written OK** to use them (or new originals, which would also be higher quality).

Selection and use:

| File (images/…) | Booking photo ID | Shows | Used in |
|---|---|---|---|
| balkon-more, balkon-more-portret | 204309708, 204309701 | 2-bedroom apt. balcony, breakfast, sea + Krk | Hero (landscape / mobile portrait), gallery, OG image |
| terasa-smokva | 50198995 | studio terrace, deck chair, fig tree | Intro |
| stube-cvijece | 50199128 | stairs with flowers, ochre façade | Intro inset, gallery |
| studio-terasa, studio-ulaz, studio-spavaca, studio-kuhinja, studio-kupaonica | 50199009, 50199008, 74079012, 8869287, 69200709 | studio (ground floor) | Unit card, gallery |
| ap2-blagovaonica, ap2-dnevni, ap2-spavaca, ap2-dvokrevetna, ap2-kuhinja | 204311256, 204310880, 204311068, 204310892, 204310902 | apartment with 2 bedrooms | Unit card, gallery |
| dvo-balkon, dvo-balkon-portret, dvo-dnevni, dvo-spavaca, dvo-blagovaonica, dvo-galerija | 204312713, 204312465, 204312451, 204312906, 204312895, 204312575 | two-level apartment | Unit card, gallery |
| kuca-procelje, ulaz-vrt, pogled-krk, pogled-balkon | 50198459, 50199412, 49815733, 8869490 | house exterior and views | Gallery |
| okolica-obala, okolica-uvala, okolica-zaljev, okolica-plaza | 8869356, 8869480, 103137551, 103137569 | **surroundings** (not the property) | Povile section, labelled as surroundings |

Photos were mapped to units using Booking's own photo-to-room associations. Excluded:
- older or low-resolution duplicates (2012–2015 interiors, 150 px thumbnails)
- photo 8869492, a harbour scene with an identifiable child
- photo 17399078, a person at a ship's wheel
- five guest-uploaded photos, which the CDN refused anyway

## Verified property details

Source: the Booking.com listing, read on **13 Oct 2026**. Destination facts come from the Novi Vinodolski Tourist Board beaches page (tz-novi-vinodolski.hr).

- **Name / address:** Apartments Jadranka Povile, Dugno 40, Povile, 51250 Novi Vinodolski. Map pin: 45.11466, 14.82509 (Booking's map).
- **Host:** Jadranka. Languages: Croatian, English, German. Quality label: *Kvarner Family – Pet Friendly*. The intro quote is translated and adapted from the host's own listing text.
- **Units** (3 types; the listing does not say how many of each exist):
  - *Studio – Prizemlje* (ground floor): 33 m², 2 adults, 1 extra-large double bed, own entrance, terrace with garden view, oven, non-smoking.
  - *Apartman s 2 spavaće sobe, balkonom i pogledom na more*: 65 m², up to 5. Bedroom 1 has a double bed, bedroom 2 has 2 single beds, and the living room has a sofa bed. Sea-view balcony, microwave, upper floor reached by stairs only.
  - *Dvoetažni apartman s balkonom* (two levels): 65 m², up to 5. One large double bed, an open upper-level sleeping area with 2 single beds, and a sofa bed. Sea-view balcony, upper floors reached by stairs only.
  - All units: private kitchen and bathroom, air conditioning, heating, flat-screen satellite TV, Wi-Fi, coffee machine, kettle, fridge, hob, linen, towels, hairdryer, free toiletries, mosquito net, outdoor furniture, paved courtyard.
- **Property:** free Wi-Fi throughout, free private parking on site (no reservation), pets on request (charges may apply), airport transfer at extra charge, baby cot free on request (under 2), extra bed €20/night on request. The extra-bed price is *not* shown on the site.
- **House rules:** check-in from 14:00, check-out until 09:00, quiet hours 23:00–08:00, cash only, deposit by bank transfer before arrival, no parties.
- **Rating:** 9.6 "Izuzetan" from 38 reviews. Sub-scores: staff 9.9, cleanliness 9.8, value 9.7, comfort 9.4, facilities 9.1, location 9.2, Wi-Fi 8.8. These are shown as an October 2026 snapshot and **should be refreshed before launch**.
- **Distances** (Booking.com, OpenStreetMap-based, approximate):
  - Plaža Dugno 20 m
  - Restoran & Pansion Garfild 300 m
  - Plaža Uvala Povile 400 m
  - Plaža Povile 550 m
  - Plaža Škrpun 1.4 km
  - Lopar beach 2.5 km
  - Pauline monastery remains 3.9 km (3.8 km in the "nearby" list)
  - Kuk – Oči Vinodola viewpoint 7.4 km
  - Rijeka Airport 34 km (35 km in the description)
- **Povile** (Tourist Board): small holiday village 2 km south of Novi Vinodolski. Pebble, concrete and hidden rocky beaches. Freshwater springs in the sea, several cafés along the beaches, quiet. Mala Draga dog beach is about 1 km toward Klenovica. Day trips (viewpoints above Vinodol, cycling routes, Plitvice) come from the host's own listing text.

## Unverified or omitted on purpose

- **Prices.** None are shown. Booking prices are date-dependent.
- **Phone, e-mail, website.** None are public, so the site has no contact details.
- **Guest review quotes.** Not reproduced; only the aggregate score is shown.
- **The "restoran" facility.** Booking lists it, but it most likely refers to the nearby Garfild, so it is not claimed as an on-site restaurant.
- **Booking's 3-star badge.** Not shown, because the official categorisation is unconfirmed.
- **How many units of each type exist.** Unknown.
- **Shower vs. bathtub.** Booking says "Kada ili tuš". The site only says "private bathroom"; the studio gallery caption mentions a shower because the photo shows one.
- **The beaches in the surroundings photos.** The exact locations are unknown, so they are not named.
- **"Pogled na Krk".** This is geography (Krk lies opposite Povile across the Vinodol Channel), mentioned only in the hero alt text and one gallery caption. "Rijeka Airport, on Krk" is a plain fact.

## Placeholders to replace before launch

1. **Domain.** `https://apartments-jadranka-povile.vercel.app/` appears in `canonical`, `hreflang`, `og:url`, `og:image` and JSON-LD (search `apartments-jadranka-povile.vercel.app`).
2. **Inquiry e-mail.** Set `CONFIG.inquiryEmail` once the owner confirms an address (see below).
3. **Rating snapshot.** Refresh the score, review count and the "stanje u listopadu 2026" note.
4. **Photo permission.** See above.

## Contact form

- **Current state: demo, not functional.** Validation is real:
  - required fields and e-mail format
  - arrival cannot be in the past, and departure must come after arrival
  - number of guests is checked against the selected unit's capacity (studio 2, apartments 5)
  - errors are announced to screen readers
- On a valid submit it shows a clearly labelled **"Upit nije poslan" (inquiry not sent)** notice that points to Booking.com. It never claims success.
- **To make it live:** put the owner's e-mail in `CONFIG.inquiryEmail`. The form then posts to FormSubmit's AJAX endpoint (`formsubmit.co/ajax/<email>`) with a Croatian-language payload, and shows a real success or error state. The first real submission triggers a FormSubmit activation e-mail that the owner must confirm.
- **"Rezervirajte putem Bookinga"** links to the verified listing (`.en-gb` in English). The site never claims live availability or direct booking.

## Run locally

Any static server works, for example:

```bash
npx serve .
# or
python -m http.server 8000
```

Opening `index.html` directly from disk also works, except that the map may not load from `file://`.

## Deploy to Vercel

1. Create a Git repo with these files and push to GitHub. Then import it in Vercel with **Framework preset: Other**, no build command and output directory `.`.
   Or use the CLI: `npm i -g vercel`, then `vercel` from this folder, then `vercel --prod`.
2. Replace the placeholder domain (above) with the real one and redeploy.
3. Optional: add long `Cache-Control` headers for `/images/*` and `/fonts/*` (the files are immutable), e.g. in `vercel.json`.

## Quality checks done (13 Oct 2026)

- **Lighthouse** (Chrome DevTools, mobile and desktop): Accessibility 100, Best Practices 100, SEO 100.
- **Performance trace** (Slow 4G, 4× CPU): LCP ≈ 1.0 s, CLS 0.00.
- **Viewports:** 320, 375/390, 768, 1024, 1440 and 1920 px, with no horizontal overflow.
- **Interactions tested in Playwright:**
  - mobile menu: focus trap, Esc, links
  - gallery filters
  - lightbox: arrows, Esc, swipe, counter, focus return
  - unit "Pošaljite upit" pre-selecting the unit
  - form validation and the demo state
  - HR ↔ EN switch: all 182 translation keys are covered
- No console errors.
