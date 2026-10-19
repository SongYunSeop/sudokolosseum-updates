# Sudoku Colosseum updates

Public distribution metadata and encrypted web bundles for Sudoku Colosseum.
Application source and signing private keys are maintained separately.

- Metadata: `https://sudokolosseum-updates.vercel.app/<platform>/<native-version>/<native-build>.json`
- `null` or a missing manifest means no update is offered.
- Files in `public/bundles` are signed/encrypted with the application's Capgo v2 key.
- No source maps, credentials, user data, or native app binaries belong here.
- Production manifests and the retired iOS smoke profile (`ios/0.0.0/1.json`) return `null`.
- Synthetic smoke metadata and bundles were removed from the active deployment after iOS rollback verification on 2026-10-16. They remain recoverable in Git history; never publish them as application updates.
- Vercel serves only `public/`. Deployment is manual; a Git push alone does not activate an update.

Bundled JavaScript remains inspectable by installed clients; encryption verifies origin and integrity, not permanent source secrecy.

On 2026-10-19, encrypted production-backend candidate `1.1.2-ota.c9a2505bcf08` and recovery `1.1.2-ota.ebc1f8aec257` were added for physical-device verification. Verification metadata is isolated under `/verification/2026-10-19/`; active application manifests remain `null`. These files do not constitute approval to advertise an OTA update.
