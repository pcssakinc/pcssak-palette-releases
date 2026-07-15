# Quality and Safety

[한국어](QUALITY-AND-SAFETY.ko.md)

This document explains what PCSSAK currently does to reduce risk. It is evidence of process,
not a promise that the application has no defects.

## Local-first boundary

- Images, colors, palettes, validation, and export are processed on the device.
- There is no PCSSAK account, advertising, analytics, tracking, automatic crash upload, or
  PCSSAK user database in the public beta.
- Core color work remains available offline.
- The standalone beta connects to the official GitHub release only to check for and download
  signed updates. Update failure does not disable the color workflow.

## Bounded native input

The Rust boundary checks untrusted images before full processing:

- maximum file size: 40 MiB;
- maximum dimensions: 40 megapixels;
- decoder allocation ceiling: 256 MiB;
- analysis downsample: no more than 128 pixels on the longest edge;
- compiled formats: PNG, JPEG, WebP, GIF, and BMP.

Metadata is checked before full decode where possible. Transparent pixels are handled before
resizing to reduce dark-edge contamination, and fixed-seed CIELab k-means keeps extraction
reproducible for the same accepted bytes and build.

## Least privilege and output validation

The WebView receives narrow dialog, clipboard-write, updater, and restart permissions rather
than broad filesystem access. User-selected files are handled by specific Rust commands.

Free CSS output must use `.css`, stay below 1 MiB, contain the expected PCssak generator marker
and `:root`, and contain no NUL byte. Library backup files must use `.json`, stay below 4 MiB,
parse correctly, and respect edition limits.

## Objective calculations

- OKLCH ramps, WCAG ratios, repair proposals, and export serialization are deterministic.
- WCAG calculation uses relative luminance for the indicated pair.
- Approximate CVD views use published Machado matrices in linear-light RGB.
- PCSSAK pair-distance thresholds are review heuristics and are labeled separately from WCAG.
- The app does not publish subjective beauty or professionalism scores.

## Public Free protection

Public builds default to Free. Internal Pro requires a compile-time feature plus a separate local
confirmation, cannot be combined with the reserved Store feature, and Pro-only native operations
check entitlement again. The release verifier rejects internal build flags, suspicious tracked
key material, version drift, and an unapproved updater endpoint.

## Release integrity

- App, Tauri, Rust package, lockfile, and UI versions are checked for agreement.
- Dependencies are locked and checked against the project's commercial license policy.
- Complete third-party notices are generated and bundled.
- x64 and x86 update packages receive architecture-specific Tauri signatures.
- Releases include `latest.json`, detached `.sig` files, and `SHA256SUMS.txt`.
- The tested local artifact size and hash are compared with the public download after release.
- A publish script requires explicit confirmation and refuses a dirty source tree.

## Verification layers

The project maintains pure color-engine tests, entitlement and history tests, persistence and
updater tests, localization completeness tests, Rust boundary tests, TypeScript production build,
Rust formatting/Clippy, license verification, installed-app smoke tests, multi-instance checks,
update/upgrade checks, and narrow/desktop visual QA. Exact results are tied to dated release notes
and work logs rather than advertised as permanent counts.

## What users should still do

- Download only from official PCSSAK locations.
- Compare the filename and SHA-256 before running the unsigned first installer.
- Do not disable SmartScreen or Defender.
- Keep important CSS exports and JSON library backups separately.
- Treat color-vision views and WCAG results as design evidence, not medical or legal certification.
- Report reproducible defects and private security details through the documented channels.

See [Known limitations](KNOWN-LIMITATIONS.md), [Security](../SECURITY.md),
[Privacy](https://palette.pcssak.com/privacy), and the [EULA](https://palette.pcssak.com/eula).
