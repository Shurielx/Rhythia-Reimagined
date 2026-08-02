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

The extension may also write a user-approved stable JSON backup to a local
folder outside Chrome extension storage. That file can contain profile IDs,
usernames, countries, closed daily statistics, ranking values, and Title
Progression state. Treat it as private user data. Do not upload it to GitHub,
attach it to an issue, or send it in an email without removing profile data
first.

Local extension storage and local backup files are not intended to be a secure
vault. Anyone with access to the browser profile or backup file may be able to
read the stored profile history.

If a backup restore reports an invalid file, keep the file private and report
only the error message, extension version, and reproduction steps. The restore
flow is intended to validate and merge local data; it is not a server upload or
a synchronization mechanism.
