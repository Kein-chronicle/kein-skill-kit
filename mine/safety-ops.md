# 안전·운영

범용성: 범용

### safe-delete-sole-copy-check
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/safe-delete-sole-copy-check
- 요약: 프로젝트 폴더를 삭제·보관하기 전에 유일본인지 확인한다. 원격, 미푸시 커밋·태그, 무시된 파일을 보고 복사본은 해시로 검증.
- 쓸 때: 폴더를 지우거나 옮기기 전, 디스크 정리 전.
- 설치: `git clone https://github.com/Kein-chronicle/safe-delete-sole-copy-check.git ~/.claude/skills/safe-delete-sole-copy-check`

### zip-bomb-budget-check
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/zip-bomb-budget-check
- 요약: 신뢰할 수 없는 ZIP(docx/xlsx/pptx 포함)을 풀지 않고 크기·항목 수 예산, 경로 탈출, 중복, CRC를 검사한다.
- 쓸 때: 업로드·가져온 압축 파일이나 오피스 문서를 파싱하기 전.
- 설치: `git clone https://github.com/Kein-chronicle/zip-bomb-budget-check.git ~/.claude/skills/zip-bomb-budget-check`

### localhost-origin-guard
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/localhost-origin-guard
- 요약: 브라우저 앱이 로컬 에이전트·브리지와 통신할 때 Host는 정확한 루프백, Origin은 명시적 허용 목록만 통과시킨다.
- 쓸 때: 브라우저 편집기를 로컬 에이전트 프로세스에 연결할 때.
- 설치: `git clone https://github.com/Kein-chronicle/localhost-origin-guard.git ~/.claude/skills/localhost-origin-guard`

### pidfile-process-watchdog
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/pidfile-process-watchdog
- 요약: 장시간 로컬 서비스용 자가 복구 감시기. pid·작업 디렉터리 식별, 재시작 유예, 재시작 폭주 경고, 포기까지의 상태 기계.
- 쓸 때: 서비스가 조용히 죽을 때, 오래된 pid 파일 때문에 죽은 서비스가 정상으로 보일 때.
- 설치: `git clone https://github.com/Kein-chronicle/pidfile-process-watchdog.git ~/.claude/skills/pidfile-process-watchdog`

### autosave-backup-ring-buffer
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/autosave-backup-ring-buffer
- 요약: 복구용 스냅샷을 제한된 개수로 보관하는 링 버퍼. 슬롯 재사용이 결정적이고, 버려지는 키를 명시하며, 시계가 거꾸로 간 경우를 거부.
- 쓸 때: 로컬 복구 스냅샷을 순환 보관할 때.
- 설치: `git clone https://github.com/Kein-chronicle/autosave-backup-ring-buffer.git ~/.claude/skills/autosave-backup-ring-buffer`

### macos-tcc-automation-permissions
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/macos-tcc-automation-permissions
- 요약: 무인 macOS 자동화(launchd, 브라우저 구동, 화면 캡처, AppleScript)가 권한 초기화에도 살아남게 하고 -1743/-1728 같은 오류를 진단한다.
- 쓸 때: AppleScript 오류 -1743/-1728, Homebrew/Python 업그레이드 뒤 권한이 풀릴 때.
- 설치: `git clone https://github.com/Kein-chronicle/macos-tcc-automation-permissions.git ~/.claude/skills/macos-tcc-automation-permissions`
