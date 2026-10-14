MR Online Shop v27 — Bank Transfer + Bank Muscat Mobile Banking (Oman)

Files:
- online-shop.html
- shop.html
- hr.html
- mr-logo-watermark.png

Update:
1. Extract this ZIP.
2. Replace the matching files in your GitHub repository with these files.
3. Keep mr-logo-watermark.png in the same folder as the HTML files.
4. Commit changes and test a new order.
5. Open Shop Panel > Admin Settings. Add your Bank Muscat and bank transfer details, then Save Settings.

Checkout payment options:
- Cash on Delivery
- Bank Transfer
- Bank Muscat Mobile Banking (Oman)

For Bank Transfer or Bank Muscat Mobile Banking, the customer can enter a Transaction ID. Admin Orders should display the selected payment method, transaction ID and payment status. Admin must verify the actual money received before marking payment as paid.

Important: This is manual payment instruction and transaction-reference collection, not an automatic payment gateway. Do not add PIN, OTP, or passwords. Test on the live Supabase-backed site before using for real orders. Existing shared JSON database architecture is not suitable for secure payment credentials; store only the public recipient details needed for transfers.
