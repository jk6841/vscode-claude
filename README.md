# VS Code + Claude Code + Codex sample

이 저장소는 코딩 에이전트에게 프로젝트 지침과 재사용 가능한 작업 절차를 제공하는 예제입니다.

## 발표자료

발표자료는 Marp UI에서 Markdown으로 편집합니다.

```bash
npm install
npm run slides
```

- `slides/marp-ui/decks/vscode-ai/vscode-ai.md`: 본문
- `slides/marp-ui/themes/vscode-ai/vscode-ai.css`: 디자인 테마
- `DESIGN.md`: 디자인 시스템과 작성 규칙
- `slides/README.md`: 실행과 편집 방법

## Claude Code

- `CLAUDE.md`: 프로젝트 전체 지침
- `.claude/settings.json`: 권한과 플러그인 설정
- `.claude/rules/`: 주제별 세부 규칙
- `.claude/commands/`: 사용자가 직접 호출하는 짧은 명령
- `.claude/skills/`: Claude가 발견해 사용할 수 있는 재사용 작업
- `.claude/agents/`: 독립적인 역할을 가진 전문 에이전트

## Codex

- `AGENTS.md`: 프로젝트 전체 지침
- `.codex/config.toml`: 모델, 승인, 샌드박스 같은 실행 설정
- `.agents/skills/`: Codex가 발견해 사용할 수 있는 재사용 작업

`examples/`에는 실제 이름으로 두면 동작에 영향을 주는 고급 설정의 예제가 있습니다.

## 시작 순서

1. 먼저 `CLAUDE.md` 또는 `AGENTS.md`에 프로젝트 설명과 검증 명령을 적습니다.
2. 같은 요청을 반복하게 되면 rule이나 skill로 분리합니다.
3. 권한과 실행 환경을 바꿔야 할 때만 settings/config 파일을 수정합니다.
