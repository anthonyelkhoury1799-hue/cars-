# CPC V2.1 image reliability verification

- [x] All seeded demo car image paths point to local SVG assets.
- [x] Hero and promotional CSS backgrounds use local image files.
- [x] Legacy or remote listing image URLs are converted to local category fallbacks in API responses.
- [x] Card and detail images have local fallback handlers.
- [x] Seller photo upload validates declared MIME type, file signature and a 3 MB limit.
- [x] Uploaded files are stored in `public/uploads` and referenced with relative paths.
- [x] Content Security Policy no longer needs remote image hosts.
- [x] `node --check server.js` and `node --check public/app.js` passed.
- [x] Local HTTP checks confirmed all seeded SVG assets return image/svg+xml.

Note: vehicle art is illustrative vector artwork, not manufacturer photography. Seller-uploaded photographs are used when provided. Keep all project folders together when moving or deploying. Run via Node.js (`start.bat` / `npm start`), not by opening HTML through `file://`.
