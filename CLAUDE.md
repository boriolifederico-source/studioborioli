# Studio Dentistico Dr. Stefano Borioli — Website

A single-page modern website for **Studio Dentistico Dr. Stefano Borioli**, a dental clinic in Intra (VB), Italy.

Live at: **https://boriolifederico-source.github.io/studioborioli**
Repo: **https://github.com/boriolifederico-source/studioborioli**

---

## Project structure

- `index.html` — the entire site (single-file HTML with inline CSS + JS)
- `logo.png` — primary clinic logo (high-resolution, auto-cropped from source)
- `favicon.ico` — browser tab icon (generated from the logo)
- `clinic.jpg` — real photo of the clinic interior with church view through window, used as parallax background banner
- `CLAUDE.md` — this file (project context)

GitHub Pages serves `index.html` from the `main` branch root.

---

## Clinic information (canonical)

- **Name:** Studio Dentistico Dr. Stefano Borioli
- **Address:** Via S. Vittore, 11, 28921 Intra VB, Italy
- **Phone:** +39 0323 52102
- **Email:** studio.borioli@libero.it
- **Province:** Verbano-Cusio-Ossola

### Opening hours (continuous, no lunch break unless stated)
- Lun (Mon): 9:00–19:00
- Mar (Tue): 12:00–19:00
- Mer (Wed): 12:00–19:00
- Gio (Thu): 9:00–16:00
- Ven (Fri): 9:00–16:00
- Sab (Sat): 9:00–12:00
- Dom (Sun): Closed

### Stats
- 20+ years of experience
- 36+ Google reviews, 5.0/5.0 stars
- We are NOT a free-first-visit clinic — never use "gratuita"

### Technologies we actually have
- **IO Scanner** (intraoral digital scanner)
- **Microscopio dentale** (we use ZEISS PRO Ergo — do not display the brand publicly to avoid IP concerns)
- **EMS Air-Flow Prophylaxis Master** (do not display the brand publicly)
- **Sterilizzazione certificata** (certified sterilization protocols)
- We do **NOT** have CBCT 3D X-ray or laser dentistry — do not list these

---

## Design system

### Colors (CSS variables)
```css
--pink: #E8437A          /* primary brand */
--pink-light: #F4C0D1
--pink-pale: #FBEAF0
--lavender: #B8B4D8
--lavender-light: #EEEDFE
--lavender-mid: #8B87C4
--dark: #2A2A35
--text: #3D3D4A
--muted: #7A7A8A
--surface: #F9F8FC
--white: #FFFFFF
--border: rgba(180, 176, 216, 0.3)
```

### Fonts
- **Cormorant Garamond** (serif) — headings, large display numbers, italic accents
- **DM Sans** (sans-serif) — body, UI, labels

### Brand voice
- Italian language throughout
- Warm, family-clinic tone ("una realtà familiare")
- Emphasis on care, technology, and humanity
- Pink + lavender palette matches the logo

---

## Page sections (in order)

1. **Nav** (fixed) — logo image + 6 links + "Prenota Ora" pink pill
2. **Hero** (`#hero`) — centered single column: eyebrow → heading "Ci prendiamo cura del *tuo sorriso*, ogni giorno." → sub → CTAs → stats row (20+ years + Google reviews badge)
3. **About** (`#about`) — heading "La tua salute è la nostra priorità." + 4 value cards (Accoglienza, Tecnologia, Cura, Sicurezza)
4. **Clinic Photo Banner** (`#clinic-photo`) — parallax `clinic.jpg` with gradient overlay and overlay text
5. **Servizi** (`#servizi`) — lavender-light background, 6 white cards: Odontoiatria Generale, Estetica Dentale, Ortodonzia, Implantologia, Pedodonzia, Protesi & Conservativa
6. **Tecnologia** (`#tecnologia`) — single centered column, numbered list 01–04 (IO Scanner, Microscopio, EMS Prophy, Sterilizzazione)
7. **Team** (`#team`) — 4-card grid with initials avatars (placeholders for real photos)
8. **Testimonials** (`#testimonials`) — carousel of 5 real Google reviews (Stephen & Elena, Paolo Oggioni, Cristina Gomez, Veronica Ruppen, Marinella Testori with LOCAL GUIDE badge); auto-plays every 7s; arrow + dot controls
9. **Per Te** (`#per-te`) — pink-pale background, 3 cards (Comfort, Flessibilità, Finanziamenti)
10. **Prenota CTA** (`#prenota`) — pink banner with "PRENOTA ORA" button
11. **Contatti** (`#contatti`) — left: address/phone/email/hours; right: booking form
12. **Footer** — 4 columns: brand (logo on white badge with sharp corners, no rounding) + Lo Studio / Servizi / Contatti link columns

---

## Important UX rules learned during this build

- **Mobile**: nav logo is centered, all sections center-align text, side padding 6%
- **Footer logo**: must sit inside a white rectangle with `border-radius: 0` (sharp corners), tight padding
- **Logo image**: must be auto-cropped to remove surrounding whitespace before deploying; use 1200px+ source for retina crispness
- **No third-party brand names**: ZEISS, EMS, etc. — describe generically
- **Reviews count**: 36 (NOT 5036 — that was an earlier mistake)
- **Hero**: no illustration / no floating cards — the user explicitly removed that section
- **Tech section**: no orbit-diagram SVG — user removed it
- **Booking dropdown**: "Prima visita" (NOT "Prima visita gratuita")

---

## Git workflow

The site is deployed via GitHub Pages from `main` branch root.

```bash
# Make changes to index.html
git add index.html
git commit -m "describe change"
git push origin main
# Wait 1-2 min for GitHub Pages rebuild
# Hard refresh in browser to bypass cache
```

The user is **federicoborioli** on macOS, GitHub username **boriolifederico-source**.

---

## Open / potential next steps

- Replace team initials avatars with real photos when available
- Add real treatment photos to the Services section (the user wants "realistic" images — recommend stock photos from Unsplash/Pexels or actual clinic photos rather than AI generation)
- Consider adding a real backend for the booking form (currently shows an alert on submit)
- Add Italian language meta tags for SEO and Open Graph image
- Possibly add a Google Maps embed in the Contatti section
