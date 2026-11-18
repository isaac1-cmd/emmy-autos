# Emmy Autos – website

A static website (no build step, no back end). Everything is in `index.html`.

## Deploy on Vercel

### Option A – GitHub (easiest, updates automatically)
1. Create a free account at github.com and make a new repository (e.g. `emmy-autos`).
2. Upload `index.html` and `vercel.json` to the repository ("Add file" > "Upload files").
3. Go to vercel.com, sign in with GitHub, click **Add New > Project**, pick `emmy-autos`.
4. Leave all settings as they are (Framework: Other, no build command) and click **Deploy**.
5. Vercel gives you a link like `emmy-autos.vercel.app`. Send that link out.

### Option B – Vercel CLI
1. Install Node.js, then in this folder run: `npx vercel`
2. Answer the questions (all defaults are fine). Then run `npx vercel --prod` for the live link.

### Your own domain (optional)
Vercel dashboard > your project > **Settings > Domains** > add e.g. `emmyautos.com` and follow the DNS steps.

## Things to edit in `index.html` (search for these)
- `WA_NUMBER` – your WhatsApp number, digits only with country code, e.g. `"2348012345678"`.
- `WA_ON` – change `false` to `true` to switch WhatsApp on. While it is `false`, every WhatsApp button shows "currently unavailable".
- Email – `info@emmyautos.com` in the footer is a made-up address; replace it.
- Address – currently `Berlin, Germany` in the footer.
- Cars – the list is `const CARS=[ ... ]` (make, model, year, price, origin, body, fuel, mileage, colour).
- Photos – in `const IMGS={ ... }`, keyed by the car's position in the list (0 = first car). A car with no photo shows blurred with an UNAVAILABLE watermark.
- Reviews – the three customer reviews are samples; replace them with real ones.
