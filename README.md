# Mi-HeatGuard dashboard demo (Render static site)

A self-contained demo of the Mi-HeatGuard surface dashboard. It runs entirely in the browser
with simulated data: no backend, no database and no real devices.

## Files

- `public/index.html`: the whole demo (HTML, CSS and JavaScript in one file)
- `render.yaml`: Render Blueprint that deploys `public/` as a static site

## Deploy on Render

1. Create a new GitHub (or GitLab) repository and push this folder to it.
2. In the Render dashboard choose New, then Blueprint, and select the repository.
   Render reads `render.yaml` and creates the static site `mi-heatguard-demo`.
3. Wait for the deploy to finish. Render gives you a URL ending in `.onrender.com`.

Without the Blueprint: choose New, then Static Site, connect the repository, set
Publish Directory to `public`, and leave the build command empty.

## Custom domain (optional)

In the site's Settings on Render, add a custom domain such as `demo.<your-domain>`, then create
the DNS record Render shows you.

## Before showing it to the mine

- The page is labelled "DEMO: simulated data". Keep that label.
- Thresholds (30, 33, 36 degrees C) are placeholders. Edit `TH` near the top of the script in
  `index.html` to change them.
- Anyone with the URL can open the page. It holds no real data.
- Test the page on the meeting room network and keep the recorded video as a backup.

## Not included

The real pilot dashboard needs a surface server with an MQTT broker, an ingestion service and a
database. That is a separate deployment from this demo.
