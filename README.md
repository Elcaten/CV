# CV (RenderCV + GitHub Pages)

This repo publishes my resume on GitHub Pages.

## Outputs (stable direct links)

- `Andrei_Lineishchikov_CV.pdf`
- `Andrei_Lineishchikov_CV.html`

They are deployed at the root of the Pages site, so the URLs are:

- `https://elcaten.github.io/<repo>/Andrei_Lineishchikov_CV.pdf`
- `https://elcaten.github.io/<repo>/Andrei_Lineishchikov_CV.html`

## Local build (Docker)

```bash
mkdir -p dist
docker run --rm -v "$PWD":/work -w /work ghcr.io/rendercv/rendercv \
  render Andrei_Lineishchikov_CV.yaml \
  --pdf-path dist/Andrei_Lineishchikov_CV.pdf \
  --html-path dist/Andrei_Lineishchikov_CV.html \
  --output-folder dist
rm -f dist/*.md dist/*.typ dist/*_*.png
```

Open `dist/Andrei_Lineishchikov_CV.html` in your browser.

