# Agent Notes

## Repo Shape
- This is a plain static GitHub Pages site, not a Node/Python/Rust app. There is no package manifest, lockfile, build step, test runner, or CI workflow in the repo.
- `index.html` is the root page and loads `static/styles.css` via `static/styles.css`.
- `housewarming/index.html` is a standalone subpage and loads the same stylesheet via `../static/styles.css`.
- `CNAME` publishes the site at `loganweir.com`; do not remove or rewrite it unless changing the custom domain.

## Local Verification
- Use a static server from the repo root when checking browser behavior, for example `python3 -m http.server 8000`, then open `http://localhost:8000/` and `http://localhost:8000/housewarming/`.
- There are no automated checks to run unless you add tooling. For HTML/CSS edits, verify by loading the affected page in a browser.

## Editing Conventions
- Keep changes framework-free unless the user explicitly asks to add tooling; the current site is intentionally just HTML and CSS.
- Preserve relative asset paths when moving or adding pages under subdirectories; root pages use `static/...`, nested pages need `../static/...` unless the structure changes.
