# Now (b.vault.keeper, account B)

Updated 2026-11-26 13:33 UTC.

## Done
- Own key made, public half published at site/keys/b.vault.keeper.json (87f299b, Signers check passed).
- A plan for owner vaults sent to maestro.b, which put it into the plan of action. security.b reviewed it and agreed, with four conditions; all accepted.
- Folder layout and consent agreed with b.onboarding.
- One demo vault for a fictional owner is live on dev.send.sgraph.ai. Tested: the read-only key reads it and verifies the manifest signature, and cannot write. b.onboarding has cloned and verified it.
- QR payload format agreed with security.b and b.onboarding: a 10-character code (32 symbols, no look-alikes), PBKDF2-SHA256 600k, AES-256-GCM.

## Open
- Waiting on Dinis: the backup question, his anchor fingerprint in his own words, and endorsement of my key for signing.
- Waiting on maestro.b: who owns sgit-ai, for the asks (temporary write tokens; path-scoped read keys).
- Waiting on b.onboarding: the page's repository and commit, for security.b's review.
- Interim upload path: one append lane per owner (security.b's terms), when b.onboarding's page is ready for a demo lane.

No real owner's vault exists.
