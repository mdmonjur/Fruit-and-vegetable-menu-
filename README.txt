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


V10 QR BILL FIX
Order QR codes on customer and management order invoices now encode a direct link to the online-shop tracking page. Scanning the QR opens the matching bill automatically and provides Download PDF, WhatsApp/Share PDF, and Print buttons. QR link includes the order number and customer phone number to allow the bill to load without retyping; only print/share the QR with the intended recipient. The website must be hosted online (HTTPS) for QR links to work; a local file:// copy cannot provide a public bill link. PDF libraries require internet access.


V11 MOBILE BROWSER COMPATIBILITY
- Updated viewport settings for responsive display on Android/iPhone mobile browsers, including Chrome, Safari, Firefox and Edge. Actual rendering may vary by browser.
- Fixed management invoice QR links to open shop.html?bill=... (the public bill screen in this package), rather than a missing bill.html page.
- Customer order QR links open online-shop.html with the order number and phone query values; the hosted page auto-loads the order and provides PDF, share and print actions.
- The files must be deployed together on an HTTPS web host (e.g. GitHub Pages or another static host) and retain their filenames. Opening directly as file:// will not provide a public QR link and cloud requests may fail.
- PDF generation and QR rendering use external CDN libraries, so internet access is required. If a browser does not support PDF file sharing, download the PDF and attach it in WhatsApp, or use Print > Save as PDF.
- Responsive syntax checks do not replace testing on the live hosting URL and actual devices.


V12 CUSTOMER ACCOUNTS + CROSS-BROWSER SUPPORT
- Customer online shop is responsive for current Android/iPhone browsers (Chrome, Safari, Firefox, Edge) and uses ordinary HTML/CSS/JavaScript. Keep all package filenames when hosting on HTTPS.
- Customers can create an account using name, phone number and password, then log in later using the same phone/password. The shop restores name, phone and address, and shows orders tied to that phone/account. Orders placed while logged in are linked to the account. Existing orders made before account creation may also appear if they use the same phone number.
- Customer login session is remembered in that browser on that device. To sign in on a different phone/browser, log in again with phone and password.
- PDF generation and QR creation depend on external CDN libraries and internet access. If PDF download fails in a browser, use Print Bill > Save as PDF; file sharing depends on browser/OS support.
- IMPORTANT SECURITY LIMITATION: this project stores accounts and orders inside one shared JSON row accessed by the public browser key. Passwords are hashed, but the current shared-data design is NOT secure authentication and must not be used for sensitive/private customer data in production. Anyone with access to that public JSON endpoint may potentially read customer records. Before production use, move accounts to Supabase Auth (prefer phone/email verification) and store profiles/orders in separate tables protected by Row Level Security (RLS) or a trusted server API. Do not store payment card details or sensitive personal data here.
- Syntax checks do not replace testing on the actual hosted URL and mobile devices.
