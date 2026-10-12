ONLINE ORDER SYSTEM UPDATE

Files in this package:
- shop.html: Cash Memo + Stock Management with Customer Online Shop shortcut.
- hr.html: HR Management with a separate Customer Online Shop shortcut.
- online-shop.html: public customer order page.

Upload all three files into the SAME folder/root of the existing GitHub Pages website. Keep your existing index.html and other assets unchanged.

Customer link (if your existing site is https://mdmonjur.github.io/HR_Shop-management/):
https://mdmonjur.github.io/HR_Shop-management/online-shop.html

Order flow:
- Customers view products loaded from the existing shop cloud data (Cloud ID 1).
- Choose Home Delivery or Shop Collection.
- Payment is cash only.
- Submit opens WhatsApp with the full order details to the shop phone configured in Cash Management Settings.
- Stock is NOT deducted when a customer merely sends an order; the shop must confirm it first.

Important: This update assumes the existing Supabase shop cloud sync (table hr_shared_data, id=1) is already working and the shop phone number is set. It does not change HR employee or salary access. Customer page exposes only the public product catalogue and shop contact details, not HR records.
