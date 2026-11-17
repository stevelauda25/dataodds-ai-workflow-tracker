# DataOdds AI workflow tracker

One page that shows how much of the DataOdds AI workflow is live, partly live or planned, grouped by area, with the open questions at the bottom.

## Update the tracker

Everything on the page comes from [`tracker.md`](tracker.md). Edit that file and commit; the page shows the change on its next load. The counts at the top are computed from the rows, so there is nothing else to keep in sync.

- **Change a status:** edit the `Status` cell of the item's row. It must be `Live`, `Partly live` or `Planned`. Any other value shows up on the page as a red warning and is left out of the counts.
- **Change a note:** edit the `Notes` cell.
- **Add an item:** add one row to the area's table: `| Item | Status | Notes |`.
- **Add an area:** add a `## Area name` heading followed by a table with the same `| Item | Status | Notes |` header.
- **Open questions:** add or remove rows in the `## Open questions` table: `| Question | Who |`.

Text between backticks renders as code. To use a `|` inside a cell, write `\|`.

## How it works

`index.html` fetches `tracker.md` in the browser and renders it. There is no build step, login or database; any static host can serve the two files. `.nojekyll` stops GitHub Pages from converting `tracker.md` into an HTML page.

To preview locally, serve this folder (for example `python3 -m http.server`) and open the printed address. Opening `index.html` straight from disk does not work, because browsers block the page from reading `tracker.md` that way.
