# Claude Code 결과물의 진짜 구조 이해하기

프롬프트 한 줄이 아니라 **Claude Code 하네스 구조**에서 결과물이 어떻게 나오는지 가르치는 HTML 강의덱입니다.

## 이 덱의 핵심 주장

같은 프롬프트를 새 컴퓨터의 Claude Code에 넣어도 우리 결과물은 안 나옵니다.
결과물은 `.claude` 하네스(에이전트·스킬·CLAUDE.md)와 `_workspace` 파이프라인에서 나오기 때문입니다.
그래서 재현하려면 프롬프트가 아니라 **repo(=하네스)를 통째로 가져가야** 합니다.

## Claude Code 프로젝트 공통 구조

```
CLAUDE.md          # 이 프로젝트가 무엇이고 어떤 트리거에 무슨 스킬을 쓰는지(하네스 지도)
.claude/skills/    # 재사용 방법론 + 오케스트레이터(작업 순서·규칙)
.claude/agents/    # 역할별 전문 에이전트(설계·제작·검증)
_workspace/        # 에이전트들이 만든 중간 산출물(설계·데이터·QA)
최종 산출물         # index.html / 스크래퍼 / 대시보드 등
```

## 두 가지 제작 패턴

- **패턴 A — 멀티에이전트 하네스** (auction_mbti): 복잡한 산출물을 전문 에이전트 6명이 파이프라인으로 만든다.
- **패턴 B — 시행착오 후 스킬 박제** (auction-crwal0629): 까다로운 자동화를 직접 뚫은 뒤 성공 패턴을 스킬로 저장해 재사용한다.

## 덱에 포함된 결과물

- friscomike94/auction_mbti — 진단형 웹앱 (멀티에이전트 하네스)
- friscomike94/auction-crwal0629 — 데이터 자동화 (시행착오→스킬)
- friscomike94/malso-standard-rights-deck — 단일 파일 HTML 덱
- earthskyisbig/apt-all-in-one — 리포트 자동화 (Private, 구조만 설명)

## 파일 구조

```
index.html            # 강의덱
data/projects.json    # 각 결과물의 실제 구조·제작흐름·재현법 데이터
```

## 새 결과물 추가법

`data/projects.json`의 `projects` 배열에 객체 하나를 추가합니다.
반드시 실제 repo 구조 기준으로 다음을 채웁니다.

- `realStructure`: 실제 핵심 파일과 역할 (git tree 기준)
- `buildMethod`: 제작 패턴
- `pipeline`: 실제 제작 흐름
- `reproduce`: 새 컴퓨터에서 재현하는 실제 명령/프롬프트
- `keyLesson`: 이 케이스의 핵심 교훈

## 원칙

- 이상적인 프롬프트가 아니라 **실제 구조**를 보여준다.
- 재현 열쇠는 최종 산출물이 아니라 `.claude` 폴더/스킬임을 강조한다.
- 디자인(폰트·색) 지시는 넣지 않는다. 로컬 폰트 의존이라 새 컴퓨터에서 그대로 재현되지 않기 때문이다.
