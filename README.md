# Ceiniog 🪙

A lightweight, self-contained coin weight calculator. Enter the weight of your coins and Ceiniog instantly calculates the total value — no app install, no server, no dependencies to manage.

---

## Features

- **Weight-based calculation** — enter coin weights in grams to get an instant total value
- **Multi-currency support** — GBP, EUR, USD, and CAD
- **Multi-language support** — English, Welsh (Cymraeg), Spanish, French, Italian, and German
- **Dark / light theme** — toggle with a single click, preference saved locally
- **Print support** — printer-friendly overlay with signature fields, optimised for standard paper and thermal receipt printers
- **Responsive layout** — inputs and results sit side by side on wider screens and stack on mobile
- **Fully self-contained** — a single `.html` file with all CSS, JavaScript, and data embedded inline; no build step, no external files required

---

## Usage

1. Download `Ceiniog.html`
2. Open it in any modern web browser
3. Select your currency and language from the **Settings** menu
4. Weigh your coins on a scale (accurate to 1g) and enter the weights
5. Results update instantly as you type
6. Use the **Print** button to generate a printable receipt

No installation, no internet connection required after the initial load (except for Google Material Symbols icons and flag images, which are loaded from CDNs — see [Offline Use](#offline-use) below).

---

## Supported Currencies

| Currency | Symbol | Coins included |
|----------|--------|----------------|
| GBP | £ | 1p, 2p, 5p, 10p, 20p, 50p, £1, £2 |
| EUR | € | 1c, 2c, 5c, 10c, 20c, 50c, €1, €2 |
| USD | $ | 1¢, 5¢, 10¢, 25¢, 50¢, $1 |
| CAD | $ | 5¢, 10¢, 25¢, $1, $2 |

---

## Supported Languages

| Code | Language |
|------|----------|
| `en` | English |
| `cy` | Welsh (Cymraeg) |
| `es` | Spanish (Español) |
| `fr` | French (Français) |
| `it` | Italian (Italiano) |
| `de` | German (Deutsch) |

Language and currency preferences are saved in `localStorage` and restored on next visit.

---

## URL Parameters

You can set the default language and currency via URL parameters, which is useful for sharing a pre-configured link:

```
Ceiniog.html?coinSet=EUR&setLang=fr
```

| Parameter | Values | Default |
|-----------|--------|---------|
| `coinSet` | `GBP`, `EUR`, `USD`, `CAD` | `GBP` |
| `setLang` | `en`, `cy`, `es`, `fr`, `it`, `de` | `cy` |

---

## Print Support

Ceiniog's print layout is optimised for multiple paper sizes:

- **A4 / standard** — full layout with coin table and signature fields
- **Thermal (80mm)** — compact receipt-style layout
- **Thermal (58mm)** — minimal layout, borders removed, large text for readability

---

## Offline Use

Ceiniog is nearly fully offline-capable. The two external resources it loads are:

- **Google Material Symbols** font (icons) — via Google Fonts CDN
- **Flag images** — via [flagcdn.com](https://flagcdn.com), loaded only when the Settings overlay is opened

To make the app fully offline, these can be replaced with:
- Inline SVG icons (replacing the Material Symbols `<span>` elements)
- Unicode flag emoji (replacing the flag images in the language/currency buttons)

---

## Project Structure

The entire project is a single file:

```
Ceiniog.html
├── <style>          — All CSS, including theme variables and print media queries
├── <body>           — HTML structure for main UI and overlays (print, FAQ, settings)
└── <script>         — All JavaScript, including embedded FAQ data and coin weight data
```

---

## Accuracy

Ceiniog uses official mint coin weights for calculations. Results are as accurate as your input — a scale precise to 1g is recommended. Mixed or worn coins may produce small variances.

---

## Browser Support

Any modern browser — Chrome, Firefox, Safari, Edge. No polyfills required.

---

## Licence

MIT — free to use, modify, and distribute.
