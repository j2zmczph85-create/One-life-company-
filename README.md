# ONE LIFE COMPANY — REAL FUNCTIONAL E-COMMERCE APP

This is a real full-stack application, not an image/mockup.

## What works
- Public product catalog backed by SQLite
- Search and categories
- Customer registration/login with hashed passwords
- Shopping cart
- Checkout
- Orders saved in database
- Stock is reduced when orders are placed
- Customer order history
- Admin login and dashboard
- Add products
- Sales/order/customer/product statistics
- Admin order-status changes
- Mobile-first responsive interface
- Single Node server serves both API and app

## Run it
Requirements: Node.js 20+.

1. Extract the ZIP.
2. Open a terminal in the project folder.
3. Run:
   npm install
4. Copy `.env.example` to `.env` and change the secret/admin password.
5. Run:
   npm start
6. Open:
   http://localhost:3000

Admin defaults come from `.env.example`. Change them before deployment.

## Production work still required
This is a functional MVP, but it is NOT safe to launch publicly with default credentials. Before real customers use it, configure:
- A strong JWT secret and admin password
- HTTPS/domain hosting
- Production database backups
- Cloud image storage
- Tanzanian payment gateway credentials/API integration (M-Pesa/Tigo Pesa/Airtel Money; exact provider depends on the business account)
- SMS/WhatsApp/push notifications
- Delivery zones and fees
- Refund/return rules and privacy/terms pages
- App-store packaging if native Android/iOS apps are required
- Server monitoring and rate limiting

The payment dropdown is intentionally not pretending to charge money: selecting M-Pesa/Tigo Pesa/Airtel Money currently records the selected method, but a real payment API must be connected with the merchant credentials.


## PWA / iPhone installation

The `public` folder now includes:
- `manifest.webmanifest`
- `sw.js`
- 192x192 and 512x512 ONE LIFE icons
- iPhone web-app metadata
- service-worker registration

After deploying the Node app on a public HTTPS domain, open the domain in Safari on iPhone and choose:
**Share → Add to Home Screen → Add**

A PWA does not by itself make the app publicly accessible; the server still needs hosting and HTTPS. The payment API also still needs merchant credentials before real payments can be processed.
