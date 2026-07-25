# Marp UI 슬라이드

발표 본문은 Markdown, 디자인은 CSS로 관리한다.

## 실행

Node.js 20 이상이 필요하다.

```bash
npm install
npm run slides
```

브라우저에서 `http://localhost:3000`을 연다. Marp UI가 프로젝트 안의 `slides/marp-ui`를 저장 공간으로 사용한다.

1. Decks에서 `vscode-ai`를 연다.
2. 왼쪽 Markdown을 수정한다.
3. 오른쪽 미리보기에서 결과를 확인한다.
4. `Ctrl+S` 또는 `Cmd+S`로 저장한다.

## 파일

- `marp-ui/decks/vscode-ai/vscode-ai.md`: 발표 본문
- `marp-ui/themes/vscode-ai/vscode-ai.css`: 사용자 테마
- `../DESIGN.md`: 디자인 시스템과 작성 규칙

Marp UI에서 사용자 테마가 바로 선택되지 않으면 Preferences → Themes에서 `vscode-ai` 테마를 선택한다.

## HTML 내보내기

```bash
npm run slides:export
```

결과는 `slides/vscode-ai.html`에 생성된다. Marp UI의 File → Export 메뉴에서도 HTML, PDF, PPTX로 내보낼 수 있다.

## Markdown 작성법

- `---`: 다음 슬라이드
- `#`: 슬라이드 제목
- `> 문장`: 강조 문장
- Markdown 표: 항목별 비교
- `<!-- _class: section -->`: 섹션 구분 슬라이드
- `<!-- 발표자 노트 -->`: 발표자 화면에 표시할 노트

카드나 흐름처럼 별도 레이아웃이 필요할 때만 `DESIGN.md`에 정의된 짧은 HTML 패턴을 사용한다.
