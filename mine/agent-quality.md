# 에이전트 작업 품질

범용성: 범용

### agent-definition-of-done-gate
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/agent-definition-of-done-gate
- 요약: 파이프라인·에이전트가 "다 끝났다"고 말하기 전에, 자동 측정이 가능한 게이트를 사람이 닫지 못하게 하고, 보류에는 근거를 요구하는 완료 규칙.
- 쓸 때: 완료/상태 표시 함수를 설계할 때, 사람·기기 단계가 남았는데 "전부 끝"으로 표시될 때.
- 설치: `git clone https://github.com/Kein-chronicle/agent-definition-of-done-gate.git ~/.claude/skills/agent-definition-of-done-gate`

### agent-false-negative-guard
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/agent-false-negative-guard
- 요약: 도구가 빈 출력을 내면 "없음/깨끗함"이라 단정하지 않게 한다. 긍정 대조군과 3상태(있음 / 없음 / 측정 불가)로 보고.
- 쓸 때: 명령이 종료코드 0에 출력이 없을 때, "device not found" 같은 결과로 결론을 내리기 직전.
- 설치: `git clone https://github.com/Kein-chronicle/agent-false-negative-guard.git ~/.claude/skills/agent-false-negative-guard`

### llm-verdict-gate
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/llm-verdict-gate
- 요약: AI·사람이 채우는 품질 게이트가 침묵으로 통과하지 못하게 한다. PASS/FAIL을 기계가 파싱하고 판정이 없으면 FAIL.
- 쓸 때: 리뷰·QA 게이트가 항상 통과할 때, 보고서에 산문만 있고 판정 줄이 없을 때.
- 설치: `git clone https://github.com/Kein-chronicle/llm-verdict-gate.git ~/.claude/skills/llm-verdict-gate`

### stale-verdict-guard
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/stale-verdict-guard
- 요약: 모든 판정·QA 통과를 심사한 소스의 지문에 묶어, 수정 후에는 통과가 자동 무효가 되게 한다.
- 쓸 때: 빌드가 바뀐 뒤에도 PASS가 남아 있을 때, 루브릭 버전을 올려 과거 판정을 무효화해야 할 때.
- 설치: `git clone https://github.com/Kein-chronicle/stale-verdict-guard.git ~/.claude/skills/stale-verdict-guard`

### unattended-agent-decide-and-record
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/unattended-agent-decide-and-record
- 요약: 무인·자율 세션 운영 규칙. 스스로 결정하고 기록하며, 되돌릴 수 없거나 외부로 나가는 일만 사람에게 묻는다.
- 쓸 때: "끝까지 알아서 해" 식 장시간 세션, 에이전트가 선택지 메뉴로 계속 끊을 때, 백그라운드 워커의 운영 계약을 쓸 때.
- 설치: `git clone https://github.com/Kein-chronicle/unattended-agent-decide-and-record.git ~/.claude/skills/unattended-agent-decide-and-record`

### agent-pipeline-resume-log
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/agent-pipeline-resume-log
- 요약: 다단계 에이전트 실행이 한도로 끊겨도 재개 지점을 찾고, 조용한 모델 다운그레이드를 기계로 검사할 수 있게 하는 텍스트 프로토콜.
- 쓸 때: 여러 역할·모델이 단계를 나눠 도는 파이프라인, 세션이 중간에 끊기는 경우.
- 설치: `git clone https://github.com/Kein-chronicle/agent-pipeline-resume-log.git ~/.claude/skills/agent-pipeline-resume-log`

### agent-job-scheduler-minihub
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/agent-job-scheduler-minihub
- 요약: 반복 AI 생산 작업을 하나의 감독 세션이 한 번에 하나씩 맡아 위임·검증·기록하는 최소 허브. 결과가 검증되지 않으면 실패로 보고 자동 일시정지.
- 쓸 때: 헤드리스 예약 에이전트가 같은 실패를 반복할 때, 결과 계약이 필요할 때.
- 설치: `git clone https://github.com/Kein-chronicle/agent-job-scheduler-minihub.git ~/.claude/skills/agent-job-scheduler-minihub`

### llm-text-edit-revision-guard
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/llm-text-edit-revision-guard
- 요약: AI가 제안한 텍스트 수정을 제안의 기준이 된 정확한 리비전에만 적용한다. 기대 텍스트를 확인하고 겹치는 수정은 거부.
- 쓸 때: AI 제안 편집이나 지연된 리뷰 제안을 문서에 반영할 때.
- 설치: `git clone https://github.com/Kein-chronicle/llm-text-edit-revision-guard.git ~/.claude/skills/llm-text-edit-revision-guard`

### llm-document-review-verifier
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/llm-document-review-verifier
- 요약: AI가 제안하고 결정적 코드가 판정하는 문서·코드 리뷰 구조. 인용 검증, 숫자·날짜 계산, 규칙 평가, 안정적인 이슈 식별.
- 쓸 때: 보고서·견적·제안서 등을 AI로 검토하는 도구를 만들 때.
- 설치: `git clone https://github.com/Kein-chronicle/llm-document-review-verifier.git ~/.claude/skills/llm-document-review-verifier`

### ci-gate-forgery-test
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/ci-gate-forgery-test
- 요약: 게이트 자체를 감사한다. 위조된 불량·빈·누락 입력을 넣어 실패해야 할 때 초록불인 게이트를 찾아낸다.
- 쓸 때: 게이트를 새로 쓰거나 느슨하게 고친 직후, 전부 수상하게 초록일 때, 0건 측정으로 통과한 게이트가 있을 때.
- 설치: `git clone https://github.com/Kein-chronicle/ci-gate-forgery-test.git ~/.claude/skills/ci-gate-forgery-test`

### cross-project-duplicate-file-audit
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/cross-project-duplicate-file-audit
- 요약: 이미 출고한 산출물을 감사해 게이트가 측정하지 못한 품질 축(동일 파일, 쪼개진 텍스트, 복붙 설명)을 찾고, 각각을 위조 테스트가 있는 게이트로 만든다.
- 쓸 때: 파이프라인이 앱·게임·글을 많이 만들었고 여러 산출물이 같은 버그를 공유한다고 의심될 때.
- 설치: `git clone https://github.com/Kein-chronicle/cross-project-duplicate-file-audit.git ~/.claude/skills/cross-project-duplicate-file-audit`

### generative-output-diversity-gate
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/generative-output-diversity-gate
- 요약: 생성 파이프라인이 같은 모양만 반복해 내놓지 않도록 여러 축에서 다양성을 측정한다. 닫힌 어휘와 이미 만든 것의 레지스트리 사용.
- 쓸 때: 산출물이 전부 똑같이 보일 때, 한 축만 막는 게이트가 있을 때.
- 설치: `git clone https://github.com/Kein-chronicle/generative-output-diversity-gate.git ~/.claude/skills/generative-output-diversity-gate`
