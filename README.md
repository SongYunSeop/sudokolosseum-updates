# Sudoku Colosseum updates

Public distribution metadata and encrypted web bundles for Sudoku Colosseum.
Application source and signing private keys are maintained separately.

- Metadata: `https://songyunseop.github.io/sudokolosseum-updates/<platform>/<native-version>/<native-build>.json`
- `null` or a missing manifest means no update is offered.
- Release assets are signed/encrypted with the application's Capgo v2 key.
- No source maps, credentials, user data, or native app binaries belong here.
- `smoke-*` releases are synthetic verification fixtures, never production updates.

Bundled JavaScript remains inspectable by installed clients; encryption verifies origin and integrity, not permanent source secrecy.
