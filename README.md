# Desa Banyukuning website

Public information website for Desa Banyukuning (Bandungan, Kabupaten Semarang, Central Java), built during the UNNES GIAT 15 community-service programme (KKN) in early 2026.

Plain HTML, CSS and JavaScript, so the village can host it anywhere for free and edit it without a build step.

**Pages:** home (live clock, prayer times from the Aladhan API, population figures), village profile, officials, news, budget, local businesses (order through WhatsApp), photo gallery, an interactive map (Leaflet) and a complaint form that opens a pre-filled WhatsApp message to the village office.

## My part

I designed the interface in Figma and built the front end. The content (news, budget, business list) came from the KKN team and the village office.

## Changes for this public copy

The site as delivered had bugs I fixed afterwards. This copy also protects the people in it:

- **13 broken images fixed.** Pages referred to `.png`/`.jpeg` files that were really `.jpg`.
- **The complaint form threw an error on every submit.** Two handlers were attached, and one read a field that had been removed. The duplicate is gone.
- **Dead code removed.** The active-menu highlighter looked for a `beranda.html` that never existed.
- **Smaller pages.** Photos are resized WebP: 12 MB became 5 MB.
- **Privacy:**
  - the officials' names and photos are replaced with placeholders;
  - residents' WhatsApp numbers are replaced with a dummy number;
  - photo alt texts now say who is pictured by role, instead of "Kepala Desa" on every photo.

## Run

Open `index.html`, or serve the folder:

```bash
python -m http.server
```

## Credits

UNNES GIAT 15 KKN team, Desa Banyukuning village office. The map embed and the official letter templates in `surat/` belong to their owners.
