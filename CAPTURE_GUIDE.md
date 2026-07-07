# 강의용 화면 캡처 체크리스트 (구조 이해 중심)

이 덱은 "어디를 클릭" 캡처가 아니라 **repo 구조와 Claude Code 실행 장면**을 보여주는 것이 목적입니다.

## 캡처하면 좋은 장면

1. repo의 파일 트리 (특히 .claude/agents, .claude/skills, _workspace)
   - GitHub repo 화면 또는 `ls -a`, `tree .claude` 터미널 출력
2. CLAUDE.md 내용 (하네스 정의·변경 이력)
3. 오케스트레이터 SKILL.md의 파이프라인 설명 부분
4. `git clone` 후 `claude` 실행 장면
5. Claude Code가 .claude 스킬을 인식/실행하는 장면
6. _workspace에 중간 산출물이 쌓이는 장면
7. 최종 산출물(웹앱/대시보드/CSV) 결과 화면

## 원칙

- 프롬프트 한 줄보다 **구조(폴더 트리)**를 먼저 보여준다.
- "재현하려면 이 폴더가 필요하다"를 시각적으로 강조한다.
- 16:9 화면, 터미널 글자는 크게.
- 폰트·색 등 디자인은 강의 포인트가 아니므로 강조하지 않는다.

## 프로젝트별

### auction_mbti (멀티에이전트 하네스)
- .claude/agents 6개 파일 목록
- rmbti-orchestrator SKILL.md 파이프라인 도식
- _workspace의 01_typology ~ 99_qa_report 목록
- 최종 테스트 화면

### auction-crwal0629 (시행착오→스킬)
- skill/SKILL.md의 "절대 하지 말 것" 목록
- trial-and-error.md
- scrape 실행 후 CSV 생성 장면
- docs/index.html 대시보드

### malso-standard-rights-deck (단일 파일)
- index.html 하나뿐인 구조
- 슬라이드 화면

### apt-all-in-one (Private)
- skills/realprice-flow, skills/apt-value 구조도(설명용)
- 리포트 미리보기
