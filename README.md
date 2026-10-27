# ChemLab 3D 🧪

A browser-based chemistry lab assistant. No build step, a single `index.html`.

## Features
- **3D molecule viewer** (three.js): ball-and-stick and space-filling, drag to rotate, scroll/pinch to zoom
- **Photo upload**: identify a compound or reaction from a picture and view it in 3D
- **Reaction assistant**: type a reaction, get the balanced equation, products, 3D bonds and a properties table (type, conditions, energy, observations, safety...)
- **Rule checking**: validates formulas, checks conservation of mass with a built-in balancer, and flags wrong or impossible reactions
- **Periodic table + editor**: pick any element, add atoms, click two atoms to make or break bonds; valence rules are enforced live

## Run it
Open `index.html` in a browser, or host it free with GitHub Pages:
1. Create a repository and upload these files.
2. **Settings → Pages → Build and deployment → Deploy from a branch → `main` / root → Save.**
3. Your site appears at `https://<your-username>.github.io/<repo-name>/`.

## Enable the AI features
Photo recognition and reaction prediction use the Anthropic API.
1. Get an API key at https://console.anthropic.com
2. Open the site, expand **AI settings**, paste the key, press **Save**.

The key is kept in your browser's `localStorage` and sent only to `api.anthropic.com`. **Never put a key in the source code or commit it.** Because the key lives in the visitor's browser, this setup is meant for personal or classroom use; for a public site, put the API call behind your own small backend.

The periodic table, 3D editor, valence rules and the formula/balance checker work offline without a key.

## Notes
- 3D coordinates for AI-generated molecules are approximate. Verdicts and property values come from an AI model, so verify anything safety-critical against a textbook or SDS.
- Lone pairs are not modeled by the geometry "tidy" step.

## License
MIT
