# 코덱스(Codex) 전용 스킬

**Codex에서만 쓰는 스킬**이다(Claude Code 용이 아님). 설치: `git clone https://github.com/Kein-chronicle/codex-imagegen-skill.git ~/.codex/skills/imagegen`

### imagegen
- 종류: 스킬(Codex 전용)
- 대상 도구: **코덱스 전용**
- 출처: https://github.com/Kein-chronicle/codex-imagegen-skill
- 요약: 사진·일러스트·텍스처·스프라이트·목업 같은 래스터 이미지를 새로 만들거나 편집하는 Codex 스킬. 기본은 Codex 내장 image_gen 도구(API 키 불필요), 사용자가 요청할 때만 CLI 대체 경로(OPENAI_API_KEY 필요). 투명 배경은 크로마키로 생성한 뒤 번들된 remove_chroma_key.py로 로컬에서 제거한다.
- 쓸 때: 새 이미지 생성, 참조 이미지로 스타일·구도 유도, 인페인팅·배경 교체·객체 제거, 여러 에셋 변형 제작, 투명 배경 컷아웃. SVG·HTML/CSS로 만들 도형·다이어그램·아이콘에는 쓰지 않는다.
- 설치: `git clone https://github.com/Kein-chronicle/codex-imagegen-skill.git ~/.codex/skills/imagegen`
- 출처·라이선스 주의: 라이선스는 Apache-2.0(레포의 LICENSE.txt, MIT 아님). 폴더 구조·라이선스가 OpenAI 의 Codex imagegen 시스템 스킬과 같은 형식이라, 재배포·수정 시 LICENSE 와 고지를 유지하고 수정 내용을 표기한다.

## 알아둘 점
- 기본 경로는 내장 `image_gen` 도구이며 `OPENAI_API_KEY`가 필요 없다. CLI 대체 경로는 사용자가 명시적으로 요청할 때만 쓰고 키가 필요하다.
- 생성 파일은 기본적으로 `$CODEX_HOME/generated_images/` 아래에 저장되므로, 프로젝트에서 쓸 에셋은 작업 폴더로 복사해야 한다.
- 기존 파일은 덮어쓰지 않고 `hero-v2.png` 같은 새 이름으로 저장하는 것이 규칙이다.
- 투명 배경은 평면 크로마키 배경으로 생성한 뒤 `scripts/remove_chroma_key.py`로 제거한다(진짜 투명도가 필요하면 CLI 경로를 사용자에게 확인).
