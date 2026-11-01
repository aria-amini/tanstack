---
'@aamini/config': patch
---

Write the workspace app port into the `[daemons.dev]` table of
`pitchfork.local.toml`. It was appended to the end of the file, so in apps
whose `pitchfork.toml` lists another daemon after `dev`, the port landed in that
daemon's table and the dev server stayed on the shared default port.
