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
(for example info@beavercreekoptical.com). Spam is filtered by a hidden honeypot field and by Netlify's built-in spam filter.
Submissions are also listed under **Forms** in the Netlify dashboard.

## Brand
- Raspberry (primary) `#B3124E` · dark `#8A0D3B` · tint `#FBEAF1`
- Green (secondary) `#2F7A55` · dark `#215A3E` · tint `#E7F3EC` · light on dark `#8FD3AE`
- Wordmark: Fraunces Black (900), uppercase · Tagline: Inter, wide letter-spacing
- `brand/logo-full.png` for light backgrounds, `brand/logo-full-reverse.png` for dark or raspberry, `brand/icon-*.png` for social avatars.

## Still to fill in
- Phone number (commented out in the Contact section of `index.html`)
- Confirm the product list and the Indian Economic Enterprise wording
