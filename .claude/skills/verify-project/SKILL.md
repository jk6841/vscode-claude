---
name: verify-project
description: Claude/Codex 설정 예제를 검토하고 문법, 경로, 비밀 값 노출 여부를 확인한다.
---

# Verify project

## Procedure

1. 저장소의 지침 파일과 설정 파일 목록을 확인한다.
2. JSON과 TOML 문법을 검사한다.
3. 문서가 가리키는 파일과 디렉터리가 실제로 존재하는지 확인한다.
4. API Key, token, password처럼 보이는 값이 있는지 검색한다.
5. 문제, 영향, 권장 수정 순서로 결과를 정리한다.

## Safety

- 검토 요청만 받은 경우 파일을 수정하지 않는다.
- 실제 인증 정보로 의심되는 값은 응답에 그대로 출력하지 않는다.

