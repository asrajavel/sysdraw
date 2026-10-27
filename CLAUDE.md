# sysdraw

- `index.html` stays one dependency-free file that opens straight from disk, with no server or build step.
- Cloudflare Pages serves this repo's `main` branch at https://sysdraw.pages.dev, so every push to `main` goes live.
- The LLD and HLD modes share all canvas, menu, undo, and import/export code. Each mode's box kinds, arrow types, row sections, and storage key live in its `MODES` entry; prefer adding a mode feature there over branching on `mode`. The shared code still names LLD's `has-a`, `extends`, `implements`, `fields`, `methods`, and `enum` directly, and HLD styling is under `body[data-mode="hld"]`.
- HLD component icons are hand-drawn SVGs in a soft-line style: a mid-strength coloured line on the palest fill of the same colour. The user found the filled versions too loud and the grey-toned ones too muted.
- A kind with a third `shape` entry (`frame`, `text`, `window`) is drawn as Box, Text, or Text with Heading instead of a normal box. A Box also stores its size as `w` and `h`.
- Pen strokes live in an optional `ink` array of flat `[x1, y1, x2, y2, ...]` point lists, shared by both modes and left out of exports when empty.
- Exports carry `"mode"`. An import without one opens in whichever mode it fits. Every box needs each of its mode's sections as an array: `fields` and `methods` in LLD, `notes` in HLD.
- Never use the browser's `alert`, `confirm`, or `prompt`. Use the page's own `ask()` dialog so every pop-up matches the diagram's style.
- Imported diagrams may be hand-written or AI-written JSON, so check every box and arrow before drawing them.
- The `uml-to-java` skill in the user's private interview-notes repo turns LLD exports into Java skeleton files, so keep the export format compatible with it.
- Test it through a local server (`python -m http.server` from the repo root, then open `/index.html`). The browser pane opens local files as `data:` URLs, where browser storage is blocked.
