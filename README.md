# sysdraw

A small diagram editor for system design interviews and screen-sharing. Open it at **https://sysdraw.pages.dev**.

- **HLD mode** draws system components (client, service, database, cache, load balancer, queue, object storage, CDN, AI, and a plain component with no icon) joined by arrows, plus boxes and text for grouping and notes.
- **LLD mode** draws UML class diagrams: classes, interfaces, enums and records with fields and methods, joined by extends, implements and has-a arrows.
- **DSA mode** is a scratch pad for coding rounds: 1D and 2D arrays with index numbers, and nodes for linked lists, trees and graphs. Right-drag from a node to empty canvas grows a new node joined to it; right-drag an array right or down to add columns or rows, and back to remove them. Tab moves through the cells and adds one past the end.

It is one HTML file with no dependencies and no server. Your browser keeps one diagram per mode, and it never leaves your computer. In Chrome or Edge, **Open folder** keeps any number of diagrams as `.json` files in a folder you pick instead, so you can keep them in git; changes made to those files by other programs show up within a second. In Brave, first enable `brave://flags/#file-system-access-api`.

## Controls

| To | Do this |
|---|---|
| Add a box | Right-click the canvas |
| Connect two boxes | Right-drag from one box onto another |
| Change or delete a box or arrow | Right-click it |
| Label an HLD arrow | Right-click it, type a number or letter, and press Enter; the label moves with the arrow |
| Move a box | Drag it; dragging a selected box moves the whole selection |
| Select several | Drag a rectangle on empty canvas, Shift+click to add or remove a box, or Ctrl+A for everything; Escape clears it |
| Copy, paste or delete the selection | Ctrl+C, then Ctrl+V pastes a copy beside it with its arrows and strokes; Delete removes it |
| Edit a name or line | Double-click it; Enter adds a line below, or above when the caret is at the start of the line; Backspace on an empty line removes it. Shift+Enter breaks the line inside the same row, for a calculation in HLD or a hint under an LLD field or method |
| Reorder a field or method | Drag the f or m tag at the start of its row |
| Pan | Scroll, Shift+scroll sideways, or drag with the middle or right button or a finger on empty canvas |
| Scribble | Draw with a pen; hold either button on its side to rub out strokes, or right-click the canvas and choose Clear ink |
| Zoom | Ctrl+scroll (Cmd+scroll on a Mac), a two-finger pinch, or the − and + in the bottom-left corner; click the percentage for 100% |
| Undo | Ctrl+Z |
| Keep several diagrams | Every edit saves at once. Open a folder, then the diagram's name in the toolbar opens the list of the current mode's diagrams: type a name and press Enter to start a new one, click one to open it, or use its pencil or bin to rename or delete it |
| Save or share a diagram | Export copies or downloads it as JSON; Import opens one as a new diagram |

To run it locally, download `index.html` and open it in a browser.
