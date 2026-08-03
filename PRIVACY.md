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
- `alarms`: running optional local backup checks; this permission does not send
  data to an external service.
- HTTPS host access for `rhythia.com`, `www.rhythia.com`, and
  `production.rhythia.com`: injecting the disclosed interface features and
  loading the Rhythia data required by them.

The extension does not request access to unrelated websites.

## Service dependency and account terms

Features that load Rhythia data depend on the availability, structure, and
access rules of Rhythia pages and the official Rhythia API. Capo Games may
change, restrict, or discontinue those services, so the maintainer does not
guarantee uninterrupted availability or compatibility with future changes.

The extension is an unofficial community tool and does not change the terms
that apply to a Rhythia account. Users are responsible for deciding whether
their use complies with those terms. The maintainer does not control account
reviews, restrictions, suspensions, or other actions taken by Capo Games and is
not responsible for those decisions, except where applicable law provides
otherwise.

## Where data is stored

The extension's settings, profile history, Title Progression state, and local
statistics remain in the user's browser. Temporary comparison information is
used only while the comparison is open or during the current browser session.
Some interface preferences may be saved locally on the Rhythia page; they do
not contain authentication data. Access to a user-selected backup folder is
also remembered locally so the user does not have to grant it every time.

Local extension data is not sent to the maintainer, GitHub, analytics
providers, advertisers, or data brokers. The extension does not sell or
monetize this data.

## Local backup

Local backup is optional and disabled by default. If the user grants access to
a selected folder, the extension can save copies of local profile history,
statistics, progression data, and selected settings there. The backup feature
does not upload, synchronize, or share those files with the maintainer or any
analytics service.

Backups can contain personal or otherwise sensitive profile information. Anyone
who can access the selected folder or the browser profile may be able to read
them. Users are responsible for choosing a suitable location, protecting their
device and files, and deleting backups they no longer need. Uninstalling the
extension does not necessarily remove files saved outside Chrome storage.

The extension provides local restore and data recovery tools. These tools are
intended to reduce the risk of accidental loss, but they are not a guarantee
against corruption, software errors, device failure, or an operating-system
problem. A damaged local data state may require a complete restore before the
extension can safely resume normal operation.

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
