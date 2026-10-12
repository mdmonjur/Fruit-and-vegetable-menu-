MR MONJUR Online Order System — v7 Order Assignment & Invoice Update

Files:
- shop.html: management panel, order assignment, sales records, invoice QR, company stamp and signature.
- online-shop.html: customer shop and tracking bill with stamp/signature/QR.
- hr.html: HR management file from the previous version.

Changes:
1. Rejected/cancelled orders are hidden from the management Customer Orders list and its filters.
2. All salesmen can see new pending orders. When a salesman accepts one, it is assigned to that salesman; when Admin accepts it, it is assigned to Admin.
3. After acceptance, salesmen see only orders assigned to their own account (plus new pending orders). Admin can see all non-rejected orders.
4. Accepting an online order adds one sale record, tagged with sourceOrderId to prevent duplicate entries. Admin sees all sales records; salesmen see their own records through existing sales filters.
5. Stock is still deducted only when the order is marked Delivered.
6. Online order bill includes QR code, company stamp and signature image/name when configured in Admin Settings.

Install: back up the current files, then upload/replace shop.html and online-shop.html. Keep the existing Supabase URL, keys, table permissions and CLOUD_ID consistent across devices.

Important: This is a browser-side app that stores shared data in a Supabase JSON record. UI filtering is not a security boundary. For production security, enforce role/order ownership using Supabase RLS and a trusted server-side API. Cloud sync was not live-tested as part of this patch.


CUSTOMER PDF / WHATSAPP BILL (v8 update)
- Customer submits an order, then the order number and phone can be used in Track Order / Print Bill.
- The bill now has Download PDF Bill, WhatsApp / Share PDF, and Print Bill buttons.
- Download PDF includes order details, status, company stamp, authorized signature and QR code (when configured).
- WhatsApp / Share PDF uses Android's native share sheet when supported; choose WhatsApp and then a contact. If file sharing is unavailable, it downloads the PDF and opens WhatsApp with a message; attach the downloaded PDF manually.
- PDF generation requires internet access to load the html2pdf library.
Customer bill stamp/signature rule (v9): Before an order status is Delivered, the customer can download/share/print a preliminary bill without company stamp and signature. Once the order status is changed to Delivered in the management system, the customer can track the same order again and download/share/print the final bill with the configured company stamp and signature. The order QR remains available on both versions.
