# Acacia Academy of Music Website

The website for [Acacia Academy of Music](https://acacia-academy.com), a private piano studio in Rogersville, Alabama. It explains the studio's approach, lists lesson formats and rates, introduces the teacher, and offers a free printable music resource.

It is a small static site written by hand in HTML, CSS, and JavaScript. There is no framework, no build step, and no server code.

## Pages

| Page | Purpose |
| --- | --- |
| `index.html` | Home page: the studio's approach, lesson formats and rates, and contact details |
| `lessons.html` | Lesson structure, elective studies, and rates |
| `about.html` | About the teacher and the studio |
| `resources.html` | Free downloads, including a printable copywork workbook |

`sitemap.xml` lists these four pages.

## How it works

- **Styling.** One shared stylesheet, `css/main.css`, defines the layout and the color palette as CSS custom properties. Pages also use some inline styles for one-off adjustments.
- **Scripts.** `js/main.js` is the only script and is loaded on every page.
- **Fonts.** Libre Baskerville, Playfair Display, Marcellus, and Inter are loaded from Google Fonts.
- **Contact.** The site has no forms or backend. Visitors reach the studio through email and phone links.
- **Downloads.** The free workbook is a PDF in `assets/downloads/`, shown with a preview image from `assets/images/`.
- **Search and sharing.** Each page has a canonical URL, Open Graph and Twitter card tags, and a meta description. The home page also includes `schema.org` `MusicSchool` structured data, and `sitemap.xml` lists the public pages.

The pages load no analytics, payment, or other tracking scripts.

## Repository layout

```
.
├── index.html
├── lessons.html
├── about.html
├── resources.html
├── sitemap.xml
├── css/
│   └── main.css
├── js/
│   └── main.js
└── assets/
    ├── images/
    └── downloads/     (PDF resources)
```

## Running locally

Pages use relative paths, so you can open `index.html` directly in a browser. To serve the site instead, run this from the repository root:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Updating the site

- **Rates.** Lesson prices appear on the home page, on `lessons.html`, and in the `priceRange` field of the structured data on the home page. Update all three together.
- **Navigation and footer.** They are copied into every page, so any change has to be made in each file.
- **New downloads.** Put the PDF in `assets/downloads/`, add a preview image, and add a card to `resources.html`.
- **Cache busting.** The stylesheet link carries a version number (`main.css?v=3`). Increase it after changing the CSS so returning visitors get the new styles.

## Contact

info@acacia-academy.com

## License

Copyright 2026 Acacia Academy of Music. All rights reserved.
