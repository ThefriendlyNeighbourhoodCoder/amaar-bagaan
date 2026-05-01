# Firebase Deployment Guide

## Firebase project

Project ID: `amaar-bagaan`

## Required Firebase products

- Authentication: Google provider enabled
- Firestore: `(default)` database
- Hosting: enabled

## Environment file

Create `.env.local` from `.env.example` and populate:

```env
VITE_FIREBASE_API_KEY=...
VITE_FIREBASE_AUTH_DOMAIN=amaar-bagaan.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=amaar-bagaan
VITE_FIREBASE_STORAGE_BUCKET=amaar-bagaan.firebasestorage.app
VITE_FIREBASE_MESSAGING_SENDER_ID=...
VITE_FIREBASE_APP_ID=...
VITE_ALLOWED_EMAILS=yourgmail@gmail.com,mothergmail@gmail.com
VITE_GARDEN_LAT=22.3612
VITE_GARDEN_LON=87.3576
VITE_GARDEN_LOCATION_NAME=Rakhajungle, Kharagpur
```

## Firestore rules

Before deploying rules, replace placeholder emails in `firestore.rules` with the family Gmail IDs allowed to access the app.

## Build and deploy

```powershell
npm run build
npx firebase-tools deploy --only firestore:rules
npx firebase-tools deploy --only hosting
```

## Upgrade to v1.3.2 from v1.3.0

After opening the deployed app with an allowed Gmail:

1. Go to Settings.
2. Run **Migrate schema**.
3. Run **Safe seed check**.
4. Confirm Firestore contains the new/custom zone documents.
5. Test Map → Add area once if you want to create a new custom home area.

## Live URL

https://amaar-bagaan.web.app/


## v1.3.2 note

This release only requires normal hosting deployment unless you want to reseed/migrate zone metadata. Existing Firebase rules remain compatible. After local validation, run `npm run build` and `npx firebase-tools deploy --only hosting`.
