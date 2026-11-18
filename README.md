# Moon & Me starter website

A responsive static website for Cloudflare Pages, using GitHub as the source repository.

## Deploy
1. Create a GitHub repository and upload `index.html` and `products.js` to its root.
2. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Select the repository. Framework preset: None. Build command: leave blank. Output directory: `/` (or use a supported static-root configuration).
4. Add `moonandmetoys.co.uk` as a custom domain once you are ready to switch from Wix. Preserve existing DNS records until cutover.

## Product links
Each entry in `products.js` can have an `asin` property, for example `asin: 'B0FNWGZFVJ'`. The website automatically constructs `https://www.amazon.co.uk/dp/ASIN?tag=rileyuk-21`.

The screenshot-supplied ASIN is NOT inserted as a real catalogue item because its product identity was not verified. The starter catalogue contains Moon & Me product names found on the existing site, but does not claim current Amazon stock. Add ASINs only after confirming each Amazon product detail page and suitability.

## Automation
To populate products automatically, integrate Amazon's authorised Creators API / Product Advertising API (subject to account access) through a Cloudflare Worker with secrets. Run a scheduled job, curate eligible results, and update a JSON feed or D1 database. Do not scrape Amazon listings or copy Amazon imagery without an authorised method. Show prices and availability only when permitted by Amazon's API rules.

## Notes
The site includes required Amazon Associate disclosure language. Review privacy/cookie notices and existing SEO redirects before launch. Character artwork and programme logos should only be used with appropriate rights.

## No-API launch mode (November 2026)

Amazon Creators API access is currently unavailable due to account eligibility. This version does not call the Amazon API, scrape Amazon, or claim that a specific product listing is currently available. All 10 entries are discovery ideas. Entries without an `asin` open an Amazon UK search URL containing the Associates tag `rileyuk-21` and are labelled **Search on Amazon**.

To upgrade an item to an exact product page, manually visit Amazon UK, check the listing matches the title, and add its verified ASIN in `products.js`, for example `asin:'B012345678'` (example only). The button will become **View on Amazon**. Do not insert ASINs you have not verified.

Edit product names, categories and optional `amazonSearch` keywords in `products.js` and commit both files to GitHub. Cloudflare Pages should redeploy automatically. Review Amazon Associates link, disclosure and content requirements before public launch, especially search-result Special Links.
