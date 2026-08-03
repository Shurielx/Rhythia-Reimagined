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

The extension may also write user-approved Automatic, Manual, and Recovery JSON
backups to a local folder outside Chrome extension storage. These files can
contain profile IDs, usernames, countries, closed daily statistics, ranking
values, Title Progression state, open-day captures, or app settings depending
on the backup type and options selected. Treat every backup as private user
data. Do not upload it to GitHub, attach it to an issue, or send it in an email
without removing profile data first.

Local extension storage and local backup files are not intended to be a secure
vault. Anyone with access to the browser profile or backup file may be able to
read the stored profile history.

If a backup restore reports an invalid file, keep the file private and report
only the error message, extension version, and reproduction steps. The restore
flow validates data locally and supports a scoped Merge or Replace operation;
it is not a server upload or a synchronization mechanism. A full Recovery copy
is created before a restore or other potentially destructive data operation.

The extension performs schema migrations locally and offline. A failed
migration leaves the previous records untouched, pauses automatic backups, and
puts storage into a read-only repair-required state. A validated local restore
can repair that state. This protection does not replace normal backups and does
not protect against physical disk failure or operating-system crashes.
