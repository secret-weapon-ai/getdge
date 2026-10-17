# getdge

Static site for dealership AI-readiness audit reports. Each report is the “do you show up in AI prompts?” test for a car dealership: whether the store appears when people ask AI assistants for a recommendation.

GitHub Pages serves this repository from the root of `main` at the custom domain `grow.getdge.co`. There is no build step. The landing page sends a `noindex` robots tag until the site is meant to be public.

## Publish a report

1. Add the report at `reports/<client-slug>/<yyyy-mm-dd>/index.html`.
   - `<client-slug>` is a lowercase, URL-safe name for the dealership.
   - `<yyyy-mm-dd>` is the audit date.
2. Link that path from the report list in the root `index.html`. Remove the “No reports published yet.” line once the first link is in place.
3. Commit to `main` and push. Pages publishes the files in the repository as they are.

See `reports/README.md` for the folder layout.

## Layout

- `index.html` — landing page and the list of report links
- `CNAME` — custom domain `grow.getdge.co`
- `.nojekyll` — serve files as-is, without Jekyll
- `reports/<client-slug>/<yyyy-mm-dd>/index.html` — one audit report
