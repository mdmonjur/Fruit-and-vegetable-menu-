ONLINE ORDER SYSTEM UPDATE

Files in this package:
- hr.html: HR Management, with Change Admin Password page.
- shop.html: Shop Management, product photo upload/preview, item-specific photos, customer orders, and cloud sync.
- online-shop.html: Customer online shop, displays each product's own saved photo.

IMPORTANT
1. Replace/upload all three HTML files together on your website/hosting. Keep these filenames exactly the same.
2. In Shop Management > Items & Stock, upload a photo for each product, then click Save Product. Each product can have a different photo.
3. Product photos are resized before saving and are synced with the shop data. Keep photos reasonably small; very many high-resolution photos may exceed database/storage limits.
4. In HR Management, log in with the current password (first-time default: Admin@1234), open “Change Admin Password”, and save the new password. This password is stored in the browser on that device only; it does not sync to other devices.
5. Cloud order/product syncing requires the configured Supabase project and its permissions to be working. This package has been syntax-checked but not live-tested against your Supabase account.

Customer orders are submitted to the shop system, and stock is reduced only when an accepted order is marked Delivered.
