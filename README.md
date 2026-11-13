# Vilhelm – Dragon Age RPG app (GitHub version)

The whole app lives here; your data stays in your Google Sheet. The app talks to it through your
Apps Script, and every request needs your password, which is never stored in this repo.

## One-time setup

**Apps Script**
1. Paste the new `Code.gs` (and `Index.html`) into Apps Script, save, and deploy a new version
   (Deploy > Manage deployments > pencil > New version > Deploy). Access must be **Anyone**.
2. Project Settings (gear icon) > Script properties > **Add script property**:
   `APP_PASSWORD` = the password you want. Save.
   From now on the plain Google link only shows "Open the app from your home-screen icon".

**GitHub**
3. Create a repo (e.g. `VilhelmApp`) and upload every file in this folder (including `.nojekyll`).
4. Edit `config.js` on GitHub and paste your Apps Script link (ends in `/exec`) between the quotes. Commit.
5. Settings > Pages > Deploy from a branch > `main` / root > Save. After a minute:
   `https://<your-username>.github.io/VilhelmApp/`

**iPad**
6. Open that address in Safari > Share > **Add to Home Screen** (dragon icon).
7. Open it from the icon and type your password once. It stays remembered on that iPad.

## Updates
- Changes to the app: upload the new `index.html` here **and** paste `Index.html` into Apps Script.
- Changes to `Code.gs`: paste it into Apps Script and deploy a new version (same pencil > New version).
- Settings > "Disconnect this device" forgets the password on that device.
- To change the password, edit `APP_PASSWORD` in Script properties; every device will ask for the new one.
- 10 wrong passwords in a row lock it for 10 minutes.
