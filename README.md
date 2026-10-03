# Htet Wai Shan Com. — Website + Backend

## Run locally
1. Install Node.js 18+.
2. In this folder run:
   npm install
3. Set an admin password:
   - Windows PowerShell: `$env:ADMIN_PASSWORD="your-strong-password"`
   - Linux/macOS: `export ADMIN_PASSWORD="your-strong-password"`
4. Start:
   npm start
5. Open: http://localhost:3000

## What it does
- Shows the gaming-style shop homepage.
- Shows KPay and Wave Money payment numbers.
- Customers can submit name, MLBB Player ID, diamond package, and a payment screenshot.
- The backend stores orders in `data/orders.json` and screenshots in `uploads/`.
- Admin API:
  GET `/api/admin/orders` with header `x-admin-password: <your password>`
  GET `/api/admin/receipt/<filename>` with the same header.

## Important for public hosting
Set `ADMIN_PASSWORD` to a strong private password. Do not publish the `data/` or `uploads/` folders as static files. For a real production shop, use HTTPS and a proper database/object storage rather than local disk storage.
