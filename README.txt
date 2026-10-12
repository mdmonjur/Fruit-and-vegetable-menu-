MR MONJUR ONLINE ORDER SYSTEM — UPDATE v6

Files:
- online-shop.html: Customer ordering, order number + phone lookup, order progress, customer bill and print/save PDF.
- shop.html: Admin/Salesman online-order workflow and management invoice tools.
- hr.html: HR management page.

Management invoice features added:
- Admin can view, download PDF, print and share every online customer order bill by WhatsApp.
- Salesman can view/download/print/share bills only for orders assigned to or handled by their own account.
- When a salesman accepts an unassigned order, the order is assigned to that salesman.
- Admin can manage all orders. Salesmen cannot change an order assigned to another salesman.
- Online order status remains: Order Received -> Accepted -> Processing -> Out for Delivery -> Delivered. Stock is deducted only when marked Delivered.

Install:
1. Back up the current files.
2. Upload/replace shop.html and online-shop.html together; keep hr.html if unchanged.
3. Keep existing Supabase cloud settings and verify read/write permissions.
4. Test with one customer order, one Admin login and two different Salesman logins.

Important limitations:
- This update uses the existing shared Supabase record and existing browser publishable key. Browser-side role checks are a convenience, not strong server-side security. For production-grade separation, enforce authorization in Supabase RLS or a server-side API.
- PDF download uses the existing jsPDF CDN and generates an English/Latin-text PDF; some non-Latin product names may not render correctly without embedding a suitable font. Print can be used as an alternative.
- Live cloud operation has not been tested from this environment.
