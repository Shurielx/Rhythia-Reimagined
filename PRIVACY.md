# Privacy Policy

Last updated: 2026-08-02

Rhythia Reimagined is an unofficial community browser extension for Rhythia.
It is maintained by Shurielx and is not affiliated with or endorsed by Capo
Games.

## Data the extension reads

The extension reads information already available on Rhythia pages, including
profile statistics, score information, ranking information, visible map names,
and the current page state needed to enhance the interface.

When the extension requests additional score data from the official Rhythia
API, it may read the Rhythia session value from the current Rhythia page in
order to authenticate that request. The session value is used only for the
request and is not stored by the extension, included in diagnostics, or sent to
GitHub.

## Data stored locally

The extension stores settings and locally generated data in Chrome extension
storage. This can include selected themes, module settings, comparison lists,
profile history, Title Progression state, and compact score data needed for
local statistics and comparisons.

This data is stored locally in the user's browser. It is not sent to the
maintainer, GitHub, an analytics provider, or an advertising service.

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

The default retention period for closed statistics and Title Progression state
is 90 days. Users can choose 30, 60, 90, or 180 days, or disable automatic
age-based cleanup. The user can also configure the local cache size between 1
and 100 MB; the default is 50 MB. The cache normally tracks up to 100 unique
profiles across statistics and Title Progression together. Whitelisted
profiles are protected from automatic cleanup, although the user can still
delete them manually.

The extension provides controls to delete saved history and Title Progression
data. Automatic retention and size limits can also remove old local records.

## Diagnostics

Debug Logging is disabled by default. When enabled, it writes redacted errors
and warnings to the browser developer console. Diagnostics do not intentionally
include sessions, cookies, request bodies, profile names, or full score
payloads.

## Feedback and issue reports

The Feedback link opens the extension's Chrome Web Store listing so a user can
leave a review. Report and suggestion links open GitHub Issues. The extension
does not automatically create GitHub issues and does not send local cache,
profile data, or authentication data to GitHub.

## Third-party services

The extension communicates with Rhythia and its official API endpoints to load
the data required by the extension. Rhythia and Capo Games have their own
terms and privacy practices, which are separate from this project.

## Changes and contact

This policy may be updated when the extension's data handling changes. For
questions, open a public issue or contact the maintainer through GitHub.
