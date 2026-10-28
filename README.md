# Budget 2026 Live

A live, plain-English tracker for the UK Autumn Budget 2026.
Live at https://mannixadev.github.io/Budget2026/

## Posting an update

Everything on the page comes from `updates.json`. Open readers' browsers re-check it every 60 seconds.

1. On GitHub, open `updates.json`, click the pencil icon, then make your edit.
2. Commit. GitHub Pages republishes in about a minute.

**Add a live update.** Put this at the top of `"updates"` (times are UTC, which is the same as UK time until March):

```json
{ "time": "2026-10-28T12:45:00Z", "title": "Headline", "body": "One or two plain sentences.", "tag": "Breaking", "measure": "optional-measure-id" },
```

**Add or change a measure.** Use `"status"`, which is `confirmed`, `expected` or `dropped`. `"who"` can include `everyone`, `renter`, `homeowner`, `landlord`, `saver`, `pensioner`, `worker`, `parent`, `driver` and `business`.

**Change the header.** Set `meta.status` to `"live"` when the speech starts and to `"post"` when it ends, then update `meta.lastUpdated`.

**Mark the latest items as new.** Add `"new": true` to any update or measure from the latest push, and remove it from the items flagged last time. Those items get a red NEW tag on the page.
