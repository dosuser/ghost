# Adoption Guide

## 결론

가장 안정적인 방식은 `공용 코어 + 플랫폼별 얇은 어댑터` 구조다.
플랫폼마다 완전히 다른 페르소나를 만들면 결국 말투와 판단 규칙이 분리된다. 그건 실패다.

## 문제 구조

플랫폼별 차이는 기능 차이이지, 페르소나 차이가 아니다.

- ChatGPT: Custom Instructions, Project, system/user 프롬프트를 잘 받음
- Claude: Project Instructions와 긴 문맥 유지에 강함
- Copilot: 저장소 지침과 짧은 규칙 세트가 더 안정적임

즉, 코어는 하나로 유지하고 입력 포맷만 바꾸면 된다.

## 개선안

### 1. ChatGPT

적용 순서:

1. `chatgpt-template.md` 내용을 Custom Instructions 또는 Project Instructions에 넣는다.
2. 도메인 규칙이 있으면 아래에 추가한다.
3. 자주 쓰는 출력 언어를 마지막 줄에 고정한다.

추천 추가 문장:

`Respond in Korean unless code or naming should remain in English.`

### 2. Claude

적용 순서:

1. `claude-template.md`를 Project Instructions에 넣는다.
2. 프로젝트 목적, 코드베이스 규칙, 산출물 포맷을 이어서 붙인다.
3. 긴 설계 대화에서는 코어를 반복하지 말고 프로젝트 지침으로만 고정한다.

### 3. Copilot

적용 순서:

1. 저장소 루트에 실제 `copilot-instructions.md`를 둔다.
2. 현재 패키지의 `copilot-instructions.md` 내용을 복사한다.
3. 저장소 특화 규칙만 추가한다.

Copilot은 길고 철학적인 페르소나보다 짧은 실행 규칙이 더 안정적이다.

## 추가 최적화

### 공용 페르소나를 더 강하게 만들고 싶을 때

성격을 더 세게 쓰지 말고, 판정 규칙을 더 강하게 써라.

좋은 강화 예시:

- `If the user asks for options, still recommend one primary path.`
- `If a design is inefficient, explain why it fails at scale.`
- `Always explain architecture before implementation.`
- `Prefer measurable criteria over opinion.`

나쁜 강화 예시:

- `Attack weak logic.`
- `Ignore repetitive users.`
- `Be aggressive.`

이런 문장은 플랫폼별로 무시되거나, 답변 품질을 망친다.

### 운영 추천안

추천 스택은 이거다.

1. 페르소나 코어는 고정
2. 도메인 규칙은 별도 블록
3. 프로젝트별 제약은 가장 아래에 추가

예시 조합:

`Persona Core` + `Domain Rules` + `Output Contract`

### 네 스타일에 맞춘 추가 한 줄

아래 한 줄을 모든 플랫폼에 공통 추가해도 된다.

`Always answer in architecture -> implementation order, and prefer executable output over explanation.`