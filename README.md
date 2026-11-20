# MegaBase Builder

Browser tools for planning Palworld megabase layouts. Each design is a single web page: pick sizes, see the top-down plan and tower, place decor, and follow a build order. No install and no server needed.

**Designs**

| Design | Folder |
| --- | --- |
| MegaBase Builder: 4-in-1 Clover | `designs/4-in-1-clover/` |

## Use it

- **In a browser:** after turning on GitHub Pages (below), share your Pages link. Guildmates open it and pick a design.
- **On a PC:** download the repository (Code, then Download ZIP), unzip it and double-click `index.html`. It works offline except the heading font, which falls back to a plain one.
- Each person's sizes, decor and build-order checkmarks are saved in their own browser only.

## Publish with GitHub Pages

1. Upload everything in this folder to the root of a repository (keep the folder structure).
2. In the repository, open **Settings, then Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then save.
4. After a minute or two the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Naming convention

- **Display name:** `MegaBase Builder: <Design name>`. This is the page title and the heading.
- **Folder name:** the design name in lowercase with hyphens, for example `4-in-1-clover`. GitHub file and folder names can't contain a colon, so the full display name lives inside the page, not in the file name.
- **Location:** `designs/<folder-name>/index.html`. Always call the page `index.html`, so the folder link opens it directly.

## Add a new design

1. Copy `designs/4-in-1-clover/` and rename the copy, for example `designs/<new-name>/`.
2. Open its `index.html` and change three things:
   - the `<title>` and the `<h1>` near the top of the body
   - `DESIGN.id` and `DESIGN.name` at the start of the script. A unique `id` keeps each design's saved settings separate.
   - the layout code itself. The sizes, rooms and floors are defined in the script, and the diagrams are drawn from them.
3. Add one entry for it in `designs.js` (copy the existing entry and change `id`, `name`, `path`, `summary`, `tags` and `added`).
4. Commit and upload. The home page picks it up from `designs.js`.

## Files

```
index.html              home page that lists every design
designs.js              the list of designs (edit this when you add one)
designs/<name>/index.html   one self-contained builder per design
.nojekyll               tells GitHub Pages to serve the files as they are
README.md               this file
```
