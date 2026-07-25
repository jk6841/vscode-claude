---
marp: true
theme: vscode-ai
paginate: true
size: 16:9
lang: ko
title: VS Code와 AI로 코딩하기
---

<!-- _class: cover -->
<!-- _paginate: false -->

# VS Code와 AI로
# 코딩하기

<div class="accent-line"></div>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">00</span>

# 개발자

---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
## 코딩이란
- 코딩은 문서 작성 중 한 종류일 뿐임
  - 이 말을 이해해야 `claude code`/`codex` 등 AI를 잘 활용할 수 있음
  - 이해하는 사람
    - "나는 코딩을 할 일이 없지만 문서 작성, 업무 자동화에 AI를 이렇게 사용할 수 있겠구나"
  - 이해 못하는 사람
    - "`claude codex`, `codex`, `github`? 이런 건 개발자들이나 쓰는 툴이지. 나는 코딩을 할 일이 없으니 알 필요 없겠네."
    - 이걸 못 받아들이면 AI의 장점을 누릴 수 없음
---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
## 개발 조직 vs 비개발 조직
- why?
  - 개발 도구를 만드는 사람들도 `개발자`들임
  - 개발자들의 사고 방식, 협업 방식, 정서를 이해해야 개발 도구를 더 잘 이해할 수 있음
---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
## Tools
<div class="columns two">
<div class="card accent">

### 비개발 조직

**Word · PowerPoint · Excel, 이메일, 공유 드라이브**

- 파일 중심
  - 파일을 보내고 받는 개념

</div>
<div class="card">

### 개발 조직

**Jira · Confluence · Notion**
- 웹 중심
  - 문서를 서버에 생성하고 문서의 접근 권한을 컨트롤하는 개념
  - 마크다운
  - 중앙화된 리소스 관리

</div>
- 퇴사자의 컴퓨터 포맷?
</div>
---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
## 표준/컨벤션
- 업계 표준/국룰을 중요하게 생각함
- 쓸데없는 곳에서 튀지 않기/창의성 발휘하지 않기
- .*ignore
  - .gitignore, .containerignore, .helmignore
- 심지어 경쟁사들끼리도 표준을 맞추려는 노력
---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
## 자동화
- 실수를 줄인다.
- 인간은 더 중요한 일을 해야한다.
- 마크다운(markdown)
  - 컨텐츠와 스타일을 분리
    - latex, web(html/css)
  - 문서 작성자는 문서의 구조와 내용에 집중
  - 화면에서 어떻게 보일지는 markdown을 렌더링하는 툴이 관리
---
<!-- _class: question -->
<!-- _paginate: false -->

# Jupyter Notebook?

---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
# Jupyter는 표준적인 프로그래밍 형태가 아니다

<div class="columns two">
<div class="card accent">

### Jupyter Notebook

- 셀과 Kernel 안의 작업
- 실행 순서와 숨은 상태
- `.ipynb`의 어려운 Diff · Merge · Review
- 모듈 · 테스트 · 자동화로 옮기기 어려움

</div>
<div class="card">

### 표준 개발 환경

- 파일과 프로젝트 단위의 작업
- Editor · Terminal · Git
- 텍스트 기반 소스와 명확한 실행 명령
- 모듈 · 패키지 · 테스트 · CLI

</div>
</div>
---
<!-- _class: question -->
<!-- _paginate: false -->

<span class="eyebrow">그렇다면</span>

# AI를 잘 사용하고 함께 일하려면,
# IT · 기술 분야에서 무엇을 공부해야 할까?

---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
# AI와 함께 일하기 위한 키워드
<div class="columns five compact">
<div class="card muted"><b>다음 단계</b><h3>Computer Science</h3><small>자료구조 · 알고리즘<br>운영체제 · 네트워크</small></div>
<div class="card accent"><b>이번 세션</b><h3>AI 서비스</h3><small>모델 · Context<br>도구 · 권한</small></div>
<div class="card accent"><b>이번 세션</b><h3>Git</h3><small>Diff · Commit<br>Branch · 복구</small></div>
<div class="card accent"><b>이번 세션</b><h3>Editor / IDE</h3><small>Workspace · Terminal<br>코드 · 확장</small></div>
<div class="card muted"><b>다음 단계</b><h3>Container</h3><small>격리된 실행 환경<br>재현 가능한 인프라</small></div>
</div>

---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
# 기술의 선택
- `프로그래밍 못 하는 사람들이 프로그래밍을 할 수 있게 만들어진 무언가`들은 결국 안 쓰게 될 것으로 보임
  - 진입 장벽을 낮추다보니 일반적인 프로그래밍 언어들과 매우 다른 방식으로 동작하는 문제
  - 이런 툴만 써왔던 사람들은 `프로그래밍을 할 줄 안다`라는 착각을 갖게 됨
---
<span class="eyebrow">0부 · 개발 조직 이해하기</span>
# 프로그래밍 언어
- 프로그래밍 언어가 중요한가? -> 그럴 수도 있고 아닐 수도 있음
  - syntax는 프로그래밍을 하다보면 익숙해지는 것. 굳이 syntax를 외우려고 할 필요는 없음
  - 하지만 언어마다의 프레임워크/라이브러리 생태계 또한 무시할 수 없는 부분임
- 유명 프로그래밍 언어
  - TypeScript/JavaScript
    - 프론트엔드에는 필수고 풀스택에도 적합
    - 개인 프로젝트를 한다면 1순위로 고려하는 대상
  - Python
  - Kotlin/Java
    - 서버 개발
    - native 안드로이드 개발
---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">01</span>

# Visual Studio Code

<div class="accent-line"></div>

---

<span class="eyebrow">1부 · VS Code</span>

# JetBrains vs Visual Studio Code

> 실무에서는 보통 JetBrains를 메인, vscode를 서브로 사용함
> 오히려 visual studio code가 초보자에게는 더 어려울 수 있음
> vscode는 무료, JetBrains는 유료(학생 인증하면 라이선스 제공)
> 앱 자체만 놓고 보면 JetBrains가 더 쓰기 편하다고 생각함
---

<span class="eyebrow">1부 · VS Code</span>

# VS Code 화면은 네 영역만 알면 시작할 수 있다

<div class="columns three">
<div class="card accent"><h3>Activity Bar</h3>Explorer<br>Search<br>Source Control<br>Run and Debug</div>
<div class="card"><h3>Editor</h3>코드 · Notebook · Diff<br>여러 파일을 탭으로 비교</div>
<div class="card"><h3>Terminal</h3>프로젝트 루트에서<br>명령과 테스트 실행</div>
</div>

> 상태 표시줄에서는 브랜치, Python 인터프리터, 오류 상태를 확인한다.

---

<span class="eyebrow">1부 · VS Code</span>

# 파일 하나가 아니라 Workspace를 연다

<div class="columns two">
<div>

```bash
cd my-project
code .
```

</div>
<div class="card accent">

### my-project/

`data/` · `notebooks/` · `src/`  
`tests/` · `README.md`

</div>
</div>

- 터미널의 현재 폴더와 프로젝트 루트를 맞춘다.
- 원본 데이터와 생성 결과의 위치를 분리한다.
- AI도 이 루트를 기준으로 파일과 지침을 찾는다.
- 맥락에 따라 `project/repository` 등으로 지칭하기도 함

---

<span class="eyebrow">1부 · VS Code</span>

# Extension은 필요한 능력만 더한다

<div class="columns three">
<div class="card accent"><h3>Python</h3>실행 · 디버깅<br>인터프리터 선택</div>
<div class="card"><h3>Formatter</h3>일관된 코드 형식<br>Black · Ruff</div>
<div class="card"><h3>Claude · Codex</h3>프로젝트 안에서<br>에이전트 작업</div>
</div>

> 처음부터 많이 설치하지 말고, 실제로 사용할 확장만 준비한다.
> 신뢰할 수 있는 publisher의 extension만 사용할 것

---

<span class="eyebrow">1부 · VS Code</span>

# 한 번의 실행 경로를 만들어 둔다

<div class="columns two">
<div>

```json
{
  "label": "Run tests",
  "type": "shell",
  "command": "python -m pytest"
}
```

</div>
<div>

- Task 이름만으로 실행 방법을 찾는다.
- `CLAUDE.md`와 `AGENTS.md`에도 같은 명령을 적는다.
- 완료 조건을 “테스트 통과”로 구체화한다.

</div>
</div>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">02</span>

# Git은 AI 작업의 안전망

변경을 기록하고, 비교하고, 작은 단위로 되돌린다.

<div class="accent-line"></div>

---

<span class="eyebrow">2부 · GitHub</span>

# Git을 사용해야하는 이유
> AI들이 Git 중심으로 또는 Git과 강하게 결합하여 동작함.
> Git을 사용하지 않으면 AI와 안정적으로 코딩하기 어려움.
> AI는 물론 cloud 서비스들도 git을 중심으로 설계됨.
> 개발 업계의 사실상 표준인 version control system
> 학부생들도 쓰는데 굳이 이걸 안 배우겠다고 버틸 이유도 없음
---

<span class="eyebrow">2부 · Git</span>

# 작업은 현재 상태 → 수정 → 확인의 루프다

<div class="flow four">
<div><strong>현재 상태</strong><small>Commit · Branch<br>git status</small></div>
<div><strong>수정</strong><small>사람 또는 AI<br>작은 작업 단위</small></div>
<div><strong>확인</strong><small>Diff · Test<br>의도와 결과 비교</small></div>
<div class="active"><strong>기록</strong><small>Stage · Commit<br>새로운 기준점</small></div>
</div>

> 버전 관리는 백업이 아니라 작업 루프를 안정적으로 반복하기 위한 기반이다.

---

<!-- _class: question -->
<!-- _paginate: false -->

# 만약 Git 없이
# AI와 코딩한다면?

---

<span class="eyebrow">2부 · Git</span>

# AI가 무엇을 바꿨는지 추적하기 어렵다

<div class="columns three">
<div class="card accent"><b>기준점 부재</b><h3>전과 후를 비교할 수 없다</h3>내 변경과 AI의 변경이 섞이고 원래 상태가 흐려진다.</div>
<div class="card"><b>변경 범위 불명</b><h3>놓치는 파일이 생긴다</h3>코드뿐 아니라 설정, 새 파일, 삭제된 파일도 바뀔 수 있다.</div>
<div class="card"><b>복구 곤란</b><h3>오류만 되돌리기 어렵다</h3>정상 변경과 오류가 섞이면 복구 범위를 판단하기 어렵다.</div>
</div>

> AI의 설명은 보고이고, 실제 변경의 근거는 **Diff**다.

---

<span class="eyebrow">2부 · Git</span>

# Stage는 ‘이번 커밋에 넣을 변경’을 고르는 단계다

<div class="columns three">
<div class="card accent"><h3>Changes</h3>아직 선택하지 않은 변경<br>U: 새 파일 · M: 수정</div>
<div class="card"><h3>Staged Changes</h3>다음 커밋에 포함할 변경<br>파일별로 선택</div>
<div class="card"><h3>Commit</h3>의미 있는 기준점<br>무엇과 왜를 기록</div>
</div>

```bash
git status        # 현재 상태
git diff          # 아직 고르지 않은 변경
git diff --staged # 다음 커밋에 들어갈 변경
```

---

<span class="eyebrow">2부 · Git</span>

# Git과 GitHub는 같은 것이 아니다

<div class="columns two">
<div class="card accent">

### Git

분산 버전 관리 도구  
Repository · Diff · Commit · Branch · Merge

</div>
<div class="card">

### GitHub

Git 저장소를 호스팅하는 웹 협업 서비스  
Pull Request · Review · Issue · Actions

</div>
</div>

> Commit은 내 컴퓨터에 기록된다. Push해야 GitHub에 공유된다.

---

<span class="eyebrow">2부 · GitHub</span>

# Issue → Branch → Pull Request → main

<div class="flow four">
<div><strong>Issue</strong><small>할 일과 문제<br>담당자 · 완료 조건</small></div>
<div><strong>Branch</strong><small>독립된 작업 공간<br>main과 분리</small></div>
<div><strong>Pull Request</strong><small>Diff · 대화<br>Review · Check</small></div>
<div class="active"><strong>main</strong><small>승인된 변경을<br>공통 기준에 반영</small></div>
</div>

> 개발 조직은 파일을 주고받기보다 공용 상태에 작은 변경을 합친다.

---
<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">03</span>

# Claude Code와 Codex

대답을 받는 도구를 넘어 프로젝트 안에서 계획하고 실행하고 검증한다.

<div class="accent-line"></div>

---

<span class="eyebrow">3부 · 코딩 에이전트</span>

# 채팅으로 코딩하면 왜 불편할까?

<div class="flow five">
<div><strong>찾기</strong><small>관련 파일<br>오류 메시지</small></div>
<div><strong>붙여넣기</strong><small>필요한 문맥을<br>채팅으로 전달</small></div>
<div><strong>답변</strong><small>코드 조각과<br>수정 방법</small></div>
<div><strong>복사 · 실행</strong><small>Editor에 반영<br>직접 명령 실행</small></div>
<div class="active"><strong>다시 전달</strong><small>새 오류와 결과를<br>채팅에 복사</small></div>
</div>

> 사용자가 프로젝트와 AI 사이의 파일 시스템·터미널·테스트 러너가 된다.

---

<span class="eyebrow">3부 · 코딩 에이전트</span>

# 채팅 AI와 코딩 에이전트의 핵심 차이

<div class="columns two">
<div class="card accent">

### 채팅 중심

질문에 답하고 코드를 제안한다.  
복사 · 실행 · 검증은 주로 사용자가 담당한다.

</div>
<div class="card">

### 에이전트 중심

파일을 읽고 수정한다.  
명령과 테스트를 실행한다.  
Git Diff를 확인하고 결과를 보고한다.

</div>
</div>

---

<span class="eyebrow">3부 · 코딩 에이전트</span>

# 코딩 에이전트는 어디까지 할 수 있을까?

<div class="columns three">
<div class="card accent"><b>PROJECT</b><h3>프로젝트 파일</h3>코드와 설정 읽기·수정<br>새 파일 생성·삭제<br>Diff 확인</div>
<div class="card"><b>TERMINAL</b><h3>명령 실행</h3>테스트 · 빌드 · Git<br>실제 파일과 Process에 영향</div>
<div class="card"><b>OUTSIDE</b><h3>경계 밖의 작업</h3>다른 폴더 · 네트워크<br>외부 서비스<br>추가 권한이나 승인</div>
</div>

> 권한 확인은 AI가 현재 작업의 경계를 넘기 전에 멈추는 순간이다.

---

<span class="eyebrow">3부 · 코딩 에이전트</span>

# MCP는 AI와 외부 도구를 연결하는 공통 규칙이다

<div class="connector">
<div class="card accent"><h3>AI 에이전트</h3>필요한 작업과 도구를 선택</div>
<strong>→</strong>
<div class="hub">MCP</div>
<strong>→</strong>
<div class="card"><h3>외부 도구</h3>GitHub · Slack · Notion<br>Drive · 데이터베이스</div>
</div>

> MCP는 모델을 더 똑똑하게 만들기보다 보고 사용할 수 있는 도구를 늘린다.

---

<span class="eyebrow">3부 · 코딩 에이전트</span>

# 할 수 있는 것과 바로 해도 되는 것은 다르다

<div class="flow four risk">
<div><strong>읽기</strong><small>대화 · 문서 확인</small></div>
<div><strong>작성</strong><small>초안 · 코드 생성</small></div>
<div><strong>변경</strong><small>기존 내용 수정</small></div>
<div class="active"><strong>중요 작업</strong><small>전송 · 삭제 · 배포</small></div>
</div>

> 최소 권한 · 읽기/쓰기 분리 · 중요한 작업은 승인 · 실행 기록 확인

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">04</span>

# AI를 위한 프로젝트 설명서

매번 설명하지 말고 프로젝트 안에 짧고 검증 가능한 지침을 남긴다.

<div class="accent-line"></div>

---

<span class="eyebrow">4부 · 프로젝트 지침</span>

# Claude Code와 Codex는 프로젝트 설명서를 읽는다

<div class="columns two">
<div class="card accent">

### Claude Code

`CLAUDE.md`  
프로젝트 또는 상위 범위 지침  
더 세분화하면 `.claude/`

</div>
<div class="card">

### Codex

`AGENTS.md`  
저장소와 하위 디렉터리 지침  
더 가까운 문서가 우선

</div>
</div>

> 파일 이름은 달라도 목적은 같다: 프로젝트에서 일하고 검증하는 방식을 알려준다.

---

<span class="eyebrow">4부 · 프로젝트 지침</span>

# 지침과 설정, 재사용 작업을 분리한다

| 역할 | Claude Code | Codex |
|---|---|---|
| 프로젝트 지침 | `CLAUDE.md` | `AGENTS.md` |
| 실행 설정 | `.claude/settings.json` | `.codex/config.toml` |
| 세부 규칙 | `.claude/rules/` | 하위 `AGENTS.md` |
| 재사용 작업 | `.claude/skills/` | `.agents/skills/` |
| 외부 도구 | `.mcp.json` | `config.toml`의 MCP 설정 |

> 처음에는 지침 파일 하나로 시작하고 반복되는 필요가 생길 때 확장한다.

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="section-no">05</span>

# 개발을 넘어: 발표자료 만들기

코딩 에이전트는 코드만 만드는 도구가 아니라 파일 기반 작업을 함께하는 에이전트다.

<div class="accent-line"></div>

---

<span class="eyebrow">5부 · 발표자료 만들기</span>

# 이 발표자료도 Markdown으로 만든다

<div class="columns three">
<div class="card accent"><b>01</b><h3>본문</h3><code>vscode-ai.md</code><br>제목 · 목록 · 표 · 코드</div>
<div class="card"><b>02</b><h3>디자인</h3><code>vscode-ai.css</code><br>색상 · 서체 · 레이아웃</div>
<div class="card"><b>03</b><h3>기준</h3><code>DESIGN.md</code><br>규칙 · 컴포넌트 · 작성법</div>
</div>

> Marp UI에서 Markdown을 수정하면 오른쪽에서 현재 슬라이드를 바로 확인할 수 있다.

---

<span class="eyebrow">마무리</span>

# 시작 체크리스트

- [ ] Workspace 루트를 열었는가?
- [ ] Python 인터프리터와 Kernel이 맞는가?
- [ ] 작업 전 Git 상태를 확인했는가?
- [ ] Goal · Context · Constraints · Done when이 있는가?
- [ ] 계획을 먼저 검토했는가?
- [ ] 테스트와 Diff를 직접 확인했는가?
- [ ] API 키와 민감 데이터가 빠져 있는가?

---

<!-- _class: question -->
<!-- _paginate: false -->

# Q&A

환경을 맞추고 · 안전하게 맡기고 · 검증해서 남긴다

<div class="accent-line"></div>

`README.md` · `CLAUDE.md` · `AGENTS.md` · `examples/`

---

<span class="eyebrow">Appendix</span>

# 공식 참고 문서

- [VS Code Python environments](https://code.visualstudio.com/docs/python/environments)
- [VS Code Source Control](https://code.visualstudio.com/docs/sourcecontrol/quickstart)
- [Claude Code common workflows](https://code.claude.com/docs/en/common-workflows)
- [Claude Code permissions](https://code.claude.com/docs/en/permissions)
- [Claude Code memory](https://code.claude.com/docs/en/memory)
- [Marp](https://marp.app/)
- [Marp UI](https://www.npmjs.com/package/marp-ui)
