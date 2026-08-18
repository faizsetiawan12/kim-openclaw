# Security Policy

Treat tokens, API keys, chat identifiers, configuration, memory, sessions,
backups, and logs as private.

If a credential is exposed, revoke or rotate it at its provider, update the
local installation, verify the service, and remove the exposed value from any
future commits. Do not report credentials in issues, pull requests, or chat.

Before pushing, review `git status`, inspect the staged diff, and scan for
secret-shaped values and private filesystem paths.
