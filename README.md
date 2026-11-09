# Piso WiFi releases

Signed update files for Piso WiFi vendos. There is no source code here.

Vendos check `channels/stable.json` once a day and on startup. A vendo
installs an update only if:

- the manifest's signature matches the release key built into the vendo
  (Ed25519);
- every file's SHA-256 matches the manifest;
- the version is newer than the one already running.

Anything else is refused. Copying, editing or re-hosting these files can't
get a vendo to run something its owner didn't sign. If a new version doesn't
start properly, the vendo switches back to the previous one by itself.

This repo is written only by the release workflow.
