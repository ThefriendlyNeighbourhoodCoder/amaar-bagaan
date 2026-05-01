# Release Notes

## v1.4.3 — Hero Illustration Lock + Mobile Tap Polish

- Applied the final approved Home hero illustration placement values.
- Removed harsh mobile/browser blue tap highlight from nav and clickable controls.
- Kept a refined `focus-visible` style for accessibility instead of removing focus feedback entirely.
- Performed a quick bottom-nav polish pass without changing data, schema, Firebase rules, or repository behavior.
- No Firestore migration required.

## v1.4.2 - Hero Illustration Placement Polish

- Repositioned the home hero illustration into the intended upper-right square above the Add Plant button.
- Updated only the existing hero CSS rules; no duplicate hero selector blocks were added.
- Preserved the v1.4.1 section spacing and responsive home layout improvements.

# Release Notes

## v1.4.1 - CSS Hygiene Recovery + Home Hero Stabilization

- Removed duplicate/overlapping Home hero CSS blocks instead of appending another competing override.
- Established one source of truth for `.hero-card.upgraded-hero-card`, `.hero-copy`, `.hero-illustration`, `.hero-add`, and plant silhouette SVG styling.
- Added a dedicated `.home-page-stack` wrapper so Home spacing is controlled by the actual React structure.
- Removed dead `.app-main` spacing rules that were never applied by the current component tree.
- Rebuilt the Home hero layout as a stable mobile grid with content on the left, SVG overlay at the upper-right, and Add Plant below the SVG.
- Improved section breathing space between Highlights, Hero, Weather, KPI cards, Weather guidance, and Today’s care.
- No Firestore schema change, no Firebase rule change, no migration required.

## v1.3.8 - Stable Brand Title Hygiene

- Locked v1.3.6 as the stable layout baseline.
- Applied a minimal, scoped CSS hygiene patch instead of broad stylesheet pruning.
- Fixed brand title clipping around descenders such as `g`.
- Changed the title gradient to a darker premium green with restrained golden finish.
- Updated the tagline to `প্রতিদিনের সহজ গাছ-যত্ন`.
- Preserved existing Firebase, Firestore schema, app layout, map, nav, settings and mobile behavior.


## v1.3.6 - Hero Balance, Brand Refinement, Map Cleanup and Status Polish

- Locked v1.3.5 as stable working baseline.
- Refined Bengali tagline to avoid repeating the garden wording.
- Added a subtle premium gradient treatment to the English brand title.
- Repositioned the Home hero illustration so it sits above the add button with better visual balance.
- Added accent color states to KPI cards for Plants, Healthy, Urgent and Watch.
- Removed the full zone list below the map to reduce visual noise.
- Rebalanced default zone positions to reduce overlap and clipping.
- Reworked custom-zone fallback positioning to avoid colliding with primary zones.
- Rebuilt compass styling as a clear static orientation marker instead of a misleading animated compass.
- Moved area removal into a small focused-zone icon action and removed duplicate add-area action from the focus panel.
- Improved Garden Status card visual hierarchy and credit line treatment.


## v1.3.5 — Bengali Identity, Hero Refinement and Readable Smart Map Polish

- Locked v1.3.4 as the current stable working baseline.
- Reworked the top brand tagline into Bengali typography: “মায়ের বাগানের স্মার্ট যত্ন”.
- Updated the welcome/sign-in screen to show both “আমার বাগান” and “Amaar Bagaan”.
- Refined splash/loading copy to better separate preparation/loading from sign-in.
- Rebalanced the Today in the Garden hero card spacing, illustration placement and button position for narrow mobile screens.
- Improved the hero card visual warmth with subtle blue accenting from the provided logo.
- Reworked the smart map to reduce label overlap and clipping on smaller screens.
- Added a selected-zone badge inside the map and compact zone selector chips below the map for clearer interaction.
- Improved map copy to clarify that care points are practical home areas for guidance, not exact measurements.
- Kept the animated compass subtle while avoiding a broken/static feel.
- Rewrote selected settings/install/status text for clearer daily-use language.
- Added “Made by Akash Patra © 2026” with a Lucide heart icon inside Garden Status.
- Bumped app package version to 1.3.5.

## v1.3.4 — Brand, Entry, Map and Weather UX Refinement

- Locked v1.3.2 as the stable working baseline.
- Replaced the custom in-app mark with the provided plant SVG as the main app identity.
- Synced the same SVG into favicon/browser tab and PWA manifest icon.
- Added subtle blue accents from the logo across the app theme.
- Separated loading and sign-in states more clearly.
- Added Google logo inside the Google sign-in button.
- Refined the sticky brand ribbon and added a soft separator below it.
- Reworked the Today in the Garden hero card to prevent text/button collision on mobile.
- Improved plant silhouette positioning and visibility inside the hero card.
- Replaced always-visible Bangla helper text with a one-touch Bangla toggle.
- Rebuilt the map presentation as dot-based interactive care-zone markers.
- Improved small-screen map sizing to avoid horizontal/vertical clipping.
- Strengthened the install action flow for PWA install prompts where supported by the browser.
- Added more earthy colors with subtle logo-blue accents.

## v1.3.2 — Brand, Navigation, Map and Weather Intelligence Polish

- Locked v1.3.1 as stable working baseline.
- Refined bottom navigation alignment so all icons and labels sit on the same visual line.
- Added a softer translucent navigation treatment with stronger active-state polish.
- Rebuilt the top brand area with the same custom Amaar Bagaan mark used for favicon/PWA identity.
- Restricted the Cloud sync badge to the Settings page only to reduce daily-use distraction.
- Added a cleaner separator/gap between brand header and page content.
- Reworked the home hero card to prevent text/button overlap on narrow screens.
- Added plant silhouette SVG treatment with warmer earthy visual layering.
- Added Bangla assistance lines in weather-aware suggestion cards.
- Expanded weather intelligence for heat, heavy rain, temperature swings, overcast light, high humidity, dry indoor air and wind.
- Reworked the map zone indicators from large blocks into clearer dot-based care markers.
- Improved map readability and reduced overlap between zones/custom areas.
- Simplified Add Area map placement with preset direction buttons instead of X/Y coordinate fields.
- Hid visible scrollbars from app shells and bottom sheets.
- Replaced fertilizer-related Leaf reuse with a distinct Sprout icon.
- Added an Install on phone card in Settings before Garden status.
- Improved toast width/positioning so success/failure messages do not cut off on mobile.


# Amaar Bagaan Release Notes

## v1.3.1 — Structural UX Polish + Professional Map/Settings Cleanup

Locked base: **v1.3.0** is the stable working release before this package.

### Fixed

- Reworked Firebase/local status language so the app no longer presents a confusing “Local demo database” message when Firebase is configured.
- Replaced demo wording with clearer states: `Cloud synced`, `Offline cache`, or `Setup needed`.
- Removed emoji usage from recent care history and plant care logs; all care actions now use Lucide icons.
- Hid the floating Smart Add button from Settings and Map where it was blocking the layout.

### Improved UI/UX

- Redesigned the top app identity area with a proper Amaar Bagaan mark, Bengali label and cleaner cloud-status pill.
- Reordered bottom navigation to: `Plants · Map · Home · Care · Settings`, with Home centered and visually emphasized.
- Moved Garden Highlights near the top of Home so the app immediately feels alive and plant-focused.
- Reworked the main “Today in the Garden” card with plant-themed iconography instead of a generic circular background.
- Refined mobile spacing, touch targets, card hierarchy, toast responsiveness and visual rhythm.
- Improved Settings by keeping daily-use controls visible and moving backup/maintenance tools into an advanced section.
- Redesigned Weather Location as a location/map-inspired card instead of a plain form.

### Map and Zone Intelligence

- Rebuilt the House Garden Map experience around a selected-zone workflow.
- Removed the long zone-card list from the Map page.
- Added a compass-style map treatment with N/E/S/W indicators.
- Added a clearer selected-zone panel showing plant count, care due, heat risk, sunlight, shade, airflow, rain exposure, wind risk and humidity profile.
- Added ability to create new home areas from the Map page.
- New areas can define sunlight, shade, heat, rain, wind, humidity and airflow metadata for future care logic.

### Data and Schema

- Bumped schema to v4.
- Bumped seed version to v1.3.1.
- Added Firestore/local persistence support for custom home zones.
- Preserved existing plant, care-log and zone behavior from v1.3.0.

### Post-upgrade actions

After starting v1.3.1 locally:

1. Copy your existing `.env.local` from v1.3.0.
2. Run the app.
3. Go to Settings → Caretaker and developer tools.
4. Run `Migrate schema` once.
5. Run `Safe seed check` once if any default areas are missing.

---

## v1.3.0 — Smart Add + Intelligent House Zones

### Added

- Smart Add performs richer plant lookup using Wikipedia and Wikidata.
- Wikidata taxon name and Bengali label are used when available.
- Reference image lookup uses Wikipedia/Wikimedia/Wikidata image sources when available.
- Smart Add shows confidence percentage and confidence label.
- Source availability chips show whether Wikipedia, Wikidata and image lookup succeeded.
- Manual correction fields are available before saving the generated plant profile.
- Source candidates are displayed for review.
- Care-template fallback is preserved when external data is incomplete.
- New house-zone definitions: Roof North Edge, Boundary East, Boundary West and Staircase.
- Zone map is tappable.
- Selected zone panel shows plant count, due care count, heat risk and risk reasons.
- Zone-wise plant chips open plant details directly.
- Weather-aware task generation considers zone heat, rain, wind and plant type more strongly.

### Improved

- Plant schema preserves smart-add metadata: source URL, source list, confidence, confidence label and template name.
- Schema version moved to v3.
- Seed version moved to v1.3.0.
- Map risk badges distinguish normal, watch, high, care due and empty zones.
- Weather advice includes exposed roof/boundary language.

---

## v1.2.0 — Premium Polish and Data Hardening

### UI/UX polish

- Refined mobile spacing, card rhythm, button feedback and bottom navigation depth.
- Improved typography hierarchy for dashboard, plant inventory, settings and detail views.
- Added richer empty states for care board and no-task scenarios.
- Improved loading/success feedback and toast styling.
- Cleaned plant detail sheet with stronger hero image, close action, status chips, next watering and next fertilizer dates.
- Improved settings page structure with dedicated database, backup and maintenance sections.

### Data model and reliability

- Introduced schema versioning for plants, zones, settings and care logs.
- Added migration utility to normalize older v1.1.1 records into the v1.2 schema.
- Normalized care logs with stable IDs, plant names, zone IDs, zone names, action type, status, note, timestamps and source.
- Improved timestamp handling for Firestore Timestamp objects and ISO strings.
- Added last watered/fertilized consistency so plant summary and care logs update using the same timestamp.
- Strengthened seed behavior to add only missing seed data and avoid duplicate seed records.
- Added safe seed check and reset-to-seed admin action.
- Added JSON export/import backup flow.
- Replaced hard delete with archive/soft-delete behavior and restore support.

### Repository hygiene

- Consolidated documentation into `README.md`, `RELEASE_NOTES.md`, and `FIREBASE_DEPLOYMENT_GUIDE.md`.
- Removed separate scattered release and quick-start markdown files.
- Updated `.gitignore` for clean source packaging.

---

## v1.1.1 — Firebase Boot Hotfix and Live-Test Baseline

- Fixed loading screen blocking Google sign-in.
- Confirmed Google Authentication and Firestore write flow.
- Confirmed Firestore seed collections for plants, zones and settings.
- Published as first private live-test release at Firebase Hosting.

---

## v1.1.0 — Firebase Connected Release

- Added Firebase Auth, Firestore and Hosting configuration.
- Added Firebase environment template and deployment guide.
- Added Google sign-in and cloud/local mode detection.
- Added Firestore-backed plant, zone, settings and care-log operations.

---

## v1.0.0 — Local MVP Baseline

- Created first mobile-first Amaar Bagaan app.
- Added home dashboard, weather card, plant list, house map, care board and settings.
- Added local demo mode and initial seed plants.

## v1.3.4 — Brand Lockup, Install Flow and Map Revamp

- Locked v1.3.3 as the previous stable baseline.
- Reworked the welcome/sign-in logo alignment and brand composition.
- Removed the extra rounded-square treatment around the provided round logo and reused the same SVG identity across app chrome and PWA icon.
- Added a subtle brand tagline under the sticky top ribbon.
- Straightened and repositioned the home hero plant silhouette for a cleaner premium visual.
- Improved the PWA install action: local development now opens the live app, while production uses the browser install prompt when available.
- Rebuilt the map into a more interactive care-zone point map with a calmer home/courtyard visual system.
- Added zone removal with safe reassignment for plants previously assigned to the removed area.
- Added responsive refinements for smaller Android screens.


## v1.3.8 — Brand Lockup Consistency Fix

- Fixed inconsistent top brand layout between Settings and other pages.
- Locked brand lockup into one stable flex-column text stack.
- Added darker green-to-gold premium title gradient.
- Preserved the selected Bengali tagline: `প্রতিদিনের সহজ গাছ-যত্ন`.
- Scope is intentionally limited to the header/brand ribbon only. No data, schema, or Firestore rule changes.
