MindBrew Shopify Addon (for Dawn)
=================================

This package contains new sections, templates, assets, and snippets you can drop into a Dawn theme to launch a mushroom coffee store quickly.

Quick start
-----------
1) In Shopify Admin → Themes → Duplicate your live theme, then Edit code.
2) Upload assets/mindbrew.css and add this to layout/theme.liquid inside <head>:
   <link href="{{ 'mindbrew.css' | asset_url }}" rel="stylesheet">
   {% render 'mindbrew-seo' %}
   Also add before </body>:
   {% render 'mindbrew-modal' %}
3) Create the following new files using the paths in this package:
   sections/mindbrew-hero.liquid
   sections/mindbrew-benefits.liquid
   sections/mindbrew-product-promo.liquid
   sections/mindbrew-testimonials.liquid
   snippets/mindbrew-seo.liquid
   snippets/mindbrew-modal.liquid
   templates/index.json
   templates/product.json
   templates/page.about.json
   templates/page.faq.json
   templates/page.policies.json
4) Open config/settings_schema.json in your theme and append the object from config/settings_schema.ADD.json to the root array.
5) Products → Import → upload content/seed-product.csv, then open the product and paste the long description from content/product-listing.md.
6) Pages → Create About, FAQ, Policies and assign the respective templates. Paste markdown from content/pages and content/policies files.
7) Install Supliful or Spocket, import your mushroom coffee product, and map it to the featured section.

GitHub workflow
---------------
1) Create a new GitHub repo (public or private), e.g. mindbrew-store.
2) In Shopify Admin → Online Store → Themes → Connect to GitHub → link your repo.
3) Commit these files into the repository (they will overlay a Dawn theme). For a full theme repo, fork Dawn and add these files on top.
4) Use branches: develop (staging), main (production). Open PRs for changes and let Shopify pull from your selected branch.

Notes
-----
• Colors and tagline can be adjusted in Theme Settings → MindBrew Theme Settings.
• Modal uses Shopify's customer form to collect emails into the Customers list with tag 'newsletter'.
• All copy is placeholder; adjust for your compliance and market claims.
