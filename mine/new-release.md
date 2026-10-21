# 이번에 새로 공개한 2건

### public-release-audit
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/public-release-audit
- 요약: 코드·스킬·레포를 공개하기 전에 읽기 전용으로 점검한다. 키·토큰, 개인 경로·이메일, 고객사 고유 내용, git 이력 노출, 라이선스, 위험 실행 패턴, 약관 의존.
- 쓸 때: "공개해도 돼?", "public 전환 전 검토", "스킬 공유해도 되나" 요청 시.
- 설치: `git clone https://github.com/Kein-chronicle/public-release-audit.git ~/.claude/skills/public-release-audit`

### reverse-spec-kit-public
- 종류: 스킬 묶음(10종)
- 출처: https://github.com/Kein-chronicle/reverse-spec-kit-public
- 요약: 목업(HTML)·요구사항·IA·디자인 가이드를 받아 Figma에 표준 구성의 화면설계서(기획서)를 작성하는 스킬 10종 묶음. 목업이 있으면 역기획, 없으면 요구사항 기반 추천안.
- 쓸 때: HTML 목업이나 요구사항에서 Figma 화면설계서를 만들 때. 필요: Claude + Chrome + Claude in Chrome 확장.
- 설치: `git clone https://github.com/Kein-chronicle/reverse-spec-kit-public.git  # 이 폴더에서 Claude를 실행`

## reverse-spec-kit-public 에 들어 있는 스킬 10종

위치: 레포의 `.claude/skills/<이름>/SKILL.md`. 키트 루트(`scripts/`, `docs/`, `templates/`)가 함께 있어야 동작하므로 **레포를 통째로 받아 그 폴더에서 Claude를 실행**한다.

| 스킬 | 역할 |
|---|---|
| `reverse-spec` | 총괄(오케스트레이터). 단계마다 게이트를 통과해야 다음으로 넘어가며 gates.md에 기록. |
| `rs-intake` | 0단계. 프로젝트·입력 폴더 생성, 자료 요청, 빈 폴더 확인, 모드(역기획/추천안) 확정. |
| `rs-setup` | 1단계. 환경 점검 — Claude, Chrome, Claude in Chrome 확장, figma.com 로그인, 한글 폰트. |
| `rs-inputs` | 2단계. 받은 자료(pdf·docx·xlsx·pptx·이미지 등)를 requirements.md, ia.md, design.json으로 정규화. |
| `rs-crawl` | 3단계. 목업을 탐색해 화면 목록을 만들고 화면별 DOM 좌표를 추출. |
| `rs-propose` | 3단계 대안. 목업이 없을 때 요구사항으로 추천 화면 목록을 제안·승인받고 저충실도 HTML 목업을 생성. |
| `rs-review` | 3c단계. 자료끼리 앞뒤가 안 맞는 곳을 찾아 "AI 추천수정"과 "확인 필요"로 분리. |
| `rs-figma-write` | 5단계. Figma 탭에 파일을 올려 표지~부록, 화면별 와이어프레임+디스크립션을 그림. |
| `rs-verify` | 6단계. 규칙 검사(페이지 분리, 보드 규격, 겹침, 넘침 등)와 스크린샷 육안 확인. |
| `rs-change` | 사후. 배포·공유된 기획서의 수정 요청을 다시 그리지 않고 제자리에서 반영. |

### 사용 전 유의
- 비공식 방식이다. Figma 공식 API/MCP가 아니라 로그인한 figma.com 탭의 편집기 객체를 Chrome 확장으로 제어한다. Figma 화면 구조가 바뀌면 깨질 수 있고 약관 적합성은 각자 확인해야 한다.
- 본인 소유이거나 열람·추출 허가를 받은 사이트·자료에만 쓴다. `rs-crawl`은 대상 페이지에서 스크립트를 실행(일부 경우 `eval`)한다.
- 고객·사내 자료는 `work/`(git 제외)에만 둔다.
- 한국어 전용.
