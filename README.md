# Amaar Bagaan

**v1.4.1 — Stable brand/title hygiene release**

Amaar Bagaan is a private, Firebase-backed, mobile-first plant-care companion for the family garden.

## Current stable baseline

- Current package: v1.3.8
- Previous stable base: v1.3.6
- Firestore schema: v4
- Firebase Hosting-ready PWA

## v1.3.8 focus

This release intentionally keeps the stable v1.3.6 layout and performs only a scoped hygiene patch around the brand title/tagline area.

- Fixed brand-title clipping for letters like `g`.
- Replaced the light/washed title gradient with a darker green-to-gold premium gradient.
- Updated the Bengali tagline to: `প্রতিদিনের সহজ গাছ-যত্ন`.
- Added one final brand CSS source-of-truth block at the end of `global.css`.
- Avoided broad CSS pruning to preserve the working mobile layout.

## Local run

```powershell
npm install
Copy-Item ..\amaar-bagaan-v1.3.6\.env.local .env.local
npm run dev
```

## Deploy hosting

```powershell
npm run build
npx firebase-tools deploy --only hosting
```

No Firestore rule or schema change is required for this release unless the family Gmail allow-list changes.
