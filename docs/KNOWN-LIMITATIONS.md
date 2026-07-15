# Known Limitations

[한국어](KNOWN-LIMITATIONS.ko.md)

## Current release

- The GitHub build is Free Early Access below version 1.0. It has no payment or Pro entitlement.
- Features, layouts, translations, and file behavior may change before 1.0.
- Undiscovered defects and compatibility problems may remain.
- Support is provided by a solo developer and has no guaranteed response or fix deadline.

## Installer and Windows

- The first NSIS installer is not Authenticode-signed and can trigger Unknown publisher or
  SmartScreen. Use only official PCSSAK sources and verify `SHA256SUMS.txt`.
- Windows 11 Home/Pro x64 is officially verified. Windows 10 22H2 x64/x86 is beta test support.
- Native ARM64, Windows S mode, macOS, and Linux are not shipped.
- Windows 10 Home/Pro is outside Microsoft's general support; app support cannot restore OS
  security updates.

## Color interpretation

- CVD views are approximate simulations, not individual measurement or medical diagnosis.
- Pair-risk distances are PCSSAK review heuristics, not WCAG or clinical thresholds.
- Contrast applies to the indicated pair and does not certify an entire product as accessible.
- The app does not judge beauty, culture, brand fit, or professional success.
- Monitor gamut, calibration, lighting, color management, and printing can change appearance.

## Files and storage

- Native extraction supports PNG, JPEG, WebP, GIF, and BMP, not HEIC, AVIF, PSD, RAW, or SVG.
- Files above 40 MiB or 40 megapixels are rejected; corrupt supported files can also fail.
- The library is local with no cloud sync or server recovery. Export JSON backups before reset,
  uninstall, or device migration and keep important outputs separately.
- Free stores up to 10 palettes. Future Pro storage and delivery features cannot be purchased yet.

## Repository

- This public repository distributes proprietary binaries and documentation. It is not an
  open-source release of the private application source.
- Third-party components remain under their own open-source licenses and notices.
