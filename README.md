# Portfolio site — no GitHub, no code editing needed

## What's in this package
- `index.html` — the site itself
- `projects.json` — your six project entries, pre-filled
- `files/` folder — put your actual PDF/PPTX files in here before deploying

## Step 1 — Add your real files
Move your actual project files into the `files` folder so the names match exactly:
- `AlphaEvolve_Technical_Report-v2.pdf`
- `Lacanian_Ethics_Course.pptx`
- `NXAirS_550_Professional_User_Manual_V2.pdf`
- `Netflix_Platform_CaseStudy.pptx`
- `Algorithmic_Bias_Mitigation_Training_Model.pdf`
- `Adaptive_Workplace_OS_MicrosoftBuildAI2026-1.pptx`

Delete the `README.txt` placeholder inside `files/` once your real files are in there — it was only there so the empty folder wouldn't get lost when you download this package.

## Step 2 — Deploy (no GitHub, no git, no command line)
1. On your phone, go to **app.netlify.com/drop** in Chrome
2. You don't need to sign up first — you can drag/select your whole folder (containing `index.html`, `projects.json`, and `files/`) right on that page
3. If your phone can't drag-and-drop a folder into the browser, zip the folder first (most Android file managers have a "Compress" or "Zip" option when you long-press the folder), then upload the `.zip` — Netlify Drop accepts zipped folders too
4. Netlify builds it instantly and gives you a live URL like `https://random-name-1234.netlify.app`
5. Optional: sign up for a free Netlify account afterward to rename that URL to something cleaner and keep the site permanently (unclaimed drops expire after a while)

## Step 3 — Turn on comments (Disqus, free, no GitHub account)
1. Go to **disqus.com** → sign up → choose "I want to install Disqus on my site"
2. Give it a name — Disqus gives you a **shortname**
3. Open `index.html` in a text editor, find the line:
   `s.src = 'https://YOUR-DISQUS-SHORTNAME.disqus.com/embed.js';`
4. Replace `YOUR-DISQUS-SHORTNAME` with your real shortname
5. Re-zip and re-drop the folder on Netlify to update the live site

## Step 4 — Figma embed
In Figma: open your file → **Share → Embed** → copy that link. In `projects.json`, replace `PASTE_YOUR_FIGMA_SHARE_LINK_HERE` with it.

## Updating the site later
Whenever you want to add a new project or fix something: edit `projects.json` or add files to `files/`, then re-zip the whole folder and drop it on **app.netlify.com/drop** again — it replaces the old version instantly. No git, no repo, no commands.
