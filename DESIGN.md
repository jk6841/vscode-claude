# 발표자료 디자인 시스템

이 문서는 `slides/marp-ui/themes/vscode-ai/vscode-ai.css`의 설계 기준이다. 본문은 Markdown에서 수정하고, 반복되는 시각 규칙은 CSS에서만 수정한다.

## 1. 디자인 방향

- 대상: 개발 경험이 적은 비개발자와 비IT 회사 재직자
- 인상: 차분하고 편집적인 문서, 따뜻한 종이 질감, 기술 내용을 위압적이지 않게 전달
- 원칙: 한 장에 하나의 주장, 짧은 문장, 넉넉한 여백, 의미가 있는 경우에만 강조색 사용
- 화면: 16:9, 1280 × 720 기준

## 2. 파일의 책임

| 파일 | 책임 |
|---|---|
| `slides/marp-ui/decks/vscode-ai/vscode-ai.md` | 슬라이드 순서와 본문 |
| `slides/marp-ui/themes/vscode-ai/vscode-ai.css` | 색상, 서체, 간격, 레이아웃, 컴포넌트 |
| `DESIGN.md` | 디자인 의도와 사용 규칙 |

Markdown에서 개별 요소에 인라인 스타일을 넣지 않는다. 반복되는 표현은 CSS 클래스로 만든다.

## 3. 색상

| Token | 값 | 용도 |
|---|---:|---|
| `--paper` | `#faf9f5` | 기본 배경 |
| `--paper-soft` | `#f5f0e8` | 인용문과 보조 표면 |
| `--ink` | `#141413` | 제목과 핵심 텍스트 |
| `--body` | `#3d3d3a` | 본문 |
| `--muted` | `#6c6a64` | 보조 설명 |
| `--coral` | `#cc785c` | 핵심 강조와 진행 상태 |
| `--card` | `#efe9de` | 기본 카드 |
| `--card-accent` | `#e8e0d2` | 강조 카드 |
| `--dark` | `#181715` | 섹션 및 질문 슬라이드 |

Coral은 한 슬라이드에서 핵심 하나를 가리키는 데 사용한다. 장식 목적으로 여러 요소에 반복하지 않는다.

## 4. 타이포그래피

- 제목: `Georgia`, `Noto Serif KR`, serif fallback
- 본문: `Inter`, `Noto Sans KR`, system-ui fallback
- 코드: `JetBrains Mono`, `D2Coding`, monospace fallback
- 기본 본문: 25px / line-height 1.45
- 슬라이드 제목: 50px
- 표지 제목: 72px
- 섹션 제목: 62px

제목은 최대 두 줄을 권장한다. 본문 한 줄은 가능한 한 45자 안쪽으로 유지한다.

## 5. 간격과 형태

- 기본 슬라이드 padding: 위 58px, 좌우 72px, 아래 52px
- 기본 grid gap: 24px
- 카드 radius: 15px
- 카드 padding: 27px
- 코드 블록 radius: 14px
- 경계선: 꼭 필요할 때만 `--hairline` 사용
- 그림자: 사용하지 않는다. 색상과 여백으로 위계를 만든다.

## 6. 슬라이드 유형

### 기본 슬라이드

Markdown 제목 `#`과 본문을 사용한다. 상단 맥락은 다음처럼 쓴다.

```md
<span class="eyebrow">2부 · Git</span>

# Git과 GitHub는 같은 것이 아니다
```

### 표지

```md
<!-- _class: cover -->
<!-- _paginate: false -->
```

### 섹션 구분

```md
<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">02</span>

# Git은 AI 작업의 안전망
```

### 질문 슬라이드

```md
<!-- _class: question -->
<!-- _paginate: false -->

# 만약 Git 없이 AI와 코딩한다면?
```

## 7. 컴포넌트

### 강조 문장

Markdown 인용문을 사용한다.

```md
> AI의 설명은 보고이고, 실제 변경의 근거는 Diff다.
```

### 카드

카드는 비교하거나 병렬 관계가 있을 때만 쓴다.

```html
<div class="columns two">
<div class="card accent">

### 첫 번째 개념

설명

</div>
<div class="card">

### 두 번째 개념

설명

</div>
</div>
```

지원하는 column 수는 `two`, `three`, `five`다. 강조 카드는 한 행에 최대 두 개만 둔다.

### 흐름

과정이나 시간 순서에만 사용한다.

```html
<div class="flow four">
<div><strong>요청</strong><small>목적과 완료 조건</small></div>
<div><strong>구현</strong><small>작은 단위의 변경</small></div>
<div><strong>검토</strong><small>Diff와 Test</small></div>
<div class="active"><strong>반영</strong><small>공통 상태 갱신</small></div>
</div>
```

마지막 또는 현재 단계를 `active`로 표시한다.

### 표

정확한 항목별 비교에는 카드보다 Markdown 표를 우선한다. 열은 두세 개를 권장한다.

## 8. 본문 작성 원칙

- 한 슬라이드에는 하나의 결론만 둔다.
- 제목 자체가 결론이 되도록 쓴다.
- 목록은 3~5개, 체크리스트는 최대 7개를 권장한다.
- 영어 용어는 처음 등장할 때 한국어 역할과 함께 설명한다.
- “개발 조직”과 “비개발 조직”의 차이는 절대적인 구분이 아니라 전형적인 경향으로 표현한다.
- 제품명 나열보다 그 도구가 해결하는 업무 문제를 먼저 설명한다.
- 가격, 기능 제공 범위처럼 바뀌는 정보는 날짜와 출처를 표시한다.

## 9. 검토 체크리스트

- Markdown의 `---` 사이에 하나의 주장만 있는가?
- 텍스트가 화면 아래로 넘치지 않는가?
- 제목이 두 줄을 넘지 않는가?
- 카드 대신 목록이나 표가 더 단순하지 않은가?
- 강조색이 핵심을 실제로 가리키는가?
- 코드와 파일 경로가 monospace로 표시되는가?
- 출처 링크가 최신이고 직접 연결되는가?
- HTML/PDF 내보내기에서도 레이아웃이 유지되는가?
