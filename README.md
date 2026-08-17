# UptimeLogger — downloads

This repository exists to host the released binaries of
[UptimeLogger](https://uptimelogger.bartels.ug/), and nothing else. It is public because
release assets have to be downloadable without an account, and because the winget manifest
points at them.

- **Downloads:** see [Releases](https://github.com/roughneck/uptime-logger/releases).
  Every release lists the SHA256 sum of each artefact in its notes.
- **Website:** served by GitLab Pages from a private repository. It used to live here; the
  older commits in this history are that site.
- **Application source:** not published.

## Releasing a version

1. Build both artefacts in the application repository
   (`packaging/macos/build.sh`, `packaging\windows\build.ps1`).
2. Create the tag `v<version>` here and upload `UptimeLogger-<version>.dmg` and
   `UptimeLogger-<version>-setup.exe` as release assets, with their SHA256 sums in the
   release notes.
3. In the website repository, update the version and the download links in `index.html`
   and `de/index.html`.
4. Update `latest.json` there **last** — it is what tells existing installations that a new
   version exists, so it must not point at a release that is not fully published yet.
