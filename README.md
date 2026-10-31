# Sessionify website

Static site for Sessionify, the offline recorder for in-person meetings. Served by GitHub Pages from `main`.

| Page | File | Address |
|---|---|---|
| Landing | `index.html` | https://sessionify-app.github.io/landing/ |
| Support | `support/index.html` | https://sessionify-app.github.io/landing/support/ |
| Privacy Policy | `privacy.html` | https://sessionify-app.github.io/landing/privacy.html |

- `style.css` is shared by all pages. After changing it, bump `?v=` in each page's stylesheet link so browsers fetch the new file.
- `assets/` holds the logo, app icons and screenshots (`screenshots/web/` are the optimised JPEGs used on the pages).
- `kit/` is the marketing kit: brief, brand rules, copy and FAQ.

## Search engines
- `sitemap.xml` lists every page. Add new pages there and update `lastmod` when a page changes.
- `.github/workflows/indexnow.yml` submits the sitemap URLs to IndexNow (Bing, Yandex, Seznam, Naver, Yep and others) after each push to `main`. The key is in `.indexnow-key` and is served as `<key>.txt`; don't delete either.
- Google and Bing Webmaster Tools are verified separately; submit `sitemap.xml` there.
