# PCssak Palette - Official Windows Downloads

[한국어](README.ko.md) · [Product website](https://palette.pcssak.com) · [User guide](https://pcssak.com/guide) · [Latest release](https://github.com/pcssakinc/pcssak-palette-releases/releases/latest)

**Build an accessible-minded color system without guessing.** Start from one HEX color or a
local image, generate an 11-step OKLCH ramp, review contrast and approximate color-vision
confusion risks, then save CSS.

![Actual PCssak Palette application showing an OKLCH ramp and validation workflow](https://pcssak.com/images/palette/overview.en.webp)

> **Repository scope:** This is the official public binary distribution, documentation, and
> issue-tracking repository. The PCssak Palette application source is private and proprietary;
> this repository is public but is not an open-source code release.

## Download

Download only from the [latest official release](https://github.com/pcssakinc/pcssak-palette-releases/releases/latest)
or from [palette.pcssak.com](https://palette.pcssak.com/download).

- Choose **x64** for normal 64-bit Windows 11 or Windows 10 PCs.
- Use **x86** only for a 32-bit Windows 10 installation.
- Compare the installer filename and SHA-256 with `SHA256SUMS.txt` in the release.

> [!WARNING]
> The first installer is not yet Windows Authenticode-signed. Windows can show **Unknown
> publisher** or **Microsoft Defender SmartScreen**. Download only from the official locations,
> verify the filename and SHA-256, select **More info**, confirm **PCssak Palette**, and choose
> **Run anyway** only when everything matches. Do not disable SmartScreen or Defender.

## Why it exists

The founder is a Korean solo developer with a color-vision deficiency that makes cyan and green
difficult to distinguish. The first idea was a small tool for finding and comparing the same
color more reliably. It grew into a local workflow that answers objective questions about color
without pretending software can decide what is beautiful.

Read the full [project story](docs/PROJECT-STORY.md).

## What the current Free beta does

1. Enter a HEX color or extract dominant colors from a local PNG, JPEG, WebP, GIF, or BMP.
2. Generate a deterministic OKLCH ramp with steps from 50 through 950.
3. Review WCAG contrast, light/dark UI previews, approximate protan/deutan/tritan/monochrome
   views, Palette Doctor findings, and semantic role-color confusion risks.
4. Correct role colors manually, use basic WCAG AA ramp correction, and undo supported repairs.
5. Copy or save CSS/OKLCH CSS, store up to 10 palettes, and back up the library as JSON.

Pro purchasing is **not available** in the public beta. Future Pro is reserved for batch role
repair, full contrast matrices, reports, advanced framework/token formats, ASE, Export Pack,
and a larger library.

## Safety and privacy

- Images, colors, palettes, validation, and exports are processed on the device.
- There is no PCSSAK account, advertising, analytics, tracking, or automatic crash upload.
- Standalone beta builds connect to the official GitHub release only for signed update checks
  and downloads that the user accepts.
- The updater verifies a PCSSAK Tauri signature. Each release also publishes SHA-256 values.
- Image size, pixel count, decoder allocation, file type, CSS output, and JSON backup boundaries
  are revalidated in the native Rust layer.
- Public binaries default to Free; Pro-only native operations use a separate entitlement check.
- Third-party licenses and source locations are bundled in `THIRD-PARTY-NOTICES.txt`.

These controls reduce risk but do not mean defects are impossible. See
[Quality and safety](docs/QUALITY-AND-SAFETY.md), [Known limitations](docs/KNOWN-LIMITATIONS.md),
[Privacy](https://palette.pcssak.com/privacy), and the [EULA](https://palette.pcssak.com/eula).

## Human-directed, AI-assisted

PCssak Palette is independently designed and maintained by a solo developer in South Korea. AI
assistants are used to accelerate research, implementation, review, testing, and documentation.
Final requirements, technical decisions, release approval, and maintenance remain under human
control. We do not ship changes that we cannot explain, test, or maintain.

The detailed acceptance rules are public in the
[AI-assisted development policy](docs/AI-DEVELOPMENT-POLICY.md).

## Early Access

- Current status: **Free Early Access**, version below 1.0.
- Officially verified environment: Windows 11 Home/Pro x64 with current updates.
- Beta test support: Windows 10 Home/Pro 22H2 x64 and x86.
- Not currently shipped: native ARM64, Windows S mode, macOS, or Linux.
- CVD views are approximations, not medical diagnosis.
- Contrast results apply to the indicated pair; they are not whole-product accessibility
  certification.
- Interfaces, translations, and file behavior may change before 1.0, and undiscovered defects
  may remain.

## Help improve the beta

- Use the [bug report form](../../issues/new?template=bug-report.yml) for a reproducible defect.
- Use the [feature request form](../../issues/new?template=feature-request.yml) to describe the
  user problem before proposing a solution.
- Read [Support](SUPPORT.md) before attaching files or logs.
- Report exploitable security details privately under [Security](SECURITY.md).

Reproducible reports, including reports prepared with AI assistance, must be checked by the
reporter before submission. Please do not submit bulk-generated or unverified issues.

## Documentation

- [Project story](docs/PROJECT-STORY.md)
- [AI-assisted development policy](docs/AI-DEVELOPMENT-POLICY.md)
- [Quality and safety](docs/QUALITY-AND-SAFETY.md)
- [Known limitations](docs/KNOWN-LIMITATIONS.md)
- [Support](SUPPORT.md)
- [Security reporting](SECURITY.md)
- [Contribution and issue conduct](CONTRIBUTING.md)
- [Release notes](https://github.com/pcssakinc/pcssak-palette-releases/releases)

PCssak Palette binaries are licensed under the PCssak Palette EULA. Third-party open-source
components remain under their own licenses. PCSSAK is an independent software brand and is not
affiliated with or endorsed by the AI tool providers named in the project history.
