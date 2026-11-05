# rotematari.github.io

Personal academic website. Plain HTML and CSS, no build step.

| file | what it holds |
|---|---|
| `index.html` | all page content |
| `style.css` | layout and colors (light and dark tokens at the top) |
| `assets/neurreps2026/` | rollout video and video poster |
| `.nojekyll` | tells GitHub Pages to serve the files as they are |

## Preview locally

```bash
cd ~/Documents/phd/rotematari.github.io && python3 -m http.server 8931
```

Then open http://127.0.0.1:8931.

## Before publishing

Optional items are commented out in `index.html` ("Add when ready"):

- [ ] Google Scholar URL once the profile exists
- [ ] LinkedIn URL and CV PDF, if wanted
- [ ] camera-ready PDF at `assets/neurreps2026/paper.pdf` and a code link

## Publish on GitHub Pages

1. On GitHub, create a public repository named exactly `rotematari.github.io`.
2. Push this folder:

   ```bash
   cd ~/Documents/phd/rotematari.github.io
   git init -b main
   git add .
   git commit -m "Initial website"
   git remote add origin git@github.com:rotematari/rotematari.github.io.git
   git push -u origin main
   ```

3. In the repository, open Settings → Pages and set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. After a minute or two the site is live at https://rotematari.github.io. Put that URL in the Google Scholar Homepage field.

To update later: edit `index.html`, then `git commit -am "Update" && git push`.
