# 데이터·파일 유틸

범용성: 범용

### csv-injection-safe-export
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/csv-injection-safe-export
- 요약: Excel·Sheets에서 안전한 CSV. 따옴표 처리와 수식 접두어(=, +, -, @, 탭, CR, LF) 무력화.
- 쓸 때: 신뢰할 수 없는 텍스트를 스프레드시트용 CSV로 내보낼 때.
- 설치: `git clone https://github.com/Kein-chronicle/csv-injection-safe-export.git ~/.claude/skills/csv-injection-safe-export`

### csv-table-diff-by-key
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/csv-table-diff-by-key
- 요약: 위치가 아니라 키 컬럼 기준으로 두 표를 비교한다. 타입을 구분한 셀 변경과 행·열 추가·삭제를 보고.
- 쓸 때: 행·열 순서가 바뀐 내보내기 데이터를 비교할 때.
- 설치: `git clone https://github.com/Kein-chronicle/csv-table-diff-by-key.git ~/.claude/skills/csv-table-diff-by-key`

### pdf-page-range-parser
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/pdf-page-range-parser
- 요약: "1-3, 5, 8-" 같은 페이지 선택을 정렬·중복 제거 없이 정확히 파싱하고 모호한 입력은 거부.
- 쓸 때: 페이지가 있는 문서를 나누거나 재정렬할 때.
- 설치: `git clone https://github.com/Kein-chronicle/pdf-page-range-parser.git ~/.claude/skills/pdf-page-range-parser`

### exif-orientation-guard
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/exif-orientation-guard
- 요약: EXIF 방향 태그 때문에 저장 크기와 표시 크기가 달라지는 이미지를 찾아 고친다.
- 쓸 때: 스크린샷이 파일 크기상 가로인데 세로로 보일 때, OCR 박스가 엉뚱한 곳을 자를 때.
- 설치: `git clone https://github.com/Kein-chronicle/exif-orientation-guard.git ~/.claude/skills/exif-orientation-guard`

### image-crop-bounds-clamp
- 종류: 스킬
- 출처: https://github.com/Kein-chronicle/image-crop-bounds-clamp
- 요약: 이미지 편집기용 크롭 수학. 경계 검증, 드래그 이동 제한, 출력 픽셀 예산.
- 쓸 때: 경계가 있는 이미지 크롭 UI나 래스터 내보내기를 구현할 때.
- 설치: `git clone https://github.com/Kein-chronicle/image-crop-bounds-clamp.git ~/.claude/skills/image-crop-bounds-clamp`
