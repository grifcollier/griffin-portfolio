# Griffin Collier portfolio

Single-page personal portfolio for Griffin Collier (Auburn ME, May 2027), aimed at UAS and defense engineering recruiters.

## Structure
- `index.html` holds all markup, CSS, and JS. No build step and no framework. Keep it that way unless asked.
- `assets/` is for photos and video. Reference them with relative paths (`assets/aeroguard-1.jpg`).
- Fonts: Geist and Geist Mono from Google Fonts.

## Design rules
- All colors are CSS tokens on `:root` with dark-mode overrides. Never hard-code a color in a component rule.
- Scroll effects use `animation-timeline` inside `@supports`; browsers without support show everything at rest. Keep the `prefers-reduced-motion` fallback working.
- Content must be visible without scrolling triggers. Nothing should rest at `opacity: 0`.
- Side gutter of at least 16px; no horizontal scroll at 400px wide.

## Content rules
- Source of truth for dates, titles, and bullets is Griffin's resume. Don't invent metrics.
- AeroGuard photos only once SCI Technology approves in writing. AFRL renders only once cleared.
- Placeholders are marked with square brackets, e.g. `[Lab and aircraft photos]`.

## Open items
- Fill the 9 media placeholders.
- Add a resume PDF to `assets/` and a download link once hosted.
- Decide whether to keep the phone number on a public deploy.

## Preview
`python3 -m http.server 8000` then open http://localhost:8000
