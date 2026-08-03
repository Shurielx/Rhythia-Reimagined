# Privacy Policy

Last updated: 2026-08-03

Rhythia Reimagined is an unofficial community browser extension for Rhythia.
It is maintained by Shurielx and is not affiliated with or endorsed by Capo
Games.

This policy describes the extension's own data handling. Rhythia and Capo Games
operate their own services and policies.

## What the extension reads

The extension reads information already shown on Rhythia pages, such as public
player identifiers, names, country labels, profile statistics, ranking values,
score information, visible map names, and the page state needed to enhance the
interface. It does not use device location to determine a country.

When the official Rhythia API requires it, the extension reads the current
Rhythia session value from the page's local storage and sends it only with the
requested API call to `production.rhythia.com`. The session value is not copied
to extension storage, backup files, diagnostics, GitHub, or the maintainer.
The extension does not use `chrome.cookies` or read browser cookies directly.

## Permissions and host access

The production extension uses the following Manifest V3 permissions:

- `storage`: local settings, profile history, Title Progression state, and
  compact statistics.
- `unlimitedStorage`: the configurable local history cache.
- `activeTab`: communication with the active Rhythia tab for user-triggered
  popup actions.
- `offscreen`: writing a user-approved local backup file.
- HTTPS host access for `rhythia.com`, `www.rhythia.com`, and
  `production.rhythia.com`: injecting the disclosed interface features and
  loading the Rhythia data required by them.

The extension does not request access to unrelated websites.

## Where data is stored

The extension's main settings, profile history, Title Progression state, and
compact local statistics are stored in Chrome extension storage. The temporary
Player Compare selection is stored only in session storage so it can survive
navigation between profiles during the current browser session. Fetched
comparison statistics are kept in memory while the comparison is open and are
not saved as comparison data.

A small interface preference, such as the selected scores view, may be stored
in the Rhythia page's local storage. It does not contain authentication data.
The backup folder handle is kept in local browser IndexedDB; the backup content
itself is kept in the user-selected local file.

Local extension data is not sent to the maintainer, GitHub, analytics
providers, advertisers, or data brokers. The extension does not sell or
monetize this data.

## Local backup

Local backup is optional and disabled by default. After the user chooses a
folder through the browser permission prompt, the extension can write local JSON
files to:

```text
Rhythia Reimagined/
  Backups/
    Automatic/
    Manual/
    Recovery/
```

Automatic backups use a rolling set of one to five copies. The default schedule
is once per day; the available schedules are once per day, once every three
days, once every seven days, or manual only. Automatic backups contain closed
daily history, the latest Title Progression state, and stable collection
settings. They do not contain current `openDay` captures, diagnostics,
sessions, cookies, tokens, request bodies, or other authentication data.

Manual backups are created on request and can optionally include the current
`openDay` and application settings. Recovery backups contain the full current
local state, including `openDay` and application settings. A recovery backup is
created before a restore or other operation that may change data, and recovery
files expire after three days. Automatic, Manual, and Recovery files are shown
and sized separately as well as together in the popup.

Files from the old backup layout are not imported or recognized. Only the new
`rhythia-reimagined-*` backup files are supported.

The backup folder handle is stored as a browser permission in local IndexedDB,
not in the JSON backup. A normal update of the same Chrome extension should
preserve that permission. After uninstalling and reinstalling, the user may
need to choose the folder again. Backup files are outside Chrome extension
storage and can survive an uninstall. Forgetting folder access does not delete
the files; deleting them is a separate user action. Anyone with access to the
selected folder can read the JSON, so treat all backup types as private profile
data.

Restore validates the JSON type, schema, export and backup versions, profile
identifiers, timestamps, metrics, and forbidden sensitive fields before any
write. It shows a preview and supports selecting profiles, a date range,
history, Title Progression, and application settings. The user can choose
`Merge`, which keeps newer local data, or `Replace`, which replaces the selected
scope. A backup can also be opened as a read-only archive without changing
local data.

The extension includes an offline data migration runner. At startup it reads
the schema version from `chrome.storage.local`, takes a migration lock, validates
records, and applies one-version-at-a-time migrations locally. Migrations do
not call the Rhythia API or send data to the internet. If validation or a
migration fails, the old records are left untouched, automatic backups are
paused, and storage enters a read-only repair-required state. A validated
external restore can mark the storage repaired. This does not protect against
physical disk failure or an operating-system crash. A normal update or first
run does not perform a destructive reset of existing history or settings.

## Retention and deletion

Closed daily history is kept for 90 days by default. Users can choose 30, 60,
90, or 180 days, or disable automatic age-based cleanup. Size limits and
rolling cleanup also apply. Users can delete selected profiles, history,
Title Progression data, settings, and the local backup file from the extension.

Uninstalling the extension removes its Chrome extension storage, but does not
automatically delete a backup file selected outside that storage. These local
controls do not delete or change records held by Rhythia or Capo Games.

## Network, diagnostics, and reports

The only automatic external network service used by the production extension
is Rhythia and its official API endpoints. The extension does not automatically
send data to GitHub, analytics, advertising, or other external services.

Debug logging is disabled by default. When enabled, it writes short local
errors and warnings to the browser developer console. Production diagnostics
are intended to exclude sessions, cookies, request bodies, profile names, and
full score payloads. The private Main Dev build contains developer-only local
instrumentation; the production build removes it.

Users may report issues or privacy questions through GitHub Issues or by email
at `shurieldev@gmail.com`. The extension does not create GitHub issues
automatically. Anything a user voluntarily includes in a public issue is
handled by GitHub under GitHub's policies; do not include sessions, cookies,
private messages, or unredacted backup files.

## Third-party services

Rhythia and Capo Games independently control their own server-side processing,
retention, terms, and privacy practices. Questions about a Rhythia account,
official server records, or the Rhythia API should be directed to the official
Rhythia support channels.

References:

- [Capo Games](https://www.capo.games/)
- [Rhythia Terms and Privacy](https://github.com/Capo-Games/terms-privacy)
- Rhythia privacy contact: `support@rhythia.com`

## Children's privacy

The extension is not directed to children. The maintainer does not knowingly
collect personal information through the extension. If you believe sensitive
information was submitted through GitHub or email, contact the maintainer so
it can be addressed.

## Changes

This policy may be updated when the extension's data handling changes. The
latest version is published in this repository.
