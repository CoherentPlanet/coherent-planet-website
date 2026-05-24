# GitHub Pages Hosting Checklist

**Status:** working checklist  
**Updated:** 2026-05-24  
**Scope:** publication of the static Coherent Planet website from GitHub Pages

## Repository files

- `CNAME` should contain the custom domain: `coherentplanet.org`.
- `.nojekyll` should exist at the repository root so GitHub Pages serves the static files directly.
- `sitemap.xml` already uses `https://coherentplanet.org/` as the canonical host.

## GitHub Pages settings

In the GitHub repository settings:

1. Open **Settings**.
2. Open **Pages** under **Code and automation**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Set the source to `main` and `/(root)`.
5. Under **Custom domain**, use `coherentplanet.org`.
6. After DNS settles, enable **Enforce HTTPS** when GitHub allows it.

## DNS records

At the DNS provider, point the apex domain `coherentplanet.org` to GitHub Pages.

Use either an `ALIAS`/`ANAME` record to the GitHub Pages default host, or these `A` records for `@`:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Optional IPv6 `AAAA` records for `@`:

```text
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

For `www.coherentplanet.org`, create a `CNAME` record pointing to the GitHub Pages default host for the account, without the repository name:

```text
CoherentPlanet.github.io
```

## Notes

- DNS changes can take up to 24 hours to propagate.
- Do not use wildcard DNS records for the domain.
- GitHub recommends verifying the custom domain to reduce takeover risk.
- A `CNAME` file in the repository helps preserve the domain setting, but the domain still needs to be configured in GitHub Pages settings.
