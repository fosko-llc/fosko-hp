# Fosko QA / Release Review

Do not redesign. Verify the release candidate.

## Desktop
Check current Chrome and Safari for header, hero, section spacing, typography, contact, footer, and privacy link.

## Mobile
At minimum test an iPhone-class viewport:
- No horizontal scrolling
- No text overlap
- No broken grid behavior
- Labels remain readable
- Headings wrap intentionally
- Contact remains usable
- Fixed header does not obscure content
- Footer remains readable

Pay special attention to CSS cascade/order.

## Functional checks
Verify home link, contact anchor, `mailto:`, privacy link, images, scroll behavior, and obvious console errors.

## HTML / accessibility
Verify one meaningful `h1`, logical heading structure, `lang="ja"`, viewport meta, keyboard focus, skip link, image alt behavior, and reduced motion.

## SEO basics
Verify title, meta description, canonical URL, Organization structured data, and production-domain consistency.

## Analytics
Verify analytics beacon presence, no duplicate snippet, dashboard activity after deployment, and privacy-policy consistency.

## Deployment
Verify:
- `https://fosko.jp/`
- HTTPS enforced
- intentional `www` behavior
- latest Git commit deployed
- no unexpected public files

## Release verdict
Return exactly one:
- **PASS**
- **PASS WITH NOTES**
- **FAIL**

For FAIL, list release-blocking defects first.
