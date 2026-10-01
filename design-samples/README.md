# 디자인 리뉴얼 시안 (2026-10)

라이브 페이지(`index.html`, `support.html`)는 그대로 두고, 리뉴얼 후보 3종을 이 폴더에 둡니다.
각 HTML은 단일 파일이며 라이트·다크 모드와 390px 모바일 폭을 지원합니다.

| 시안 | 파일 | 미리보기 |
| --- | --- | --- |
| 현재 | `../index.html` | `previews/current.png` |
| A · Cloud Soft | `a-cloud-soft.html` | `previews/a-cloud-soft.png` |
| B · Liquid Glass | `b-liquid-glass.html` | `previews/b-liquid-glass.png` |
| C · Cute-alism | `c-cutealism.html` | `previews/c-cutealism.png` |

모바일 전체 화면(`*-mobile.png`)과 다크 모드(`*-mobile-dark.png`)도 `previews/`에 있습니다.

## 현재 디자인 진단

잘 된 점
- 본문 가독성: 46rem 폭, 줄간격 1.7, `word-break: keep-all`, 시스템 다크 모드 대응
- 가벼움: 외부 리소스 없이 즉시 로딩

부족한 점
- 브랜드 부재: 앱 아이콘·마스코트·브랜드 색이 없어 App Store에서 넘어온 사용자가 같은 앱인지 확신하기 어려움
- 요약 없음: "서버 전송 없음, 계정 없음" 같은 핵심 장점이 9개 조항 안에 묻혀 있음
- 탐색: 목차·접기 없이 긴 문서가 한 번에 노출, 기본 파란 밑줄 링크
- 메타 정보: favicon, `og:image`, `theme-color` 없음 (링크 공유 시 미리보기가 비어 보임)
- `support.html`의 `h3` 스타일 미지정

## 조사한 2026 트렌드와 시안 매핑

- Pantone 2026 올해의 색 **Cloud Dancer**(따뜻한 화이트), Soft 3D·Plushcore 아이콘 → **A**
- Apple **Liquid Glass**(iOS 26) 반투명 레이어, 벤토 그리드, 그라데이션 타이포 → **B**
- **Cute-alism**(귀여움 + 네오 브루탈리즘), Pinterest Predicts 2026 **Fun Haus/서커스 스트라이프**, 마스코트 아이콘 → **C**
- 공통: 개인정보처리방침의 "요약 먼저(Highlights) → 상세는 펼치기" 구조 (Apple·Notion·Best Buy 방식)

## 실제 적용 시 체크리스트

- 시안의 3~9조는 축약/생략 상태 → 적용 시 `index.html` 원문 전체를 옮길 것
- Pretendard 웹폰트는 jsDelivr CDN 사용 (실패 시 시스템 폰트로 대체됨)
- 토끼 일러스트는 임시 SVG → 실제 앱 아이콘·마스코트 에셋으로 교체 권장
- favicon, `og:image`, `theme-color` 메타 추가
