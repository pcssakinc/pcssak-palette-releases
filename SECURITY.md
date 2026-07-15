# Security Policy / 보안 정책

## Supported releases

Security fixes are evaluated for the **latest public Early Access release**. Older beta builds
may not receive a separate fix. Confirm the current version on the
[latest release page](https://github.com/pcssakinc/pcssak-palette-releases/releases/latest)
before reporting.

## Report a vulnerability privately

Do not post public exploit details for update-signature bypass, entitlement bypass, arbitrary
file access or write, malicious image processing, code execution, secret exposure, or another
issue that could harm users.

Email `pcssakinc@gmail.com` with:

- PCssak Palette version, Windows version, and architecture;
- impact and the conditions required to reproduce it;
- minimal, safe reproduction steps or a non-sensitive sample;
- whether the issue is already public;
- a safe contact method and any disclosure constraints.

Do not send passwords, payment information, personal identifiers, customer data, confidential
design files, private keys, or production credentials. Replace sensitive content with the
smallest synthetic example possible.

PCSSAK will confirm and triage reports as solo-maintainer capacity allows, investigate impact,
prepare a fix and regression check where practical, and coordinate a reasonable disclosure
after users have a safe update path. This is not a guaranteed response-time or bounty program.

## Authenticity checks

- Download only from `palette.pcssak.com` or this official `pcssakinc` repository.
- Compare release filenames and SHA-256 values with `SHA256SUMS.txt`.
- The in-app updater verifies PCSSAK's Tauri update signature.
- The first external installer is not yet Authenticode-signed; SmartScreen should not be
  disabled to install it.

## 한국어

보안 수정은 **최신 공개 Early Access 버전**을 기준으로 검토합니다. 업데이트 서명 우회,
권한 검사 우회, 임의 파일 접근·쓰기, 악성 이미지 처리, 코드 실행, 비밀정보 노출처럼 사용자를
위험하게 할 수 있는 문제는 공개 Issue에 상세 재현 방법을 올리지 말고
`pcssakinc@gmail.com`으로 보내주세요.

앱·Windows 버전과 아키텍처, 영향, 최소 재현 조건, 이미 공개됐는지 여부와 안전한 연락 방법을
포함하면 도움이 됩니다. 비밀번호, 결제 정보, 주민등록번호, 고객 자료, 회사 비공개 디자인,
개인키나 운영 자격증명은 보내지 말고 합성 자료로 바꾸세요.

PCSSAK은 1인 운영 범위에서 접수와 영향을 확인하고, 가능한 경우 수정·회귀 검증과 안전한
업데이트 경로를 준비한 뒤 공개 시점을 협의합니다. 응답 시간이나 포상금을 보장하는 제도는
아닙니다.
