# ZA Online Cafe – Static Website

A clean, mobile-friendly, **single-file static website** for a local internet café in Langa, Cape Town.  
The site highlights services with **collapsible sections**, includes **WhatsApp call-to-actions**, an in-page **booking form**, testimonials, business hours, and contact details — all in one `index.html`.

Ready to be hosted on GitHub Pages. **No external libraries** required (pure HTML + CSS + a tiny bit of JS).

---

## Features

- **Single file**: everything (markup + styles + minimal JS) is contained in `index.html`.
- **Responsive layout**: works across desktop, tablet, and mobile.
- **Collapsible services (accordion)**: built with native `<details>/<summary>` — accessible, no JavaScript required.
- **WhatsApp CTAs**:
  - Top-right “WhatsApp” button
  - “Contact for Pricing” under each service group
  - Bottom-left **floating** WhatsApp button
- **Booking**:
  - In-page booking form (`mailto:` action by default)
  - Optional one-click **Book via WhatsApp**
- **Sections included**: About, Services, CV Tool, Testimonials, Visit & Hours.
- **Footer**: brand, quick description, simple social placeholders, contact info.
- **SEO basics**: `<title>`, `meta description`, and `theme-color` included.

---

## Project Structure

└── index.html # Single-page site (HTML + inline CSS + tiny JS)

> You may later add:
> - `assets/` (images, favicon, icons)  
> - `CNAME` (custom domain support)  
> - `robots.txt` / `sitemap.xml` (SEO improvements)

---

## Quick Start (Local Preview)

Simply double-click `index.html` to open it in a browser.  
For a lightweight local server, run:

```bash
# Python 3
python -m http.server 8000
# Open http://localhost:8000
# Node.js
npx serve .
# Open the local address provided

Deploy – GitHub Pages
Place index.html in the root of your branch and push to GitHub.
Go to Repository → Settings → Pages.
Source: select the branch (e.g., main or your custom branch)
Folder: select / (root)
Save → wait 1–2 minutes.
GitHub Pages will generate a live URL for your site.
(Optional) Add a custom domain:
Configure it in Pages settings.
Add a CNAME file with your domain name (e.g., zaonlinecafe.co.za).

Customization
  Branding and Text
Update <title> and <meta description> in the <head>.
Edit hero tagline and section texts inside index.html.
WhatsApp Numbers and Messages
Search for wa.me/27210652027 and replace with your number in international format (no +).
Example:
<a href="https://wa.me/27210652027?text=Hi%20ZA%20Online%20Cafe%2C%20I%27d%20like%20to%20ask%20about%20your%20services.">WhatsApp</a>
  Booking Form
Current setup:
<form action="mailto:zaonlinecafe@gmail.com" method="post" enctype="text/plain">
Replace with Formspree, Netlify Forms, or your backend endpoint for real submissions.
  Booking via Calendly (or similar)
Change all href="#booking" to your scheduling link (e.g., https://calendly.com/...).
  Business Hours, Address, Contact Info
Update directly in the Visit & Hours and footer sections.

Code Notes
Accordion: Implemented with <details>/<summary>, styled with CSS, arrow indicator flips via .caret.
Mobile nav: Minimal JS toggles nav ul.show.
Floating buttons:
Bottom-left: WhatsApp (.float-wa)
Bottom-right: Book Now (.float-book)
No external dependencies: vanilla HTML, CSS, and JS.

Accessibility & SEO
<details>/<summary> is accessible out of the box (keyboard + screen reader).
Buttons and links use clear text or aria-label.
Includes meta description and theme-color.
Further improvements:
Add Open Graph / Twitter Card meta tags
Provide a favicon and manifest.webmanifest

Known Behaviors
mailto: depends on user’s default mail client. If none is configured, it won’t work.
Recommendation: use Formspree/Netlify for reliability.
WhatsApp links:
On mobile: opens WhatsApp app.
On desktop: opens WhatsApp Web.

License
This site template was created for ZA Online Cafe’s public presence.
If reusing for other purposes, consider adding an open-source license (e.g., MIT).

Credits
Design & development: Single-file static site with vanilla HTML/CSS/JS.
Icons: native emojis (you may replace with SVGs).

