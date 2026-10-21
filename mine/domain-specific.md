# 특정 분야용

범용성: 특정 분야

### canvas-render-pixel-gate
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/canvas-render-pixel-gate
- 요약: 렌더된 게임 캔버스의 고유 색 수와 단색 채움 비율을 측정해 "회색 박스" 스크린샷을 잡는다. 측정하지 못한 것은 통과시키지 않는다.
- 쓸 때: 게임이 에셋을 갖고 있다는데 실제로는 회색 박스로 보일 때. [게임]
- 설치: `git clone https://github.com/Kein-chronicle/canvas-render-pixel-gate.git ~/.claude/skills/canvas-render-pixel-gate`

### ai-sprite-pipeline-audit
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ai-sprite-pipeline-audit
- 요약: AI 생성 스프라이트 일괄 감사. 불변 스타일 마스터, 생성 원장, 중복 프레임, 실제 투명도, 안전한 배경 키잉.
- 쓸 때: 이미지 생성기로 캐릭터·스프라이트를 대량 제작할 때. [게임]
- 설치: `git clone https://github.com/Kein-chronicle/ai-sprite-pipeline-audit.git ~/.claude/skills/ai-sprite-pipeline-audit`

### game-asset-license-ledger
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/game-asset-license-ledger
- 요약: 내려받은 아트·오디오 팩의 라이선스 원장. 알 수 없는 팩, 상용 릴리스 속 비상업 라이선스를 실패 처리하고 크레딧을 생성.
- 쓸 때: CC0·CC-BY 에셋을 모아 쓰는 중, 릴리스 준비 때. [게임]
- 설치: `git clone https://github.com/Kein-chronicle/game-asset-license-ledger.git ~/.claude/skills/game-asset-license-ledger`

### web-game-asset-reality-check
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/web-game-asset-reality-check
- 요약: 선언만 되고 실제로는 없는 것을 잡는다. 번들되지 않은 폰트, 런타임 CDN 의존, 헤드리스 Chromium의 페이지 오류.
- 쓸 때: 웹앱·게임 출시 전. [웹/게임]
- 설치: `git clone https://github.com/Kein-chronicle/web-game-asset-reality-check.git ~/.claude/skills/web-game-asset-reality-check`

### swift-runtime-trap-fuzz
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/swift-runtime-trap-fuzz
- 요약: 단위 테스트가 못 보는 Swift 런타임 트랩(Int 오버플로, Int(Double.nan), 잘못된 캐스트, 인덱스 오류)을 퍼즈 방법과 안전한 산술로 잡는다.
- 쓸 때: 사용자 입력으로 산술하는 Swift/SwiftUI 앱. [iOS]
- 설치: `git clone https://github.com/Kein-chronicle/swift-runtime-trap-fuzz.git ~/.claude/skills/swift-runtime-trap-fuzz`

### ios-simulator-ui-test-hygiene
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ios-simulator-ui-test-hygiene
- 요약: iOS 시뮬레이터 UI 테스트·크래시 퍼즈가 노트북에서 죽지 않게 한다. 16GB 메모리 한계와 끝없이 뜨는 크래시 리포트 창.
- 쓸 때: xcodebuild UI 테스트가 메모리 부족으로 중단될 때. [iOS]
- 설치: `git clone https://github.com/Kein-chronicle/ios-simulator-ui-test-hygiene.git ~/.claude/skills/ios-simulator-ui-test-hygiene`

### app-store-connect-api-gotchas
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/app-store-connect-api-gotchas
- 요약: App Store Connect 자동화의 실전 함정. 심사 제출 순서, 연령 등급의 광고 플래그, 스크린샷 추가 버그, 새 버전에서 사라지는 첨부.
- 쓸 때: ASC API로 제출·메타데이터를 자동화할 때. [iOS]
- 설치: `git clone https://github.com/Kein-chronicle/app-store-connect-api-gotchas.git ~/.claude/skills/app-store-connect-api-gotchas`

### ffmpeg-video-qa-gates
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ffmpeg-video-qa-gates
- 요약: ffmpeg로 짧은 영상을 기계 검수한다. 멈춘 프레임, 무음 구간, 음량·트루피크, 용량, 밋밋한 오프닝, 자막 읽기 속도.
- 쓸 때: 영상을 대량 생성하고 눈으로 확인하지 않고 검수하려 할 때. [영상]
- 설치: `git clone https://github.com/Kein-chronicle/ffmpeg-video-qa-gates.git ~/.claude/skills/ffmpeg-video-qa-gates`

### deterministic-html-motion-render
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/deterministic-html-motion-render
- 요약: HTML 모션 장면을 어떤 프레임이든 순서와 무관하게 똑같이 렌더하도록 린트·검증한다. 시계, 난수, 타이머 금지.
- 쓸 때: AI가 쓴 애니메이션 코드가 재실행마다 다르게 렌더될 때. [영상]
- 설치: `git clone https://github.com/Kein-chronicle/deterministic-html-motion-render.git ~/.claude/skills/deterministic-html-motion-render`

### cold-read-comprehension-review
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/cold-read-comprehension-review
- 요약: 영상·페이지가 실제로 전달되는지, 기억 없는 독립 독자에게 주고 작성자의 정답 파일과 대조해 채점한다. 오래된 판정을 표시.
- 쓸 때: "체크는 다 통과했는데 사람들이 헷갈려 한다"일 때. [콘텐츠]
- 설치: `git clone https://github.com/Kein-chronicle/cold-read-comprehension-review.git ~/.claude/skills/cold-read-comprehension-review`

### ai-content-editorial-lint
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ai-content-editorial-lint
- 요약: 폴더 속 글들의 AI 콘텐츠 획일화를 잡고, 승인된 원고가 조용히 수정되었는지 감지한다.
- 쓸 때: AI가 웹 자료로 글을 쓰고 모든 글이 비슷해 보일 때. [콘텐츠]
- 설치: `git clone https://github.com/Kein-chronicle/ai-content-editorial-lint.git ~/.claude/skills/ai-content-editorial-lint`

### llm-adaptation-fidelity-check
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/llm-adaptation-fidelity-check
- 요약: 원문을 각색한 결과가 충실한지 문자열 비교로 검사한다. 인용문 원문 일치, 지어낸 문장·숫자 없음, 틀 씌우기 범위, 명시된 생략.
- 쓸 때: 글을 영상 대본·요약·SNS 글로 바꿀 때. [콘텐츠]
- 설치: `git clone https://github.com/Kein-chronicle/llm-adaptation-fidelity-check.git ~/.claude/skills/llm-adaptation-fidelity-check`

### ai-image-pairwise-eval
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ai-image-pairwise-eval
- 요약: 골든 레퍼런스 대비 AI 생성 이미지를 감(感) 없이 평가한다. 위치 편향을 뺀 쌍대 비교와 open_clip 유사도.
- 쓸 때: 에셋이 충분히 좋은지 판단하거나 후보를 순위 매길 때. [이미지]
- 설치: `git clone https://github.com/Kein-chronicle/ai-image-pairwise-eval.git ~/.claude/skills/ai-image-pairwise-eval`

### ai-resume-screening-safeguards
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ai-resume-screening-safeguards
- 요약: AI 이력서 선별의 안전장치. 루브릭에서 보호 속성 린트, 경력 계산은 코드로, 이력서 속 프롬프트 인젝션 탐지.
- 쓸 때: AI로 지원자를 평가하는 도구를 만들 때. [채용]
- 설치: `git clone https://github.com/Kein-chronicle/ai-resume-screening-safeguards.git ~/.claude/skills/ai-resume-screening-safeguards`

### pdf-annotation-rotation
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/pdf-annotation-rotation
- 요약: PDF·캔버스 주석(상자, 선, 잉크, 원본 마스크)을 표시 좌표에서 90도 단위로 회전한다. 입력은 변경하지 않음.
- 쓸 때: PDF/캔버스 주석 회전을 구현할 때. [PDF]
- 설치: `git clone https://github.com/Kein-chronicle/pdf-annotation-rotation.git ~/.claude/skills/pdf-annotation-rotation`

### pdf-text-position-table-extract
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/pdf-text-position-table-extract
- 요약: 위치가 있는 텍스트 조각(x, 기준선, 크기, 글자)으로 직사각형 표를 복원하고 빈 칸을 제자리에 유지한다.
- 쓸 때: 위치 정보가 있는 문서 텍스트를 CSV 행으로 바꿀 때. [PDF]
- 설치: `git clone https://github.com/Kein-chronicle/pdf-text-position-table-extract.git ~/.claude/skills/pdf-text-position-table-extract`

### ai-companion-persona-kit
- 종류: 키트(SKILL.md 없음)
- 출처: https://github.com/Kein-chronicle/ai-companion-persona-kit
- 요약: 장기 실행 AI 동반자 캐릭터용 뼈대. 데이터로서의 페르소나, 일일 상황 엔진, 결정적 선제 메시지, 웰빙 가드.
- 쓸 때: 장기 실행 AI 동반자(캐릭터) 서비스를 설계할 때. [페르소나] — SKILL.md 없는 도구·문서 키트
- 설치: `git clone https://github.com/Kein-chronicle/ai-companion-persona-kit.git`
