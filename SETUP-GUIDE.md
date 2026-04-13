# Hila Teller Website — Setup Guide

## What's in this folder

| File | Purpose |
|------|---------|
| `index.html` | Your complete website (edit this) |
| `sitemap.xml` | Helps Google find and index your pages |
| `robots.txt` | Tells search engines they can crawl your site |
| `CNAME` | Links your custom domain to GitHub Pages |
| `SETUP-GUIDE.md` | This file |

---

## Step 1: Fill in Your Personal Details

Open `index.html` and search for each of these placeholders. Replace them with your real information:

| Placeholder | Replace With |
|-------------|-------------|
| `YOUR PHONE NUMBER` | e.g. `(650) 555-0123` |
| `YOUR-PHONE-NUMBER` | URL-safe version, e.g. `6505550123` (in `tel:` links) |
| `YOUR-EMAIL` | e.g. `hila@hilateller.com` |
| `YOUR EMAIL ADDRESS` | Same email, display version |
| `YOUR STREET ADDRESS` | Your office street address |
| `YOUR_FORMSPREE_ENDPOINT` | From step 3 below |
| Photo placeholder | Your professional headshot (see Step 2) |

---

## Step 2: Add Your Photo

1. Save your professional headshot as `photo.jpg` in this folder.
2. In `index.html`, find the `<!-- Replace the div below with: -->` comment.
3. Replace the entire `<div class="photo-placeholder">...</div>` block with:

```html
<img src="photo.jpg" alt="Hila Teller, LCSW — Therapist in Los Altos, CA" loading="lazy">
```

**Photo tips for SEO:**
- File name: `hila-teller-therapist-los-altos.jpg` (keyword-rich filename)
- Keep it under 200KB (use https://squoosh.app to compress)
- Warm, professional headshot works best with this design

---

## Step 3: Set Up the Contact Form (Free)

1. Go to **https://formspree.io** and sign up for a free account.
2. Click "New Form" and name it something like "hilateller.com contact".
3. Copy the form endpoint URL (looks like `https://formspree.io/f/xabcdefg`).
4. In `index.html`, find `YOUR_FORMSPREE_ENDPOINT` and replace it with your endpoint.

That's it — Formspree handles form submissions for free (up to 50/month on the free plan).

---

## Step 4: Deploy to GitHub Pages

### First time setup:
1. Go to **https://github.com** and create a free account (if you don't have one).
2. Click the **+** button → **New Repository**.
3. Name it anything (e.g. `hilateller-website`).
4. Set it to **Public**.
5. Click **Create repository**.

### Upload your files:
1. Click **Add file → Upload files**.
2. Drag all files from this folder into the upload area.
3. Click **Commit changes**.

### Enable GitHub Pages:
1. Go to your repo → **Settings** → **Pages** (in the left sidebar).
2. Under "Source", select **Deploy from a branch**.
3. Choose **main** branch and **/ (root)** folder.
4. Click **Save**.

Your site will be live at `https://YOUR-USERNAME.github.io/hilateller-website/` within a few minutes.

---

## Step 5: Connect Your Custom Domain (hilateller.com)

1. In your GitHub repo → Settings → Pages → Custom domain, enter: `hilateller.com`
2. Log in to your domain registrar (where you bought hilateller.com — e.g. GoDaddy, Namecheap).
3. Go to your DNS settings and add these **A records**:

```
Type: A  |  Host: @  |  Value: 185.199.108.153
Type: A  |  Host: @  |  Value: 185.199.109.153
Type: A  |  Host: @  |  Value: 185.199.110.153
Type: A  |  Host: @  |  Value: 185.199.111.153
```

4. Also add a **CNAME record**:
```
Type: CNAME  |  Host: www  |  Value: YOUR-GITHUB-USERNAME.github.io
```

5. In GitHub Pages settings, check **Enforce HTTPS** once the domain is verified (can take up to 24 hours).

---

## Step 6: Critical Google SEO Steps

Once your site is live:

### Google Search Console (free, essential)
1. Go to **https://search.google.com/search-console/**
2. Add property → enter `https://hilateller.com`
3. Verify ownership (GitHub Pages makes this slightly tricky — use the HTML tag method)
4. Submit your sitemap: `https://hilateller.com/sitemap.xml`

### Google Business Profile (most important for local SEO)
1. Go to **https://business.google.com**
2. Create or claim your listing for "Hila Teller LCSW"
3. Set your address to your Los Altos office
4. Add photos, hours, services
5. Ask satisfied clients for Google reviews (reviews are huge for local ranking)

### Psychology Today Profile
- Make sure your Psychology Today listing exists and links to `https://hilateller.com`
- Keep your name, address, and phone consistent across all listings (Google uses this to verify legitimacy)

### Other directory listings to create/update:
- TherapyDen (free)
- Zencare
- Open Path Collective (if applicable)
- Yelp for Business
- Healthgrades

---

## SEO Features Already Built Into This Site

✅ Keyword-optimized title tag ("Therapist in Los Altos, CA")  
✅ Meta description targeting local search queries  
✅ Schema.org JSON-LD for LocalBusiness, Person, and FAQ  
✅ FAQ schema (eligible for rich results in Google)  
✅ H1 tag with city + service keywords  
✅ LocalBusiness areaServed with nearby cities  
✅ Semantic HTML5 with aria-label attributes  
✅ Mobile responsive design  
✅ Fast-loading (no heavy frameworks)  
✅ sitemap.xml and robots.txt  
✅ Open Graph tags for social sharing  
✅ HTTPS-ready  
