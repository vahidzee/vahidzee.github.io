# vahidzee.github.io

Personal website for [vahidz.com](https://vahidz.com), generated from structured content with [Webifier](https://github.com/webifier/build).

The source of the site lives in `index.yml`, `content/`, and `assets/`. The generated static website is written to `webified/` and deployed through GitHub Pages.

This repository uses Webifier and the [Webifier GitHub Action](https://github.com/webifier/build#github-action) so changes made here can automatically rebuild and update the published GitHub Pages site at [vahidz.com](https://vahidz.com).

## Local Development

From this repository:

```bash
../build/.venv/bin/webify --index index.yml --output webified --baseurl ""
```

Then serve the generated site:

```bash
python -m http.server 4174 --directory webified
```

Open [http://127.0.0.1:4174](http://127.0.0.1:4174) to review the result.

## Repository Layout

- `index.yml`: site entry point and top-level page structure.
- `content/`: resume content, publications, bio, and page data.
- `assets/`: templates and site-specific static assets.
- `webified/`: generated static output.

## Publishing

Push changes to GitHub after rebuilding and reviewing the generated output. The [publishing workflow](.github/workflows/main.yml) runs Webifier through the Webifier action and publishes the generated static files to GitHub Pages.
