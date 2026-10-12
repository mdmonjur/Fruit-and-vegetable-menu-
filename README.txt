MR MONJUR Online Order System - v16 Visual + Product Gallery

Included files:
- online-shop.html: customer-facing online shop with colorful gradient background, mobile responsive layout, tap-to-enlarge product image gallery, up to 3 photos per product, and illustrated order progress (receipt, accepted, packing, delivery vehicle, delivered).
- shop.html: shop/admin panel. In Items & Stock, select up to 3 product images at once. Images are compressed before being saved. When editing an existing product, selecting new images replaces its image gallery; leaving the photo picker empty preserves existing images.
- hr.html: HR panel carried forward from the previous version.

How to update GitHub Pages:
1. Download and extract this ZIP.
2. Open https://github.com/mdmonjur/Fruit-and-vegetable-menu-
3. Replace online-shop.html, shop.html, and hr.html with the matching files from this ZIP.
4. Commit changes, wait for GitHub Pages to update, then refresh the website. On Android Chrome, use the menu > Reload; if the old page remains, clear site cache or open in an incognito tab.

Notes:
- Customer taps a product photo to open a larger viewer. If there are multiple photos, thumbnails and Previous/Next controls are shown.
- Product images are stored inside the shared Supabase JSON record, as in the existing system. Many high-resolution photos can increase record size; images are compressed and limited to 3 per product.
- JavaScript syntax checks passed for the embedded scripts. The live Supabase/GitHub end-to-end flow was not tested from this build environment.
