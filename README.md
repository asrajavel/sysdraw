# sysdraw

A small diagram editor for system design interviews and screen-sharing. Open it at **https://sysdraw.pages.dev**.

- **HLD mode** draws system components (client, service, database, cache, load balancer, queue, object storage, CDN) joined by arrows, plus boxes and text for grouping and notes.
- **LLD mode** draws UML class diagrams: classes, interfaces, enums and records with fields and methods, joined by extends, implements and has-a arrows.
- **DSA mode** is a scratch pad for coding rounds: 1D and 2D arrays with index numbers, and nodes for linked lists, trees and graphs. Right-drag from a node to empty canvas grows a new node joined to it; right-drag an array right or down to add columns or rows, and back to remove them. Tab moves through the cells and adds one past the end.

It is one HTML file with no dependencies and no server. Your diagrams are saved in your own browser and never leave it.

## Controls

| To | Do this |
|---|---|
| Add a box | Right-click the canvas |
| Connect two boxes | Right-drag from one box onto another |
| Change or delete a box or arrow | Right-click it |
| Move a box | Drag it; dragging a selected box moves the whole selection |
| Select several | Drag a rectangle on empty canvas, Shift+click to add or remove a box, or Ctrl+A for everything; Escape clears it |
| Copy, paste or delete the selection | Ctrl+C, then Ctrl+V pastes a copy beside it with its arrows and strokes; Delete removes it |
| Edit a name or line | Double-click it; Enter adds a line, Backspace on an empty line removes it. Shift+Enter breaks the line inside the same row, for a calculation in HLD or a hint under an LLD field or method |
| Pan | Scroll, Shift+scroll sideways, or drag with the middle or right button or a finger on empty canvas |
| Scribble | Draw with a pen; hold either button on its side to rub out strokes, or right-click the canvas and choose Clear ink |
| Zoom | Ctrl+scroll (Cmd+scroll on a Mac), a two-finger pinch, or the − and + in the bottom-left corner; click the percentage for 100% |
| Undo | Ctrl+Z |
| Save or share a diagram | Export copies or downloads it as JSON; Import loads one |

To run it locally, download `index.html` and open it in a browser.
