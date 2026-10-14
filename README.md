# Kit-Built Panel House — PWA

Concept app for the steel-kit + 100 mm IBR/EPS panel house. Version v1 · 14 Oct 2026.

## Tabs
- **Overview** – render (artist's impression), key figures, assembly steps, Share button.
- **System** – cutaway, end section, rail–panel–rail lock detail, open questions for the factory.
- **Layout** – tap wall panels to make windows/doors; bracing check; front elevation.
- **3D** – drag to rotate; Finished / Floor plan / X-ray / Frame; cladding colours.
- **Costing** – price comparison for 3 suppliers, WhatsApp quote requests, steel cutting list.
- **Info** – version, clear saved data.

Layout, prices, supplier names and numbers are saved on the device (localStorage).
The 3D view and costing use whatever layout is set on the Layout tab.

## Files (keep them together in one folder)
index.html · manifest.json · sw.js · render.jpg · icon-192.png · icon-512.png · apple-touch-icon.png

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
