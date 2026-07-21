# Solar in SD

A static site helping South Dakota homeowners navigate solar permitting, utility
interconnection, and incentives. Plain HTML/CSS/JS — no build step.

## Pages

- `index.html` — home
- `permits.html` — SD Electrical Commission homeowner wiring permit + local building permits
- `interconnection.html` — net metering (SD has none mandated) + utility interconnection agreements
- `incentives.html` — federal ITC + SD property tax exemption
- `resources.html` — links to official forms, statutes, and agencies

## Deploying on GitHub Pages

1. Create a new GitHub repo (e.g. `solarinsd`) and push everything in this folder to the
   `main` branch (or a `docs/` folder — either works).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**, then pick
   `main` and the `/ (root)` folder (or `/docs` if you used that layout).
4. Save. GitHub will publish at `https://<your-username>.github.io/<repo-name>/`.

## Using your own domain (solarinsd.com)

This folder already includes a `CNAME` file containing `solarinsd.com`, which is what
GitHub Pages uses to know which custom domain to serve.

1. At your domain registrar, add these DNS records for the apex domain:
   - `A` records pointing `solarinsd.com` to GitHub Pages' IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Optionally, a `CNAME` record for `www.solarinsd.com` pointing to
     `<your-username>.github.io`
2. In **Settings → Pages → Custom domain**, enter `solarinsd.com` and save. GitHub will
   verify DNS and can auto-provision HTTPS — check **Enforce HTTPS** once available.
3. DNS changes can take anywhere from a few minutes to 24+ hours to propagate.

## Updating content

Every page repeats its own header/footer (no templating), so a nav or footer change
needs to be made in all five HTML files. Shared design tokens (colors, type, spacing)
live in `css/style.css`.

## Content accuracy

The permitting, interconnection, and incentive details in this guide were researched
from the SD PUC, SD Electrical Commission, SD Codified Laws, and Xcel Energy's public
pages as of July 2026. Fees, forms, and rates change — before publishing, it's worth
re-checking anything with a dollar figure or a specific process step against the
source links on the Resources page, and updating the "Not legal advice" disclaimer
dates if you keep this live long-term.
