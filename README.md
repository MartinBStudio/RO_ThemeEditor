# RO_ThemeEditor

RO_ThemeEditor lets you edit and preview ROSE Online UI themes without
launching the game client. It runs locally on your PC in a browser; no server
connection is needed.

## Get started

1. Install **Node.js 22 or newer** from [nodejs.org](https://nodejs.org/). Keep
   the option to add Node.js to `PATH` enabled; npm is included with Node.js.
2. Copy the complete **`.dev-preview`** folder into the directory that
   contains your ROSE Online game folder. It must sit **next to** the game
   folder, not inside it. Do not copy only the files inside `.dev-preview`.
3. Double-click **`.dev-preview\Start-UI-Preview.cmd`**.
4. Wait for RO_ThemeEditor to open in your browser. On its first launch, it may
   download the required packages; keep the console window open while it starts.
5. Choose a theme and UI window to preview. Edit theme files in your usual
   editor, or use the code pane. Saved theme changes are written to
   the selected theme folder.

The game itself can remain closed. Keep the command window open while using the
RO_ThemeEditor; close it or press **Ctrl+C** when you are finished. Closing the browser
tab alone does not stop the server.

The folders should look like this:

```text
Your folder
├── ROSE Online
│   └── (game files)
└── .dev-preview
    ├── Start-UI-Preview.cmd
    └── (workshop files)
```

## If it doesn't start

- Check that `node --version` reports **v22 or newer**. If Node.js was just
  installed, open a new command window and try again.
- Allow internet access on the first launch so npm can install the workshop's
  dependencies. Later launches can use the installed dependencies offline.
- RO_ThemeEditor looks for theme folders alongside `.dev-preview`, in the same
  parent directory as the game folder.
  Each theme folder must contain a `manifestUi.json` file. If no themes appear,
  check that the theme folders are beside `.dev-preview`.
- If the browser does not open automatically, visit
  [http://127.0.0.1:4173](http://127.0.0.1:4173). If that port is in use, the
  launcher selects another available port and prints its address in the console.

For editor features, preview limitations, optional asset paths, and developer
build instructions, see [`.dev-preview/README.md`](.dev-preview/README.md).
