# AGENTS.md

Static personal portfolio site, served by host nginx at `/` on the VPS from `/srv/portfolio`.

- Plain HTML + CSS, no build step (open `index.html`, or `python3 -m http.server 8080`).
- Deployed by `git pull` inside `/srv/portfolio` on the VPS (no nginx reload needed).
- Serve-only static: use **relative** asset paths; do not use absolute `/...` paths, since the
  server also hosts other apps under other path prefixes.
- Infra and deploy config live in the `infra` repo (see its `docs/port-map.md` and ADRs).

## Server
- leonardof108.vps-kinghost.net (186.202.209.59), user `leonardo`, SSH key-only.
