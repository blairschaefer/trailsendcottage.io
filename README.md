# Trail's End Cottage — Website

A lightweight, single-page static site for the Trail's End cottage. No build step, no
frameworks, no external fonts — just HTML, CSS, and images. It loads fast and works on
any modern browser, phone or desktop.

## What's in this folder

```
index.html      The whole site (HTML + CSS + a little JS, all in one file)
404.html        A friendly "page not found" page
favicon.svg     The little "T" tab icon
images/         Six optimized photos used across the page
README.md       This file (you don't need to upload it)
```

## How to put it online with Cloudflare Pages (free)

You have two easy options. **Direct Upload** is the simplest — no GitHub needed.

### Option A — Direct Upload (easiest)

1. Sign in at https://dash.cloudflare.com and choose **Workers & Pages** in the sidebar.
2. Click **Create application** → **Pages** → **Upload assets**.
3. Give the project a name (e.g. `trails-end-cottage`).
4. Drag the **contents** of this folder (the `index.html`, `404.html`, `favicon.svg`,
   and the `images` folder) into the upload box. You can drag the whole folder — just
   make sure `index.html` ends up at the top level, not inside another folder.
5. Click **Deploy site**. In a few seconds you'll get a live URL like
   `https://trails-end-cottage.pages.dev`.

To update the site later, open the project, click **Create new deployment**, and upload
the changed files again.

### Option B — Connect a Git repository (if you use GitHub)

1. Put this folder's contents in a GitHub repository.
2. In Cloudflare Pages, choose **Connect to Git** and select the repo.
3. For **Build settings**, since there's no build step:
   - Framework preset: **None**
   - Build command: *(leave blank)*
   - Build output directory: `/`
4. Deploy. Every push to the repo will redeploy automatically.

## Using your own domain (e.g. trailsendcottage.io)

Once the site is live on `*.pages.dev`:

1. In the Pages project, open **Custom domains** → **Set up a custom domain**.
2. Enter your domain (e.g. `trailsendcottage.io` or `www.trailsendcottage.io`).
3. If your domain's DNS is already on Cloudflare, it configures automatically. If not,
   Cloudflare will show you the DNS record to add at your registrar.

The footer and page text currently reference `trailsendcottage.io` — update those in
`index.html` if your final domain is different.

## Editing the site

Everything lives in `index.html`. To change wording, search for the text you want to edit
and type over it. A few common spots:

- **Phone number:** search for `352.448.1048` (appears in the footer link too, as `tel:+13524481048`).
- **Instagram handle:** search for `@trailsendcottage` / `instagram.com/trailsendcottage`.
- **Booking note:** search for "Airbnb and Vrbo" — once you have live listing links, you can
  turn the "Inquire & Book" button into a real link by replacing `href="#contact"` with the URL.
- **Photos:** replace any file in `images/` with a new one of the same name to swap it. Keep
  new images optimized (long edge ~1600–2000px, JPEG quality ~80) so the site stays fast.

## A note on photos

The site reuses the property photos you provided, including the cottage exterior, the
dune-grass bluff, the Lake Michigan sunset, the interior stairway, and the blue-bench
detail. If you'd rather not feature the bench photo (the one of the gentleman on the deck),
open `index.html`, search for `bench.jpg`, and remove that full-bleed image band — the page
will close up cleanly without it.
