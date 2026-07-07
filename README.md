# Claude Build Workshop Deck

Claude로 부동산 AI 결과물을 만드는 과정을 설명하는 GitHub Pages용 HTML 강의덱입니다.

## 파일 구조

```
index.html                  # GitHub Pages에서 열리는 강의덱
data/projects.json          # 결과물 목록과 슬라이드 내용 데이터
assets/screenshots/         # 화면 캡처 이미지 저장 폴더
assets/prompts/             # 긴 프롬프트나 보조 자료 저장 폴더
```

## GitHub에 올리는 법

1. 새 GitHub repo를 만듭니다.
2. 이 폴더 안의 파일을 그대로 업로드합니다.
3. GitHub repo에서 **Settings → Pages**로 이동합니다.
4. Source를 **Deploy from a branch**로 선택합니다.
5. Branch는 **main**, folder는 **/(root)**로 선택합니다.
6. Save를 누릅니다.
7. 1~2분 뒤 표시되는 GitHub Pages URL로 접속합니다.

## 새 결과물 추가법

1. 새 결과물 화면을 캡처합니다.
2. 이미지를 `assets/screenshots/새파일명.png`에 넣습니다.
3. `data/projects.json`을 엽니다.
4. `projects` 배열 마지막에 기존 항목 하나를 복사해서 붙여넣습니다.
5. 아래 필드를 바꿉니다.

필수 필드:

- `id`: 짧은 영문 ID
- `repo`: GitHub repo 이름
- `title`: 슬라이드 제목
- `kind`: 제작 패턴, 예: 진단형 웹앱 / 데이터 대시보드 / 리포트 자동화 / HTML 강의덱
- `liveUrl`: 배포 URL, 없으면 빈 문자열
- `oneLine`: 한 문장 설명
- `workflow`: 만드는 순서
- `clickGuide`: GitHub/Claude에서 누를 순서
- `claudePrompt`: 초보자가 복사할 프롬프트
- `screenshots[0].file`: 캡처 파일명

## 캡처 규칙

- 16:9 화면으로 캡처합니다.
- 주소창이 필요한 장면은 주소창까지 포함합니다.
- 클릭 위치가 중요한 장면은 빨간 박스 대신 라임색 박스/화살표를 사용합니다.
- 한 슬라이드에는 한 화면만 보여줍니다.
- 파일명은 영문 소문자와 하이픈을 사용합니다.

예:

```
auction-mbti-home.png
auction-mbti-github-upload.png
auction-crwal-pages-settings.png
```

## Claude에게 새 결과물 추가 요청하기

```text
이 GitHub Pages 강의덱에 새 결과물을 추가하고 싶어.
data/projects.json에 들어갈 JSON 객체를 만들어줘.
결과물 정보는 아래와 같아.

repo: owner/repo
제목: ...
종류: ...
완성 URL: ...
초보자에게 가르칠 핵심: ...
만드는 순서: ...
GitHub에서 누르는 순서: ...
복붙 프롬프트: ...
```

## 현재 포함된 결과물

- earthskyisbig/apt-all-in-one
- friscomike94/auction_mbti
- friscomike94/auction-crwal0629
- friscomike94/malso-standard-rights-deck
