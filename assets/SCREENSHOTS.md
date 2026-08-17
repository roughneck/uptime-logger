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
- **Theme: either, and it matters less than this file first claimed.** The reasoning here
  used to be "light is the safer default on a white page" — but the page has a dark mode of
  its own, so it is not always a white page, and no single choice is right for every visitor.
  The shipped pair is deliberately mixed: dark on the English page, light on the German one.
  Both show the theme selector, so it reads as a feature rather than an accident.

  The proper fix, if it ever seems worth two more screenshots: one of each theme per language
  and a `<picture>` with `media="(prefers-color-scheme: dark)"`, so the screenshot always
  matches the page around it.
- **With real data.** A heatmap with a few coloured days and a log with a handful of entries
  says more than an empty one.
- **Browser chrome**: either a clean window with no bookmarks bar, or cropped away entirely.
  Both look fine, mixed does not.

## Before handing them over

Check what is visible: the log shows **Wi-Fi network names** and interface names, and the
address bar shows the port. Crop or blur anything you would not want on a public page.

## Done

Both files were taken on 17 August 2026 and are in place; `assets/placeholder.svg` is gone.
This file stays as the recipe for the next pair — a screenshot ages with every visible
change, and these already show a dashboard from before whatever comes after 0.1.0.
