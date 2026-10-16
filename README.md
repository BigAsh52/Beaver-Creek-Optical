# Beaver Creek Optical — Website

Static brochure site for **beavercreekoptical.com**, deployed on Netlify from GitHub.

```
site/          ← everything Netlify publishes (the live website)
  index.html, thank-you.html, styles.css
  images/      mascot, header icon, footer logo, social share image
  fonts/       self-hosted Fraunces + Inter (no Google Fonts call)
brand/         ← full-size logo files for print, email, social (NOT published)
netlify.toml   ← tells Netlify to publish /site, plus headers and the www redirect
```

## 1. Put it on GitHub
1. On github.com, click **New repository** and name it `beaver-creek-optical`. Make it private, and don't add a README.
2. In this folder, run:
   ```
   git remote add origin https://github.com/<your-account>/beaver-creek-optical.git
   git push -u origin main
   ```
   (If you use GitHub Desktop instead: **File → Add Local Repository**, choose this folder, then **Publish repository**.)

## 2. Connect Netlify
1. Go to app.netlify.com, then **Add new site → Import an existing project → GitHub**, and pick the repo.
2. Leave the build command blank. The publish directory comes from `netlify.toml` (`site`). Click **Deploy**.
3. From then on, every push to `main` redeploys the site automatically.

## 3. Domain
**Domain management → Add a domain** → `beavercreekoptical.com`, then follow Netlify's DNS steps at your registrar.
HTTPS is issued automatically. `www` redirects to the bare domain.

## 4. Contact form email
After the first deploy, Netlify detects the form named **contact**. To get leads by email:
**Site configuration → Forms → Form notifications → Add notification → Email notification** and enter the inbox
(for example julie@beavercreekoptical.com). Spam is filtered by a hidden honeypot field and by Netlify's built-in spam filter.
Submissions are also listed under **Forms** in the Netlify dashboard.

## Brand
- Navy (primary) `#022241` · dark `#011A33` · tint `#E4E9F0`
- Brown (accent) `#814F30` · dark `#5F3A22` · light on dark `#D9B48E` · tint `#F2E8DC`
- Cream (background) `#FAF5EC`
- Logo: `brand/bc-logo.png` (full, transparent), `brand/bc-logo-reverse.png` (for navy backgrounds),
  `brand/bc-wordmark.png` (no arcs, for headers), `brand/bc-icon.png` (BC monogram, for social avatars and the favicon),
  `brand/bc-logo-original-cream.png` (the original file on cream).
- Fonts on the site: Fraunces (headings) and Inter (body), self-hosted.

## Still to fill in
- Phone number (commented out in the Contact section of `index.html`)
- Confirm the product list and the Indian Economic Enterprise wording
