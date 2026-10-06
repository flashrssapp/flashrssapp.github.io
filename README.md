# flashrssapp.github.io

Website for **Flash RSS Reader**, an Android feed reader published by DVM Software.

Live at <https://flashrssapp.github.io>

## Pages

| File | Purpose |
|---|---|
| `index.html` | Homepage. Describes what the app does. Required by Google Play for a listed app website, and the page a reviewer reads first. |
| `privacy.html` | Privacy policy. **Required by Google Play**, entered under App content → Privacy policy and in the store listing. Also linked from inside the app. |
| `support.html` | Contact details, publisher identity and FAQ. Covers Play's News &amp; Magazines requirement that contact information be reachable via a URL. |
| `terms.html` | Terms of use. |

## Deploying

Static HTML. GitHub Pages serves the `main` branch from the repository root, so pushing to `main` publishes. Changes usually appear within a minute.

`.nojekyll` is present so Pages serves the files as-is rather than running them through Jekyll.

## Look

Quiet Ink, as in the app (6 Oct 2026). Colours are CSS custom properties at the top of `style.css`, copied from the app's theme (`lib/theme/app_theme.dart`): teal `#0E6A70` (dark `#7BD0D3`) is the only interactive colour; light and dark follow the visitor's system. The pool-tile mosaic (`img/pool-tile.png`, the app's own texture) sits dim behind the header and the home hero only, at the app's own opacity (7% light, 10% dark), never behind body text.

## Images

`img/` holds the Mosaic F ("Solid F + halo") exactly as exported from the app repo's `icon/mosaic-f/`: `mosaic-f.svg` (header and favicon), `favicon-32.png`, `apple-touch-icon.png`, `icon-192.png`, and `og-image.png` (the Play icon, used for link previews). Re-export them there; never redraw.

## Fonts

`fonts/` holds the app's own fonts as WOFF2, served from this repository, so **the site makes no third-party requests at all**: no Google Fonts, no CDN, no analytics, no cookies. That is deliberate. A site whose main claim is that the app does not phone home should not phone home itself.

- Literata for headlines, Instrument Sans for text, JetBrains Mono (subset) for numbers and prices only.
- All three are under the SIL Open Font License 1.1; `fonts/OFL.txt` carries their copyright lines and the licence.

## Editing

No build step, no dependencies. Open the HTML files and edit them.

The masthead and footer are duplicated across all four pages. Four copies is simpler than a build step at this size, but change one and change the rest. `terms.html#your-own-gemini-key` is linked from inside the app: keep that anchor.

## Keep accurate

`privacy.html` lists **every** network connection the app makes. If the app gains or loses one, this page is wrong until it is updated, and an inaccurate privacy policy is a Play policy violation rather than a cosmetic problem. The same applies to the permissions list.
