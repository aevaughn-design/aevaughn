# Deploying Your Portfolio to GitHub Pages (Free)

Your portfolio is a single `index.html` file; it ships as-is to any static host. Below is the easiest free path: GitHub Pages.

---

## Option A: Drag-and-drop (no command line, ~5 minutes)

1. **Create a free GitHub account** at [github.com](https://github.com) if you don't have one.
2. **Create a new repository**:
   - Click the green "New" button (or go to [github.com/new](https://github.com/new)).
   - Repository name: `alexvaughn.github.io` (use *your* GitHub username); this special name lets GitHub serve it at `yourusername.github.io`.
   - Set it to **Public**.
   - Check "Add a README file."
   - Click **Create repository**.
3. **Upload your site**:
   - On the new repo page, click **Add file** &rarr; **Upload files**.
   - Drag `index.html` (and `DEPLOY.md` if you want) from this Portfolio folder into the page.
   - Scroll down, click **Commit changes**.
4. **Turn on GitHub Pages**:
   - Click the **Settings** tab.
   - Scroll to **Pages** in the left sidebar.
   - Under "Source," select **Deploy from a branch** &rarr; branch **main** &rarr; folder **/ (root)** &rarr; **Save**.
5. **Wait 30&ndash;60 seconds**, then visit `https://yourusername.github.io`. Done; your portfolio is live.

---

## Option B: Netlify drag-and-drop (also free, no GitHub needed)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Drag the `Portfolio` folder onto the drop zone.
3. Netlify gives you a live URL like `random-name-123.netlify.app`.
4. Sign up (free) to claim the site and rename it to something like `alexvaughn.netlify.app`.

---

## Custom domain (optional, ~$10/year)

If you ever want `alexvaughn.com` or similar:

1. Buy a domain at [Namecheap](https://www.namecheap.com), [Cloudflare Registrar](https://www.cloudflare.com/products/registrar/), or [Porkbun](https://porkbun.com).
2. In your GitHub Pages settings, add the custom domain.
3. Point your domain&rsquo;s DNS to GitHub Pages per their [docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

GitHub Pages and Netlify both serve custom domains for free; you only pay for the domain registration.

---

## Editing the site later

The whole site is one HTML file with embedded CSS and JavaScript. To update it:

- **Add a project**: search the file for `<a class="work-item` and copy one of the existing blocks; swap the `href`, image URL, title, and category.
- **Update bio or experience**: search for `id="about"` or `id="experience"` and edit the prose.
- **Change contact links**: search for `linkedin.com` or `behance.net/aevaughn` and update.

Then re-upload `index.html` to the same GitHub repo (or drop it back on Netlify).

---

## A note on the project images

Project covers are hot-linked from Behance&rsquo;s CDN; this keeps the site lean and lets your Behance updates flow through automatically. If Behance ever changes hotlink policy and an image breaks, simply right-click the broken image, copy the original URL from your Behance project, and replace the `src` attribute in `index.html` with a self-hosted copy (place files in an `/img` folder next to `index.html` and update the path).

---

## Notes on the design

- **Bold creative aesthetic**: heavy display type (Archivo Black) paired with editorial italic (Fraunces); cream/black palette with a yellow highlight that nods to your existing Behance brand.
- **Recruiter-grade copy**: positions you as a Senior Art Director / Creative Director, leads with the SXSW 2025 credit, and surfaces the Hello Eyes and Content Haus initiatives that distinguish you from junior or mid-level candidates.
- **Projects link to Behance**: keeps your work in one place; Behance updates automatically flow through the cover images.
- **Responsive**: works on phones, tablets, and desktops.
- **Zero dependencies**: no build step, no framework, no CMS; just open `index.html` in any browser.
