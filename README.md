# Kollel Chatzos · נקודת חצות

A bilingual (English / Yiddish) promotional website for **Kollel Chatzos — Nekudas Chatzos**, the Brooklyn kollel whose chashuva young men learn Torah every night from *chatzos* until *alos hashachar* — illuminating and safeguarding the city.

The site explains what the kollel does and why it is worth supporting, and invites visitors to become a partner.

## Pages

| Page | English | Yiddish |
|------|---------|---------|
| `index.html` | Home — hero, the mission, three pillars | היים |
| `about.html` | The Kollel — the avodah of the night, the *seder hakollel*, the 24-hour cycle | דער כולל |
| `segulos.html` | Segulos & Maalos of chatzos (Zohar, Kaf HaChaim, Sefer HaMiddos) | סגולות |
| `partner.html` | Become a Partner — dedication tiers + contact form | ווערט א שותף |

## Language toggle

Every page is fully bilingual. The **EN / יידיש** toggle in the navbar switches all content and flips the layout to right-to-left for Yiddish. The choice is remembered between pages via `localStorage`.

## Tech

Pure static site — no build step, no dependencies. Each page is **fully self-contained**: the CSS and JavaScript are inlined into every HTML file, so the design shows no matter how the file is opened (double-clicked, in a preview pane, or on a web host).

- `index.html`, `about.html`, `segulos.html`, `partner.html`
- Inlined per page: midnight theme + starfield + responsive layout (CSS), and the language toggle / mobile nav / reveal-on-scroll / demo form (JS).

Fonts are loaded from Google Fonts (Cormorant Garamond, Inter, Frank Ruhl Libre, Heebo).

## Running locally

Just open `index.html` in a browser — there is nothing to compile.

To serve it locally:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploying

This is a static site, so it can be hosted free on **GitHub Pages**:

1. Push this repo to GitHub.
2. In the repo go to **Settings → Pages**.
3. Under *Build and deployment*, set **Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Save — the site goes live at `https://<username>.github.io/kollel-chatzos/`.

## Notes

- The phone, email and donation amounts on the **Partner** page are placeholders — replace them with the kollel's real details.
- The contact form is a front-end demo; connect it to a form service (Formspree, Netlify Forms, etc.) or an email handler to receive submissions.

*Content adapted from the kollel's own flyers and the liqut on the maalos of kimas chatzos.*
