> Layout update: the page now lives in `docs/` of the code repository `Jia1018/Freeze`; GitHub Pages serves it from branch `main`, folder `/docs`. The Code and Freeze Benchmark buttons point to the repository ("coming soon").

# Freeze project page

Static project page for *Camera and Scene Motion Interfere with Each Other in Video Representations*
(benchmark: Freeze; representations: CamBit and SceneBit). Built on the Nerfies template, same look as the CineGEN page.

## Contents

- `index.html`: the page (relative paths only; Bulma, Font Awesome, Academicons and Google Fonts from CDNs)
- `static/css/index.css`: styles (CineGEN stylesheet plus a "Freeze additions" block)
- `static/images/`: figures rendered from the paper PDFs (teaser, Freeze visualisation rows, method overview, four analysis figures)
- `static/videos/`: demo triplet / same-moment videos (mp4) and their poster frames (jpg)

Open `index.html` directly in a browser to preview; videos play when scrolled into view.

## Publish on GitHub Pages

1. Create a GitHub repository named `Freeze` under the account that should host the page.
2. Push the *contents* of this folder (index.html, static/, README.md) to the root of the `main` branch:
   ```
   git init && git add . && git commit -m "Project page"
   git branch -M main
   git remote add origin https://github.com/<account>/Freeze.git
   git push -u origin main
   ```
3. In the repository: Settings -> Pages -> Build and deployment -> Source: "Deploy from a branch",
   Branch: `main`, folder `/ (root)`. Save.
4. After a minute the page is live at `https://<account>.github.io/Freeze/`.

## TODO placeholders (all marked with `TODO` comments in index.html)

1. **Author block switch (decide before publishing).** The hero shows Variant A (named: Ziqi Zhou, Laura Sevilla-Lara,
   University of Edinburgh, as in the arXiv build). Variant B ("Anonymous authors") is commented out right below it.
   If the page goes public before the review period ends, switch to Variant B and also anonymise the BibTeX author line.
2. `TODO(author-links)`: optional homepage links around the author names.
3. `TODO(venue)`: the venue line currently reads "Under review".
4. `TODO(paper-link)`: Paper (PDF) button, `href="#"` and disabled.
5. `TODO(supp-link)`: Supplementary button, `href="#"` and disabled.
6. `TODO(code-link)`: Code button, `href="#"` and disabled.
7. `TODO(data-link)`: Freeze Benchmark button, `href="#"` and disabled.
   (For each button: set the `href` and delete the `disabled` attribute.)
8. `TODO(bibtex)`: citation key, venue (`booktitle`) and year are placeholders.

Also check before release: the teaser shows Something-Something v2 frames and the demo videos come from
Kubric renders and Cam×Time; confirm the dataset terms allow showing them on a public page.
