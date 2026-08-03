# Security Policy

Please do not include authentication sessions, cookies, private messages,
local backup files, profile exports, or other sensitive data in a public issue.

For a suspected security problem, email `shurieldev@gmail.com` before opening
a public issue. Include a short description, affected version, reproduction
steps, and the minimum information needed to verify the report. GitHub does
not provide a general private direct-message channel between user profiles, so
do not rely on a GitHub profile for confidential reports.

This public repository contains the community Streamslop catalog, user-facing
documentation, issue templates, and policy files for Rhythia: Reimagined. It
does not contain extension source code, build scripts, credentials, private
developer tooling, or user data. This is a statement about repository
contents, not a claim that the maintainer receives or stores user data. The
installed extension may process limited Rhythia page data locally in the user's
browser as described in `PRIVACY.md`.

The extension may also write user-approved backups to a local folder outside
Chrome extension storage. These files can contain profile information, history,
statistics, progression data, and settings. Treat every backup as private user
data. Do not upload it to GitHub, attach it to an issue, or send it in an email
without removing sensitive information first.

Local extension storage and local backup files are not intended to be a secure
vault. Anyone with access to the browser profile or backup file may be able to
read the stored profile history.

If a backup restore reports an invalid file, keep the file private and report
only the error message, extension version, and reproduction steps. Restore and
recovery are local features, not server uploads or synchronization. They are
intended as safety measures, but they cannot guarantee recovery from every
form of corruption, data loss, device failure, or operating-system problem.

If the extension detects a problem with its local data, it may restrict changes
until the data is restored and checked. This reduces the risk of making a bad
state worse, but it does not replace normal backups or protect against every
possible failure.

## External service and account risks

Features that load Rhythia data depend on Rhythia pages and the official API.
Changes to their availability, structure, access rules, or terms may reduce or
break extension functionality. The maintainer does not control Capo Games'
services or its decisions about account reviews, restrictions, suspensions, or
other enforcement actions. Users should review the terms that apply to their
account before using the extension and should not assume that the extension is
approved or endorsed by Capo Games.
