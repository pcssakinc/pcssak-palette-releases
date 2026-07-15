# AI-Assisted Development Policy

[한국어](AI-DEVELOPMENT-POLICY.ko.md)

PCSSAK uses AI assistants for research, implementation, review, testing, translation, and
documentation. AI output is a proposal, not proof and not a release decision.

## Human accountability

The solo developer remains responsible for requirements, product boundaries, credentials, risk
acceptance, release approval, user communication, and maintenance. AI providers are not product
co-owners, security contacts, or publishers of PCssak Palette.

## A change may ship only when

1. The user problem and acceptance criteria are clear.
2. The change fits the current architecture instead of creating an unexplained parallel path.
3. Its data flow, important assumptions, failure modes, and rollback can be explained.
4. Tests or reproducible checks provide evidence appropriate to the risk.
5. New dependencies and APIs are verified for source, maintenance, version, and commercial
   license compatibility.
6. File input, permissions, network behavior, privacy, update integrity, and denial-of-service
   boundaries are reviewed where relevant.
7. Supported Windows environments, locales, upgrade behavior, and user recovery are considered.
8. User-facing documentation and known limitations change with the behavior.
9. The human owner explicitly approves public release, signing, Store, or paid-entitlement work.

Compilation alone is not proof. A generated test that merely repeats generated implementation is
also not independent evidence.

## What PCSSAK will not do intentionally

- ship unreviewed generated code;
- remove or weaken tests only to make a build pass;
- install a package that was not verified to exist and be appropriately licensed;
- claim perfect security, certification, medical accuracy, or unsupported compatibility;
- hide material network access, collection, or known limitations;
- publish secrets, signing keys, private user files, or confidential samples;
- send bulk-generated, speculative, or untested issues and patches to upstream maintainers;
- describe this public binary repository as open source without an open-source source license.

## When a mistake is found

PCSSAK records the affected version and reproduction, finds the root cause, adds a regression
check where practical, applies a maintainable fix, reruns the scaled release gate, and documents
remaining risk and recovery. The lesson should become a test, verifier, checklist item, or design
rule when possible.

See [Quality and safety](QUALITY-AND-SAFETY.md), [Known limitations](KNOWN-LIMITATIONS.md), and
[Security](../SECURITY.md).
