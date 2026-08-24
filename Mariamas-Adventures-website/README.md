# Mariama's Adventures

The website for **Mariama's Adventures** — bird and nature tours in The Gambia,
guided by Mariama Sanneh.

**Contact:** +220 751 0351 (WhatsApp) · Mariamaksanneh@gmail.com

---

## What is in here

| File | What it is |
|---|---|
| `index.html` | The entire website. One file. All CSS, JavaScript and photos are inside it. |
| `404.html` | Shown if someone opens a link that does not exist. |
| `favicon.svg` | The little bird icon in the browser tab. |
| `og-image.png` | The preview card shown when the link is shared on WhatsApp or Facebook. |
| `robots.txt` | Tells search engines they may index the site. |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. Leave it. |
| `CNAME.example` | Template for a custom domain. See below. |

There is no build step, no framework and no dependencies. Open `index.html`
in any browser and it works, online or offline.

---

## Putting it online with GitHub Pages

1. Create the repository **under Mariama's own GitHub account** — not someone
   else's. If you name it `mariamasanneh.github.io` the site gets a clean address
   instead of `username.github.io/repo-name`.
2. Upload every file in this folder to the root of the repository.
3. Go to **Settings → Pages**.
4. Under *Build and deployment*, set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
5. Wait a minute or two, then reload the page. The address appears at the top.
6. Tick **Enforce HTTPS** once it becomes available.

The repository must be **public** for free GitHub Pages. That is fine — everything
in it is already visible on the website itself.

### Connecting a custom domain

1. At the domain registrar, add these DNS records:
   - Four `A` records for the bare domain pointing to `185.199.108.153`,
     `185.199.109.153`, `185.199.110.153` and `185.199.111.153`
   - One `CNAME` record for `www` pointing to `username.github.io`
2. Rename `CNAME.example` to `CNAME` and put the real domain inside it,
   on one line, with no `https://` and no trailing slash.
3. In **Settings → Pages**, enter the domain under *Custom domain* and save.
4. Wait for the certificate, then tick **Enforce HTTPS**.

DNS changes can take a few hours. Do not panic on the first attempt.

---

## Changing the website

Everything is in `index.html`. Open it in any text editor and search for the
text you want to change. Commit the change and GitHub Pages republishes it
within about a minute.

**Prices** appear in two places: the tour cards (search for `class="price"`)
and the note below them. Change both.

**Photos.** The three certificate images are embedded directly in the file as
`data:image/jpeg;base64,...`. The coloured blocks marked *PHOTO —* are
placeholders waiting for real pictures. To replace one, swap the
`<div class="ph">…</div>` for an `<img>` tag pointing at an image file you have
added to the repository.

**The WhatsApp number** appears in five places. Search for `wa.me` and change
them all if the number ever changes.

---

## Before you share the link

- [ ] The WhatsApp button opens a chat with the right number
- [ ] The email link opens a new message
- [ ] It looks right on a phone, not just a laptop
- [ ] The prices match the current rate card
- [ ] Real photos have replaced the placeholders

---

## Notes

The two fonts (Fraunces and Karla) load from Google Fonts. Everything else —
styles, script, images — is inside `index.html`, so the site works even if that
request fails.

The site collects nothing: no forms, no cookies, no tracking, no analytics.
Visitors contact Mariama directly through WhatsApp or email.
