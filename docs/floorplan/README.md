# Source Floorplan

Open [the offline map](index.html) after downloading it. GitHub may show HTML source rather than execute it. Use **Start here**, **Flows**, search and the details-panel toggle to read the architecture. On narrow screens the fit-to-view overview can be small; readable details/tour prose is the preferred path.

A terminal batch script reads a roster, balances experience across three teams and writes a practice letter per player. No web server or HTTP routes.

## Source boundary

The input CSV is deliberately outside the admitted snapshot. Allocation balances counts within experience cohorts, not player height. No app execution or generated letters were inspected.

Pinned original source: `d1a57e5233b178b6ed442a2d951b4da15c8dff27`. Original project licensing is unchanged. See [notices](NOTICE.md), [omissions](source-census.json), [authoring](architecture.json) and [integrity pins](source-manifest.json). This is source documentation, not application execution, secure deployment approval or automatic refresh.

## Check without running the application

```sh
python3 docs/floorplan/check_freshness.py
python3 -B -m unittest discover -s docs/floorplan/tests -v
python3 -B -O -m unittest discover -s docs/floorplan/tests -v
```

The checker compares original source/config/static/input-file hashes and file membership, and all reviewed map artifacts. It does not regenerate on drift. Tests create disposable copies, never import the application, and require only Python standard library and Git. Regeneration requires a separately qualified renderer and reviewed authoring; its runtime is not bundled here.
