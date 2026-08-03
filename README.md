# Rhythia: Reimagined

Rhythia: Reimagined is a browser extension that adds a clearer and more useful
way to explore Rhythia profiles, scores, progression, and performance data.

The extension also includes a community-maintained catalog of Streamslop maps.
Streamslops are tagged manually for now because the Rhythia API does not expose
a Streamslop tag yet.

## Status

The current public release is `1.0.0` (`v1.0 - Initial Release`). The core
functionality is working as intended and the extension is ready for regular use.
Future updates will continue to improve polish, usability, visual consistency,
and edge-case handling.

## What It Provides

- Enhanced profile and score views
- Performance statistics and score filters
- Progression and rank tracking
- Local history and storage management
- Optional local automatic, manual, and recovery backups
- Profile and score comparison tools
- Streamslop catalog integration

## This Repository

This is the public companion repository for Rhythia: Reimagined. It contains:

- The public Streamslop catalog
- User-facing documentation
- Privacy and security policies
- Issue templates for bug reports and feature requests

The browser extension source code, private developer tooling, credentials, and
user data are not included in this repository.

## Privacy & Data Handling

The extension stores public Rhythia profile identifiers and names, the country
label shown on a profile, settings, profile history, Title Progression state,
and compact statistics locally in Chrome extension storage. It does not send
local cache data to the maintainer, GitHub, analytics providers, or advertising
services, and it does not include a telemetry or analytics system. The
extension communicates with the official Rhythia API only when needed to load
data for its user-facing features. Server-side Rhythia and Capo Games data
practices are governed by their own policies.

The extension also supports optional local backups. After the user chooses a
folder, it can write rolling Automatic copies plus on-demand Manual and
short-lived Recovery copies under `Rhythia Reimagined/Backups/`. Automatic
backups default to once per day, keep one to five generations, and exclude
current open-day snapshots. Manual backups may include the open day and app
settings when the user selects those options. A full Recovery point is created
before restore operations and expires after three days.

The backup files are never uploaded, synchronized through Google, or sent to
the maintainer. The folder permission is held in browser IndexedDB, while the
backup contents remain in the user-selected local folder. Users can inspect
current and previous automatic copies, open a manual backup as a read-only
archive, restore selected data with Merge or Replace, reconnect or forget the
folder permission, and delete local backup files from the History & Data
controls. Files from the old backup layout are not imported or recognized; only
the new `rhythia-reimagined-*` backup files are supported.

The extension also runs schema migrations offline at startup. It validates
existing records before applying one-version-at-a-time migrations and uses a
lock so concurrent extension contexts do not migrate the same storage at once.
If a migration fails, existing records are not replaced by partial results;
storage becomes read-only until a validated restore repairs it, and automatic
backups are paused. A normal update or first run does not perform a destructive
reset of existing history or settings.

## Credits

Rhythia is created by [Capo Games](https://capo.games). This is an unofficial community project and is not affiliated with or endorsed by Capo Games.

Rhythia Reimagined is maintained by [Shurielx](https://github.com/Shurielx).

## Source Code and Attribution

The extension source code is maintained separately from this public companion
repository. Original Rhythia: Reimagined code may be copied, modified, and
redistributed under the terms of [`LICENSE.md`](LICENSE.md).

Any public use, redistribution, or derivative work containing the original
project code must include a clear and visible attribution to Shuriel. The
attribution requirement is satisfied by any of the following:

- `Shuriel` with a hyperlink to [the GitHub profile](https://github.com/Shurielx);
- `Shuriel` displayed alongside a hyperlink to [the GitHub profile](https://github.com/Shurielx);
- a direct hyperlink to [the GitHub profile](https://github.com/Shurielx).

The attribution must be reasonably easy to find in a Credits, About,
Attribution, README, documentation, project, or release page. It must not be
hidden only in source comments, metadata, or an otherwise inaccessible legal
notice. No specific wording beyond one of the forms above is required.

This repository's license does not grant rights to Rhythia.com's code, content,
data, design, trademarks, or other materials belonging to Capo Games. The
community Streamslop catalog and any third-party materials remain subject to
their applicable rights and licenses.

## Support

- [Report a bug](https://github.com/Shurielx/Rhythia-Reimagined/issues/new?template=bug_report.md)
- [Suggest an improvement](https://github.com/Shurielx/Rhythia-Reimagined/issues/new?template=feature_request.md)
- [Privacy policy](PRIVACY.md)
- [Security policy](SECURITY.md)
