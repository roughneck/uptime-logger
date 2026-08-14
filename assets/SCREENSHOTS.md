# Screenshots the page needs

Two files, one per language, because the dashboard is bilingual and the German page should
not show an English screenshot:

| File | Language | Used on |
|---|---|---|
| `assets/dashboard-en.png` | English | `index.html` |
| `assets/dashboard-de.png` | German | `de/index.html` |

## How to take them

- **Browser window about 1400 px wide**, so the heatmap shows a full year without scrolling.
  Take it on a Retina display if possible — the page scales the image down, and a 2× shot
  stays sharp.
- **Show the whole dashboard in one shot**: status, the figures block, the heatmap and the
  first rows of the log. Scroll so that no section is cut off in the middle.
- **Light mode.** The page adapts to the visitor's theme, the screenshot cannot; light is the
  safer default on a white page.
- **With real data.** A heatmap with a few coloured days and a log with a handful of entries
  says more than an empty one.
- **Browser chrome**: either a clean window with no bookmarks bar, or cropped away entirely.
  Both look fine, mixed does not.

## Before handing them over

Check what is visible: the log shows **Wi-Fi network names** and interface names, and the
address bar shows the port. Crop or blur anything you would not want on a public page.

## Putting them in

Drop both files in `assets/` and change one line per page — `assets/placeholder.svg` becomes
`assets/dashboard-en.png` in `index.html`, `../assets/placeholder.svg` becomes
`../assets/dashboard-de.png` in `de/index.html`. Then `assets/placeholder.svg` can go.
