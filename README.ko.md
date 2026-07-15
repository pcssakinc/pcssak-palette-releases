# PCssak Palette - 공식 Windows 다운로드

[English](README.md) · [제품 홈페이지](https://palette.pcssak.co.kr) · [사용설명서](https://pcssak.co.kr/guide) · [최신 릴리스](https://github.com/pcssakinc/pcssak-palette-releases/releases/latest)

**색을 추측하지 않고 접근성까지 고려한 색상 시스템을 만듭니다.** HEX 색 하나 또는 내
PC의 이미지에서 11단계 OKLCH 램프를 만들고, 대비와 색각이상 혼동 위험을 확인한 뒤
CSS로 저장합니다.

![OKLCH 램프와 검증 흐름을 보여주는 실제 PCssak Palette 프로그램](https://pcssak.co.kr/images/palette/overview.ko.webp)

> **저장소 범위:** 이곳은 공식 바이너리 배포·문서·이슈 접수 저장소입니다. PCssak
> Palette 애플리케이션 소스는 비공개 독점 소프트웨어이며, 저장소가 공개되어 있다는
> 이유만으로 오픈소스 코드가 되는 것은 아닙니다.

## 다운로드

[최신 공식 릴리스](https://github.com/pcssakinc/pcssak-palette-releases/releases/latest)나
[palette.pcssak.com](https://palette.pcssak.com/download)에서만 내려받으세요.

- 일반적인 64비트 Windows 11·10 PC는 **x64**를 선택합니다.
- **x86**은 32비트 Windows 10에서만 사용합니다.
- 릴리스의 `SHA256SUMS.txt`와 설치 파일 이름·SHA-256을 비교하세요.

> [!WARNING]
> 최초 설치 파일에는 아직 Windows Authenticode 서명이 없어 **알 수 없는 게시자** 또는
> **Microsoft Defender SmartScreen**이 표시될 수 있습니다. 공식 경로에서만 받고 파일
> 이름과 SHA-256을 확인한 뒤 **추가 정보**에서 앱 이름이 **PCssak Palette**인지 확인하세요.
> 모두 일치할 때만 **실행/그래도 실행**을 선택하고 SmartScreen이나 Defender는 끄지 마세요.

## 왜 만들었나요

기획자는 청록색과 녹색을 구분하기 어려운 색각이상이 있는 한국의 1인 개발자입니다.
처음에는 같은 색을 더 안정적으로 찾고 비교하기 위한 작은 도구를 생각했습니다. 이후
소프트웨어가 아름다움을 대신 판단한다고 주장하지 않으면서, 색을 객관적인 근거로 확인할
수 있는 로컬 작업 흐름으로 발전했습니다.

자세한 내용은 [프로젝트 이야기](docs/PROJECT-STORY.ko.md)에 기록했습니다.

## 현재 Free 베타 기능

1. HEX 색을 입력하거나 로컬 PNG·JPEG·WebP·GIF·BMP 이미지에서 주요 색을 추출합니다.
2. 50부터 950까지 결정론적인 11단계 OKLCH 램프를 생성합니다.
3. WCAG 대비, 라이트·다크 UI, 적·녹·청색맹 및 흑백 근사 보기, 팔레트 닥터와 역할 색
   혼동 위험을 확인합니다.
4. 역할 색을 직접 수정하고 기본 WCAG AA 램프 보정과 지원되는 실행 취소를 사용합니다.
5. CSS·OKLCH CSS를 복사·저장하고 최대 10개 팔레트와 JSON 백업을 사용합니다.

공개 베타에서는 Pro를 구매할 수 없습니다. 향후 Pro는 역할 색 일괄 보정, 전체 대비
매트릭스, 보고서, 고급 프레임워크·토큰 형식, ASE, Export Pack과 확장 저장 기능을
제공할 예정입니다.

## 안전과 개인정보

- 이미지·색·팔레트·검증·내보내기는 기기에서 처리합니다.
- PCSSAK 계정, 광고, 사용 분석, 추적, 자동 오류 업로드가 없습니다.
- 독립형 베타는 공식 GitHub의 서명된 업데이트 확인과 사용자가 선택한 다운로드에만
  연결됩니다.
- 업데이트는 PCSSAK Tauri 서명을 검증하며 릴리스마다 SHA-256도 공개합니다.
- 이미지 크기·픽셀·디코더 메모리·파일 형식·CSS·JSON 경계를 Rust 계층에서 다시 검사합니다.
- 공개 바이너리는 Free가 기본이며 Pro 전용 네이티브 작업은 별도 권한 검사를 거칩니다.
- 제3자 라이선스와 소스 위치는 앱의 `THIRD-PARTY-NOTICES.txt`에 포함합니다.

이 장치들은 위험을 줄이지만 오류가 절대 없다는 뜻은 아닙니다. [품질과 안전](docs/QUALITY-AND-SAFETY.ko.md),
[알려진 한계](docs/KNOWN-LIMITATIONS.ko.md), [개인정보처리방침](https://palette.pcssak.com/privacy),
[이용약관](https://palette.pcssak.com/eula)을 확인하세요.

## 사람이 지휘하고 AI가 보조합니다

PCssak Palette는 한국의 1인 개발자가 직접 기획하고 관리합니다. AI 도구는 조사·구현·검토·
테스트·문서화 속도를 높이는 보조 수단으로 사용합니다. 요구사항, 기술 결정, 출시 승인과
유지보수의 최종 책임은 개발자에게 있습니다. 설명하거나 검증하고 유지할 수 없는 변경은
배포하지 않습니다.

자세한 기준은 [AI 보조 개발 정책](docs/AI-DEVELOPMENT-POLICY.ko.md)에 공개합니다.

## Early Access

- 현재 상태: 1.0 이전의 **무료 Early Access**
- 공식 검증: 최신 업데이트가 설치된 Windows 11 Home/Pro x64
- 베타 시험 지원: Windows 10 Home/Pro 22H2 x64·x86
- 현재 미지원: ARM64 네이티브, Windows S 모드, macOS, Linux
- 색각이상 보기는 근사 시뮬레이션이며 의료 진단이 아닙니다.
- 대비 결과는 표시된 색 조합에 대한 것이며 제품 전체 접근성 인증이 아닙니다.
- 1.0 전에는 화면·번역·파일 동작이 바뀔 수 있고 발견되지 않은 오류가 남아 있을 수 있습니다.

## 베타 개선에 참여하기

- 재현 가능한 오류는 [버그 제보 양식](../../issues/new?template=bug-report.yml)을 사용하세요.
- 기능 제안은 해결책보다 사용자 문제를 먼저 [기능 제안 양식](../../issues/new?template=feature-request.yml)에 적어주세요.
- 파일이나 로그를 첨부하기 전에 [지원 안내](SUPPORT.md)를 확인하세요.
- 악용 가능한 보안 문제는 [보안 안내](SECURITY.md)에 따라 비공개로 알려주세요.

AI의 도움으로 작성한 제보도 제출자가 직접 재현하고 확인해야 합니다. 검증하지 않은 이슈를
대량으로 등록하지 마세요.

## 문서

- [프로젝트 이야기](docs/PROJECT-STORY.ko.md)
- [AI 보조 개발 정책](docs/AI-DEVELOPMENT-POLICY.ko.md)
- [품질과 안전](docs/QUALITY-AND-SAFETY.ko.md)
- [알려진 한계](docs/KNOWN-LIMITATIONS.ko.md)
- [지원 안내](SUPPORT.md)
- [보안 제보](SECURITY.md)
- [이슈·기여 원칙](CONTRIBUTING.md)
- [릴리스 노트](https://github.com/pcssakinc/pcssak-palette-releases/releases)

PCssak Palette 바이너리는 PCssak Palette EULA에 따라 사용합니다. 제3자 오픈소스 구성요소는
각 라이선스를 따릅니다. PCSSAK은 독립 소프트웨어 브랜드이며 개발 기록에 언급된 AI 도구
제공사와 제휴하거나 보증을 받은 관계가 아닙니다.
