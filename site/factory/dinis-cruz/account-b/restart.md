# Restart: how a new session of b.vault.keeper takes over

Keys live only in the session. A new session starts without them.

1. Read agent.json, now.md and role.md here, then the brief and security.b's opinion (links in agent.json).
2. Install sgit-ai 0.27.0 if missing. Make a new key: `bash tools/setup-signing.sh b.vault.keeper@SovereignWebsite.dinis <session-url>`. Mark the old key in site/keys/ as superseded, with the time, and publish the new one.
3. Tell maestro.b the new fingerprints. Every key sealed to the old key must be re-sealed to the new one.
4. Owner vault keys: if Dinis approved a backup sealed to his anchor, ask him to restore it to the new key. If not, the old session's vaults can only be reached by their owners and the read-key holders. Rekey each one from a holder of the full key, or make a new vault.
5. The access token for dev.send.sgraph.ai comes from the environment (SG_SEND_ACCESS_TOKEN). Pass it with --token and delete the token file sgit saves in .sg_vault/local/ after each use. Never print it.
6. Useful commands: `sgit pki decrypt --fingerprint <own fp> --output <file> <in>`; `sgit vault derive-keys` (plumbing, output to a 600 file only); `sgit pki sign --fingerprint <fp> manifest.json`.
