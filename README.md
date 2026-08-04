# Vizbl integration playground

Five self-contained demo storefronts, one per Vizbl product. Each page is plain
HTML + CSS — the kind of page a client already has — with two clearly marked
spots for pasting the Vizbl integration code.

| Page | Demo shop | Product | Integration |
| --- | --- | --- | --- |
| `index.html` | hub with links to all five | — | — |
| `core-ar.html` | NORDE — furniture | Fjord Armchair | Core AR |
| `wall-art.html` | MURAL — art prints | The Great Wave off Kanagawa | Wall Art |
| `rugs.html` | LOOM & FIELD — rugs | Antique Oushak rug | Rugs |
| `flooring.html` | FLOORWERK — flooring | Heritage Oak parquet | Flooring |
| `ai-tryon.html` | ODE Atelier — womenswear | Aurélie tulle gown | AI Try-On |

## How to use

1. Open a storefront and view the source. Every page has two marked comment blocks.
2. **STEP 1** sits in `<head>` — paste the Vizbl `<script>` tag there.
3. **STEP 2** sits right under the "Add to cart" button — paste the trigger element there.
4. To make the pasted button look native, give it the store's button class:
   - room-viewer / AI try-on button: `class="btn-cart"`
   - Core AR `<vizbl-core>` element: `unstyled trigger-class="btn-cart"` (both attributes are required)

Reload the page and the button appears in the store's own design.

## Running locally

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Notes

- The analytics snippets in each `<head>` (GTM, Meta Pixel, Hotjar, Segment, Matomo,
  Klaviyo, Intercom, Zendesk and friends) are deliberate set dressing with made-up IDs,
  so the pages look like real production storefronts. They are not expected to work, and
  a few of them 404 in the console by design.
- Shop names, prices, reviews and specs are fictional.

## Image credits

| File | Source | Licence |
| --- | --- | --- |
| `images/great-wave.jpg` | [The Great Wave off Kanagawa](https://commons.wikimedia.org/wiki/File:Tsunami_by_hokusai_19th_century.jpg), Hokusai, via Wikimedia Commons | Public domain |
| `images/starry-night.jpg` | [The Starry Night](https://commons.wikimedia.org/wiki/File:Van_Gogh_-_Starry_Night_-_Google_Art_Project.jpg), Van Gogh, via Wikimedia Commons | Public domain |
| `images/rug-oushak.jpg` | [Antique Turkish Oushak Carpet](https://commons.wikimedia.org/wiki/File:Antique_Turkish_Oushak_Carpet.jpg), via Wikimedia Commons | Public domain |
| `images/oak-parquet.jpg` | [Parquet floor wood texture](https://commons.wikimedia.org/wiki/File:Parquet_floor_wood_texture.jpg), via Wikimedia Commons | Public domain |
| `images/sofa-living.jpg` | Chair render | Supplied by repo owner |
| `images/dress.jpg` | ["Wedding Dress - Lan Chi"](https://www.flickr.com/photos/53579370@N07/8035928857) by [Mac Vincente](https://www.flickr.com/photos/53579370@N07) | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) |

The CC BY 2.0 credit is also shown on `ai-tryon.html` itself, under the product photo.
