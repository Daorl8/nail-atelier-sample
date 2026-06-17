# CHANGELOG

## 2026-06-17
### Fixed
- KO/EN 언어 토글이 `<br>`·`<em>`을 포함한 요소(히어로 서브카피·소개 본문·영업시간 등)에서 영어로 전환되지 않던 버그 수정 — `setLang`이 모든 `[data-ko]` 요소를 `innerHTML`로 일괄 처리하도록 변경, `<html lang>`도 동기화.
- 스크롤 리빌 안정화 — IntersectionObserver `threshold:0` + `rootMargin:'0px 0px -8% 0px'`로 변경(뷰포트보다 큰 섹션이 안 나타나던 위험 제거, 더 일찍 노출), IntersectionObserver 미지원 시 전체 노출 폴백, `prefers-reduced-motion` 사용자에겐 애니메이션 비활성화.
