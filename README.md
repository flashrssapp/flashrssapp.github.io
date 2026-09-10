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

## Fonts

`fonts/` contains PT Serif (Regular and Bold) converted to WOFF2 and served from this repository, so **the site makes no third-party requests at all**: no Google Fonts, no CDN, no analytics, no cookies. That is deliberate. A site whose main claim is that the app does not phone home should not phone home itself.

PT Serif is © ParaType and licensed under the SIL Open Font License 1.1. The OFL requires the licence to travel with the font, so add `fonts/OFL.txt` (from <https://openfontlicense.org>) before treating redistribution as fully compliant.

## Editing

No build step, no dependencies. Open the HTML files and edit them.

Shared styles live in `style.css`. Colours are CSS custom properties at the top: `--teal` is `#14A08B`, taken from the launcher icon, and `--amber` is `#E07A1F`, the app's default palette accent.

The masthead and footer are duplicated across all four pages. Four copies is simpler than a build step at this size, but change one and change the rest.

## Keep accurate

`privacy.html` lists **every** network connection the app makes. If the app gains or loses one, this page is wrong until it is updated, and an inaccurate privacy policy is a Play policy violation rather than a cosmetic problem. The same applies to the permissions list.
