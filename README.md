# Avik.dev — editable GitHub Pages portfolio

A static portfolio matching the provided dark design, with an easy Pages CMS editor.

## Pages included
- **Home**: hero and responsive cards for all agent projects
- **About**: introduction, three info cards, lessons, interests and skills
- **Agent details**: one reusable page per project at `agent.html?slug=study-buddy` (each card links to its own page)

## Publish with GitHub Pages
1. Create a **public** repository on GitHub, e.g. `avik-portfolio`.
2. Upload the *contents* of this folder to the repository root. Upload hidden `.pages.yml` too (it is important).
3. Go to repository **Settings → Pages**. Select **Deploy from a branch**, **main**, **/(root)** and Save.
4. Your site will be at `https://YOUR-USERNAME.github.io/avik-portfolio/` (typically within a few minutes).
5. Open https://app.pagescms.org/ and sign in with GitHub. Grant it access to the repository. Select the repository and open **Portfolio content**.
6. Edit text, upload images, add/reorder agents, and save. Pages CMS commits the new content to GitHub; GitHub Pages republishes automatically.

## How images work
In Pages CMS, upload images into the **media** folder. Use the **Cover image** field for a card's image; use **Project screenshots** to add as many screenshots as you want to each agent. A project with no uploaded screenshots shows 3 placeholders (like the reference). Empty cover images show a screenshot placeholder.

## How to edit directly
`data/site.json` contains **all content**. It is also the source read by Pages CMS. `assets/style.css` controls styling; `assets/site.js` renders the sections. The Pages CMS config is `.pages.yml`.

## Local preview
Since browsers block `fetch` from local file URLs, open a terminal inside this folder and run:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/`.

## Notes
- This is a static website (no server or database required).
- Agent IDs/slugs must be unique and use letters, numbers and hyphens. Existing URLs depend on the slug, so avoid changing a slug after sharing an agent link.
- Pages CMS changes directly to the connected GitHub repository; no manual upload is needed for future content edits.
- The content is a starter based on the user's provided screenshots. Verify descriptions, skills, and work claims before publishing.
