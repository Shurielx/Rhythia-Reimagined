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

## Permissions used

The extension requests the following Manifest V3 permissions because they are
needed for its user-facing features:

- `storage`: saves settings, profile history, Title Progression state, and
  compact local statistics in Chrome extension storage.
- `unlimitedStorage`: supports the extension's configurable local cache without
  relying on the browser's smaller default storage quota. The extension still
  applies its own cache size and profile limits.
- `activeTab`: lets the popup communicate with the currently active Rhythia
  profile tab when the user uses actions such as saving the current profile
  state.
- Host access for `rhythia.com`, `www.rhythia.com`, and
  `production.rhythia.com`: injects the disclosed interface features and loads
  the Rhythia data needed by those features. The extension does not request
  access to unrelated websites.

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

## Data sharing and monetization

The extension does not sell, rent, trade, or otherwise monetize user data. It
does not share profile data, score data, ranking data, authentication data, or
local cache data with advertising networks, data brokers, analytics providers,
or the maintainer. It does not use this data for personalized, retargeted, or
interest-based advertising.

The only external service the extension communicates with for extension
functionality is Rhythia and its official API endpoints. The extension sends
only the requests and authentication information needed to load the Rhythia
data requested by the user. This use is limited to providing the extension's
disclosed Rhythia interface features and follows the Chrome Web Store User
Data Policy, including the Limited Use requirements.

This policy describes the extension's own handling of data. The maintainer
does not operate Rhythia's servers or the official API and cannot confirm how
Rhythia or Capo Games independently retain, process, or monetize data on their
services. The extension does not administer, alter, or control records on
Rhythia's servers.

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
