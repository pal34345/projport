# Portfolio site — Vercel + new GitHub repo

## What's in this package
- `index.html` — the site
- `projects.json` — your six project entries, pre-filled with the right file paths
- `files/` folder — put your real PDF/PPTX files in here before pushing

## Step 1 — Add your real files
Drop your actual files into the `files` folder with these exact names (matches `projects.json`):
- `AlphaEvolve_Technical_Report-v2.pdf`
- `Lacanian_Ethics_Course.pptx`
- `NXAirS_550_Professional_User_Manual_V2.pdf`
- `Netflix_Platform_CaseStudy.pptx`
- `Algorithmic_Bias_Mitigation_Training_Model.pdf`
- `Adaptive_Workplace_OS_MicrosoftBuildAI2026-1.pptx`

Delete `files/README.txt` once your real files are in — it's just a placeholder so the folder isn't empty.

## Step 2 — Create the new GitHub repo
1. github.com → **+ → New repository** → name it (e.g. `portfolio`) → **Public** → Create
2. **Add file → Upload files** → upload `index.html` and `projects.json` to the root
3. Create the `files` folder the same way as before (upload something into a path like `files/placeholder.txt` — GitHub creates the folder automatically), then upload your real PDFs/PPTs into it

## Step 3 — Import into Vercel
1. Go to **vercel.com** → sign in (you can use your GitHub account to sign in — this just authenticates you, it doesn't require any coding)
2. **Add New → Project**
3. Select your new repo from the list (you may need to tap "Adjust GitHub App Permissions" and grant Vercel access to it first)
4. Vercel auto-detects this as a static site. On the configure screen:
   - **Framework Preset:** Other
   - **Build Command:** leave empty
   - **Output Directory:** leave as `.` (root)
5. Tap **Deploy** — takes under a minute
6. You get a live URL like `https://portfolio-yourname.vercel.app` — this is permanent, no expiry, and updates automatically every time you push a change to the repo

## Step 4 — Turn on comments (Giscus)
1. In your repo: **Settings → General → Features** → tick **Discussions**
2. Go to **giscus.app** → sign in with GitHub → point it at your repo → it generates real `data-repo-id` and `data-category-id` values
3. Open `index.html` in your repo → find the `giscus.app/client.js` script block near the bottom → replace `data-repo`, `data-repo-id`, and `data-category-id` with your real values
4. Commit — Vercel auto-redeploys within a minute since it's watching your repo

## Step 5 — Figma embed
In Figma: open your file → **Share → Embed** → copy the link. In `projects.json`, replace `PASTE_YOUR_FIGMA_SHARE_LINK_HERE` with it.

## Updating the site later
Just edit `projects.json` or add new files in your GitHub repo directly — Vercel watches the repo and redeploys automatically within about a minute of any commit. No manual redeploy step needed.
