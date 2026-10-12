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
- Customer presses Submit Order to save the order directly into the shop cloud system. WhatsApp is not used.
- Stock is NOT deducted when a customer merely sends an order; the shop must confirm it first.

Important: This update assumes the existing Supabase shop cloud sync (table hr_shared_data, id=1) is already working and the shop phone number is set. It does not change HR employee or salary access. Customer page exposes only the public product catalogue and shop contact details, not HR records.


UPDATED CUSTOMER ORDER WORKFLOW (v2):
- Customer submissions are saved into the shared cloud data as individual orders (status Pending). No WhatsApp step is used.
- Admin and Salesman see the separate “Customer Orders” tab in shop.html.
- Pending orders can be Accepted or Rejected; accepted orders can be marked Delivered.
- Stock is deducted exactly once when an Accepted order is marked Delivered. Accepting or rejecting does not deduct stock.
- This requires the Supabase hr_shared_data row (id=1) to allow the public customer page to PATCH its data. If Supabase Row Level Security/policies block updates, a secure server-side order endpoint is required instead; do not make the HR data table broadly writable without appropriate access controls.
