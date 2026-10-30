# Bridge Gate

Responsive static ICT consulting website for https://bridgegate.eu, with Home, Services, Enterprise, About, Contact, Privacy Notice, Website Terms and a 404 page. Local transparent logo branding and no runtime dependencies. Existing layout, liquid-glass controls and motion effects are preserved.

## Preview

Run `python -m http.server 8000` from this directory.

## GitHub Pages and DNS

Repository Settings → Pages: Deploy from a branch, main, / (root). Custom domain: `bridgegate.eu` (also stored in CNAME). Enable Enforce HTTPS after DNS validation and certificate issuance.

Add the following records at the DNS provider for bridgegate.eu; TTL 3600 or Auto:

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | vimplayapi-cpu.github.io |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |

AAAA records are optional IPv6 support. Replace conflicting website records at @ and www. Preserve email MX/TXT records. Do not use a wildcard. If using Cloudflare, use DNS only while GitHub validates the domain and issues the certificate. DNS propagation and HTTPS provisioning can take up to 24 hours.

Official reference: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

The old domain needs a separate redirect service for permanent path-preserving redirects to the new domain; DNS alone cannot perform HTTP redirects.

## Contact behaviour

The form validates fields and prepares a mailto draft; the visitor must send the email. A visible copyable draft is provided if no email app is configured. The site has no contact backend, cookies, analytics or form-data storage. The existing owner-supplied mailbox remains the enquiry destination until the owner supplies a verified replacement. Do not infer a new Gmail address or domain mailbox from the new brand.

## Business content

Brand: Bridge Gate. Owner-supplied address: Street Bulair 22, Pomorie, 8200, Bulgaria. ICT consulting business focus. No registration number, VAT ID, founding date, client endorsements, accreditations or banking approval is asserted. Add verified legal entity and registration details when available.

## Security and assets

Owner-supplied gold Bridgegate monogram and wordmark in assets/bridgegate-logo-transparent.png. Black background removed with alpha transparency; original gold artwork preserved. Header, footer and About page use this asset; favicon retains the bridge motif. Local assets avoid mixed content. Every HTML page retains its restrictive static Content Security Policy and referrer policy. HTTPS issuance and enforcement require the hosting settings, not HTML.
