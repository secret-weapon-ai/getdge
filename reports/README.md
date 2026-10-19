# Reports

Reports live under `/reports/<dealer>/…` and are not linked from the home page.

Each audit report lives at:

```
reports/<client-slug>/<yyyy-mm-dd>/index.html
```

- `<client-slug>` is a lowercase, URL-safe identifier for the dealership.
- `<yyyy-mm-dd>` is the date of the audit.

The report itself is a self-contained `index.html` in that folder. After adding it, link the folder from the report list on the root `index.html` so it appears on the landing page.

```html
<li><a href="reports/<client-slug>/<yyyy-mm-dd>/">Dealership name <span class="date">YYYY-MM-DD</span></a></li>
```

Remove the “No reports published yet.” paragraph on the landing page when the first link is added.
