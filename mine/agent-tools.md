# 에이전트 도구 운영

범용성: 범용

### claude-code-memory-lint
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/claude-code-memory-lint
- 요약: 메모리 폴더를 린트한다. 고아·누락 파일, 비대해진 인덱스 줄, 로드 시 조용히 잘리는 인덱스 줄을 찾는다.
- 쓸 때: 메모리 인덱스가 커졌을 때, 로더가 인덱스가 잘렸다고 경고할 때, 새 메모리를 넣기 전.
- 설치: `git clone https://github.com/Kein-chronicle/claude-code-memory-lint.git ~/.claude/skills/claude-code-memory-lint`

### claude-code-session-cost
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/claude-code-session-cost
- 요약: 세션 로그(서브에이전트 포함)로 프로젝트·작업 주기의 실제 비용을 추정한다. 캐시 TTL 가정 2종을 함께 표시.
- 쓸 때: 토큰·사용량 청구가 예상보다 클 때, 긴 세션이 왜 비싼지 알고 싶을 때.
- 설치: `git clone https://github.com/Kein-chronicle/claude-code-session-cost.git ~/.claude/skills/claude-code-session-cost`

### claude-code-launchd-loops
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/claude-code-launchd-loops
- 요약: Claude Code를 macOS launchd로 헤드리스 주기 실행하는 잡(셸 래퍼 + LaunchAgent plist + 로드·확인·중지 명령)을 한 번에 생성.
- 쓸 때: "N분/시간마다 X를 며칠간" 반복이 필요하고 세션 내 cron이 누락될 때.
- 설치: `git clone https://github.com/Kein-chronicle/claude-code-launchd-loops.git ~/.claude/skills/claude-code-launchd-loops`
