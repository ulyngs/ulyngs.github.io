# ulyngs.github.io

Legacy update endpoints for **Digital Habits: Blocker** (formerly ReDD Blocker).

The app's GitHub repo was renamed from `ulyngs/redd-block` to
`ulyngs/digital-habits-blocker`, then moved to
[`digitalhabits/dh-blocker`](https://github.com/digitalhabits/dh-blocker).
GitHub Pages URLs do not redirect after a rename or transfer, so
already-shipped clients would silently stop discovering new versions:

| Clients | Poll |
| --- | --- |
| v3.8.7 and earlier | `https://ulyngs.github.io/redd-block/latest-versions.json` |
| v3.8.8 – v3.8.11 | `https://ulyngs.github.io/digital-habits-blocker/latest-versions.json` |
| v3.9 and later | `https://digitalhabits.github.io/dh-blocker/latest-versions.json` (served by the main repo) |

This repo serves both old paths again, each with `latest-versions.json`
(update manifest) and `changelog.md` (release notes):

- [`redd-block/`](redd-block/)
- [`digital-habits-blocker/`](digital-habits-blocker/)

Both are mirrors of `docs/` in the main repo, kept in sync by the
[sync workflow](.github/workflows/sync-legacy-endpoints.yml) (every 6 hours and
on manual dispatch).

**Do not** create a repo named `ulyngs/redd-block` or
`ulyngs/digital-habits-blocker`: that would break GitHub's automatic redirect
for the old release-download URLs (`github.com/ulyngs/<old-name>/releases/download/...`)
that those same legacy clients use to fetch installers. Serving the Pages path from this user site
keeps both working.
