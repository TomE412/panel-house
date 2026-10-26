# Kit-Built Panel House — PWA

Concept app for the steel-kit + 100 mm IBR/EPS panel house. Version v5 · 26 Oct 2026 (adds the Miombo House tab; spine + pillars versions A and B, gallery, walkthrough).

## Tabs
- **Overview** – render (artist's impression), key figures, assembly steps, Share button.
- **Miombo House** – one-bedroom single-slope design: board of impressions, key sizes, rooms, 12 model renders (tap to enlarge), plan + structure sheet.
- **Gallery** – walkthrough video, 3D model views (living, both bedrooms), artist's impressions of interior and exterior finishes.
- **System** – cutaway, end section, version A vs B comparison, open questions.
- **Layout** – tap wall panels to make windows/doors; bracing check; front elevation.
- **3D** – drag to rotate; versions A and B; build steps; Finished / Floor plan / X-ray / Steel only; cladding colours.
- **Costing** – versions A and B, price comparison for 3 suppliers, WhatsApp quote requests, steel cutting list.
- **Info** – version, clear saved data.

Layout, prices, supplier names and numbers are saved on the device (localStorage).
The 3D view and costing use whatever layout is set on the Layout tab.

## Files (keep them together in one folder)
index.html · manifest.json · sw.js · miombo-*.jpg · render.jpg · interior.jpg · finishes.jpg · walkthrough.mp4 · walkthrough-poster.jpg · model-living-B.jpg · model-bedroom-B.jpg · model-bedroom-A.jpg · icon-192.png · icon-512.png · apple-touch-icon.png

## Publish on GitHub Pages
1. GitHub Desktop → File → New repository → name it `panel-house`.
2. Drag all the files from this folder into the repository folder. Commit, then Publish.
3. On github.com → the repo → Settings → Pages → Source: `main` branch, `/ (root)` → Save.
4. After a minute the app is at `https://<your-username>.github.io/panel-house/`. Send that link to George.
   On a phone: open the link → browser menu → Add to Home screen.

If you put it in a different repo or sub-folder, change `"id"` in manifest.json to match the path.

## Updating
Change the files, then bump the cache name in `sw.js` (`panelhouse-v1` → `panelhouse-v2`) and
`APP_VERSION` in index.html. Without the bump, phones keep showing the old version.

## Testing offline
Open the link once online. Then airplane mode → close the app fully → reopen. All tabs should work;
only the WhatsApp buttons need a connection.

The walkthrough video is not cached for offline use (videos stream in pieces); it needs a connection.
