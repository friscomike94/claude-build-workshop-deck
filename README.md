# 검증해서 다시 만든 Claude 제작 레시피

빈 폴더 재현 테스트를 거쳐, 원본과 맞는 구조·기능·검수 기준만 남긴 초보자용 설명서 덱입니다.

## 이번 버전

- 버전: 1.2.0-verified
- 총 슬라이드: 66장
- 핵심 변경: 각 케이스를 실제로 빈 폴더에서 재현해 보고, 누락되기 쉬운 필수 조건을 덱에 반영

## 포함 케이스

1. auction_mbti: 매매 16유형 + 경매 8유형 + 결과 URL 공유/복원
2. auction_crawl: 법원경매 스크래퍼 + templates + skill/trial-and-error + Mono Signal 대시보드
3. malso_deck: 단일 index.html 강의 웹덱
4. apt_report: realprice-flow / apt-value 두 Claude Code 스킬 패키지

## 검증 기준

- 파일 구조가 원본 repo의 필수 구조와 맞는가
- 핵심 기능이 작동하는가
- 샘플 데이터로 파이프라인이 끝까지 도는가
- GitHub Pages에서 렌더링되는가
- 원본 대비 빠지는 기능은 검수 슬라이드에 명시되는가
