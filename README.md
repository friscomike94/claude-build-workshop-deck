# Claude Code Build Workshop Deck

Claude Code에 어떤 명령어와 프롬프트를 넣으면 부동산 AI 결과물이 만들어지는지 가르치는 HTML 강의덱입니다.

## 강의 목적

이 덱은 GitHub 사용법 강의가 아닙니다.
핵심은 **Claude Code 터미널에서 실제로 무엇을 입력해야 결과물이 만들어지는지**를 초보자가 따라 할 수 있게 보여주는 것입니다.

## 파일 구조

```
index.html                  # GitHub Pages에서 열리는 강의덱
data/projects.json          # 결과물별 Claude Code 명령/프롬프트 데이터
assets/screenshots/         # 완성 결과물 화면 캡처
assets/prompts/             # 긴 프롬프트 보조 자료 저장 폴더
CAPTURE_GUIDE.md            # 강의용 화면 캡처 기준
```

## 덱에 포함된 결과물

- earthskyisbig/apt-all-in-one: 리포트 자동화
- friscomike94/auction_mbti: 진단형 웹앱
- friscomike94/auction-crwal0629: 데이터 대시보드
- friscomike94/malso-standard-rights-deck: HTML 강의덱

## 한 프로젝트의 기본 강의 흐름

1. 터미널에서 작업 폴더 생성
2. `claude` 명령으로 Claude Code 실행
3. Claude Code에 “먼저 계획만 세워줘” 프롬프트 입력
4. 계획 확인 후 “이제 실제 파일을 만들어줘” 프롬프트 입력
5. 터미널에서 `open index.html` 또는 실행 명령으로 결과 확인
6. Claude Code에 수정 요청 입력
7. 필요하면 GitHub Pages로 배포

## 새 결과물 추가법

`data/projects.json`의 `projects` 배열에 새 객체를 추가합니다.
중요한 필드는 `commandBlocks`입니다.

예시:

```json
{
  "id": "new-project",
  "repo": "owner/repo",
  "title": "새 결과물",
  "kind": "제작 패턴",
  "commandBlocks": [
    {
      "label": "1. 작업 폴더 만들기",
      "type": "terminal",
      "code": "mkdir new-project\ncd new-project\nclaude",
      "say": "터미널에서 그대로 입력합니다."
    },
    {
      "label": "2. Claude Code에 붙여넣기",
      "type": "claude",
      "code": "너는 ... 바로 코딩하지 말고 먼저 PLAN.md를 만들어줘.",
      "say": "Claude Code 입력창에 그대로 붙여넣습니다."
    }
  ]
}
```

## 강의 원칙

- “어디를 클릭하나”보다 “무엇을 입력하나”를 보여준다.
- 한 슬라이드에는 하나의 명령 또는 하나의 프롬프트만 보여준다.
- 초보자가 복사해서 그대로 쓸 수 있어야 한다.
- Claude Code가 파일을 만든 뒤에는 반드시 확인 명령을 보여준다.
- 수정 요청 예시까지 보여줘야 실제 제작법이 된다.
