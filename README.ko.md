# 모션 디자인 도감 Motion Design Field Guide

[繁體中文](README.md) ｜ [简体中文](README.zh-CN.md) ｜ [English](README.en.md) ｜ [日本語](README.ja.md) ｜ 한국어

[![GitHub stars](https://img.shields.io/github/stars/qpalzm963/animation-gallery?style=social)](https://github.com/qpalzm963/animation-gallery/stargazers)

[![모션 디자인 도감 미리보기](og.png)](https://qpalzm963.github.io/animation-gallery/?lang=ko)

**76가지 웹 애니메이션 기법**을 담은 단일 페이지 인터랙티브 도감입니다 — 가장 흔한페이드·이동부터 FLIP, View Transitions, 스크롤 타임라인, 구이(gooey) 블롭, 글리치 아트같은 흔치 않은 기법까지. 모든 카드는 **실제로 움직이는** 구현입니다: 카드에 마우스를올리거나 「다시 재생」을 누르면 다시 볼 수 있고, 언제 쓰면 좋은지에 대한 메모와 그대로복사해 갈 수 있는 핵심 코드가 함께 담겨 있습니다.

**단일 HTML 파일, 의존성 제로, 전부 네이티브 CSS / Web Animations API / Canvas / SVG.**
카드에 실린 코드 스니펫은 실제로 페이지에 주입되는 바로 그 문자열입니다 — 보이는 것이 곧실행되는 것입니다.

## 온라인으로 보기

**https://qpalzm963.github.io/animation-gallery/?lang=ko**

또는 [`index.html`](index.html)을 직접 열면 됩니다 — 빌드나 설치는 전혀 필요 없습니다:

```bash
open index.html
# 또는 로컬 서버 실행 (일부 View Transitions 데모는 file:// 이 아닌 http:// 가 필요합니다)
python3 -m http.server 8991
```

## 화면 미리보기

| 라이트 테마 | 다크 테마（`?theme=dark`） |
|---|---|
| ![라이트 테마](assets/home-light.png) | ![다크 테마](assets/home-dark.png) |

인터페이스는 5개 언어를 지원하며, URL에 `?lang=` 을 붙이면 특정 언어로 바로 공유할 수 있습니다. 예: [일본어판](https://qpalzm963.github.io/animation-gallery/?lang=ja):

![일본어 인터페이스](assets/lang-ja.png)

## 콘텐츠

12개 카테고리, 76가지 기법:

| 카테고리 | 수록 내용 |
|---|---|
| 기본 변화 | 페이드, 페이드 업, 스케일 팝, 스핀, 블러 인, 플립 인, 방향 와이프 |
| 타이밍과 이징 | 이징 비교, 스프링, 오버슈트, 예비 동작, 스태거, 스쿼시 & 스트레치, 팔로 스루 |
| 레이아웃 전환 | FLIP, 공유 요소 전환, View Transitions API, 리스트 재정렬, 셰이프 모프, 높이 자동 확장 |
| 스크롤 연동 | 스크롤 리빌, 패럴랙스, 스크롤 진행률, 스티키 씬, 네이티브 `animation-timeline` |
| 텍스트 애니메이션 | 타자기 효과, 텍스트 스크램블, 스플릿 텍스트, 마스크 리빌, 숫자 카운터, 무한 마퀴, 가변 폰트, 키네틱 타이포그래피 |
| 드로잉과 마스크 | 라인 드로잉, 패스 팔로우, 클립 리빌, 체크마크 드로잉, 그레이디언트 마스크, 패스 모프 |
| 물리와 인터랙션 | 마그네틱 호버, 커서 트레일, 관성 / 모멘텀, 러버 밴드, 파티클, 리플 |
| 공간과 3D | 틸트 카드, 카드 플립, 큐브, 레이어드 뎁스, 원근 리스트 |
| 빛과 질감 | 스켈레톤 시머, 그레이디언트 플로우, 글로우 펄스, 필름 그레인, 글래스모피즘, 구이 / 메타볼 |
| 실험적 기법 | 글리치, 색수차, 스프라이트 / steps(), 웨이브 그리드, 커튼 전환, 픽셀 디졸브, 탄성 인디케이터, 오빗 |
| 모던 CSS 전환 | `@starting-style`, `allow-discrete`, `calc-size()`, `linear()` 순수 CSS 스프링, `@property`, 멀티트랙 키프레임 |
| View Transitions | old / new 커스터마이즈, `::view-transition-group()`, 방향 인식 전환, 이름 충돌 티칭 카드, 리스트 → 상세 확장, 크로스 도큐먼트 전환（`vt-a.html` / `vt-b.html`） |

이 외에도 수록되어 있습니다:

- **애니메이션 12원칙 → 인터페이스 대응** — 디즈니의 12원칙을 인터페이스 어휘로 옮겼습니다
- **크로스 플랫폼 대조표** — CSS / Web, Flutter, SwiftUI의 개념 대응표와 각 플랫폼 고유의 표현 기법（SwiftUI의 `KeyframeAnimator`, `PhaseAnimator`, Liquid Glass; Flutter의 `Hero`, `Curves`）
- **지속 시간·커브 치트시트**

## 프롬프트 생성기

각 카드에서 구조화된 프롬프트를 원클릭으로 복사할 수 있습니다. 아무 AI 코딩 에이전트에나붙여 넣으면 해당 기법을 대상 프레임워크의 관용적인 방식으로 구현해 줍니다. 툴바에서 대상프레임워크（Flutter / SwiftUI / React + Framer Motion / 순수 CSS）를 선택하세요. 프롬프트에담기는 것은 CSS를 한 줄씩 번역해 달라는 요청이 아니라 **비주얼 스펙**이며, 해당 프레임워크의관용 표현에 대한 리마인더도 함께 들어갑니다.

## 기능

- 카테고리 필터, 키워드 검색
- 카드 단위 다시 재생 / 전체 다시 재생
- 5개 언어 인터페이스（繁體中文／简体中文／English／日本語／한국어, 우측 상단에서 전환）, 선택은 기억됩니다
- 모든 카드에 딥 링크 제공（카드 번호를 클릭하면 `#t-기법id` 링크가 복사됩니다）— 특정 기법을 바로 공유할 수 있습니다
- 다크／라이트 테마 전환（기본은 라이트）, 선택은 기억됩니다
- `prefers-reduced-motion` 감지 — 데모 애니메이션을 자동으로 일시정지하고 「그래도 보기」 옵션을 제공합니다
- 화면 밖 데모는 자동 언마운트되어, 많은 데모가 동시에 실행되며 성능을 끌어내리는 일을 막습니다

## 라이선스

[MIT](LICENSE) — 자유롭게 사용·수정·재배포할 수 있습니다.

---

도움이 되셨다면 우측 상단의 ⭐ Star를 눌러 주세요. 더 많은 사람이 이 도감을 만날 수 있습니다.
