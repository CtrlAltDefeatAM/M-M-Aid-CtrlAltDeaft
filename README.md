# MMAid Web

Client-side website starter for the Mutants & Masterminds Aid (MMAid) project.

## What this first commit does

- Provides a GitHub Pages-ready static website.
- Lets a player drag/drop a character file.
- Directly reads Mastermind Maker `.mm3` files as JSON.
- Detects Foundry Actor JSON.
- Provides a conservative Hero Lab XML preview adapter.
- Produces a normalized character preview.
- Runs a small starter review only on values that can be safely derived.
- Downloads a JSON review report.
- Uses no account system, database, analytics service, or server-side character upload.

## Important limitation

This repo is intentionally **not** a second independent copy of the full Foundry MMAid validator.

The next major engineering task is to extract the platform-neutral portions of MMAid into a shared core so that:

Foundry Adapter -> MMAid Core -> PlayerFix

and

Web Adapter -> MMAid Core -> PlayerFix

use the same rules and mathematics.

Do not manually reimplement 79+ validators in the website.

## Supported starter inputs

| Format | Starter status |
|---|---|
| Mastermind Maker `.mm3` | Direct structured import |
| Foundry Actor `.json` | Recognized / preview |
| Hero Lab `.xml` | Conservative preview |
| Generic `.json` | Basic mapping |
| `.txt` / `.html` | Conservative text preview |

## GitHub Pages

This repo includes a GitHub Pages workflow.

1. Upload the files to your repository.
2. Open **Settings -> Pages**.
3. Under **Build and deployment**, select **GitHub Actions** if GitHub has not already selected it.
4. Push to `main`.
5. The workflow publishes the static site.

## Local testing

No build step is required.

Because the site uses ES modules, serve the folder with a local web server rather than double-clicking `index.html`.

Examples:

```bash
python -m http.server 8080
```

or use Cursor/VS Code Live Server.

Then open:

```text
http://localhost:8080
```

## Privacy

All starter parsing happens in the player's browser. There is no character upload endpoint in this repository.
