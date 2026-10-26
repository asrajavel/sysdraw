# Diagram tool

- `index.html` stays one dependency-free file that opens straight from disk, with no server or build step.
- The LLD and HLD modes share all canvas, menu, undo, and import/export code. Each mode's box kinds, arrow types, row sections, and storage key live in its `MODES` entry; prefer adding a mode feature there over branching on `mode`. The shared code still names LLD's `has-a`, `extends`, `implements`, `fields`, `methods`, and `enum` directly, and HLD styling is under `body[data-mode="hld"]`.
- Exports carry `"mode"`. An import without one opens in whichever mode it fits. Every box needs each of its mode's sections as an array: `fields` and `methods` in LLD, `notes` in HLD.
- Never use the browser's `alert`, `confirm`, or `prompt`. Use the page's own `ask()` dialog so every pop-up matches the diagram's style.
- Imported diagrams may be hand-written or AI-written JSON, so check every box and arrow before drawing them.
- The `uml-to-java` skill turns an LLD export into Java skeleton files.
- Test it through a local server (`python -m http.server` from the repo root, then open `/diagram-tool/index.html`). The browser pane opens local files as `data:` URLs, where browser storage is blocked.
