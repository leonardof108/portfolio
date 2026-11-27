# portfolio

Personal site for [Leonardo Ferreira](https://github.com/leonardof108) — a static, no-build portfolio in HTML and CSS.

The page introduces Leonardo as a full-stack and backend developer in Porto Alegre, showcases six public projects, and lists a verified core stack plus contact links (GitHub, LinkedIn, and email).

## Develop

There is no build step. Open `index.html` in a browser, or serve the folder locally:

```sh
python3 -m http.server 8080
```

Use **relative** asset paths only. The site can be hosted at `/` alongside other apps under path prefixes, so absolute `/...` URLs would break those apps.

## Deploy

The site is served by host nginx from `/srv/portfolio` on the VPS (site root `/`). Deploy is managed from the private `infra` repo: on the VPS, pull this repository and nginx will serve the updated files with no reload.

```sh
cd /srv/portfolio && git pull
```

GitHub Pages is not enabled for this repository.
