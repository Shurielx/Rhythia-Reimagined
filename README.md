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
- Optional local stable backups for recovery and migration
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

The extension stores settings, profile history, Title Progression state, and
compact statistics locally in Chrome extension storage. It does not send local
cache data to the maintainer, GitHub, analytics providers, or advertising
services, and it does not include a telemetry or analytics system. The
extension communicates with the official Rhythia API only when needed to load
data for its user-facing features. Server-side Rhythia and Capo Games data
practices are governed by their own policies.

The extension also supports an optional local stable backup. After the user
chooses a folder once, the extension can update the same JSON backup file on
the user's device. The backup contains closed daily history, Title Progression
state, and stable collection settings. It excludes open-day snapshots,
diagnostics, sessions, cookies, tokens, request bodies, and authentication
data. The backup is never uploaded, synchronized through Google, or sent to
the maintainer. A user can inspect, download a copy, restore, disconnect, or
delete the backup from the extension's History & Data controls.

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
