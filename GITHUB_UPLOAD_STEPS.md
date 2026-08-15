# GitHub Upload Steps

Use these steps for the new MMAid Web repository.

## 1. Extract the ZIP

Extract:

`MMAid-Web-Starter-v0.1.0.zip`

You should see these items at the top level:

```text
.github/
data/
src/
.gitignore
404.html
CURSOR_BUILD_PROMPT.md
PRIVACY.md
README.md
SITE_MAP.md
VERSION
index.html
```

Do NOT upload the outer `MMAid-Web-Starter` folder as one nested folder.
The files above should live at the repository root.

## 2. Upload to GitHub

On the repository page:

1. Click **Add file**.
2. Click **Upload files**.
3. Drag the extracted contents into GitHub.
4. Confirm that `index.html` will be at the repository root.
5. Commit to `main`.

If GitHub's browser upload makes nested folders awkward, open the repository in Cursor/GitHub Desktop and copy the extracted contents into the repo folder, then commit/push.

## 3. Enable GitHub Pages

This starter includes:

`.github/workflows/pages.yml`

After the files are on `main`:

1. Open **Settings**.
2. Open **Pages**.
3. Under **Build and deployment**, choose **GitHub Actions** if needed.
4. Open the **Actions** tab.
5. The workflow named `Deploy static MMAid Web to GitHub Pages` should run.
6. When it succeeds, GitHub will show the Pages URL.

## 4. Test the website

Open the Pages URL.

Test with:

- a Mastermind Maker `.mm3` file;
- a Foundry Actor `.json` file.

Expected starter behavior:

- file remains local to the browser;
- format is detected;
- character name / PL / counts are previewed;
- a conservative starter review appears;
- a JSON review report can be downloaded.

## 5. Open in Cursor

After the starter works, open the repository in Cursor.

Give Cursor the contents of:

`CURSOR_BUILD_PROMPT.md`

That prompt tells Cursor how to continue without creating a second divergent copy of the MMAid rules engine.

## Important

Do NOT upload private player character files to the public repository.

The `.gitignore` blocks `.mm3` and `.por`, but always verify the staged/changed files before pushing.
