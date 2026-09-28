# Narok County Projects Tracker

A mobile-first, illustrative prototype for reviewing county project progress, mapping project localities, submitting field updates, and previewing approved updates for residents.

**All projects, names, budgets, dates, photos, and progress figures are illustrative demo data.** The coordinates represent checked localities, not verified project sites. No submission is transmitted to Narok County or saved permanently. Updates remain in the current browser session and require approval in the local review queue before appearing in the public view.

## Run locally

From this repository's root:

```bash
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000. An internet connection is needed for Leaflet and OpenStreetMap map tiles. The project list remains usable if the map is unavailable.

## Five-minute demo

1. Open the dashboard and select **Narok Town drainage improvements** under Needs attention.
2. Inspect the blocker and next action in the project record.
3. Open **Project map** and tap the delayed project's marker.
4. Use **Submit field update** to enter milestone progress, a note, and optionally a photo.
5. Approve the update in the local review queue. Open **Public view**, select Narok Town, and inspect the approved note.

## Editable data

Edit `dist/data.js` to replace the sample projects. Use county-approved records and verified project coordinates before making factual claims. The initial locality coordinates were checked against the Narok Municipal Spatial Plan, Kenya Master Health Facility Registry, and geographic-name listings. Project-specific coordinates have **not** been verified.

## Architecture

`dist/index.html` is the static shell, `dist/style.css` the responsive visual system, `dist/data.js` the single sample dataset, and `dist/app.js` the interaction layer. Authentication, staff roles, verified imports, server review, and persistent storage are future integrations; this prototype does not claim to provide them.
