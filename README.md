# Matt Moore portfolio site

A lightweight static portfolio built with plain HTML, CSS, and a small amount of JavaScript. There is no build step, framework, database, or CMS required.

## What's included

- `index.html` — page content and structure
- `styles.css` — layout, responsive design, earthy visual system, focus states, and reduced-motion handling
- `script.js` — mobile menu, sticky-header state, and current year
- `Matt-Moore-Resume.pdf` — résumé linked from the site
- `favicon.svg` — browser icon
- `robots.txt` and `sitemap.xml` — basic search-engine files
- `netlify.toml` — optional security/cache headers when hosted on Netlify

## Preview it locally

You can double-click `index.html`, but using a tiny local web server gives you a more realistic preview.

1. Open Terminal (macOS) or PowerShell/Terminal (Windows).
2. Change directory into this folder.
3. Run:

   ```bash
   python3 -m http.server 8080
   ```

   On Windows, `python -m http.server 8080` may be the command instead.

4. Open `http://localhost:8080` in a browser.

## Recommended path to publish it

### Option A: Netlify — simplest for these files

1. Create or sign in to a Netlify account.
2. Use Netlify Drop and drag this whole project folder into the drop zone.
3. Netlify will publish a temporary `*.netlify.app` URL. Review the site there before changing your domain.
4. In the project, open **Domain management** and add `mattmoore.design` as a domain you already own.
5. Follow the DNS records Netlify shows for your exact setup.
6. Keep the old site live until the new temporary URL is fully checked, then make the DNS change.

**Important because your email uses `@mattmoore.design`:** if you move DNS/nameservers, copy your existing MX/TXT records for email before changing anything. Changing only web records is often safer than moving all DNS if your registrar already manages email correctly.

Your current public site appears to use Webflow-hosted assets. Moving this static version to Netlify means you are changing the hosting destination for the domain; you are not transferring the domain registration itself.

### Option B: Git-based hosting

If you want version history and easy future edits, create a GitHub repository with these files, then connect that repository to Netlify (or another static host). Each push can deploy automatically.

## Update content

### Résumé

Replace `Matt-Moore-Resume.pdf` with a new file using the **same filename** and all résumé links will continue to work.

### LinkedIn

The site currently links to:

`https://www.linkedin.com/in/mattmooredesign/`

Search `index.html` for `linkedin.com` if you ever need to change it.

### Email

Search `index.html` for `me@mattmoore.design` to replace the contact email everywhere.

### Project copy

The Bass Pro Shops case studies are intentionally high-level. Before publishing, make sure every statement is appropriate for a public portfolio and does not reveal confidential metrics, screenshots, workflow details, or compliance logic.

## Add real project images later

The current visuals are CSS/SVG abstractions so the site can ship without exposing internal screenshots. When you have approved images:

1. Create an `images/` folder.
2. Export web-friendly AVIF or WebP images at roughly 1600px wide.
3. Add meaningful `alt` text when the image communicates content. Use `alt=""` only for purely decorative images.
4. Set explicit `width` and `height` attributes to reduce layout shift.
5. Use `loading="lazy"` for images below the first viewport.

For bird photography or pottery images, a good next addition would be a small “Field notes” gallery beneath About. Those personal photos can add the outdoorsy character without making the professional case studies feel themed.

## Accessibility checks before sharing

The code already includes semantic landmarks, a skip link, keyboard-visible focus, a keyboard-operable mobile menu, responsive layouts, reduced-motion support, descriptive link text, and high-contrast typography. Still, accessibility needs real testing.

Before launch:

1. **Keyboard:** use only Tab, Shift+Tab, Enter, and Escape. Every interactive control should be reachable, visible when focused, and usable.
2. **Zoom:** test at 200% browser zoom and at a narrow phone width. Content should reflow without horizontal scrolling.
3. **Screen reader:** test at least the page title, headings, navigation, case-study sections, links, and mobile menu with VoiceOver (macOS/iOS) or NVDA (Windows).
4. **Automated audit:** run Chrome DevTools → Lighthouse → Accessibility. Treat failures as issues to fix, not just a score to raise.
5. **Manual review:** automated tools cannot prove WCAG conformance. Check heading order, focus order, link purpose, motion, contrast, and any image alternatives yourself.
6. **PDF:** the linked résumé is a separate document. If you want the portfolio to be fully accessible, make sure the PDF has real text, a logical reading order, document language, and tags/headings—not just visual layout.

## Domain cutover checklist

- [ ] New temporary URL looks correct on desktop and mobile
- [ ] Email and LinkedIn links work
- [ ] Résumé opens correctly
- [ ] Keyboard navigation works
- [ ] Lighthouse accessibility audit reviewed
- [ ] Existing email DNS records are recorded/backed up
- [ ] Domain added to the new host
- [ ] DNS updated only after preview approval
- [ ] HTTPS works at both `mattmoore.design` and `www.mattmoore.design` as intended
- [ ] Search Console / analytics reconnected if you use them
- [ ] Old Webflow project kept available briefly in case you need to roll back

## Optional next improvements

- Add approved project screenshots and outcome metrics.
- Create dedicated case-study pages for LineUp, ProGrade, retail systems, and Forerunner.
- Add a bird photography / pottery “Field notes” gallery.
- Add an Open Graph social preview image.
- Add privacy-friendly analytics (for example, Plausible or Cloudflare Web Analytics) only if you want traffic data.

## Image source

The Forerunner 965 project uses an official Garmin product image downloaded from Garmin's product media (`res.garmin.com`). The image remains copyright Garmin Ltd. or its subsidiaries. For a public portfolio, confirm that your use complies with Garmin's brand/media permissions; otherwise replace it with a photo you have permission to publish.


### About-section image credits

The three About cards intentionally use sourced archival / open-access imagery and preserve visible source links in the site:

- **Clay:** *Terracotta neck-amphora (jar)*, Greek, Attic, ca. 540–530 BCE, The Metropolitan Museum of Art, object 96.9.10. The Met marks this image Public Domain and makes its Open Access images available under CC0. Source: `https://www.metmuseum.org/art/collection/search/246113`
- **Birds:** John James Audubon, *Dusky Albatros*, Plate 407, *Birds of America*. Credit required by Audubon: “Courtesy of the John James Audubon Center at Mill Grove, Montgomery County Audubon Collection, and Zebra Publishing.” Source: `https://www.audubon.org/art/birds-of-america/dusky-albatros`
- **Plains:** *The Vast Tallgrass Prairie in the Flint Hills*, photo by Mike Blair, Kansas Department of Wildlife and Parks. National Archives identifier 7718391; the Federal Highway Administration source marks the image Public Domain. NARA catalog: `https://catalog.archives.gov/id/7718391`; image record: `https://fhwaapps.fhwa.dot.gov/bywaysp/photos/58932`
