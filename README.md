# ulyngs.github.io

Legacy update endpoints for **Digital Habits: Blocker** (formerly ReDD Blocker).

The app's GitHub repo was renamed from `ulyngs/redd-block` to
[`ulyngs/digital-habits-blocker`](https://github.com/ulyngs/digital-habits-blocker).
GitHub Pages URLs do not redirect after a repo rename, so already-shipped
clients (v3.8.7 and earlier) that check
`https://ulyngs.github.io/redd-block/latest-versions.json` for updates would
silently stop discovering new versions.

This repo serves that old path again:

- [`redd-block/latest-versions.json`](redd-block/latest-versions.json) — update manifest
- [`redd-block/changelog.md`](redd-block/changelog.md) — release notes

Both are mirrors of `docs/` in the main repo, kept in sync by the
[sync workflow](.github/workflows/sync-legacy-endpoints.yml) (every 6 hours and
on manual dispatch).

**Do not** create a repo named `ulyngs/redd-block`: that would break GitHub's
automatic redirect for the old release-download URLs
(`github.com/ulyngs/redd-block/releases/download/...`) that those same legacy
clients use to fetch installers. Serving the Pages path from this user site
keeps both working.
