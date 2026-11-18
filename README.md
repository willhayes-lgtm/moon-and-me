# Moon & Me SEO-preserving website migration draft

## Important
This is a **staging migration** and not a finished switch-over. The live Wix site has indexed content and established URLs. This version preserves those URLs and much of the distinctive subject matter with refreshed wording (not an exact archival transfer). Before moving the domain, compare copy, images, metadata, backlinks, redirects and Search Console performance page by page. Do **not** terminate Wix before validating the migration.

## Deploy
Upload extracted files and folders to the root of `willhayes-lgtm/moon-and-me` on `main`. Cloudflare Pages framework preset: None, build command blank, output directory `.`. Test all routes on pages.dev.

## Images / Amazon
No Amazon images are scraped or copied in this version. Image slots show icons until you add **licensed** product images. For a product with appropriate rights, upload image under `/assets/` and add e.g. `"image": "/assets/pepi-nana.jpg"` to its object in `products.js`. Amazon product imagery should come from Amazon-approved tools or independently licensed manufacturer / owner-provided media. Amazon's affiliate content terms restrict copying/scraping and certain rehosting; do not assume images on your Wix site can legally be downloaded/reused unless you control the rights.

Three product ASINs were extracted from link URLs on the EXISTING user-owned website, not independently verified against current Amazon inventory: B07Q6SMT6R (VTech phone), B07QNH8MJ5 (Goodnight Pepi Nana), 1407188542 (Goodnight Moon Baby book). Other cards link to search results, not a verified exact listing. Confirm that affiliate links are compliant with UK Associates rules.

## SEO notes
- Canonical URLs intentionally target **www.moonandmetoys.co.uk** even in staging so temporary Cloudflare pages do not supplant the indexed Wix domain. Add noindex to staging at the Cloudflare edge if exposing publicly for extended periods.
- Existing URLs preserved include /all-toys, /moon-me-books, /pepinana, /moon-baby, /col, /copy-of-all-toys-2, /who-are-we, /about-moon-and-me, /all-characters plus some low-volume routes.
- Some original routes (blog, DVD, old page variants) still require inventory/content audit and migration; do not launch yet.
- Match and audit SEO titles/H1s and preserve high-performing copy in final version. Some original historical copy references 2019/2024 releases and should be preserved in archive context, rather than presented as current stock.
- Before launch: export Wix content and licensed images, collect Search Console rankings and top landing pages; preserve URLs or configure 301 mappings, add missing blog content, confirm product links and image rights, inspect robots/sitemap, then switch DNS and monitor indexing.
