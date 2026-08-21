

# Goal:  Personally-managed website for professional use

This website was created using Jekyll.  It is hosted at braunm.github.io.  I want some help improving the structure and "look and feel," and simplifying processes.

# Current workflow

- Edited in Aquamacs 4 (currently aquamacs-alpha2)
- Served locally by running `bundle exec jekyll serve` in a separate Terminal window.  The site is visable at localhost:4000.
- Before publishing, I run `bundle exec jekyll build` and confirm that any new files were added to git.
- `_config.yml` sets `destination: docs`, and GitHub Pages is configured (Settings → Pages) to build directly from `main:/docs` (build type "legacy") — there is no GitHub Actions workflow. Committing and pushing the rebuilt `docs/` folder *is* the deploy step.

# Site map (for orientation, so future sessions don't need to re-explore)

- Layouts (`_layouts/`): `default`, `page`, `post`, `blog`, `blog_categories`, `class`.
- Key data files (`_data/`): `papers.yml`, `computing.yml`, `frontcards.yml`, `newsbox.yml`.
- Top-level pages: `about.md`, `blog.md`, `categories.html`, `computing.md`, `cv.md`, `index.md`, `papers.md`, `teaching.md`, `404.html`.
- Navigation is hardcoded HTML in `_includes/nav.html`, not data-driven from `_config.yml`.
- Styling is Bootstrap 5 + custom Sass: `css/custom.scss` imports Bootstrap pieces (functions, variables, mixins, reboot, grid, buttons, ...); `_config.yml` adds `node_modules` to `sass.load_paths` so Bootstrap comes from the npm install (`package.json`: bootstrap, masonry-layout). `Gemfile.lock`, `package.json`, and `package-lock.json` should stay committed so builds are reproducible.

# Editing caution

- `_data/*.yml` files (e.g. `papers.yml`) are structured YAML, not prose. On 2026-08-21, auto-fill/fill-paragraph in Aquamacs hard-wrapped one entry into run-on lines, breaking its YAML structure (text content was unaffected). A one-time slip, not a recurring pattern — noted here only so a similar-looking diff is recognized quickly if it ever resurfaces.

# Publishing / build-output notes

- `docs/` is not a Jekyll source folder — it's pre-rendered static output. GitHub Pages' "legacy" build (source: `main:/docs`) doesn't run Liquid/layouts/Sass; it just serves whatever static files are already in `docs/`. All real building (templating, markdown conversion, Sass compilation) happens locally via `bundle exec jekyll build` — pushing source changes without rebuilding first changes nothing on the live site.
- `_config.yml` has an `exclude:` list keeping non-content project files (`CLAUDE.md`, `package.json`, `package-lock.json`) and known scratch paths (`assets/computing.html`, `assets/computing.yml`, `assets/computing2.yml`, `assets/posts_temp/`) out of `docs/`. Jekyll copies whatever's physically on disk regardless of git tracking status, so a new WIP file dropped into a non-underscore directory (e.g. `assets/`) will get published into `docs/` on the next build unless it's also added to `exclude:` — `.gitignore` alone doesn't stop this.
- The repo (`braunm/braunm.github.io`) is public — required for free GitHub Pages hosting of a `<username>.github.io` site. Anything committed and pushed stays in public history indefinitely, even if later removed from HEAD. Nothing that's only ever uncommitted (working-tree changes never `git add`ed) is exposed.

# Repo structure decisions

- Considered splitting Jekyll source (private) from published output (public repo) — e.g. a nested git repo inside `docs/`, or an orphan `gh-pages` branch — so in-progress drafts could never reach the public repo at all. Decided (2026-08-21) to keep the current single-repo structure (source + `docs/` output, one repo, pushed as-is) since nothing in source is actually sensitive. Revisit only if that changes.
- Scratch/draft files intentionally left untracked at the repo root — `assets/computing.html`, `assets/computing.yml`, `assets/computing2.yml`, `assets/posts_temp/` — are WIP the user hasn't decided what to do with. Leave them alone unless asked.
- For low-risk housekeeping (config fixes, lockfiles, reverting accidental corruption), commit directly to `main` rather than a feature branch — this is a solo-maintained personal site, not a collaborative repo.

# Current needs
- Set up this directory so Claude can efficiently help me manage and modify the site on an ongoing basis.
- Get recommendations on how to improve the site.
- Create a plan on those recommendations.

# Rules
- Ask a lot of clarifying questions.  Do not assume anything.  You need to learn what my preferences are for this project.
- Default to plan mode.
- Don't build for deployment until a local version is accepted.
- Stay within the jekyll and bootstrap framework, because that is what I'm familiar with.
- Remember that I am not a professional web developer.  Simple is better than complex.
- I am not using Claude for new website content... yet.  Do not read all of my papers; it's not necessary.
