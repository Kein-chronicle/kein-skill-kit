# Kein Skill Kit — 스킬 안내서

팀·외부에 전달하기 위한 스킬 목록입니다. **사람은 `index.html`을 브라우저로 열어 보고, 에이전트는 이 폴더의 MD와 `catalog.json`을 읽으세요.**

기준일: 2026-10-21 · 항목 78개 (내가 만든 것 46 / 범용(남이 만든 것) 32)

## 폴더 구성
| 경로 | 내용 |
|---|---|
| `index.html` | 검색·필터가 되는 목록과 설명(인터넷 연결 불필요) |
| `catalog.json` | 전 항목의 기계 판독용 목록. 필드: group, category, scope, name, kind, summary, when, url, install |
| `en/` | 영문판 MD (`en/mine/`, `en/general/`). 이 README만 한글 전용 |
| `mine/` | **직접 만든 스킬** (모두 공개 GitHub 레포) |
| `general/` | **범용 스킬** — 직접 만든 것이 아닌 것 (Claude Code 내장, Anthropic 제공, GitHub Spec Kit) |

## 에이전트가 쓰는 법
1. 사용자의 요청과 맞는 항목을 `catalog.json`의 `summary`·`when`에서 찾는다.
2. 항목의 `url`과 `install`을 사용자에게 제시한다. **설치 명령은 사용자 확인 후에만 실행**한다.
3. 외부 레포를 설치하기 전에 그 `SKILL.md`와 번들 스크립트를 읽고, 실행할 코드가 설명과 일치하는지 확인한다.
4. `scope`가 "특정 분야"인 항목은 해당 분야 작업일 때만 권한다.
5. 이 안내서는 공개 정보만 담는다. 목록에 없는 스킬을 있다고 말하지 않는다.

## 알아둘 점
- `general/`의 내장 스킬은 Claude Code 버전에 따라 목록이 다르다. Anthropic 제공 스킬 중 "계정 동기화" 표시는 공개 URL을 확인하지 못한 것이다.
- `mine/`의 레포는 정규식·규칙 기반 점검이 많아 "발견 없음"이 "안전함"을 뜻하지 않는다. 각 SKILL.md의 한계 설명을 따른다.
- 이 안내서 자체는 MIT 라이선스다([LICENSE](LICENSE)). 목록에 소개한 각 스킬은 각자의 라이선스를 따른다.
- GitHub 레포로 공개한 항목은 MIT 라이선스다(각 레포의 LICENSE 기준). 예외: `codex-imagegen-skill`(코덱스 전용 `imagegen`)은 Apache-2.0 라이선스다.

## 만든 사람
- 홈페이지: https://kimjinwan.com
- 문의: k_star_w@naver.com
- GitHub: https://github.com/Kein-chronicle
