# sysdraw

A small diagram editor for system design interviews and screen-sharing. Open it at **https://sysdraw.pages.dev**.

- **HLD mode** draws system components (client, service, database, cache, load balancer, queue, object storage, CDN) joined by arrows, plus boxes and text for grouping and notes.
- **LLD mode** draws UML class diagrams: classes, interfaces, enums and records with fields and methods, joined by extends, implements and has-a arrows.

It is one HTML file with no dependencies and no server. Your diagrams are saved in your own browser and never leave it.

## Controls

| To | Do this |
|---|---|
| Add a box | Right-click the canvas, or use the toolbar's add button |
| Connect two boxes | Right-drag from one box onto another |
| Change or delete a box or arrow | Right-click it |
| Move a box | Drag it |
| Edit a name or line | Double-click it; Enter adds a line, Backspace on an empty line removes it |
| Pan | Scroll, Shift+scroll sideways, or drag with the middle or right button on empty canvas |
| Zoom | Ctrl+scroll (Cmd+scroll on a Mac), or the − and + in the bottom-left corner; click the percentage for 100% |
| Undo | Ctrl+Z |
| Save or share a diagram | Export copies or downloads it as JSON; Import loads one |

To run it locally, download `index.html` and open it in a browser.
