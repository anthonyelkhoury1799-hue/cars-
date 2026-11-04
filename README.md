# CAR PRODUCTS CONSULTANT — Lebanon (V2)

A responsive, multi-page automotive marketplace MVP for Lebanon. Built with Node.js 18+ and browser JavaScript; no third-party Node packages are required.

## Start the website

**Windows**
1. Install Node.js 18 or newer from https://nodejs.org/.
2. Extract this ZIP.
3. Double-click `start.bat`, or open Command Prompt in this folder and run `npm start`.
4. Visit http://localhost:3000.

**macOS / Linux**
1. Install Node.js 18 or newer.
2. Extract this ZIP and open a terminal in the project folder.
3. Run `chmod +x start.sh && ./start.sh` or `npm start`.
4. Visit http://localhost:3000.

The JSON database is created automatically at `data/db.json` on first launch. Back it up before replacing or updating the project.

## Local demo accounts

| Role | Email | Password |
|---|---|---|
| Administrator | `admin@carconsultant.lb` | `Admin123!` |
| Seller | `seller@carconsultant.lb` | `Seller123!` |
| Customer | `customer@carconsultant.lb` | `Customer123!` |

Change these demo passwords before any shared or public use. The administrator can enable or disable seller access for registered customer accounts.

## Included features

- Separate pages: Home, Find a Car, Vehicle Details, Compare, Favorites, Sign In/Register, Seller Workspace, Admin Dashboard, AI Consultant.
- **175 vehicle make/model options** in the seller listing form, with make-dependent model selection.
- **120 accent colour themes** (24 hue families × 5 shade levels), saved in the current browser.
- Vehicle search, make/body/budget filters, sorting and vehicle detail pages.
- Compare up to four vehicles; browser-local comparison list.
- Favorites for signed-in users stored on the server; guest favorites remain on the current browser.
- Seller listing submissions with pending moderation; approved listings appear in the public catalogue.
- Buyer inquiry form and administrator inquiry inbox.
- Admin moderation and customer/seller role management.
- Automotive consultant with rule-based guidance and compatibility cautions.
- Responsive layout for desktop, tablet and mobile.
- Server-side password hashing (scrypt), hashed persistent session tokens, HttpOnly/SameSite cookies, CSRF token checks, basic login/register rate limiting, input validation, safer static-file path handling and atomic JSON writes.

## Important truth about the sample data

The nine starter vehicles are **illustrative demo listings**, not verified cars currently offered for sale. Their prices, details and images are examples. No real seller contact details are fabricated or displayed. A seller-created listing is marked pending until an administrator approves it.

The model selector is a broad make/model helper, not an OEM vehicle-fitment database. Model availability, trim names and specifications vary by country and model year. Confirm any part or vehicle specification using the VIN and a trusted source.

## What is and is not production-ready

This is a functional local MVP. It does not yet include a production database such as PostgreSQL, image upload/storage, email verification, password reset, seller KYC, payments, shipping integrations, analytics, automated backups, or a live AI provider. The consultant is rule-based, not a live AI model. Do not expose this local JSON database server directly to the public internet for commercial use.

Before public launch, deploy behind HTTPS, use PostgreSQL with migrations and backups, configure secure secrets and cookie settings, add monitoring and audit logs, implement seller verification and privacy/terms policies, and connect trusted AI, email and payment services as needed. Have the deployment security-reviewed.

## Verify the code

Run `npm run check` to check JavaScript syntax. Start the server and open `/api/health` to confirm the backend is responding.


## Offline-first vehicle images (V2.1)
- All demo vehicle artwork is stored locally in `public/assets/images/` as self-contained SVG files.
- CSS hero and promotional images also use local assets; no remote image host is required.
- Missing or legacy external image URLs automatically fall back to local CPC illustrations.
- Seller image upload accepts JPG, PNG and WebP up to 3 MB and saves the image under `public/uploads/`; the listing stores a relative project path.
- Keep the complete `public/assets` and `public/uploads` folders when copying or deploying the project.
- This website requires the Node.js server; opening HTML directly with `file://` will not run the API or marketplace features. Use `start.bat` or `npm start`.
