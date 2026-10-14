# portfolio

Static personal portfolio site, served by nginx on the VPS as the site root (`/`).

- No build step — plain HTML + CSS.
- Deployed by cloning this repo to `/srv/portfolio` on the VPS and running `git pull`
  (see the `infra` repo for the nginx config).

## Develop

Just open `index.html` in a browser, or serve locally:

```sh
python3 -m http.server 8080
```

## Deploy

Managed centrally from the `infra` repo. On the VPS:

```sh
cd /srv/portfolio && git pull
# nginx reads files directly; no reload needed for content changes
```
