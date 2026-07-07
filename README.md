# 아무것도 몰라도 따라 만드는 설명서

빈 폴더에서 시작해 GitHub에 완성품을 올리기까지, 이 덱만 보고 그대로 따라 하는 초보자용 설명서입니다.

## 읽는 법

- 초록 박스 = 터미널에 그대로 입력
- 파란 박스 = Claude Code에 그대로 붙여넣기
- 회색 번호 단계 = 웹사이트에서 순서대로 클릭

## 담긴 설명서 (각각 백지 → GitHub 완성까지)

1. auction_mbti — 투자성향 테스트 웹앱 (11단계)
2. auction_crawl — 법원경매 수집기 + 대시보드 (10단계)
3. malso_deck — 강의용 슬라이드 웹페이지 (9단계)
4. apt_report — 아파트 실거래 분석 리포트, API 키 필요 (8단계)

## 파일 구조

```
index.html            # 설명서 덱 (단계당 한 슬라이드)
data/projects.json    # 준비물 + 4개 결과물의 단계별 명령/프롬프트/클릭
```

## 새 설명서 추가법

`data/projects.json`의 `projects` 배열에 객체를 추가합니다.
`manual` 배열에 단계별로 넣습니다. 각 단계는:

- `phase`: 폴더 준비 / 제작 / 확인 / 깃허브 올리기 / 배포 / 완성
- `kind`: terminal(초록) / claude(파랑) / browser(클릭) / check(완성확인)
- `title`, `code` 또는 `clicks`, `note`
