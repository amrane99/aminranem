# Dr. Amin Ranem — Personal Website

A single-page professional website (pure HTML/CSS/JS, no build step).

## Structure

```
index.html                  — the entire site (styles and scripts inlined)
assets/images/profile.jpg   — profile photo
assets/Amin_Ranem_CV.pdf    — CV served by the "Download CV" buttons
                              (source: ~/Desktop/Amin_Ranem_CV.docx — re-export to
                              PDF and replace this file after editing)
```

## Preview locally

Just double-click `index.html`, or run:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to GitHub Pages (replace the current site)

The site currently lives at https://github.com/amrane99/aminranem and is served at
https://amrane99.github.io/aminranem/.

```bash
git clone https://github.com/amrane99/aminranem.git
cd aminranem
# remove the old template files
git rm -r assets contact.html resume.html index.txt index.html Folder.DotSettings
# copy in the new site
cp -R /path/to/amin-ranem-website/* .
git add .
git commit -m "Redesign personal website"
git push
```

GitHub Pages will update automatically within a minute or two.

## Updating content

Everything is in `index.html`:

- **Hero / title / intro** — the `<header>` block
- **AI4EVAR project** — the `<section id="ai4evar">` block
- **Experience & education** — the `<section id="experience">` block
- **Publications** — the `<section id="publications">` block (copy an existing
  `<div class="pub">…</div>` card to add a new paper; use `class="venue top"`
  for highlighted venues)
- **Talks & community** — the `<section id="talks">` block
- **Contact links** — the `<footer>` block
