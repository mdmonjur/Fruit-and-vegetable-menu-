MR Online Shop v24 - Customer Inbox

Features:
- Customer must log in to send messages from the shop chat.
- Messages are stored in the shared shop data row in Supabase.
- Admin and Salesman can open the Inbox tab, select a customer conversation, and reply.
- Salesman conversations can be assigned to the salesman who first opens an unassigned thread.
- Customer chat checks for staff replies while the chat window is open.

Install:
1. Extract this ZIP.
2. Upload online-shop.html, shop.html, hr.html, and mr-logo-watermark.png to the same GitHub repository folder, replacing the matching files.
3. Commit changes.
4. Log in to Shop Panel as Admin/Salesman and open Inbox.

Important:
The current shared-row/public-client-key architecture is not suitable for sensitive customer messages or secure role permissions. For production use, implement Supabase Auth, dedicated messages table, and Row Level Security policies. Browser end-to-end testing is still required after deployment.
