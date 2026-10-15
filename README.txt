MR MONJUR Online Shop v32 — Local Banner Manager + Customer Language Switch

Files to replace in your GitHub repository root:
- online-shop.html
- shop.html
- hr.html
- mr-logo-watermark.png

New features:
- Admin Settings now includes 4 banner slots.
- Upload banner images from your device; images are resized/compressed in browser and saved with shared shop settings.
- Each banner has heading, subtitle and four style options (dark overlay, centered, clean card, bold red).
- Customer Home Page banner images are loaded from saved shop settings, not external image URLs. If no banners are configured, a built-in gradient promo is shown.
- Customer Home Page has English / Arabic / Bengali language switch at the top.

Setup:
1. Extract this ZIP.
2. Open the order_v32 folder and upload/replace the listed files at the root of your GitHub repository (do not upload the enclosing folder).
3. Commit changes.
4. Open Shop Panel and sign in as Admin.
5. Open Admin Settings > Customer Home Page Banners. Upload images, set text and select a style for each banner; then press Save Home Page Banners.
6. Open the customer website and refresh. Select English, العربية, or বাংলা from the language selector.

Notes:
- Images are compressed in the browser before saving. Large banner images may still increase shared cloud JSON size; use a few reasonably sized images.
- Banner settings sync through the existing Supabase shared-data setup. This has not been end-to-end tested against the live Supabase project.
- The language switch translates the supported customer interface labels; not every product name entered by the shop owner is automatically translated.
