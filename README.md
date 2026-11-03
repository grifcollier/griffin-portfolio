# Griffin Collier portfolio

Open `index.html` in a browser, or run `python3 -m http.server 8000` and visit http://localhost:8000.

## Adding photos, video, and your résumé (drop-in)

Every media spot shows a placeholder label until a correctly-named file exists in `assets/`.
Drop a file in with the exact name below, reload, and it appears — no code changes.
Missing files never show a broken image; they just keep the label. Slots that accept more
than one file (VSDDL, Purdue, AeroGuard) turn into a lightbox gallery when multiple are present.

| Where on the page | File to drop in `assets/` |
|---|---|
| Experience · AeroGuard *(hold until SCI approves in writing)* | `aeroguard-1.jpg`, `aeroguard-2.jpg` |
| Experience · VSDDL lab & aircraft | `vsddl-1.jpg`, `vsddl-2.jpg` |
| Experience · Purdue airframe & layup | `purdue-1.jpg`, `purdue-2.jpg` |
| Experience · AFRL concept renders *(hold until cleared)* | `afrl-1.jpg` |
| Project · foam cutter CAD render | `foamcutter-render.png` |
| Project · foam cutter wiring photo | `foamcutter-wiring.jpg` |
| Project · foam cutter cutting clip | `foamcutter-cut.mp4` (+ optional poster `foamcutter-cut.jpg`) |
| Full-width flight media | `flightline.mp4` and/or `flightline.jpg` |
| Résumé (enables the Download button) | `griffin-collier-resume.pdf` |

Tips:
- Keep images roughly 4:3 and under ~500 KB each (JPG for photos, PNG for the render).
- Videos: short, muted, looping — they autoplay on the page and pause under reduced-motion.
- Click any photo to open the lightbox; arrow keys move between images in that slot; `Esc` closes.
- **Add `griffin-collier-resume.pdf` before deploying**, or the Download button will 404.

## Deploy — GitHub + Vercel

1. From this folder: `git init`, commit, then `gh repo create griffin-portfolio --public --source . --push`.
2. In Vercel: **New Project → Import** the GitHub repo → Framework preset **Other** →
   Root Directory = repo root → **Deploy**. No build command, no `vercel.json` needed.
3. Every `git push` to `main` auto-deploys.

Alternative: drag this folder onto Netlify Drop.
