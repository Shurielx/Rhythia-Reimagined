# Privacy Policy

Last updated: 2026-08-02

Rhythia Reimagined is an unofficial community browser extension for Rhythia.
It is maintained by Shurielx and is not affiliated with or endorsed by Capo
Games.

## Data the extension reads

The extension reads information already available on Rhythia pages, including
public profile identifiers and names, the country label shown on a profile,
profile statistics, score information, ranking information, visible map names,
and the current page state needed to enhance the interface. It does not use
device location to determine a user's country.

When the extension requests additional score data from the official Rhythia
API, it may send the requested public profile identifier and read the Rhythia
session value from the current Rhythia page in order to authenticate that
request. The session value is used only for the request and is not stored by
the extension, included in diagnostics, or sent to GitHub.

The session value is read at request time from the current Rhythia page's local
storage. The extension does not copy it into its own Chrome storage, persist it
as extension data, or log it. It is transmitted only as part of the request to
the official Rhythia API that requires it for authentication, and is not sent
to any other third party or external service.

## Permissions used

The extension requests the following Manifest V3 permissions because they are
needed for its user-facing features:

The extension requests only the minimum permissions necessary to provide its
features. It does not collect or process data for secondary purposes unrelated
to enhancing the Rhythia interface.

- `storage`: saves settings, profile history, Title Progression state, and
  compact local statistics in Chrome extension storage.
- `unlimitedStorage`: supports the extension's configurable local cache without
  relying on the browser's smaller default storage quota. The extension still
  applies its own cache size and profile limits.
- `activeTab`: lets the popup communicate with the currently active Rhythia
  profile tab when the user uses actions such as saving the current profile
  state.
- `offscreen`: provides a hidden extension document that writes a user-approved
  local backup file when stable local data changes. It does not provide access
  to unrelated websites or a cloud storage service.
- Host access for `rhythia.com`, `www.rhythia.com`, and
  `production.rhythia.com`: injects the disclosed interface features and loads
  the Rhythia data needed by those features. The extension does not request
  access to unrelated websites.

## Data stored locally

The extension stores settings and locally generated data in Chrome extension
storage. This can include public Rhythia profile identifiers and names, the
country label shown on a profile, selected themes, module settings, comparison
selections, profile history, Title Progression state, and compact score data
needed for local statistics and comparisons.

This data is stored locally in the user's browser. It is not sent to the
maintainer, GitHub, an analytics provider, or an advertising service.

The extension can also maintain an optional external local backup file after
the user chooses a folder through the browser's file access prompt. The default
backup interval is 3 days and users can choose an interval from 1 to 30 days or
disable backups. The backup may be placed in a folder such as
`Documents/Rhythia Reimagined/Backups`, but the exact location is selected by
the user and is not silently chosen by the extension.

The stable backup contains only closed daily history, the latest Title
Progression state, and stable collection settings. It does not contain
open-day snapshots, diagnostics, sessions, cookies, tokens, request bodies,
or authentication data. The extension updates the same file after the initial
folder permission when the browser continues to grant access. It does not
create recurring automatic Downloads or use `chrome.storage.sync`.

The backup file is outside Chrome extension storage and can therefore survive
an extension uninstall. It remains a local file controlled by the user. The
user can view it, download a copy, restore it through the validation and merge
preview, forget folder access, or delete it from the History & Data controls.
The extension cannot guarantee access if the file is moved, deleted, or if the
browser revokes the folder permission.

Profile statistics use a compact local cache. During the current calendar day,
the extension keeps an open state for a profile and updates it when the page is
refreshed. It does not create a permanent history record for every refresh.
When a later calendar day is first observed, the previous day is closed and at
most one closed statistics record is kept for that day. Ranking history uses
the last observed state of each closed day.

Title Progression is separate from daily statistics history. It keeps one
latest RP and Global rank state per profile so the next visit can show an
increase or decrease animation. It is replaced when a newer state is saved and
is not a list of hourly or daily snapshots.

The default retention period for closed daily profile history is 90 days.
Users can choose 30, 60, 90, or 180 days, or disable automatic age-based
cleanup. Current-day captures are also subject to snapshot and storage limits.
Title Progression keeps one latest local RP and Global Rank state per tracked
profile. It is replaced when a newer valid state is saved and is not removed
automatically by the age-based history setting.

The user can configure the full local cache size between 1 and 1024 MB; the
default is 300 MB. The open-day portion has a separate 25 MB default limit.
The extension also limits open-day captures per profile and uses rolling
cleanup rather than deleting the complete cache at once.
Whitelisted profiles are protected from automatic cleanup, although the user
can still delete them manually.

The extension provides controls to delete saved history and Title Progression
data. Automatic retention and size limits can also remove old local records.

## User rights and data control

All data created and stored by the extension, including settings, profile
history, and local caches, remains under the user's control in the browser. You
can change retention settings, remove individual profiles or records, clear
saved history and Title Progression data, delete the external backup file, or
remove all extension storage by uninstalling the extension from Chrome. An
extension uninstall removes Chrome extension storage, but it does not
necessarily remove a backup file that the user selected outside that storage.
These controls apply to local extension data and local backup files only; they
do not delete or change records held by Rhythia or Capo Games. Requests
concerning server-side data should be sent to Capo Games through official
Rhythia support channels.

## Data sharing and monetization

The extension does not sell, rent, trade, or otherwise monetize user data. It
does not share profile data, score data, ranking data, authentication data, or
local cache or local backup data with advertising networks, data brokers,
analytics providers, or the maintainer. It does not use this data for
personalized, retargeted, or interest-based advertising.

The only external service used for the extension's automatic network requests
is Rhythia and its official API endpoints. The extension sends only the
requests and authentication information needed to load the Rhythia data
requested by the user. This use is limited to providing the extension's
disclosed Rhythia interface features and follows the Chrome Web Store User
Data Policy, including the Limited Use requirements. Links that a user opens
manually are not used for analytics or data collection.

This policy describes the extension's own handling of data. The maintainer
does not operate Rhythia's servers or the official API and cannot confirm how
Rhythia or Capo Games independently retain, process, or monetize data on their
services. The extension does not administer, alter, or control records on
Rhythia's servers.

## Diagnostics

Debug Logging is disabled by default. When enabled, it writes redacted errors
and warnings to the browser developer console. Diagnostics do not intentionally
include sessions, cookies, request bodies, profile names, or full score
payloads. Backup permission failures and file errors are represented only by
short local status messages; raw backup contents are not sent to diagnostics.

## Local backup security

The local backup is a user-readable JSON file and should be treated as private
profile data. Anyone who can access the file can read the stored profile
history and Title Progression values. Do not attach a backup file to a public
issue or share it with support unless it has been reviewed and redacted.

Restore validates the file format, schema, profile identifiers, timestamps,
metrics, and forbidden sensitive field names before changing extension storage.
Restore uses a preview and merges newer local records rather than silently
replacing the complete local history.

## Feedback and issue reports

The Feedback link opens the extension's Chrome Web Store listing so a user can
leave a review. Report and suggestion links open GitHub Issues. The extension
does not automatically create GitHub issues and does not send local cache,
profile data, or authentication data to GitHub.

## Third-party services

The extension communicates with Rhythia and its official API endpoints to load
the data required by the extension. The terms, privacy practices, retention,
and monetization practices published by Capo Games are separate from this
project and are not controlled by the extension maintainer.

Questions, complaints, or requests about a Rhythia account, official API
processing, server-side records, authentication sessions, or how Capo Games
handles data should be directed to Capo Games through official Rhythia support
channels. The contact address below is only for the extension's own local data
handling and privacy questions.

Official provider references:

- [Capo Games](https://www.capo.games/)
- [Rhythia Terms and Privacy](https://github.com/Capo-Games/terms-privacy)
- Rhythia privacy contact: `support@rhythia.com`

GitHub is used only for public documentation, issue reports, and links shown in
the extension. The extension does not automatically send local cache, profile
data, or authentication data to GitHub. Any information a user voluntarily
includes in a public issue is handled under GitHub's own policies.

## Children's privacy

The extension is not directed to children under 13, and the maintainer does
not knowingly collect personal information from children under 13. If you
believe that a child has provided personal information through the extension,
please contact the maintainer so it can be addressed.

## Changes and contact

This policy may be updated when the extension's data handling changes. For
privacy questions, contact `shurieldev@gmail.com`. General questions and
feature reports may also be opened as public GitHub issues. Do not include
sessions, cookies, private messages, or other sensitive data in a public issue.
