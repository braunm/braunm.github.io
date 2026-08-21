

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

- `_data/*.yml` files (e.g. `papers.yml`) are structured YAML, not prose. Auto-fill/fill-paragraph in Aquamacs has previously mangled an entry by hard-wrapping it into run-on lines, breaking the YAML structure while leaving the text content unchanged. Disable auto-fill when editing these files, and diff carefully before committing.

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
