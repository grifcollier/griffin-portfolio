# Griffin Collier portfolio

Open `index.html` in a browser, or run `python3 -m http.server 8000` and visit http://localhost:8000.

## Adding photos, video, and your résumé (drop-in)

Every media spot shows a placeholder label until a correctly-named file exists in `assets/`.
Drop a file in with the exact name below, reload, and it appears — no code changes.
Missing files never show a broken image; they just keep the label. Each project has a **lead
photo**, three **build-story steps**, and a **gallery** (any number of files → a lightbox grid).

### Origin strip (after the hero)
| Slot | File in `assets/` |
|---|---|
| Ferris wheel, age 6 | `origin-6.jpg` |
| K'nex bridge & coaster, age 7 | `origin-7.jpg` |
| Log barge, age 11 *(optional — un-hide the figure in `index.html` to show it)* | `origin-barge.jpg` |

### Projects (lead · build steps · gallery)
| Project | Lead | Build-story steps | Gallery |
|---|---|---|---|
| **AeroGuard** (SCI) | `aeroguard-lead.jpg` | `aeroguard-step1.jpg` … `-step3.jpg` | `aeroguard-g1.jpg` … `-g4.jpg` |
| **Shock-test stand** (SCI) | `shocktester-lead.jpg` | `shocktester-step1.jpg` … `-step3.jpg` | `shocktester-g1.jpg` … `-g3.jpg` |
| **SUAS airframe** (Purdue) | `suas-lead.jpg` | `suas-step1.jpg` … `-step3.jpg` | `purdue-1.jpg`, `purdue-2.jpg`, `suas-g1.jpg`, `suas-g2.jpg` |
| **CNC foam cutter** (VSDDL) | `foamcutter-lead.jpg` | `foamcutter-render.png`, `foamcutter-wiring.jpg`, `foamcutter-cut.mp4` (poster `foamcutter-cut.jpg`) | `foamcutter-g1.jpg` … `-g3.jpg` |
| **Subscale VTOL** (VSDDL) | `vtol-lead.jpg` | `vtol-step1.jpg` … `-step3.jpg` | `vtol-1.jpg`, `vtol-2.jpg`, `crate-1.jpg` |
| **AFRL counter-UAS** *(renders when cleared)* | `afrl-lead.jpg` | `afrl-step1.jpg` … `-step3.jpg` | `afrl-g1.jpg`, `afrl-g2.jpg` |

### Other
| Slot | File in `assets/` |
|---|---|
| Full-width flight-testing band | `flightline.mp4` and/or `flightline.jpg` |
| Résumé (enables the Download button) | `griffin-collier-resume.pdf` |

Tips:
- Lead photos read best at ~16:8; gallery thumbs crop to a grid; the foam-cutter render is a PNG.
- Keep images under ~500 KB each (JPG for photos). Videos: short, muted, looping — they
  autoplay and pause under reduced-motion.
- Galleries take **any number** of files — add `…-g5`, `…-g6`, etc. and they just appear.
- Click any photo to open the lightbox; arrow keys move through that project's images; `Esc` closes.
- **Add `griffin-collier-resume.pdf` before deploying**, or the Download button will 404.

## Deploy — GitHub + Vercel

1. From this folder: `git init`, commit, then `gh repo create griffin-portfolio --public --source . --push`.
2. In Vercel: **New Project → Import** the GitHub repo → Framework preset **Other** →
   Root Directory = repo root → **Deploy**. No build command, no `vercel.json` needed.
3. Every `git push` to `main` auto-deploys.

Alternative: drag this folder onto Netlify Drop.
