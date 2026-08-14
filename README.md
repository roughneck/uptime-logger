# UptimeLogger — website and releases

This repository is the public face of [UptimeLogger](https://uptimelogger.bartels.ug/): the
download page served by GitHub Pages, and the releases the page links to. **It does not
contain the application's source code**, which is not published.

## Layout

    index.html              landing page (English)
    install.html            installation guide (English)
    privacy.html            privacy notice (English, informational)
    imprint.html            imprint (English, informational)
    de/                     the same four pages in German — the legally binding versions
    latest.json             what the application's update check reads
    style.css               palette taken from the dashboard, so both look like one product
    assets/                 icon and screenshots
    CNAME                   uptimelogger.bartels.ug

## Releasing a version

1. Build both artefacts in the application repository
   (`packaging/macos/build.sh`, `packaging\windows\build.ps1`).
2. Create the tag `v<version>` here and upload `UptimeLogger-<version>.dmg` and
   `UptimeLogger-<version>-setup.exe` as release assets, with their SHA256 sums in the
   release notes.
3. Update the version and the download links in `index.html` and `de/index.html`.
4. Update `latest.json` **last** — it is what tells existing installations that a new version
   exists, so it must not point at a release that is not fully published yet.

## DNS

`uptimelogger.bartels.ug` is a CNAME to `roughneck.github.io`.
