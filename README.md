# Dotair Studio website

Static website for Dotair Studio, the studio name of DOTAIR LLC.

## Edit

- Page content: `index.html`
- Layout and colors: `styles.css`
- Icon: `favicon.svg`
- Custom domain: `CNAME`

No build step is required. GitHub Pages can publish the root of the `main` branch. For a local preview, run `python3 -m http.server 8000` here and open `http://localhost:8000`.

The site deliberately contains no unverified product claims or private company information.

## Publish with GitHub Pages

1. Create a **public** repository named `dotair-od1.github.io` in the `dotair-od1` account. GitHub Free requires a public repository for Pages.
2. Push this repository's `main` branch to `git@github-dotair:dotair-od1/dotair-od1.github.io.git`.
3. In the GitHub repository, open **Settings → Pages**. Publish from the `main` branch, `/ (root)` folder. Set the custom domain to `dotairstudio.com` before editing DNS.
4. In Cloudflare **DNS → Records**, add four DNS-only `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`. Add a DNS-only `CNAME` for `www` pointing directly to `dotair-od1.github.io`.
5. Leave all existing mail-related `MX` and `TXT` records untouched. Once GitHub provisions its certificate, select **Enforce HTTPS** in Pages settings.
6. Verify `https://dotairstudio.com/` loads and `https://www.dotairstudio.com/` redirects to it. Confirm Cloudflare Email Routing remains active and send a test message to `admin@dotairstudio.com` from another mailbox.

GitHub's current [custom-domain instructions](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) list these DNS values. DNS and certificate changes may take up to 24 hours.
