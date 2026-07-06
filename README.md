# Chazel — Official Website

A 5-page site for Chazel (Iradukunda Chalom), Burundian memelord & content
creator. Built from the same structure as the Kirikou Akili template, reskinned
with a bold/meme visual theme.

## Pages
- `index.html` — Home (hero, social stats)
- `about.html` — About (bio, quick facts, content stats)
- `collaboration.html` — Brand/business collaboration pitch (promotion,
  sponsored content, social campaigns, creative partnerships, video marketing)
- `partnership.html` — Business & Partnerships: Superbat (roofing sheets,
  nails, construction materials) + Adda Global Company (travel agency —
  flight booking, visa assistance, international travel access)
- `contact.html` — Contact info + message form

## Files you need to add
Create an `images/` folder next to these files and add:
- `chazel-icon.jpg` — browser tab favicon
- `chazel_home_page.jpeg` — home hero background (also used as the social
  share preview image)
- `chazel_about_page.jpeg` — about page hero background
- `chazel_collaboration.jpg` — collaboration page hero background
- `chazel_superbat.jpg` — partnership page hero background
- `facebook.png`, `instagram.png`, `tiktok.png`, `x.png`, `youtube.png` —
  social icons
- `gmail.jpg`, `whatsapp.png` — contact icons (whatsapp.png is reused for
  both the WhatsApp Channel card on the home page and the contact page)

## Editing
- Colors, fonts, and the "sticker" badge style all live in `style.css` under
  `:root` — change the hex values there to retheme the whole site at once.
- `script.js` handles the hamburger menu, video play/pause, active nav
  highlighting via CSS, and the contact form's real submission (see below).
- Update the phone number / WhatsApp link and email address in `contact.html`
  and `about.html` once you have the final ones you want published.

## Contact form — Formspree setup (do this before going live!)
The form in `contact.html` is wired to submit to **Formspree**, but it needs
your own Form ID to actually deliver messages:
1. Go to https://formspree.io and create a free account.
2. Click "New Form", name it, and confirm your own email as the recipient.
3. Formspree gives you an endpoint like `https://formspree.io/f/abcdwxyz`.
4. In `contact.html`, find the `<form id="contact-form" ...>` tag and replace
   `YOUR_FORM_ID` in its `action` attribute with your real ID.
5. Upload the site and send yourself a test message from the live form.

Full step-by-step instructions are also written directly above the `<form>`
tag in `contact.html` as HTML comments, so you'll see them again right where
you need them.

## One row on desktop, wrap on mobile
Two grids were built to always fit in a single row on desktop/tablet, and
wrap onto multiple rows on small phones for readability:
- Home page social platforms (`.social-grid-home` in `style.css`) — currently
  sized for 6 cards. If you add/remove a platform, update the
  `repeat(6, 1fr)` number in that rule to match your new count.
- Collaboration page boxes (`.collab-grid` in `style.css`) — currently sized
  for 5 cards, same idea if you add/remove one.

## Active page indicator
Each page's own nav link has `class="active"` added to it (e.g. `about.html`
marks its own "About Me" link). This is styled in `style.css` under
`.nav-links a.active` — currently shown as a pink underline + pink text. If
you ever add a new page, remember to add `class="active"` to that page's own
link and leave the others plain.
